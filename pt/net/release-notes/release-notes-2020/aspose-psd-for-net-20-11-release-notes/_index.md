---
title: Notas de Lançamento Aspose.PSD para .NET 20.11
type: docs
weight: 20
url: /pt/net/aspose-psd-para-net-20-11-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 20.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-713|Aspose.PSD não pode converter PSD para outros modos de cor/BitDepth sem salvá-los como arquivos|Recurso|
|PSDNET-754|Adicionar capacidade de copiar Camada de Objeto Inteligente na imagem PSD|Recurso|
|PSDNET-267|Exceção ao carregar e salvar o arquivo PSD com Efeitos de Camada|Erro|
|PSDNET-579|O método "Image.LoadRawData" lança uma exceção de NullPointer|Erro|
|PSDNET-741|ImageLoadException é lançada ao tentar abrir o arquivo|Erro|
|PSDNET-744|Aspose.PSD 20.10: Não é possível carregar Psd|Erro|

## **Alterações na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.Convert(Aspose.PSD.ImageOptions.PsdOptions)
- F:Aspose.PSD.FileFormats.Psd.ResourceBlock.ResouceBlockMeSaSignature
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.NewSmartObjectViaCopy
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.DuplicateLayer
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.NewSmartObjectViaCopy(Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer)
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(System.Int32[])
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-267. Exceção ao carregar e salvar o arquivo PSD com Efeitos de Camada**
{{< highlight csharp >}}
            string dataDir = "PSDNET267_1\\";
            string inputFilePath = dataDir + "LayerEffectsTest.psd";
            string outputFilePath = dataDir + "LayerEffectsTestOutput.psd";
            using (var image = (PsdImage)Image.Load(inputFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFilePath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-579. O método "Image.LoadRawData" lança uma exceção de NullPointer**
{{< highlight csharp >}}
            string dataDir = "PSDNET579_1\\";
            string srcFile = dataDir + "CmykWithAlpha_raw.psd";
            using (RasterImage image = (RasterImage)Image.Load(srcFile))
            {
                Rectangle rect = image.Bounds;
                RawDataRetriever rawDataRetriever = new RawDataRetriever(rect, image.RawDataSettings);
                image.LoadRawData(rect, image.RawDataSettings, rawDataRetriever);
                rawDataRetriever.GetData();
            }

    class RawDataRetriever : Aspose.PSD.IPartialRawDataLoader
    {
        private readonly byte[] rawData;
        private int rawDataIndex;

        public RawDataRetriever(Rectangle rectangle, RawDataSettings rawDataSettings)
        {
            int totalSize = rawDataSettings.LineSize * rectangle.Height;
            if (totalSize == 0)
            {
                totalSize = rectangle.Width * rectangle.Height * 5;
            }

            this.rawData = new byte[totalSize];
        }

        public byte[] GetData()
        {
            return this.rawData;
        }

        public void Process(Rectangle rectangle, byte[] data, Point start, Point end)
        {
            Array.Copy(data, 0, this.rawData, this.rawDataIndex, data.Length);
            this.rawDataIndex += data.Length;
        }

        public void Process(Rectangle rectangle, byte[] data, Point start, Point end, LoadOptions loadOptions)
        {
            throw new NotImplementedException();
        }
    }
{{< /highlight >}}
**PSDNET-713. Aspose.PSD não pode converter PSD para outros modos de cor/BitDepth sem salvá-los como arquivos**
{{< highlight csharp >}}
            string dataDir = "PSDNET713_1\\";
            string outputDir = dataDir + "output\\";

            // Esses exemplos demonstram a conversão do formato de imagem PSD para outros modos de cor/BitDepth.
            ConversaoDeImagem(ColorModes.Grayscale, 16, 2);
            ConversaoDeImagem(ColorModes.Grayscale, 8, 2);
            ConversaoDeImagem(ColorModes.Grayscale, 8, 1);
            ConversaoDeImagem(ColorModes.Rgb, 8, 4);
            ConversaoDeImagem(ColorModes.Rgb, 16, 4);
            ConversaoDeImagem(ColorModes.Cmyk, 8, 5);
            ConversaoDeImagem(ColorModes.Cmyk, 16, 5);

            void ConversaoDeImagem(ColorModes colorMode, short channelBitsCount, short channelsCount)
            {
                var compression = channelBitsCount > 8 ? CompressionMethod.Raw : CompressionMethod.RLE;
                SalvarEmPsdDepoisCarregarESalvarEmPng(
                    "ExemploDestaqueCorSheet",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    1);
                SalvarEmPsdDepoisCarregarESalvarEmPng(
                    "ExemploOpacidadePreenchimento",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    2);
                SalvarEmPsdDepoisCarregarESalvarEmPng(
                    "RecorteMascaraRegular",
                    colorMode,
                    channelBitsCount,
                    channelsCount,
                    compression,
                    3);
            }

            // Salva em PSD e em seguida carrega o arquivo salvo e salva em PNG.
            void SalvarEmPsdDepoisCarregarESalvarEmPng(
                string arquivo,
                ColorModes colorMode,
                short channelBitsCount,
                short channelsCount,
                CompressionMethod compression,
                int numeroCamada)
            {
                string srcFile = dataDir + arquivo + ".psd";
                string postfix = colorMode.ToString() + channelBitsCount + "bits" + channelsCount + "channels" +
                                 compression;
                string fileName = arquivo + "_" + postfix + ".psd";
                string exportPath = outputDir + fileName;
                PsdOptions psdOptions = new PsdOptions()
                {
                    ColorMode = colorMode,
                    ChannelBitsCount = channelBitsCount,
                    ChannelsCount = channelsCount,
                    CompressionMethod = compression
                };
                using (var image = (PsdImage)Image.Load(srcFile))
                {
                    image.Convert(psdOptions);

                    RasterCachedImage raster = image.Layers.Length > 0 && numeroCamada >= 0
                        ? (RasterCachedImage)image.Layers[numeroCamada]
                        : image;
                    Aspose.PSD.Graphics graphics = new Graphics(raster);
                    int largura = raster.Width;
                    int altura = raster.Height;
                    Rectangle rect = new Rectangle(
                        largura / 3,
                        altura / 3,
                        largura - (2 * (largura / 3)) - 1,
                        altura - (2 * (altura / 3)) - 1);
                    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1), rect);

                    image.Save(exportPath);
                }

                string pngExportPath = Path.ChangeExtension(exportPath, "png");
                using (PsdImage image = (PsdImage)Image.Load(exportPath))
                {
                    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
**PSDNET-741. ImageLoadException é lançada ao tentar abrir o arquivo**
{{< highlight csharp >}}
            string dataDir = "PSDNET741_1\\";
            string inputFile = dataDir + "input.psd";
            string outputFile = dataDir + "output.psd";

            using (var psdImage = (PsdImage)Image.Load(inputFile))
            {
                psdImage.Save(outputFile, new PsdOptions(psdImage));
            }

            using (var psdImage2 = (PsdImage)Image.Load(outputFile))
            {
                // Nenhuma exceção aqui...
            }
{{< /highlight >}}
**PSDNET-744. Aspose.PSD 20.10: Não é possível carregar Psd**
{{< highlight csharp >}}
            void SaoIguais(object esperado, object real)
            {
                if (!object.Equals(esperado, real))
                {
                    throw new Exception("Os valores não são iguais.");
                }
            }

            string srcFile = "GST-CHALLAN(2)1..psd";
            string output = "output.psd";

            using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
            {
                SaoIguais(ResourceBlock.ResouceBlockMeSaSignature, psdImage.ImageResources[23].Signature);
                SaoIguais(ResourceBlock.ResouceBlockMeSaSignature, psdImage.ImageResources[24].Signature);
                psdImage.Save(output);
            }
{{< /highlight >}}
**PSDNET-754. Adicionar capacidade de copiar Camada de Objeto Inteligente na imagem PSD**
{{< highlight csharp >}}
            string dataDir = "PSDNET754_1\\";
            string outputDir = dataDir + "output\\";

            // Estes exemplos demonstram como copiar camadas de objetos inteligentes em uma imagem PSD.
            ExemploDeCopiarCamadaObjetoInteligente("r-embedded-psd");
            ExemploDeCopiarCamadaObjetoInteligente("r-embedded-png");
            ExemploDeCopiarCamadaObjetoInteligente("r-embedded-transform");
            ExemploDeCopiarCamadaObjetoInteligente("new_panama-papers-8-trans4");

            void ExemploDeCopiarCamadaObjetoInteligente(string nomeArquivo)
            {
                int numeroCamada = 0; // O número da camada a ser copiado
                string filePath = dataDir + nomeArquivo + ".psd";
                string outputFilePath = outputDir + nomeArquivo + "_copy_" + numeroCamada;
                string pngOutputPath = outputFilePath + ".png";
                string psdOutputPath = outputFilePath + ".psd";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = (SmartObjectLayer)image.Layers[numeroCamada];
                    var novaCamada = smartObjectLayer.NewSmartObjectViaCopy();
                    novaCamada.IsVisible = false;
                    AssertIsTrue(object.ReferenceEquals(novaCamada, image.Layers[numeroCamada + 1]));
                    AssertIsTrue(object.ReferenceEquals(smartObjectLayer, image.Layers[numeroCamada]));

                    var camadaDuplicada = smartObjectLayer.DuplicateLayer();
                    camadaDuplicada.DisplayName = smartObjectLayer.DisplayName + " imagem compartilhada";
                    AssertIsTrue(object.ReferenceEquals(novaCamada, image.Layers[numeroCamada + 2]));
                    AssertIsTrue(object.ReferenceEquals(camadaDuplicada, image.Layers[numeroCamada + 1]));
                    AssertIsTrue(object.ReferenceEquals(smartObjectLayer, image.Layers[numeroCamada]));

                    using (var imagemInterna = (RasterImage)smartObjectLayer.LoadContents(null))
                    {
                        // Vamos inverter a imagem de objeto inteligente incorporada (para uma imagem PSD interna invertemos apenas sua primeira camada)
                        InverterImagem(imagemInterna);

                        // Vamos substituir a imagem de objeto inteligente incorporada na camada PSD
                        smartObjectLayer.ReplaceContents(imagemInterna);
                    }

                    // A camada duplicada compartilha sua imagem incorporada com o objeto inteligente original
                    // e ela deve ser atualizada explicitamente, caso contrário seu cache de renderização permanece inalterado.
                    // Atualizamos todos os objetos inteligentes para garantir que a nova camada criada por NewSmartObjectViaCopy
                    // não compartilhe a imagem incorporada com os outros.
                    image.SmartObjectProvider.UpdateAllModifiedContent();

                    image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                    image.Save(psdOutputPath, new PsdOptions(image));
                }
            }

            // Inverte a imagem raster, incluindo a imagem PSD.
            void InverterImagem(RasterImage imagemInterna)
            {
                var imagemPsdInterna = imagemInterna as PsdImage;
                if (imagemPsdInterna != null)
                {
                    InverterImagemRaster(imagemPsdInterna.Layers[0]);
                }
                else
                {
                    InverterImagemRaster(imagemInterna);
                }
            }

            // Inverte a imagem raster.
            void InverterImagemRaster(RasterImage imagemInterna)
            {
                var pixels = imagemInterna.LoadArgb32Pixels(imagemInterna.Bounds);
                for (int i = 0; i < pixels.Length; i++)
                {
                    var pixel = pixels[i];
                    var alpha = (int)(pixel & 0xff000000);
                    pixels[i] = (~(pixel & 0x00ffffff)) | alpha;
                }

                imagemInterna.SaveArgb32Pixels(imagemInterna.Bounds, pixels);
            }

            void AssertIsTrue(bool condicao)
            {
                if (!condicao)
                {
                    throw new FormatException(string.Format("Expected true"));
                }
            }
{{< /highlight >}}
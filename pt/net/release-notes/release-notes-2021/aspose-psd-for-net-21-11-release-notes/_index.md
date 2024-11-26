---
title: Aspose.PSD para .NET 21.11 - Notas de Lançamento
type: docs
weight: 20
url: /pt/net/aspose-psd-para-net-21-11-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para [Aspose.PSD para .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-767|Exceção ao adicionar a camada de texto existente a um grupo de camadas|Erro|
|PSDNET-988|IndexOutOfRangeException em TextLayer.UpdateText|Erro|
|PSDNET-989|Formas exportadas têm coordenadas erradas no arquivo de resultado|Erro|
|PSDNET-1002|Exportação incorreta de forma vetorial na exportação da pasta|Erro|

## **Alterações na API Pública**
# **APIs Adicionadas:**
- Nenhuma

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-767. Exceção ao adicionar a camada de texto existente a um grupo de camadas**

{{< highlight csharp >}}
            string outputPsd = "out_dummy_group.psd";

            var psdOptions = new PsdOptions()
            {
                Source = new StreamSource(new MemoryStream(), true),
                ColorMode = ColorModes.Rgb,
                ChannelsCount = 4,
                ChannelBitsCount = 8,
                CompressionMethod = CompressionMethod.RLE
            };
            using (PsdImage image = (PsdImage)Image.Create(psdOptions, 10, 15))
            {
                var group = image.AddLayerGroup("Grupo de Teste", 0, true);
                var layer = image.AddTextLayer("Texto", Rectangle.FromLeftTopRightBottom(-2, 3, 14, 17));
                group.AddLayer(layer);

                image.Save(outputPsd);
            }
{{< /highlight >}}

**PSDNET-988. IndexOutOfRangeException em TextLayer.UpdateText**

{{< highlight csharp >}}
            string srcFile = "M1TTTT16062021001.psd";
            string fontsFolder = "Fonts";
            string outputPng = "out_M1TTTT16062021001.png";

            FontSettings.SetFontsFolder(fontsFolder);
            FontSettings.UpdateFonts();

            string[] palavras = new[] { "Mãe", "Stacy" };
            string[] fontes = new[] { "Caveat", "Gochi Hand", "Lobster", "Satisfy" };

            using (var imagem = (PsdImage)Image.Load(srcFile))
            {
                foreach (var camada in imagem.Layers)
                {
                    var camadaTexto = camada as TextLayer;
                    if (camadaTexto != null)
                    {
                        for (int w = 0; w < palavras.Length; w++)
                        {
                            for (int f = 0; f < fontes.Length; f++)
                            {
                                camadaTexto.UpdateText(palavras[w]);
                                foreach (var itemTexto in camadaTexto.TextData.Items)
                                {
                                    itemTexto.Style.FontName = FontSettings.GetAdobeFontName(fontes[f]);
                                }

                                camadaTexto.TextData.UpdateLayerData();
                            }
                        }
                    }
                }

                imagem.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-989. Formas exportadas têm coordenadas erradas no arquivo de resultado**

{{< highlight csharp >}}
        public void CriarExemploCaminhoVetorial()
        {
            string outputPsd = "outputPsd.psd";

            using (var psdImagem = (PsdImage)Image.Create(new PsdOptions() { Source = new Sources.StreamSource(new MemoryStream()), }, 500, 500))
            {
                FillLayer camada = FillLayer.CreateInstance(PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                psdImagem.AddLayer(camada);

                VectorPath caminhoVetorial = VectorDataProvider.CreateVectorPathForLayer(camada);
                caminhoVetorial.FillColor = Color.IndianRed;
                PathShape forma = new PathShape();
                forma.Points.Add(new BezierKnot(new PointF(50, 150), true));
                forma.Points.Add(new BezierKnot(new PointF(100, 200), true));
                forma.Points.Add(new BezierKnot(new PointF(0, 200), true));
                caminhoVetorial.Shapes.Add(forma);
                VectorDataProvider.UpdateLayerFromVectorPath(camada, caminhoVetorial, true);

                psdImagem.Save(outputPsd);
            }
        }
    #region Editor de caminho vetorial (Aqui estão localizadas as classes para edição de caminhos vetoriais).

    ...
{{< /highlight >}}

**PSDNET-1002. Exportação incorreta de forma vetorial na exportação da pasta**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var imagem = (PsdImage)Image.Load(srcFile))
            {
                imagem.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
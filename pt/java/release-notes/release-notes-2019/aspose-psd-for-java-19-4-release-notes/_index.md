---
title: Aspose.PSD para Java 19.4 - Notas da Versão
type: docs
weight: 20
url: /pt/java/aspose-psd-para-java-19-4-notas-da-versao/
---

{{% alert color="primary" %}} 

Esta página contém as notas de lançamento para Aspose.PSD para Java 19.4

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-1|Criar recurso para carregar arquivos de imagem JPEG/PNG/etc em PsdImage sem carregamento direto (O que não é suportado no Aspose.PSD)|Recurso|
|PSDJAVA-2|Suporte ao modo de cor RGB com 16 bits/canal (64 bits por cor)|Recurso|
|PSDJAVA-3|Suporte a Máscaras Vetoriais de Camada e Rotação Personalizada de Texto de Camada|Recurso|
|PSDJAVA-4|Todos os caracteres asiáticos não são renderizados corretamente|Erro|
|PSDJAVA-5|Símbolos \r\n são interpretados como quebra de linha dupla, o que está incorreto|Erro|
|PSDJAVA-6|Se a TextLayer for atualizada com uma string que contenha quebras de linha, o arquivo PSD se torna ilegível|Erro|
|PSDJAVA-7|Se a TextLayer for atualizada com uma string que contenha símbolos de tabulação, o processamento falha com exceção|Erro|
# **Mudanças na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **APIs Removidas:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTrailer
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsPaletteSorted
- P:Aspose.PSD.FileFormats.Gif.GifImage.PaletteColorResolutionBits
- P:Aspose.PSD.FileFormats.Gif.GifImage.Width
- P:Aspose.PSD.FileFormats.Gif.GifImage.Height
- P:Aspose.PSD.FileFormats.Gif.GifImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Gif.GifImage.Blocks
- P:Aspose.PSD.FileFormats.Gif.GifImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColorIndex
- P:Aspose.PSD.FileFormats.Gif.GifImage.PixelAspectRatio
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsCached
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.TransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasBackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.ImageOpacity
- M:Aspose.PSD.FileFormats.Gif.GifImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.CacheData
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.OrderBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.ClearBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.InsertBlock(System.Int32,Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AddBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RemoveBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Grayscale
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceNonTransparentColors(System.Int32)
- T:Aspose.PSD.FileFormats.Tiff.TiffImage
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeBradley(System.Double,System.Int32)
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HasAlpha
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.FileFormat
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.PremultiplyComponents
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ByteOrder
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HorizontalResolution
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.VerticalResolution
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Frames
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Height
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Width
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.IsCached
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ExifData
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ImageOpacity
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.XmpData
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AlignResolutions
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.SetResolution(System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.CacheData
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AddFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Add(Aspose.PSD.FileFormats.Tiff.TiffImage)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AddFrames(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.InsertFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RemoveFrame(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RemoveFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeWidthProportionally(System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeHeightProportionally(System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Grayscale
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Crop(System.Int32,System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
# **Exemplos de Uso:**

**PSDJAVA-1. Criar recurso para carregar arquivos de imagem JPEG/PNG/etc em PsdImage sem carregamento direto (O que não é suportado no Aspose.PSD)**

{{< highlight java >}}

 String caminhoArquivo = "ExemploPsd.psd";

    String caminhoArquivoSaida = "ResultadoPsd.psd";

    PsdImage imagem = new PsdImage(200, 200);

    try 

    { 

         PsdImage im = Image.load(caminhoArquivo);

         try 

         {

              Layer camada = null;

              try

              {

                  camada = new Layer((RasterImage)im);

                  imagem.addLayer(camada);

                  imagem.save(caminhoArquivoSaida);

              }

              catch

              {

                  if (camada != null)

                  {

                       camada.dispose();

                  }

                  throw;

              }

         }    

         finally 
         {
              im.dispose(); 
         }
    }

    finally

    {

         imagem.dispose();

    }

{{< /highlight >}}

**PSDJAVA-2. Suporte ao modo de cor RGB com 16 bits/canal (64 bits por cor)**

{{< highlight java >}}

  // Suporte ao modo de cor RGB com 16 bits/canal (64 bits por cor)

        String nomeArquivoFonte = "emRgb16.psd.psd";

        String caminhoArquivoSaidaJpg = "saidaRgb16.jpg";

        String caminhoArquivoSaidaPsd = "saidaRgb16.psd";

        PsdLoadOptions opcoes = new PsdLoadOptions();

        PsdImage imagem = (PsdImage)Image.load(nomeArquivoFonte, opcoes);

        try

        {

            PsdOptions optPsd = new PsdOptions(imagem);

            imagem.save(caminhoArquivoSaidaPsd, optPsd);
            
            JpegOptions optJpeg = new JpegOptions();

            optJpeg.setQuality(100);

            imagem.save(caminhoArquivoSaidaJpg);

        }

        finally 

        {

             imagem.dispose();

        }

    // Arquivos devem ser abertos sem exceção e legíveis para o Photoshop    

   imagem = Image.load(caminhoArquivoSaidaPsd));

   imagem.dispose(); 

{{< /highlight >}}

**PSDJAVA-3. Suporte a Máscaras Vetoriais de Camada e Rotação Personalizada de Texto de Camada**

{{< highlight java >}}

 // A operação RotateFlip não funciona como esperado com PSD

    String arquivoFonte = "1.psd";

    String caminhoPng = "TesteRotaçãoFlip2617.png";

    String caminhoPsd = "TesteRotaçãoFlip2617.psd";

    int tipoFlip = RotateFlipType.Rotate270FlipXY;

    PsdImage im = (PsdImage)(Image.load(arquivoFonte));



    try

    {

        im.rotateFlip(tipoFlip);

        PngOptions opcoes = new PngOptions();

        opcoes.setColorType(PngColorType.TruecolorWithAlpha);

        im.save(caminhoPng, opcoes);

        im.save(caminhoPsd);

    }

    finally 

    {

        im.dispose();

    }

{{< /highlight >}}

**PSDJAVA-4. Todos os caracteres asiáticos não são renderizados corretamente**

[**Por favor, verifique o exemplo anexado**](attachments/92602686/92766213.java)

**PSDJAVA-5. Símbolos \r\n são interpretados como quebra de linha dupla, o que está incorreto**

{{< highlight java >}}

 // Símbolos \r\n são interpretados como quebra de linha dupla, o que está incorreto

            String nomeArquivoFonte = "TesteTexto.psd";

            String caminhoExportacao = "Resultado.psd";



            PsdImage imagem = (PsdImage)Image.load(nomeArquivoFonte);

            TextLayer camada = (TextLayer)imagem.getLayers()[0];

            PsdOptions opcoesImagem = new PsdOptions(imagem);

            try

            {

                camada.updateText("Primeiro Parágrafo\r\nSegundo Parágrafo\rTerceiro parágrafo\nQuarto Parágrafo");

                imagem.save(caminhoExportacao, opcoesImagem);

                // A imagem criada deve ser legível pelo Aspose.PSD/Aspose.Imaging e pelo Photoshop

                PsdImage imagemCriada = (PsdImage)Image.load(caminhoExportacao);

                imagemCriada.dispose();

            }

            finally

            {

                imagem.dispose();

            }

{{< /highlight >}}



**PSDJAVA-6. Se a TextLayer for atualizada com uma string que contenha quebras de linha, o arquivo PSD se torna ilegível**

{{< highlight java >}}

 // Se a TextLayer for atualizada com uma string que contenha quebras de linha, o arquivo PSD se torna ilegível.

            String nomeArquivoFonte = "TesteTexto.psd";

            String caminhoExportacao = "Resultado.psd";



            PsdImage imagem = (PsdImage)Image.load(nomeArquivoFonte);

            TextLayer camada = (TextLayer)imagem.getLayers()[0];

            PsdOptions opcoesImagem = new PsdOptions(imagem);

            try

            {

                camada.updateText("Primeiro Parágrafo\r\nSegundo Parágrafo\r\nTerceiro parágrafo\r\nQuarto Parágrafo");

                imagem.save(caminhoExportacao, opcoesImagem);

                // A imagem criada deve ser legível pelo Aspose.PSD/Aspose.Imaging e pelo Photoshop

                PsdImage imagemCriada = (PsdImage)Image.load(caminhoExportacao);

                imagemCriada.dispose();



            }

            finally

            {

                imagem.dispose();

            }

{{< /highlight >}}



**PSDJAVA-7. Se a TextLayer for atualizada com uma string que contenha símbolos de tabulação, o processamento falha com exceção**

{{< highlight java >}}

 // Se a TextLayer for
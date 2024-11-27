---
title: Aspose.PSD para .NET 19.10 - Notas de Lançamento
type: docs
weight: 30
url: /pt/net/aspose-psd-para-net-19-10-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém as notas de lançamento para o Aspose.PSD para .NET 19.10

{{% /alert %}} 

|**Chave**|**Sumário**|**Categoria**|
| :- | :- | :- |
|PSDNET-207|[Suporte à Camada de Ajuste de Equilíbrio de Cor](/psd/pt/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|Recurso|
|PSDNET-145|[Suporte à Camada de Inversão de Cores](/psd/pt/net/modifying-images/#modifyingimages-invertadjustmentlayer)|Recurso|
|PSDNET-139|[Implementar Bicubic Resampler](/psd/pt/net/modifying-images/#modifyingimages-implementbicubicresampling)|Recurso|
|PSDNET-169|[Adicionar suporte à exportação de PSD para PDF com Máscara de Recorte](/psd/pt/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|Recurso|
|PSDNET-168|[Adicionar suporte à exportação de PSD para PDF com Camadas de Ajuste](/psd/pt/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|Recurso|
|PSDNET-179|Problema Obter Efeito DropShadowEffect da Camada|Melhoria|
|PSDNET-203|Quando o texto é atualizado com caracteres / (barra inclinada), o arquivo não pode ser aberto no Photoshop|Erro|
|PSDNET-199|Arquivo PSD não pode ser salvo quando a camada de texto contém apenas quebra de linha|Erro|
|PSDNET-185|Tamanho de fonte errado extraído|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P: Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P: Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M: Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M: Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F: Aspose.PSD.ResizeType.CatmullRom
- F: Aspose.PSD.ResizeType.CubicConvolution
- F: Aspose.PSD.ResizeType.CubicBSpline
- F: Aspose.PSD.ResizeType.Mitchell
- F: Aspose.PSD.ResizeType.SinC
- F: Aspose.PSD.ResizeType.Bell
# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**
**PSDNET-207. Suporte à Camada de Ajuste de Equilíbrio de Cor**

{{< highlight java >}}

            var caminhoArquivo = "ColorBalance.psd";

            var caminhoSaida = "ColorBalance_out.psd";

            using (var im = (PsdImage)Image.Load(caminhoArquivo))

            {

                foreach (var camada in im.Layers)

                {

                    var camadaEquilibrioCor = camada as ColorBalanceAdjustmentLayer;

                    if (camadaEquilibrioCor != null)

                    {

                        camadaEquilibrioCor.ShadowsCyanRedBalance = 30;

                        camadaEquilibrioCor.ShadowsMagentaGreenBalance = -15;

                        camadaEquilibrioCor.ShadowsYellowBlueBalance = 40;

                        camadaEquilibrioCor.MidtonesCyanRedBalance = -90;

                        camadaEquilibrioCor.MidtonesMagentaGreenBalance = -25;

                        camadaEquilibrioCor.MidtonesYellowBlueBalance = 20;

                        camadaEquilibrioCor.HighlightsCyanRedBalance = -30;

                        camadaEquilibrioCor.HighlightsMagentaGreenBalance = 67;

                        camadaEquilibrioCor.HighlightsYellowBlueBalance = -95;

                        camadaEquilibrioCor.PreserveLuminosity = true;

                    }

                }

                im.Save(caminhoSaida);

            }

{{< /highlight >}}

**PSDNET-145. Suporte à Camada de Inversão de Cores**

{{< highlight java >}}

            var caminhoArquivo = "InvertStripes_before.psd";

            var caminhoSaida = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(caminhoArquivo))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(caminhoSaida);

            }

{{< /highlight >}}

**PSDNET-139. Implementar Bicubic Resampler**

{{< highlight java >}}

             string arquivoFonte = "amostra.psd";

            string nomeDestino = "ResamplerCubicConvolutionStripes_after.psd";

            // Carregar uma imagem existente em uma instância da classe PsdImage

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))

            {

                imagem.Resize(300, 300, ResizeType.CubicConvolution);

                imagem.Save(nomeDestino, new PsdOptions(imagem));

            }

            string arquivoFonte = "amostra.psd";

            string nomeDestino = "ResamplerCatmullRomStripes_after.psd";

            // Carregar uma imagem existente em uma instância da classe PsdImage

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))

            {

                imagem.Resize(300, 300, ResizeType.CatmullRom);

                imagem.Save(nomeDestino, new PsdOptions(imagem));

            }

            string arquivoFonte = "amostra.psd";

            string nomeDestino = "ResamplerMitchellStripes_after.psd";

            // Carregar uma imagem existente em uma instância da classe PsdImage

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))

            {

                imagem.Resize(300, 300, ResizeType.Mitchell);

                imagem.Save(nomeDestino, new PsdOptions(imagem));

            }

            string arquivoFonte = "amostra.psd";

            string nomeDestino = "ResamplerCubicBSplineStripes_after.psd";

            // Carregar uma imagem existente em uma instância da classe PsdImage

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))

            {

                imagem.Resize(300, 300, ResizeType.CubicBSpline);

                imagem.Save(nomeDestino, new PsdOptions(imagem));

            }

            string arquivoFonte = "amostra.psd";

            string nomeDestino = "ResamplerSinCStripes_after.psd";

            // Carregar uma imagem existente em uma instância da classe PsdImage

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))

            {

                imagem.Resize(300, 300, ResizeType.SinC);

                imagem.Save(nomeDestino, new PsdOptions(imagem));

            }

            string arquivoFonte = "amostra.psd";

            string nomeDestino = "ResamplerBellStripes_after.psd";

            // Carregar uma imagem existente em uma instância da classe PsdImage

            using (PsdImage imagem = (PsdImage)Image.Load(arquivoFonte))

            {

                imagem.Resize(300, 300, ResizeType.Bell);

                imagem.Save(nomeDestino, new PsdOptions(imagem));

            }

{{< /highlight >}}

**PSDNET-169. Adicionar suporte à exportação de PSD para PDF com Máscara de Recorte**

{{< highlight java >}}

     using (PsdImage imagem = (PsdImage)Image.Load("clip.psd"))

    {

      imagem.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}



**PSDNET-168. Adicionar suporte à exportação de PSD para PDF com Camadas de Ajuste**

{{< highlight java >}}

      using (PsdImage imagem = (PsdImage)Image.Load("exemplo.psd"))

    {

      imagem.Save("documento.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. Quando o texto é atualizado com / (barra inclinada), o arquivo não pode ser aberto no Photoshop**

{{< highlight java >}}

         var imagemPsd = (PsdImage)imagem;

        var camadas = imagemPsd.Layers;

        for (var indice = camadas.Length - 1; indice >= 0; indice--)

        {

            var camada = camadas[indice];

            if (!(camada is TextLayer)) continue;

            var camadaTexto = (TextLayer)camada;

            camadaTexto.UpdateText("/");

        }

        var opcoesImagem = new PsdOptions(imagemPsd);

        var nomeArquivo = Path.GetFileName(caminhoArquivo);

        var caminhoSaidaArquivo = Path.GetDirectoryName(caminhoArquivo) + "\\alvo_" + nomeArquivo;

        imagemPsd.Save(caminhoSaidaArquivo, opcoesImagem);



{{< /highlight >}}

**PSDNET-199. Arquivo PSD não pode ser salvo quando a camada de texto contém apenas quebra de linha**

{{< highlight java >}}

 string caminhoArquivo = "testLineBreaks2.psd";

string caminhoSaida = "testLineBreaks2_modificado.psd";

var novoTexto = "\r";

        using (var imagem = Image.Load(caminhoArquivo))

        {

            var imagemPsd = imagem as PsdImage;

            if (imagem == null)

            {

                return;

            }

            var camadas = imagemPsd.Layers;

            for (var indice = camadas.Length - 1; indice >= 0; indice--)

            {

                var camada = camadas[indice] as TextLayer;

                if (camada == null)

                {

                    continue;

                }

                camada.UpdateText(novoTexto);

            }

            var opcoesImagem = new PsdOptions(imagemPsd);

            imagemPsd.Save(caminhoSaida, opcoesImagem);

        }

{{< /highlight >}}

**PSDNET-185. Tamanho de fonte errado extraído**

{{< highlight java >}}

             // Tamanho de fonte errado extraído

            string caminhoArquivo = "直播+电商.psd";

            var tolerancia = 0.001;

            using (var imagem = Image.Load(caminhoArquivo))

            {

                int indiceCamada = 22;

                // API antiga (Usando o tamanho da fonte do primeiro parágrafo)

                PsdImage imagemPsd = imagem as PsdImage;

                double[] matriz = ((TextLayer)imagemPsd.Layers[indiceCamada]).TransformMatrix;

                double tamanhoBaseFonte = ((TextLayer)imagemPsd.Layers[indiceCamada]).Font.Size;

                double tamanhoFonte = matriz[0] * tamanhoBaseFonte;

                // Verificando o tamanho base da fonte

                if (Math.Abs(100.0 - tamanhoBaseFonte) > tolerancia)

                {

                    throw new Exception("O tamanho da fonte foi lido incorretamente");

                }

                // Verificando o tamanho real da fonte

                if (Math.Abs(88.425 - tamanhoFonte) > tolerancia)

                {

                    throw new Exception("A matriz de transformação foi lida incorretamente");

                }

                // Nova API (Uma camada de texto pode conter qualquer quantidade de tamanhos de fonte)

                ITextPortion[] porções = ((TextLayer)imagemPsd.Layers[indiceCamada]).TextData.Items;

                ITextStyle estilo = porções[0].Style;

                double tamanhoFonteDaPorção = matriz[0] * estilo.FontSize;

                // Verificando o tamanho da fonte da porção base

                if (Math.Abs(100.0 - estilo.FontSize) > tolerancia)

                {

                    throw new Exception("O tamanho da fonte foi lido incorretamente");

                }

                // Verificando o tamanho real da fonte da porção

                if (Math.Abs(88.425 - tamanhoFonteDaPorção) > tolerancia)

                {

                    throw new Exception("A matriz de transformação foi lida incorretamente");

                }

            }

{{< /highlight >}}

**PSDNET-179. Problema Obter Efeito de Sombra na Camada**

{{< highlight java >}}

       // Quando a propriedade DropShadowEffect.UseGlobalLight é 'true', então o objeto DropShadowEffect utiliza o valor do ângulo da propriedade PsdImage.GlobalAngle.

		using (PsdImage imagem = (PsdImage)Image.Load("4.psd"))

		{

    		imagem.GlobalAngle = 30;

    		imagem.Save("output.psd");

		}

{{< /highlight >}}
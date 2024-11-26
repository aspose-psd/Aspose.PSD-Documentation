---
title: Notas de Lançamento do Aspose.PSD para .NET 23.12
type: docs
weight: 10
url: /pt/net/aspose-psd-for-net-23-12-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 23.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                                 | **Categoria** |
|:------------|:----------------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1679 | [Formato AI] Adicionar suporte à renderização de Imagem de Raster na nova versão do AI                    |   Funcionalidade   |
| PSDNET-1454 | Lidar com Ruído do tipo Gradiente em GdflResrource                                                       |   Funcionalidade   |
| PSDNET-1827 | Erro "Referência de objeto não definida para uma instância de um objeto." ao salvar a Camada de Texto após a Atualização        |     Bug     |
| PSDNET-1776 | Corrigir o carregamento manual de fontes no MacOS usando System.Drawing.Common e Aspose.Drawing.        |     Bug     |
| PSDNET-1536 | AllowWarpRepaint nas PsdLoadOptions leva à exceção                                                      |     Bug     |
| PSDNET-1714 | [Formato AI] Implementar o processamento de fluxos de referência cruzada                                | Melhoria |
| PSDNET-1834 | Controle de Licença para VectorPathDataResource funciona incorretamente                                 | Melhoria |
| PSDNET-770  | Abrir qualquer arquivo de imagem como um objeto inteligente incorporado na imagem PSD                 | Melhoria |
| PSDNET-1864 | Sistema de Licença do Plugin Aspose.PSD                                                                  | Melhoria |



## **Alterações na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.#ctor(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.RGB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.HSB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.LAB
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientMode
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.#ctor
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.Metered.GetProductName
- M:Aspose.PSD.Metered.IsMeteredLicensed
- T:Aspose.PSD.PluginLicenseException
- M:Aspose.PSD.PluginLicenseException.#ctor
- M:Aspose.PSD.Metered.Equals(System.Object)

# **APIs Removidas:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **Exemplos de Uso:**

**PSDNET-1679. [Formato AI] Adicionar suporte à renderização de Imagem de Raster na nova versão do AI**

{{< highlight csharp >}}
            string arquivoOrigem = Path.Combine(pastaBase, "raster.ai");
            string arquivoSaida = Path.Combine(pastaSaida, "raster_output.png");

            using (AiImage imagem = (AiImage)Image.Load(arquivoOrigem))
            {
                imagem.Save(arquivoSaida, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1454. Lidar com Ruído do tipo Gradiente em GdflResrource**

{{< highlight csharp >}}
            string arquivoOrigem = "Gradient-Fill.psd";
            string arquivoDestino = "Gradient-Fill-out.psd";

            using (var imagem = (PsdImage)Image.Load(arquivoOrigem, new PsdLoadOptions()))
            {
                Layer camada = imagem.Layers[1];

                foreach (LayerResource recurso in camada.Resources)
                {
                    GdFlResource recursoGdFl = recurso as GdFlResource;

                    if (recursoGdFl != null)
                    {
                        recursoGdFl.Scale = 90;
                        recursoGdFl.Angle = 30;
                        recursoGdFl.Dither = false;
                        recursoGdFl.AlignWithLayer = true;
                        recursoGdFl.Reverse = false;

                        break;
                    }
                }

                imagem.Save(arquivoDestino, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-1827. Erro "Referência de objeto não definida para uma instância de um objeto." ao salvar a Camada de Texto após a Atualização**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "input_1827.psd");
string arquivoSaida = Path.Combine(pastaSaida, "out_1827.psd");

using (var imagemPSD = (PsdImage)Image.Load(arquivoOrigem))
{
    foreach (var camada in imagemPSD.Layers)
    {
        if (camada is TextLayer camadaTexto)
        {
            camadaTexto.TextData.UpdateLayerData();
        }
    }

    // Não deve haver erro aqui
    imagemPSD.Save(arquivoSaida);
}
{{< /highlight >}}

**PSDNET-1536. AllowWarpRepaint nas PsdLoadOptions leva à exceção**

{{< highlight csharp >}}
            string arquivoOrigem = @"SizeChart-4 Colors.psd";
            string arquivoSaida = @"SizeChart-4 Colors.png";

            using (var imagemPSD = (PsdImage)Aspose.PSD.Image.Load(arquivoOrigem, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true })) 
			{ 
				imagemPSD.Save(arquivoSaida + "_original.png", new PngOptions()
				{
					ColorType = PngColorType.TruecolorWithAlpha,
					Progressive = true,
					CompressionLevel = 9
				});
			}
{{< /highlight >}}

**PSDNET-1834. Controle de Licença para VectorPathDataResource funciona incorretamente**

{{< highlight csharp >}}
 using (PsdImage im = (PsdImage)Image.Load(DifferentLayerMasks.psd))
 {
     im.Save(complexFiles[i] + "out" + "output.psd");
     im.Save(complexFiles[i] + "out" + "output.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
 }
{{< /highlight >}}

**PSDNET-770. Abrir qualquer arquivo de imagem como um objeto inteligente incorporado na imagem PSD**

{{< highlight csharp >}}
string arquivoOrigem = Path.Combine(pastaBase, "empty.psd");

string arquivoAdicionarArvore = Path.Combine(pastaBase, "tree.psd");
string arquivoAdicionarGelo = Path.Combine(pastaBase, "frost.png");

string arquivoSaidaArvore = Path.Combine(pastaSaida, "tree_export.psd");
string arquivoSaidaGelo = Path.Combine(pastaSaida, "frost_export.psd");

using (var imagemPSD = (PsdImage)Image.Load(arquivoOrigem, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream stream = new FileStream(arquivoAdicionarArvore, FileMode.Open))
    {
        using (SmartObjectLayer camadaInteligente = new SmartObjectLayer(stream))
        {
            imagemPSD.AddLayer(camadaInteligente);

            imagemPSD.Save(arquivoSaidaArvore, new PsdOptions());                        
        }
    }
}

using (var imagemPSD = (PsdImage)Image.Load(arquivoOrigem, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream stream = new FileStream(arquivoAdicionarGelo, FileMode.Open))
    {
        using (SmartObjectLayer camadaInteligente = new SmartObjectLayer(stream))
        {
            imagemPSD.AddLayer(camadaInteligente);

            imagemPSD.Save(arquivoSaidaGelo, new PsdOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1864. Sistema de Licença do Plugin Aspose.PSD**

{{< highlight csharp >}}            
    var metered = new Metered();
    metered.SetMeteredKey(pluginPublic, pluginPrivate);
			
	// Manipulação específica do Plugin
{{< /highlight >}}
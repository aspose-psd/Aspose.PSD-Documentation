---
title: Aspose.PSD para .NET 19.11 - Notas de Lançamento
type: docs
weight: 20
url: /pt/net/aspose-psd-para-net-19-11-notas-de-lancamento/
---

{{% alert color="primary" %}} 

Esta página contém as notas de lançamento para [Aspose.PSD para .NET 19.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-151|[Suporte ao Efeito de Sombra Interna](/psd/pt/net/efeitos-de-sombra-no-photoshop/#efeitosdesombranophotoshop-sombradentro)|Recurso|
|PSDNET-135|[Implementar renderização da Camada de Preenchimento: Padrão](/psd/pt/net/suporte-de-camadas-de-preenchimento/#suportedecamadasdepreenchimento-camadasdepreenchimentocompadrao)|Recurso|
|PSDNET-187|[Suporte a Imagens Raster em Arquivos de Formato AI](/psd/pt/net/manipulando-formatos-adobe-illustrator/#manipulandoformatosadobeillustrator-imagensrasternoillustrator)|Recurso|
|PSDNET-225|[Obter propriedades de formatação inline de TextLayer](/psd/pt/net/trabalhando-com-camadas-de-texto/#trabalhandocomcamadasdetexto-obterpropriedadesdetextodeumacamadadetexto)|Recurso|
|PSDNET-214|Exportação incorreta de PSD para outros formatos se contém Efeitos de Camada e Camadas de Ajuste|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Ai.AiSection
- M:Aspose.PSD.FileFormats.Ai.AiSection.GetData
- P:Aspose.PSD.FileFormats.Ai.AiImage.Layers
- M:Aspose.PSD.FileFormats.Ai.AiImage.AddLayer(Aspose.PSD.FileFormats.Ai.AiLayerSection)
- T:Aspose.PSD.FileFormats.Ai.AiLayerSection
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.RasterImages
- M:Aspose.PSD.FileFormats.Ai.AiLayerSection.AddRasterImage(Aspose.PSD.FileFormats.Ai.AiRasterImageSection)
- T:Aspose.PSD.FileFormats.Ai.AiRasterImageSection
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Pixels
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.OffsetX
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.OffsetY
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Width
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Angle
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.LeftBottomShift
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Height
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddInnerShadow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.UseGlobalLight
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Distance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.UseGlobalLight
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Distance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Noise
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.GetFonts
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.FontType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Script
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Synthetic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.PostScriptName
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.FamilyName
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Style
# **APIs Removidas:**
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData

## **Exemplos de Uso:**
**PSDNET-151. Suporte ao Efeito de Sombra Interna**

{{< highlight java >}}

            string sourceFile = "sample.psd";

            string destName = "sample_out.psd";

            var loadOptions = new PsdLoadOptions()

            {

                LoadEffectsResource = true

            };

            // Carregar uma imagem existente em uma instância da classe PsdImage

            using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))

            {

                var layer = image.Layers[image.Layers.Length - 1];

                var shadowEffect = (IShadowEffect)layer.BlendingOptions.Effects[0];

                shadowEffect.Color = Color.Green;

                shadowEffect.Opacity = 128;

                shadowEffect.Distance = 1;

                shadowEffect.UseGlobalLight = false;

                shadowEffect.Size = 2;

                shadowEffect.Angle = 45;

                shadowEffect.Spread = 50;

                shadowEffect.Noise = 5;

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-135. Implementar a renderização da Camada de Preenchimento: Padrão**

{{< highlight java >}}

            string sourceFile = "sample.psd";

            string destName = "sample_out.psd";

            // Carregar uma imagem existente em uma instância da classe PsdImage

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                foreach (var layer in image.Layers)

                {

                    if (layer is FillLayer)

                    {

                        var fillLayer = (FillLayer)layer;

                        var settings = (IPatternFillSettings)fillLayer.FillSettings;

                        settings.HorizontalOffset = -5;

                        settings.VerticalOffset = 12;

                        settings.Scale = 300;

                        settings.Linked = true;

                        settings.PatternData = new int[]

                                                   {

                                                       Color.Black.ToArgb(), Color.Red.ToArgb(),

                                                       Color.Green.ToArgb(), Color.Blue.ToArgb(),

                                                       Color.White.ToArgb(), Color.AliceBlue.ToArgb(),

                                                       Color.Violet.ToArgb(), Color.Chocolate.ToArgb(),

                                                       Color.IndianRed.ToArgb(), Color.DarkOliveGreen.ToArgb(),

                                                       Color.CadetBlue.ToArgb(), Color.YellowGreen.ToArgb(),

                                                       Color.Black.ToArgb(), Color.Azure.ToArgb(),

                                                       Color.ForestGreen.ToArgb(), Color.Sienna.ToArgb(),

                                                   };

                        settings.PatternHeight = 4;

                        settings.PatternWidth = 4;

                        settings.PatternName = "$$$/Presets/Patterns/ColorfulSquare=Colorful Square New\0";

                        settings.PatternId = Guid.NewGuid().ToString() + "\0";

                        fillLayer.Update();

                        break;

                    }

                }

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-187. Suporte a Imagens Raster em Arquivos de Formato AI**

{{< highlight java >}}

const double TolerânciaPadrao = 1e-6;

void AssertIsTrue(bool condição, string mensagem) {

 if (!condição) {

  throw new FormatException(mensagem);

 }

}

string arquivoFonte = "sample.ai";

using(AiImage imagem = (AiImage) Image.Load(arquivoFonte)) {

 AiLayerSection camada = imagem.Layers[0];

 AssertIsTrue(camada.RasterImages != null, "A propriedade RasterImages deve ser diferente de nulo");

 AssertIsTrue(camada.RasterImages.Length == 1, "A propriedade RasterImages deve conter exatamente um item");

 AiRasterImageSection imagemRaster = camada.RasterImages[0];

 AssertIsTrue(imagemRaster.Pixels != null, "A propriedade Pixels da imagemRaster deve ser diferente de nulo");

 AssertIsTrue(imagemRaster.Pixels.Length == 100, "A propriedade Pixels da imagemRaster deve conter exatamente 100 itens");

 AssertIsTrue((uint) imagemRaster.Pixels[99] == 0xFFB21616, "imagemRaster.Pixels[99] deve ser 0xFFB21616");

 AssertIsTrue((uint) imagemRaster.Pixels[19] == 0xFF00FF00, "imagemRaster.Pixels[19] deve ser 0xFF00FF00");

 AssertIsTrue((uint) imagemRaster.Pixels[10] == 0xFF01FD00, "imagemRaster.Pixels[10] deve ser 0xFF01FD00");

 AssertIsTrue((uint) imagemRaster.Pixels[0] == 0xFF0000FF, "imagemRaster.Pixels[0] deve ser 0xFF0000FF");

 AssertIsTrue(Math.Abs(0.999875 - imagemRaster.Width) < TolerânciaPadrao, "A largura da imagemRaster deve ser 0.99987");

 AssertIsTrue(Math.Abs(0.999875 - imagemRaster.Height) < TolerânciaPadrao, "A altura da imagemRaster deve ser 0.99987");

 AssertIsTrue(Math.Abs(387 - imagemRaster.OffsetX) < TolerânciaPadrao, "O OffsetX da imagemRaster deve ser 387");

 AssertIsTrue(Math.Abs(379 - imagemRaster.OffsetY) < TolerânciaPadrao, "O OffsetY da imagemRaster deve ser 379");

 AssertIsTrue(Math.Abs(0 - imagemRaster.Angle) < TolerânciaPadrao, "O Ângulo da imagemRaster deve ser 0");

 AssertIsTrue(Math.Abs(0 - imagemRaster.LeftBottomShift) < TolerânciaPadrao, "O Deslocamento Inferior Esquerdo da imagemRaster deve ser 0");

 AssertIsTrue(Math.Abs(0 - imagemRaster.ImageRectangle.X) < TolerânciaPadrao, "O X do retângulo da imagemRaster deve ser 0");

 AssertIsTrue(Math.Abs(0 - imagemRaster.ImageRectangle.Y) < TolerânciaPadrao, "O Y do retângulo da imagemRaster deve ser 0");

 AssertIsTrue(Math.Abs(10 - imagemRaster.ImageRectangle.Width) < TolerânciaPadrao, "A largura do retângulo da imagemRaster deve ser 10");

 AssertIsTrue(Math.Abs(10 - imagemRaster.ImageRectangle.Height) < TolerânciaPadrao, "A altura do retângulo da imagemRaster deve ser 10");

}

{{< /highlight >}}

**PSDNET-225. Obter propriedades de formatação inline de TextLayer**

{{< highlight java >}}

     using (var psdImage = (PsdImage)Image.Load("inline_formatting.psd"))

            {

                List<ITextPortion> textoRegular = new List<ITextPortion>();

                List<ITextPortion> textoNegrito = new List<ITextPortion>();

                List<ITextPortion> textoItálico = new List<ITextPortion>();

                var camadas = psdImage.Layers;

                for (int índice = 0; índice < camadas.Length; índice++)

                {

                    var camada = camadas[índice];

                    if (!(camada is TextLayer))

                    {

                        continue;

                    }

                    var camadaTexto = (TextLayer)camada;

                    // obter fontes contidas na camada de texto

                    var fontes = camadaTexto.GetFonts();

                    var porçõesTexto = camadaTexto.TextData.Items;

                    foreach (var porçãoTexto in porçõesTexto)

                    {

                        TextFontInfo fonte = fontes[porçãoTexto.Style.FontIndex];

                        if (fonte != null)

                        {

                            switch (fonte.Style)

                            {

                                case FontStyle.Regular:

                                    textoRegular.Add(porçãoTexto);

                                    break;

                                case FontStyle.Bold:

                                    textoNegrito.Add(porçãoTexto);

                                    break;

                                case FontStyle.Italic:

                                    textoItálico.Add(porçãoTexto);

                                    break;

                                default:

                                    throw new ArgumentOutOfRangeException();

                            }

                        }

                    }

                }

            }

{{< /highlight >}}



**PSDNET-214. Exportação incorreta de PSD para outros formatos se contém Efeitos de Camada e Camadas de Ajuste**

{{< highlight java >}}

     var loadOptions = new PsdLoadOptions();

   loadOptions.LoadEffectsResource = true;

   using (var image = (PsdImage)Image.Load("clip_shadow.psd", loadOptions))

   {

       image.Save("output.png", new PngOptions());

   }

{{< /highlight >}}
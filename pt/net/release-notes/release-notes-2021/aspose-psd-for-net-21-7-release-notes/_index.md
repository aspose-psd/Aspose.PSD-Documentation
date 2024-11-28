---
title: Notas de Lançamento do Aspose.PSD para .NET 21.7
type: docs
weight: 60
url: /pt/net/aspose-psd-for-net-21-7-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém as notas de lançamento para o [Aspose.PSD para .NET 21.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-806|Suporte para edição de fonte usando TextPortions|Recurso|
|PSDNET-917|Aspose.PSD 21.6: ImageSaveException ao tentar converter PSD para PNG|Erro|
|PSDNET-858|Adicionar à Configuração Aspose.PSD .Net 5.0|Melhoria|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FontSettings.GetAdobeFontName(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontName

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDNET-806. Suporte para edição de fonte usando TextPortions**

{{< highlight csharp >}}
            string outputFilePng = "resultado_fontEditTest.png";
            string outputFilePsd = "fontEditTest.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Os objetos não são iguais.");
                }
            }

            using (var image = new PsdImage(500, 500))
            {
                FillLayer backgroundFillLayer = FillLayer.CreateInstance(FillType.Color);
                ((IColorFillSettings)backgroundFillLayer.FillSettings).Color = Color.White;
                image.AddLayer(backgroundFillLayer);

                TextLayer textLayer = image.AddTextLayer("Texto 1", new Rectangle(10, 35, image.Width, 35));

                ITextPortion firstPortion = textLayer.TextData.Items[0];
                firstPortion.Style.FontName = FontSettings.GetAdobeFontName("Comic Sans MS");

                var secondPortion = textLayer.TextData.ProducePortion();
                secondPortion.Text = "Texto 2";
                secondPortion.Paragraph.Apply(firstPortion.Paragraph);
                secondPortion.Style.Apply(firstPortion.Style);
                secondPortion.Style.FontName = FontSettings.GetAdobeFontName("Arial");

                textLayer.TextData.AddPortion(secondPortion);
                textLayer.TextData.UpdateLayerData();

                image.Save(outputFilePng, new PngOptions());
                image.Save(outputFilePsd);
            }

            using (var image = (PsdImage)Image.Load(outputFilePsd))
            {
                TextLayer textLayer = (TextLayer)image.Layers[2];

                string adobeFontName1 = FontSettings.GetAdobeFontName("Comic Sans MS");
                string adobeFontName2 = FontSettings.GetAdobeFontName("Arial");

                AssertAreEqual(adobeFontName1, textLayer.TextData.Items[0].Style.FontName);
                AssertAreEqual(adobeFontName2, textLayer.TextData.Items[1].Style.FontName);
            }
{{< /highlight >}}

**PSDNET-917. Aspose.PSD 21.6: ImageSaveException ao tentar converter PSD para PNG**

{{< highlight csharp >}}
            string srcFile = "entrada.psd";
            string output = "saida.png";

            using (var image = Aspose.PSD.Image.Load(srcFile))
            {
                image.Save(output, new Aspose.PSD.ImageOptions.PngOptions());
            }
{{< /highlight >}}

---
title: Релизные заметки Aspose.PSD для .NET 21.7
type: docs
weight: 60
url: /ru/net/aspose-psd-for-net-21-7-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся релизные заметки для [Aspose.PSD для .NET 21.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-806|Поддержка редактирования шрифтов с использованием TextPortions|Функциональность|
|PSDNET-917|Aspose.PSD 21.6: ImageSaveException при попытке конвертации PSD в PNG|Ошибка|
|PSDNET-858|Добавление конфигурации для Aspose.PSD .Net 5.0|Улучшение|

## **Изменения в общедоступном API**
# **Добавленные API:**
- M:Aspose.PSD.FontSettings.GetAdobeFontName(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontName

# **Удаленные API:**
- Нет

## **Примеры использования:**

**PSDNET-806. Поддержка редактирования шрифтов с использованием TextPortions**

{{< highlight csharp >}}
            string outputFilePng = "result_fontEditTest.png";
            string outputFilePsd = "fontEditTest.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Объекты не равны.");
                }
            }

            using (var image = new PsdImage(500, 500))
            {
                FillLayer backgroundFillLayer = FillLayer.CreateInstance(FillType.Color);
                ((IColorFillSettings)backgroundFillLayer.FillSettings).Color = Color.White;
                image.AddLayer(backgroundFillLayer);

                TextLayer textLayer = image.AddTextLayer("Текст 1", new Rectangle(10, 35, image.Width, 35));

                ITextPortion firstPortion = textLayer.TextData.Items[0];
                firstPortion.Style.FontName = FontSettings.GetAdobeFontName("Comic Sans MS");

                var secondPortion = textLayer.TextData.ProducePortion();
                secondPortion.Text = "Текст 2";
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

**PSDNET-917. Aspose.PSD 21.6: ImageSaveException при попытке конвертации PSD в PNG**

{{< highlight csharp >}}
            string srcFile = "input.psd";
            string output = "output.png";

            using (var image = Aspose.PSD.Image.Load(srcFile))
            {
                image.Save(output, new Aspose.PSD.ImageOptions.PngOptions());
            }
{{< /highlight >}}

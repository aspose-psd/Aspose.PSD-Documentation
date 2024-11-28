---
title: Aspose.PSD за .NET 21.7 - Бележки към версията
type: docs
weight: 60
url: /bg/net/aspose-psd-za-dotnet-21-7-belejki-kam-versiyata/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележките за версията на [Aspose.PSD за .NET 21.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-806|Поддръжка за редакция на шрифтове, използвайки TextPortions|Функционалност|
|PSDNET-917|Aspose.PSD 21.6: ImageSaveException при опит за конвертиране на PSD към PNG|Проблем|
|PSDNET-858|Добавяне на конфигурация за Aspose.PSD .Net 5.0|Подобрение|

## **Промени в публичното API**
# **Добавени API:**
- M:Aspose.PSD.FontSettings.GetAdobeFontName(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontName

# **Премахнати API:**
- Няма

## **Примери за използване:**

**PSDNET-806. Поддръжка за редакция на шрифтове, използвайки TextPortions**

{{< highlight csharp >}}
            string outputFilePng = "резултат_fontEditTest.png";
            string outputFilePsd = "fontEditTest.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("Обектите не са равни.");
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

**PSDNET-917. Aspose.PSD 21.6: ImageSaveException при опит за конвертиране на PSD към PNG**

{{< highlight csharp >}}
            string srcFile = "вход.psd";
            string output = "изход.png";

            using (var image = Aspose.PSD.Image.Load(srcFile))
            {
                image.Save(output, new Aspose.PSD.ImageOptions.PngOptions());
            }
{{< /highlight >}}

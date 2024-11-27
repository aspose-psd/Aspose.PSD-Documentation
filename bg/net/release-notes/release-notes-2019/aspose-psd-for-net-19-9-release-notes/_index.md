---
title: Aspose.PSD за .NET 19.9 - Бележки към версията
type: docs
weight: 40
url: /bg/net/aspose-psd-for-net-19-9-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки към версията за [Aspose.PSD за .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-160|Грешно извлечено име на слой|Функционалност|
|PSDNET-175|Получаване на свойствата на текста от различен порцион текст във PSD TextLayer|Функционалност|
|PSDNET-190|Поддръжка за добавяне на група слой|Функционалност|
|PSDNET-192|Поддръжка на свойство Scale за Gradient Fill Layer|Функционалност|
|PSDNET-162|Настройка на яркостта|Подобрение|
|PSDNET-174|IndexOutOfRangeException при запазване на PSD изображение като JPEG|Проблем|
|PSDNET-180|Актуализация на текстов слой, който хвърля изключение|Проблем|
|PSDNET-182|Запазване на PSD изображение след операция RotateFlip произвежда повреден файл, който не може да бъде отворен|Проблем|

## **Промени в публичното API**
# **Добавени API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **Премахнати API:**
- Нито едно

## **Примери за използване:**
**PSDNET-160. Грешно извлечено име на слой**

За да се покаже името на слоя правилно, използвайте свойството **DisplayName**. Вече е добавен setter за това свойство и то може да бъде модифицирано. Когато Photoshop запазва име на слоя, използвайки свойството Име, към него като ASCII се запазват корейски знаци като байт 63 '?'. Използвайте свойството **DisplayName**, защото свойството Име не поддържа корейски знаци.

{{< highlight java >}}

             // направете промени в имената на слоевете и ги запазвайте

            using (var image = (PsdImage)Image.Load("layers with names.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var layer = image.Layers[i];

                    // задаване на нова стойност в свойството DisplayName

                    layer.DisplayName += "_changed";

                }

                image.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. Получаване на свойствата на текста от различен порцион текст във PSD TextLayer**

{{< highlight java >}}

            const double Tolerance = 0.0001;

            var filePath = "ThreeColorsParagraphs.psd";

            var outputPath = "ThreeColorsParagraph_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var layer = im.Layers[i] as TextLayer;

                    if (layer != null)

                    {

                        var portions = layer.TextData.Items;

                        if (portions.Length != 4)

                        {

                            throw new Exception();

                        }

                        // Проверка на текста във всеки порцион

                        if (portions[0].Text != "Стар " ||

                            portions[1].Text != "цвят" ||

                            portions[2].Text != " текст\r" ||

                            portions[3].Text != "Втори параграф\r")

                        {

                            throw new Exception();

                        }

                        // Проверка на данните на параграфите

                        // Параграфите имат различно подравняване

                        if (

                            portions[0].Paragraph.Justification != 0 ||

                            portions[1].Paragraph.Justification != 0 ||

                            portions[2].Paragraph.Justification != 0 ||

                            portions[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // Всички други свойства на първия и втория параграф са равни

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var paragraph = portions[j].Paragraph;

                            if (Math.Abs(paragraph.AutoLeading - 1.2) > Tolerance ||

                                paragraph.AutoHyphenate != false ||

                                paragraph.Burasagari != false ||

                                paragraph.ConsecutiveHyphens != 8 ||

                                Math.Abs(paragraph.StartIndent) > Tolerance ||

                                Math.Abs(paragraph.EndIndent) > Tolerance ||

                                paragraph.EveryLineComposer != false ||

                                Math.Abs(paragraph.FirstLineIndent) > Tolerance ||

                                paragraph.GlyphSpacing.Length != 3 ||

                                Math.Abs(paragraph.GlyphSpacing[0] - 1) > Tolerance ||

                                Math.Abs(paragraph.GlyphSpacing[1] - 1) > Tolerance ||

                                Math.Abs(paragraph.GlyphSpacing[2] - 1) > Tolerance ||

                                paragraph.Hanging != false ||

                                paragraph.HyphenatedWordSize != 6 ||

                                paragraph.KinsokuOrder != 0 ||

                                paragraph.LetterSpacing.Length != 3 ||

                                Math.Abs(paragraph.LetterSpacing[0]) > Tolerance ||

                                Math.Abs(paragraph.LetterSpacing[1]) > Tolerance ||

                                Math.Abs(paragraph.LetterSpacing[2]) > Tolerance ||

                                paragraph.LeadingType != LeadingMode.Auto ||

                                paragraph.PreHyphen != 2 ||

                                paragraph.PostHyphen != 2 ||

                                Math.Abs(paragraph.SpaceBefore) > Tolerance ||

                                Math.Abs(paragraph.SpaceAfter) > Tolerance ||

                                paragraph.WordSpacing.Length != 3 ||

                                Math.Abs(paragraph.WordSpacing[0] - 0.8) > Tolerance ||

                                Math.Abs(paragraph.WordSpacing[1] - 1.0) > Tolerance ||

                                Math.Abs(paragraph.WordSpacing[2] - 1.33) > Tolerance ||

                                Math.Abs(paragraph.Zone - 36.0) > Tolerance)

                            {

                                throw new Exception();

                            }

                        }

                        // Проверка на данните за стиловете

                        // Стиловете имат различни цветове и размер на шрифта

                        if (Math.Abs(portions[0].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[1].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[2].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[3].Style.FontSize - 10) > Tolerance)

                        {

                            throw new Exception();

                        }

                        if (portions[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            portions[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            portions[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            portions[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var style = portions[j].Style;

                            if (style.AutoLeading != false ||

                                style.HindiNumbers != false ||

                                style.Kerning != 0 ||

                                style.Leading != 0 ||

                                style.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                style.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // Пример за редакция на текста

                        portions[0].Text = "Здравейте ";

                        portions[1].Text = "Свят";

                        // Пример за премахване на порции от текста

                        layer.TextData.RemovePortion(3);

                        layer.TextData.RemovePortion(2);

                        // Пример за добавяне на нова порция текст

                        var createdPortion = layer.TextData.ProducePortion();

                        createdPortion.Text = "!!!\r";

                        layer.TextData.AddPortion(createdPortion);

                        portions = layer.TextData.Items;

                        // Пример за редакция на параграфа и стиловете за порциите

                        // Задаване на право подравняване

                        portions[0].Paragraph.Justification = 1;

                        portions[1].Paragraph.Justification = 1;

                        portions[2].Paragraph.Justification = 1;

                        // Различни цветове за всеки стил. Те ще бъдат променени, но рендерирането не е изцяло поддържано

                        portions[0].Style.FillColor = Color.Aquamarine;

                        portions[1].Style.FillColor = Color.Violet;

                        portions[2].Style.FillColor = Color.LightBlue;

                        // Различен шрифт. Той ще бъде променен, но рендерирането не е изцяло поддържано

                        portions[0].Style.FontSize = 6;

                        portions[1].Style.FontSize = 8;

                        portions[2].Style.FontSize = 10;

                        layer.TextData.UpdateLayerData();

                        im.Save(outputPath, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Поддръжка за добавяне на група слой**

{{< highlight java >}}

             // -Група 1

            // --Слой 1

            // --Група 2

            // ---Слой 2

            // ---Слой 3

            // --Слой 4

            string dataDir = "psdnet190_test.psd";

            var createOptions = new PsdOptions();

            createOptions.Source = new FileCreateSource(dataDir, false);

            createOptions.Palette = new PsdColorPalette(new Color[] { Color.Green });

            using (var psdImage = (PsdImage)Image.Create(createOptions, 500, 500))

            {

                LayerGroup group1 = psdImage.AddLayerGroup("Група 1", 0, true);

                Layer layer1 = new Layer(psdImage);

                layer1.Name = "Слой 1";

                group1.AddLayer(layer1);

                LayerGroup group2 = group1.AddLayerGroup("Група 2", 1);

                Layer layer2 = new Layer(psdImage);

                layer2.Name = "Слой 2";

                group2.AddLayer(layer2);

                Layer layer3 = new Layer(psdImage);

                layer3.Name = "Слой 3";

                group2.AddLayer(layer3);

                Layer layer4 = new Layer(psdImage);

                layer4.Name = "Слой 4";

                group1.AddLayer(layer4);

                psdImage.Save();

            }

{{< /highlight >}}

**PSDNET-192. Поддръжка на свойство Scale за Gradient Fill Layer**

{{< highlight java >}}

            using (var image = (PsdImage)Image.Load("FillLayerGradient.psd"))

            {

                // получаване на слой за запълване

                FillLayer fillLayer = null;

                foreach (var layer in image.Layers)

                {

                    fillLayer = layer as FillLayer;

                    if (fillLayer != null)

                    {

                        break;

                    }

                }

                var settings = fillLayer.FillSettings as IGradientFillSettings;

                // актуализация на стойността на мащаба

                settings.Scale = 200;

                fillLayer.Update(); // Актуализализиране на данни за пиксели

                image.Save("scaledImage.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}



**PSDNET-174. IndexOutOfRangeException при запазване на PSD изображение като JPEG**

{{< highlight java >}}

         using (var image = Aspose.PSD.Image.Load("SamplePSD.psd"))

        {

            image.Save("sampleJPG.jpg", new JpegOptions());

        }

{{< /highlight >}}



**PSDNET-180. Актуализация на текстов слой, който хвърля изключение**

{{< highlight java >}}

           // Актуализация на текстов слой, който хвърля изключение

            string filePath = "FlipVertical.psd";

            string outputPath = "FlipVertical_changed.psd";

            var newText = "Тест";

            using (var image = Image.Load(filePath))

            {

                var psdImage = image as PsdImage;

                if (image == null)

                {

                    return;

                }

                var layers = psdImage.Layers;

                for (var index = layers.Length - 1; index >= 0; index--)

                {

                    var layer = layers[index] as TextLayer;

                    if (layer == null)

                    {

                        continue;

                    }

                    layer.UpdateText(newText);

                }

                var imageOptions = new PsdOptions(psdImage);

                psdImage.Save(outputPath, imageOptions);

            }

{{< /highlight >}}



**PSDNET-182. Запазване на PSD изображение след операция RotateFlip произвежда повреден файл, който не може да бъде отворен**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Трябва да се изпълнява без изключения

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Направете нищо

}

{{< /highlight >}}
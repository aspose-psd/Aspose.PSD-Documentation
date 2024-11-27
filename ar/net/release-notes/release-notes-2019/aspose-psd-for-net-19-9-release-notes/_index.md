```md
---
title: ملاحظات الإصدار Aspose.PSD لـ .NET 19.9
type: docs
weight: 40
url: /ar/net/aspose-psd-for-net-19-9-release-notes/
---

{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

** 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-160|استخراج اسم الطبقة بشكل خاطئ|ميزة|
|PSDNET-175|الحصول على خصائص النص من جزء نصي مختلف داخل طبقة النص في ملف PSD|ميزة|
|PSDNET-190|دعم إضافة مجموعة طبقات|ميزة|
|PSDNET-192|دعم خاصية Scale لطبقة تعبئة التدرج|ميزة|
|PSDNET-162|ضبط السطوع|تحسين|
|PSDNET-174|خطأ في مؤشر الخارجة عند حفظ صورة PSD كملف JPEG|خلل|
|PSDNET-180|تحديث نص الطبقة النصية يثير استثناء|خلل|
|PSDNET-182|حفظ صورة PSD بعد عملية RotateFlip ينتج ملف معطوب لا يمكن فتحه|خلل|

## **تغييرات واجهة برمجة التطبيقات العامة**
# **APIs المُضافة:**
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
# **APIs المُزالة:**
- None

## **أمثلة الاستخدام:**
**PSDNET-160. استخراج اسم الطبقة بشكل خاطئ**

لعرض اسم الطبقة بشكل صحيح، استخدم خاصية **DisplayName**. تمت إضافة setter الآن لهذه الخاصية ويمكن تعديل الخاصية. عندما يقوم Photoshop بحفظ اسم الطبقة باستخدام خاصية Name، يتم تخزين الأحرف الكورية كبايت 63'?' في ASCII. استخدم خاصية **DisplayName** لأن الخاصية Name لا تدعم الأحرف الكورية.

{{< highlight java >}}

             // قم بإجراء تغييرات في أسماء الطبقات واحفظها

            using (var image = (PsdImage)Image.Load("layers with names.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var layer = image.Layers[i];

                    // قم بتعيين قيمة جديدة في خاصية DisplayName

                    layer.DisplayName += "_changed";

                }

                image.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. الحصول على خصائص النص من جزء نصي مختلف داخل طبقة النص في ملف PSD**

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

                        // التحقق من نص كل جزء

                        if (portions[0].Text != "Old " ||

                            portions[1].Text != "color" ||

                            portions[2].Text != " text\r" ||

                            portions[3].Text != "Second paragraph\r")

                        {

                            throw new Exception();

                        }

                        // التحقق من بيانات الفقرات

                        // الفقرات لها تبرير مختلف

                        if (

                            portions[0].Paragraph.Justification != 0 ||

                            portions[1].Paragraph.Justification != 0 ||

                            portions[2].Paragraph.Justification != 0 ||

                            portions[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // جميع الخصائص الأخرى للفقرتين الأولى والثانية متساوية

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

                        // التحقق من بيانات الأسلوب

                        // الأساليب لها ألوان وحجم خط مختلفة

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

                        // مثال على تحرير النصوص

                        portions[0].Text = "Hello ";

                        portions[1].Text = "World";

                        // مثال على حذف أجزاء النص

                        layer.TextData.RemovePortion(3);
                        layer.TextData.RemovePortion(2);

                        // مثال على إضافة جزء نص جديد

                        var createdPortion = layer.TextData.ProducePortion();
                        createdPortion.Text = "!!!\r";

                        layer.TextData.AddPortion(createdPortion);

                        portions = layer.TextData.Items;

                        // مثال على تحرير الفقرة والأسلوب للأجزاء

                        // تعيين تبرير صحيح

                        portions[0].Paragraph.Justification = 1;
                        portions[1].Paragraph.Justification = 1;
                        portions[2].Paragraph.Justification = 1;

                        // ألوان مختلفة لكل أسلوب. سيتم التغيير، ولكن لم يتم دعم التقديم بشكل كامل
                        
                        portions[0].Style.FillColor = Color.Aquamarine;
                        portions[1].Style.FillColor = Color.Violet;
                        portions[2].Style.FillColor = Color.LightBlue;

                        // خط مختلف. سيتم التغيير، ولكن لم يتم دعم التقديم بشكل كامل

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

**PSDNET-190. دعم لإضافة مجموعة طبقات**

{{< highlight java >}}

             // -Group 1

            // --Layer 1

            // --Group 2

            // ---Layer 2

            // ---Layer 3

            // --Layer 4

            string dataDir = "psdnet190_test.psd";

            var createOptions = new PsdOptions();
            createOptions.Source = new FileCreateSource(dataDir, false);
            createOptions.Palette = new PsdColorPalette(new Color[] { Color.Green });

            using (var psdImage = (PsdImage)Image.Create(createOptions, 500, 500))

            {
                LayerGroup group1 = psdImage.AddLayerGroup("Group 1", 0, true);
                Layer layer1 = new Layer(psdImage);
                layer1.Name = "Layer 1";
                group1.AddLayer(layer1);
                LayerGroup group2 = group1.AddLayerGroup("Group 2", 1);
                Layer layer2 = new Layer(psdImage);
                layer2.Name = "Layer 2";
                group2.AddLayer(layer2);
                Layer layer3 = new Layer(psdImage);
                layer3.Name = "Layer 3";
                group2.AddLayer(layer3);
                Layer layer4 = new Layer(psdImage);
                layer4.Name = "Layer 4";
                group1.AddLayer(layer4);
                psdImage.Save();
            }

{{< /highlight >}}

**PS
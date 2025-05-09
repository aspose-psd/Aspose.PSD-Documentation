---
title: مصادر Aspose.PSD لـ .NET 21.3 - ملاحظات الإصدار
type: docs
weight: 100
url: /ar/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**مفتاح**|**ملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-823|إضافة SectionDividerLayer لتحسين التجربة مع مجموعات الطبقات|تعزيز|
|PSDNET-694|عند قراءة PattResource، تم تبديل العرض والارتفاع|خلل|
|PSDNET-789|الامتزاج غير صحيح لأكثر من تأثير في الطبقة الواحدة|خلل|
|PSDNET-805|ترتيب مزيج غير صحيح والمنطق عند وجود أكثر من تأثير في الطبقة الواحدة|خلل|
|PSDNET-842|خصائص تأثير الستروك لا تُحفظ في ملف PSD|خلل|

## **تغييرات الواجهة العامة (API)**
# **إضافة واجهات برمجة التطبيقات:**
- T: Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M: Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P: Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **إزالة واجهات البرمجة القديمة:**
- لا شيء

## **أمثلة الاستخدام:**

**PSDNET-694. عند قراءة PattResource، تم تبديل العرض والارتفاع**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // invoke pattern rendering

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. الامتزاج غير صحيح لأكثر من تأثير في الطبقة الواحدة**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Best";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }

                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. ترتيب مزيج غير صحيح والمنطق عند وجود أكثر من تأثير في الطبقة الواحدة**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. إضافة SectionDividerLayer لتحسين التجربة مع مجموعات الطبقات**

{{< highlight csharp >}}
            // The following code demonstrates SectionDividerLayer layers and how to get the related to it LayerGroup.

            // Layers hierarchy
            //    [0]: '</Layer group>' SectionDividerLayer for Group 1
            //    [1]: 'Layer 1' Regular Layer
            //    [2]: '</Layer group>' SectionDividerLayer for Group 2
            //    [3]: '</Layer group>' SectionDividerLayer for Group 3
            //    [4]: 'Group 3' GroupLayer
            //    [5]: 'Group 2' GroupLayer
            //    [6]: 'Group 1' GroupLayer

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objects are not equal.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Creating layers hierarchy
                // Add the LayerGroup 'Group 1'
                LayerGroup group1 = image.AddLayerGroup("Group 1", 0, true);
                // Add regular layer
                Layer layer1 = new Layer();
                layer1.DisplayName = "Layer 1";
                group1.AddLayer(layer1);
                // Add the LayerGroup 'Group 2'
                LayerGroup group2 = group1.AddLayerGroup("Group 2", 1);
                // Add the LayerGroup 'Group 3'
                LayerGroup group3 = group2.AddLayerGroup("Group 3", 0);

                // Gets the SectionDividerLayer's
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // using the SectionDividerLayer.GetRelatedLayerGroup() method, obtains the related LayerGroup instance.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // the same LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // the same LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // the same LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Group 1' contains 5 layers
            }
{{< /highlight >}}

**PSDNET-842. خصائص تأثير الستروك لا تُحفظ في ملف PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objects are not equal.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Will not throw ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Checks saved values
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}
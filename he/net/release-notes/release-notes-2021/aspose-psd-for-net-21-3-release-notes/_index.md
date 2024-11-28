---
title: הערות שחרור - Aspose.PSD for .NET 21.3
type: docs
weight: 100
url: /he/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל את ההערות לשחרור של [Aspose.PSD for .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-823|הוספת השכבת SectionDividerLayer על מנת לשפר את ההתנסות עם קבוצות שכבות|שיפור|
|PSDNET-694|כאשר נקרא PattResource, גובה ורוחב הוחלפו|באג|
|PSDNET-789|עמעום שגוי של יותר מאשר שכבת אפקט אחת|באג|
|PSDNET-805|סדר עמעום והלוגיקה שגויים כאשר קיימים יותר מכמה שכבות אפקט אחת|באג|
|PSDNET-842|מאפייני אפקט קווי שטיח לא נשמרים לקובץ PSD|באג|

## **שינויים ב-API הציבורי**

# **API's הנוספים:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **API's ההוסרים:**
- אף אחד

## **דוגמאות לשימוש:**

**PSDNET-694. כאשר נקרא PattResource, גובה ורוחב הוחלפו**

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

**PSDNET-789. עמעום שגוי של יותר מאשר שכבת אפקט אחת**

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
                                    // מחפש שכבת טקסט
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
                // באמצעות כך אנחנו שומרים את הקובץ PSD ששתולב
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. סדר עמעום שגוי והוגייקה כאשר קיימים יותר מכמה שכבות אפקט אחת**

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

                // באמצעות כך אנחנו שומרים את הקובץ PSD ששתולב
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. הוספת השכבת SectionDividerLayer על מנת לשפר את ההתנסות עם קבוצות שכבות**

{{< highlight csharp >}}
            // הקוד הבא מדגים שכבות שכבת SectionDividerLayer ואיך לקבל את הקבוצת השכבות הקשורה אליו.

            // היררכיית השכבות
            //    [0]: '</Layer group>' SectionDividerLayer עבור קבוצה ראשונה
            //    [1]: 'Layer 1' שכבה רגילה
            //    [2]: '</Layer group>' SectionDividerLayer עבור קבוצה שנייה
            //    [3]: '</Layer group>' SectionDividerLayer עבור קבוצה שלישית
            //    [4]: 'Group 3' שכבת קבוצה
            //    [5]: 'Group 2' שכבת קבוצה
            //    [6]: 'Group 1' שכבת קבוצה

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "האובייקטים לא שווים.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // יצירת היררכיה של השכבות
                // הוספת השכבת קבוצה 'Group 1'
                LayerGroup group1 = image.AddLayerGroup("Group 1", 0, true);
                // הוספת שכבה רגילה
                Layer layer1 = new Layer();
                layer1.DisplayName = "Layer 1";
                group1.AddLayer(layer1);
                // הוספת שכבת קבוצה 'Group 2'
                LayerGroup group2 = group1.AddLayerGroup("Group 2", 1);
                // הוספת שכבת קבוצה 'Group 3'
                LayerGroup group3 = group2.AddLayerGroup("Group 3", 0);

                // מקבל את הSectionDividerLayer
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // באמצעות השימוש בשיטת SectionDividerLayer.GetRelatedLayerGroup(), מוצא את המופע של LayerGroup הקשור.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // אותה LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // אותה LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // אותה LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Group 1' מכיל 5 שכבות
            }
{{< /highlight >}}

**PSDNET-842. מאפייני אפקט קווי שטיח לא נשמרים לקובץ PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "האובייקטים לא שווים.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // לא יזרוק באג ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // בודק את הערכים שנשמרו
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}

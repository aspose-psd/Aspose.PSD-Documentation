---
title: Aspose.PSD עבור .NET 21.1 - הערות לשחרור
type: docs
weight: 120
url: /he/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל הערות לשחרור עבור [Aspose.PSD עבור .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: חריגה בעת ניסיון להמיר קובץ Psd מסוים ל־png|באג|
|PSDNET-792|חריגה בשמירת PSD עם Smart Object ל־PNG|באג|

## **שינויים ב-API הציבורי**
# **APIים שהתווספו:**
- אין

# **APIים שהוסרו:**
- אין

## **דוגמאות לשימוש:**
**PSDNET-766. Aspose.PSD 20.10: חריגה בעת ניסיון להמיר קובץ Psd מסוים ל־png**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. חריגה בשמירת PSD עם Smart Object ל־PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder + "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // מחפש שכבת Smart Object
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // אנחנו טוענים שכבת Smart Object מ־Memory Stream,
                        // אך ניתן להשתמש ב־smart.ExportContents(somePath) כדי לייצא את האובייקט החכם לקובץ
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
                                        // ניתן להשתמש ב־UpdateText הפשוט, אך הדרך הזו נותנת לנו אפשרות לעריכת טקסט חלקית
                                        // יצירת שכבות טקסט מרובות שורות ותכונות סגנון אחרות לפיסות טקסט
                                        // אנא היה זהיר. אם תוכן האובייקט החכם אינו PSD, אי אפשר להשתמש בדרך זו של עריכת טקסט
                                        // במקרה כזה עליך להשתמש ב־Graphic API: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Best";

                                        // עליך לשנות את גודל הטקסט אם ברצונך שהתמונה תיראה יפה.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // מומלץ להשתמש ב־ReplaceContents. זה יציג מחדש את האובייקט החכם באופן אוטומטי
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // בדרך זו אנחנו שומרים את קובץ ה־PSD ששונה
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

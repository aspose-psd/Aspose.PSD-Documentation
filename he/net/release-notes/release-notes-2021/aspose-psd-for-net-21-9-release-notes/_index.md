---
title: כדי־לפרסם את Aspose.PSD עבור .NET 21.9 - פתח גרסאות
type: docs
weight: 40
url: /he/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל את פתח גרסאות עבור [Aspose.PSD עבור .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**תקציר**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-574|הפעלת RLE Compression כברירת המחדל עבור שמירת PSD |תכונה|
|PSDNET-747|תמיכה ב-Overlay Pattern Layer Effects עם מצב צבע מרובע בקובץ PSD|תכונה|
|PSDNET-951|אחרי יצירת השכבה החדשה, מאפייני המשאבים שלה הם null ומונעים פעולות (שינוי גודל למשל)|תקלה|
|PSDNET-955|חסר תמיכה בשיטות דחיסה ZipWithPrediction ל-8bit|תקלה|

## **שינויים ציבוריים ב- API**
# **APIs שנוספו:**
- לא נוספו

# **APIs שהוסרו:**
- לא הוסרו

## **דוגמאות שימוש:**

**PSDNET-574. הפעלת RLE Compression כברירת המחדל עבור שמירת PSD כדי למנוע פלט PSD עצום**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. תמיכה ב-Overlay Pattern Layer Effects עם מצב צבע מרובע בקובץ PSD**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // לא צריך לזרוק חריגה
            using (var im = Image.Load(fileName, loadOptions))
            {
                // לא צריך לזרוק חריגה
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. אחרי יצירת השכבה החדשה, מאפייני המשאבים שלה הם null ומונעים פעולות (שינוי גודל למשל)**

{{< highlight csharp >}}
            string PSDFile = "Layer1.psd";
            string layer1File = "Layer2.png";
            string layer2File = "Layer3.png";
            string outFileName = "finaloutput.psd";

            void ReplaceColor(RasterImage image, Color oldColor, int diff, Color newColor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var length = pixels.Length;

                var oldR = oldColor.R;
                var oldG = oldColor.G;
                var oldB = oldColor.B;
                var newColorValue = newColor.ToArgb();

                for (int i = 0; i < length; i++)
                {
                    // אדום
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // ירוק
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // כחול
                    var b = (byte)(pixels[i] & 0xff);

                    int actualDiff = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (actualDiff <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Layer2 = null;
            Layer Layer3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region Adding Layer 1

                using (var stream = new FileStream(layer1File, FileMode.Open))
                {
                    Layer2 = new Layer(stream);

                    Layer2.Resize(image.Width, image.Height);
                    var width = Layer2.Width;
                    var height = Layer2.Height;

                    Layer2.Left = 675;
                    Layer2.Top = 0;

                    Layer2.Right = Layer2.Left + width;
                    Layer2.Bottom = Layer2.Top + height;

                    image.AddLayer(Layer2);
                }

                #endregion

                using (var stream = new FileStream(layer2File, FileMode.Open))
                {
                    Layer3 = new Layer(stream);
                    // מחליף צבע לבן בשקוף
                    ReplaceColor(Layer3, Color.White, 256, Color.Transparent);
                    Layer2.DrawImage(new Point(0, 0), Layer3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. אין תמיכה בשיטות דחיסה ZipWithPrediction ל-8bit**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}

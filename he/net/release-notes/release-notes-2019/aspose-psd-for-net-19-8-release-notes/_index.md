---
title: מחזורי הוצאה לאור של Aspose.PSD עבור .NET 19.8
type: מסמכים
weight: 50
url: /he/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

עמוד זה מכיל מחזורי הוצאה לאור עבור Aspose.PSD עבור .NET 19.8

{{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-184|טעינת קבצי תמונה מסוג JPEG, PNG וכל סוגי התמונה האחרים ל-PsdImage מהזרם|תכונה|
|PSDNET-134|מימוש עיבוד שכבת מילוי: שוליים|תכונה|
|PSDNET-166|שמירת PSD כקובץ PDF לא מספקת טקסט נבחר|תכונה|
|PSDNET-158|תמיכה בשמירת PSB כקובץ PDF|תכונה|
|PSDNET-189|שימוש גבוה בזיכרון בעת טעינת PSD במצב "קריאה בלבד"|שיפור|
|PSDNET-171|לאחר יצירת שכבת טקסט חדשה, קובץ PSD הפך לא נקרא עבור PS|תקלה|
|PSDNET-156|חריגה בעת טעינת PSD|תקלה|

## **שינויים ב- API הציבוריים**
# **APIs שהתווספו:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **APIs שהוסרו:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **דוגמאות שימוש:**
**PSDNET-184. טעינת קבצי תמונה מסוג JPEG, PNG וכל סוגי התמונה האחרים ל-PsdImage מהזרם**

{{< highlight java >}}

    // טעינת קבצי תמונה מסוג JPEG, PNG וכל סוגי התמונה האחרים ל-PsdImage מהזרם

    string outputFilePath = "PsdResult.psd";

    var filesList = new string[]

    {

        "PsdExample.psd",

        "BmpExample.bmp",

        "GifExample.gif",

        "Jpeg2000Example.jpf",

        "JpegExample.jpg",

        "PngExample.png",

        "TiffExample.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. מימוש עיבוד שכבת מילוי: שוליים**

{{< highlight java >}}

             // מימוש עיבוד שכבת מילוי: שוליים

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. שמירת PSD כקובץ PDF לא מספקת טקסט נבחר**

{{< highlight java >}}

  // שמירת PSD כקובץ PDF לא מספקת טקסט נבחר

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. לאחר יצירת שכבת טקסט חדשה, קובץ PSD הפך לא נקרא עבור PS**

{{< highlight java >}}

 // לאחר יצירת שכבת טקסט חדשה בשרת בנייה, קובץ PSD הפך לא נקרא עבור PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Some text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. חריגה בעת טעינת PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. שימוש גבוה בזיכרון בעת טעינת PSD במצב "קריאה בלבד"**

{{< highlight java >}}

 // שימוש גבוה בזיכרון של Aspose.PSD בעת טעינת PSD במצב "קריאה בלבד"

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // שימוש בזיכרון צריך להיות פחות מ-100 מגה-בייט לדוגמאות אלו

            if (memoryUsed > 100)

            {

                throw new Exception("השימוש בזיכרון גדול מדי");

            }

{{< /highlight >}}

**PSDNET-158. תמיכה בשמירת PSB כקובץ PDF**

{{< highlight java >}}

 // תמיכה בשמירת PSB כקובץ PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

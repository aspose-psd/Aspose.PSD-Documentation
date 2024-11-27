---
title: הערות גרסה - Aspose.PSD עבור .NET 18.8
type: מסמכים
weight: 50
url: /he/net/aspose-psd-for-net-18-8-release-notes/
---

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-68|תמיכה במאפיין LayerCreationDateTime.|תכונה|
|PSDNET-67|תמיכה בסימון צבע הדף|תכונה|
|PSDNET-66|יכולת למזג שכבות אחת לשניה|תכונה|
|PSDNET-65|הוספת תמיכה חלקית בנכס ה-BoundBox של שכבת הטקסט|תכונה|
|PSDNET-64|הוספת תמיכה ב-IopaResource|תכונה|
|PSDNET-56|תמיכה באפקטי שכבה עבור פורמט PSD|תכונה|
|PSDNET-55|תמיכה ב-InterruptMonitor עבור .Net|תכונה|
|PSDNET-50|יצירת אפשרות למיזוג שכבות|תכונה|
|PSDNET-49|הוספת תמיכה לעיבוד של מאפיין כסף במסכות.|תכונה|
|PSDNET-43|מימוש בעיבוד של שכבת תיקוני עקומות|תכונה|
|PSDNET-42|הוספת תמיכה בשכבת תיקוני עקומות|תכונה|
|PSDNET-41|מימוש בעיבוד של שכבת תיקוני רמות|תכונה|
|PSDNET-40|הוספת יכולת לבצע בעיבוד של שכבת תיקוני רמות|תכונה|
|PSDNET-37|הוספת תמיכה בשכבת עיצוב ערבוב צבעים|תכונה|
|PSDNET-35|הוספת תמיכה בשכבת תיקוני הוא/רוויות הצבע|תכונה|
|PSDNET-34|מימוש בעיבוד של שכבת עריכת חשיפה עבור יצוא|תכונה|
|PSDNET-31|הוספת תמיכה בעיבוד לייצוא שכבת תיקוני קומיקס|תכונה|
|PSDNET-26|הוספת תמיכה במסכת חיתוך|תכונה|
|PSDNET-13|הוספת תמיכה במסכת שכבה|תכונה|
|PSDNET-9|הוספת תמיכה בשכבת סנפילטר תמונה|תכונה|
|PSDNET-8|הוספת תמיכה בשכבת עיבוד שכבת מערבל צבעוניות|תכונה|
|PSDNET-7|הוספת תמיכה בשכבת עיבוד חשיפת צבעים|תכונה|
|PSDNET-6|הוספת תמיכה בשכבת עיבוד בהירות/ניגודיות|תכונה|
|PSDNET-5|הוספת תמיכה חלקית בשכבות התאמות|תכונה|
|PSDNET-2|יכולת להוסיף שכבת טקסט בזמן ריצה|תכונה|
|PSDNET-62|קודקוד ה-TIFF אינו יכול לשמור תמונת ערוץ 16-bit|שיפור|
|PSDNET-61|שמירת תמונת PSD יוצרת צבעים בלתי תקפים|שיפור|
|PSDNET-60|שימוש בפינות השמאלית העליונה בעדכון|שיפור|
|PSDNET-59|חריגה בעדכון מסמכי טקסט|שיפור|
|PSDNET-58|חשיפת שדה קודקוד לתמונת JPEG2000 לציבור|שיפור|
|PSDNET-57|תיקון הגדרות 24bpp לייצוא ל-BMP|שיפור|
|PSDNET-46|שכבת ההתאמה מתעלמת מהמרת PSD של CMYK ל-TIFF או JPG|שיפור|

## **דוגמאות שימוש:**

**PSDNET-68 תמיכה במאפיין LayerCreationDateTime**

{{< highlight java >}}

 // דוגמא לשימוש במאפיין LayerCreationDateTime

מחרוזת שמקורית = "OneLayer.psd";

עם (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // בדיקה אם זמן יצירה מתעדכן על שכבות שנוצרו חדשות

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 תמיכה בסימון צבע הדף**

{{< highlight java >}}

 // דוגמא לשימוש בפונקציונאליות של סימון צבע הדף

מחרוזת שמקורית = "SheetColorHighlightExample.psd";

מחרוזת שם ייצוא = "SheetColorHighlightExampleChanged.psd";

עם (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);

    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;

    im.Save(exportPath);    

}

{{< /highlight >}}

**PSDNET-66 יכולת למזג שכבות אחת לשניה**

{{< highlight java >}}

 // דוגמא למזג שתי שכבות

מחרוזת שם קובץ מקור = "FillOpacitySample.psd";

מחרוזת שם קובץ מקור 2 = "ThreeRegularLayersSemiTransparent.psd";

מחרוזת שם קובץ ייצוא = "MergedLayersFromTwoDifferentPsd.psd" 

עם (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    עם (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

    im2.Save(exportPath);    

    }

}

{{< /highlight >}}

**PSDNET-65 הוספת תמיכה חלקית בנכס ה-BoundBox של שכבת הטקסט**

{{< highlight java >}}

 // דוגמא ל-Text BoxBounds

מחרוזת שם קובץ מקור = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

עם (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // גודל השכבה הוא גודל האיזור המוצג

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    //  TextBoundBox הוא הגודל המירבי של השכבה לשכבת טקסט. 

    // באזור זה ה-PS תנסה להתאים את הטקסט שלך

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 הוספת תמיכה ב-IopaResource**

{{< highlight java >}}

 // שינוי במאפיין של הכסף באמצעות השינוי של IopaResource

מחרוזת שם קובץ מקור = "FillOpacitySample.psd";

מחרוזת שם קובץ ייצוא = "FillOpacitySampleChanged.psd";

עם (var im = (PsdImage)(Image.Load(sourceFileName)))

{

var layer = im.Layers[2];

var resources = layer.Resources;

foreach (var resource in resources)

{

    if (resource is IopaResource)

    {

        var iopaResource = (IopaResource)resource;

        iopaResource.FillOpacity = 200;

    }

}

    im.Save(exportPath);    

}

{{< /highlight >}}

**PSDNET-56 תמיכה באפקטים שכבתיים עבור פורמט PSD**

{{< highlight java >}}

 עם (

    PsdImage image = (PsdImage)

    Aspose.PSD.Image.Load(

        sourceFileName,

        new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

        {

            LoadEffectsResource = true,

            UseDiskForLoadEffectsResource = true

        }))

{

    image.Save(

                output,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 תמיכה ב-InterruptMonitor עבור .Net**

{{< highlight java >}}

         פונקציה ציבורית לבדיקת Monitor (dir, ouptDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // הזמן המרבי צריך להיות פחות מהזמן הנדרש להמרת תמונה מלאה (ללא הפסקה).

                System.Threading.Thread.Sleep(3000);

                // להפסיק את התהליך

                monitor.Interrupt();

                System.Console.WriteLine("נקיע את תהליך השמירה מספר #{0} ב-{1}", thread.ManagedThreadId, System.DateTime.Now);

                // להמתין על הפסקת תהליך...

                thread.Join();

            }

            finally

            {

                // אם הקובץ שיש למחוק אינו קיים, אז אין יוצא דופן.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// להתחיל את ההמרת תמונה ולהמתין להפסקה

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// הנתיב לתמונת הקלט.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// הנתיב לתמונת הפלט.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// המוניטור להפסקה.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// האפשרויות לשמירה.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// לאחר שהמרה מתבצע בין אותן פורמט לאחר.

            /// </summary>

            /// <param name="inputPath">נתיב לתמונת הקלט.</param>

            /// <param name="outputPath">נתיב לתמונת הפלט.</param>

            /// <param name="saveOptions">אפשרויות שמירה.</param>

            /// <param name="monitor">מוניטור הפסקה.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// להוריד את התמונה מאופן לאחר. מטופל בהפסקה.

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("ציפייה להפסקה");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("התהליך שמור מספר #{0} ב-{1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

```
                        System.Console.WriteLine(e);

                    }

                    finally

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 ליצירת אפשרות למיזוג שכבות**

{{< highlight java >}}

 // למזג את כל ה-PSD שלך

מחרוזת שם קובץ מקור = "ThreeRegularLayersSemiTransparent.psd";

מחרוזת שם קובץ ייצוא = "ThreeRegularLayersSemiTransparentFlattened.psd";

עם (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);     

}

// למזג שכבה אחת בשנייה

מחרוזת שם קובץ מקור = "ThreeRegularLayersSemiTransparent.psd";

מחרוזת שם קובץ ייצוא = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

עם (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // הגדרת השכבות שמוזמנות

    im.Layers = new Layer[] { layer2 };

    im.Save(exportPath);    

}

{{< /highlight >}}

**PSDNET-49 הוספת תמיכה בעיבוד של מאפיין הכסף בשכבות**

{{< highlight java >}}

 // שינוי במאפיין הכסף

מחרוזת שם קובץ מקור = "FillOpacitySample.psd";

מחרוזת שם קובץ ייצוא = "FillOpacitySampleChanged.psd";

עם (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);    

}

{{< /highlight >}}

**PSDNET-43 מימוש בעיבוד של שכבת התיקוני עקומות**

{{< highlight java >}}

 // עריכת שכבת עקומות

מחרוזת שם קובץ מקור = "CurvesAdjustmentLayer";

מחרוזת נתיב אחרי השינוי = "CurvesAdjustmentLayerChanged";

מחרוזת נתיב ייצוא Png = "CurvesAdjustmentLayerChanged";

עבור (int j = 1; j < 2; j++)

{

    עם (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

        foreach (var layer in im.Layers)

    {

            if (layer is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

                      }

                 }

                 else

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

        }

    }



    // שמירת PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");



    // שמירת PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

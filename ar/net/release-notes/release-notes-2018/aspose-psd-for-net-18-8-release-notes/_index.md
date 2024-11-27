---
title: ملحوظات إصدار Aspose.PSD لـ .NET 18.8
type: docs
weight: 50
url: /ar/net/aspose-psd-for-net-18-8-release-notes/
---

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-68|دعم خاصية LayerCreationDateTime.|ميزة|
|PSDNET-67|دعم تسليط الضوء SheetColor|ميزة|
|PSDNET-66|القدرة على دمج الطبقات الواحدة مع الأخرى|ميزة|
|PSDNET-65|إضافة دعم جزئي لخاصية حدود Text Layer|ميزة|
|PSDNET-64|إضافة دعم IopaResource|ميزة|
|PSDNET-56|دعم طبقة الأثر لتنسيق PSD|ميزة|
|PSDNET-55|دعم InterruptMonitor لـ .Net|ميزة|
|PSDNET-50|جعل إمكانية تقسيم الطبقات|ميزة|
|PSDNET-49|إضافة تقديم لخاصية تعبئة الشفافية في الطبقات|ميزة|
|PSDNET-43|تنفيذ تقديم Curves Adjustment Layer|ميزة|
|PSDNET-42|إضافة دعم Curves Adjustment Layer|ميزة|
|PSDNET-41|تنفيذ تقديم Levels Adjustment Layer|ميزة|
|PSDNET-40|إضافة دعم Levels Adjustment Layer|ميزة|
|PSDNET-37|إضافة دعم Channel Mixer Adjustment Layer|ميزة|
|PSDNET-35|إضافة دعم Hue/Saturation Adjustment Layer|ميزة|
|PSDNET-34|تنفيذ تقديم Exposure Adjustment Layer للتصدير|ميزة|
|PSDNET-31|إضافة دعم التقديم للتصدير لطبقة ChannelMixer adjusment|ميزة|
|PSDNET-26|إضافة دعم Clipping mask|ميزة|
|PSDNET-13|إضافة دعم طبقة القناع|ميزة|
|PSDNET-9|إضافة دعم طبقة تصحيح Photo Filter|ميزة|
|PSDNET-8|إضافة دعم طبقة التحكم في القنوات|ميزة|
|PSDNET-7|إضافة دعم طبقة التعديل على التعرض|ميزة|
|PSDNET-6|إضافة دعم طبقة التعديل على السطوع/التباين|ميزة|
|PSDNET-5|إضافة دعم جزئي لطبقات التعديل|ميزة|
|PSDNET-3|إضافة دعم لخيار النص NoBreak في PSD|ميزة|
|PSDNET-2|القدرة على إضافة طبقة نص أثناء التشغيل|ميزة|
|PSDNET-62|القانونcan't لا يمكن حفظ صورة قناة 16 بت في تنسيق TIFF|تحسين|
|PSDNET-61|حفظ صورة PSD ينتج ألوان صورة غير صالحة|تحسين|
|PSDNET-60|إن الإحداثيات للزاوية العلوية اليسرى غير صحيحة عند التحديث|تحسين|
|PSDNET-59|استثناء في تحديث طبقات النص|تحسين|
|PSDNET-58|تعرض خاصية Codec لصورة JPEG2000 للجمهور|تحسين|
|PSDNET-57|إصلاح إعدادات 24bpp للتصدير إلى BMP|تحسين|
|PSDNET-46|الطبقة التعديلية تتجاهل بالنسبة للتحويل من CMYK PSD إلى TIFF أو JPG|تحسين|

## **أمثلة الاستخدام:**
**PSDNET-68 دعم خاصية LayerCreationDateTime**

{{< highlight java >}}

 // مثال على خاصية LayerCreationDateTime

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // التحقق من تحديث وقت إنشاء الطبقات الجديدة

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 دعم تسليط الضوء SheetColor**

{{< highlight java >}}

 // مثال على خاصية SheetColorHighlight

string sourceFileName = "SheetColorHighlightExample.psd";

string exportPath = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);



    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 القدرة على دمج الطبقات الواحدة مع الأخرى**

{{< highlight java >}}

 // مثال على دمج طبقتين

var sourceFile1 = "FillOpacitySample.psd";

var sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

var exportPath = "MergedLayersFromTwoDifferentPsd.psd" 

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

    im2.Save(exportPath);	

    }

}

{{< /highlight >}}

**PSDNET-65 إضافة دعم جزئي لخاصية حدود Text Layer**

{{< highlight java >}}

 // مثال على حوزة TextBox

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // حجم الطبقة هو حجم المنطقة المقدمة

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox هو أقصى حجم للطبقة لـ Text Layer. 
     // في هذه المنطقة سيحاول PS أن يصلح نصك

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 إضافة دعم IopaResource**

{{< highlight java >}}

 // تغيير خاصية Fill Opacity عن طريق تغيير IopaResource

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

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

**PSDNET-56 دعم أثر الطبقة لتنسيق PSD**

{{< highlight java >}}

 using (

    PsdImage image =

        (PsdImage)

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

**PSDNET-55 دعم InterruptMonitor لـ .Net**

{{< highlight java >}}

         public void InterruptMonitorTest(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // يجب أن يكون وقت الانتظار أقل من الوقت الذي يتطلبه التحويل الكامل للصورة (بدون انقطاع).

                System.Threading.Thread.Sleep(3000);

                // انقطاع العملية

                monitor.Interrupt();

                System.Console.WriteLine("انقطاع خيط التحويل  #{0} عندة {1}", thread.ManagedThreadId, System.DateTime.Now);

                // الانتظار للانقطاع...

                thread.Join();

            }

            finally

            {

                // إذا لم يتم حذف الملف الذي سيتم حذفه فلا يتم رمي أي استثناء.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// يبدأ تحويل الصورة وينتظر انقطاعها.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// المسار إلى الصورة الداخلية.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// المسار إلى الصورة الناتجة.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// المُراقب للانقطاع.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// خيارات التحويل.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// يبدأ العملية

            /// </summary>

            /// <param name="inputPath">المسار إلى الصورة الداخلية.</param>

            /// <param name="outputPath">المسار إلى الصورة الناتجة.</param>

            /// <param name="saveOptions">خيارات التحويل.</param>

            /// <param name="monitor">المُراقب للانقطاع.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// يحاول تحويل الصورة من تنسيق إلى آخر. يتعامل مع الانقطاع. 

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("الانقطاع المتوقع.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("انتهاء خيط التحويل  #{0} خلال {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

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

**PSDNET-50 جعل إمكانية تقسيم الطبقات**

{{< highlight java >}}

 // تقسيم PSD بالكامل

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// دمج طبقة في أخرى

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // تعيين الطبقات المدمجة

    im.Layers = new Layer[] { layer2 };

    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 إضافة تقديم لخاصية تعبئة الشفافية في الطبقات**

{{< highlight java >}}

 // تغيير خاصية Fill Opacity

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 تنفيذ تقديم Curves Adjustment Layer**

{{< highlight java >}}

 // تحرير طبقة الانحناءات

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

string pngExportPath = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

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



    // حفظ PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");



    // حفظ PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 إضافة دعم Curves Adjustment Layer**

{{< highlight java >}}

 // تحرير طبقة الانحناءات

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

for (int
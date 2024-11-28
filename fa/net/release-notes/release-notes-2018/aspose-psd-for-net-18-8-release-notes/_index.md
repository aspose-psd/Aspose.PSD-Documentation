---
title: گزارش انتشار Aspose.PSD برای .NET 18.8
type: مستندات
weight: 50
url: /fa/net/aspose-psd-for-net-18-8-release-notes/
---

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-68|پشتیبانی از ویژگی LayerCreationDateTime|ویژگی|
|PSDNET-67|پشتیبانی از رنگ سفید برجسته شیت|ویژگی|
|PSDNET-66|توانایی ادغام لایه‌ها با یکدیگر|ویژگی|
|PSDNET-65|افزودن پشتیبانی جزئی از خصوصیت Text Layer BoundBox|ویژگی|
|PSDNET-64|افزودن پشتیبانی از IopaResource|ویژگی|
|PSDNET-56|پشتیبانی از اثرات لایه برای فرمت PSD|ویژگی|
|PSDNET-55|پشتیبانی از InterruptMonitor برای .Net|ویژگی|
|PSDNET-50|ایجاد امکان تسطیح لایه‌ها|ویژگی|
|PSDNET-49|افزودن تصویرگری خاصیت توان پر کردن در لایه‌ها|ویژگی|
|PSDNET-43|پیاده‌سازی تصویرگری لایه تنظیم کرنج|ویژگی|
|PSDNET-42|افزودن پشتیبانی از لایه تنظیم کرنج|ویژگی|
|PSDNET-41|پیاده‌سازی تصویرگری لایه تنظیم سطوح|ویژگی|
|PSDNET-40|افزودن پشتیبانی از لایه تنظیم سطوح|ویژگی|
|PSDNET-37|افزودن پشتیبانی از لایه تنظیم Channel Mixer|ویژگی|
|PSDNET-35|افزودن پشتیبانی از لایه تنظیم Hue/Saturation|ویژگی|
|PSDNET-34|پیاده‌سازی تصویرگری لایه تنظیم Exposure برای صادرات|ویژگی|
|PSDNET-31|افزودن پشتیبانی از تغییرات برای صادرات لایه تنظیم ChannelMixer|ویژگی|
|PSDNET-26|افزودن پشتیبانی از ماسک Clipping|ویژگی|
|PSDNET-13|افزودن پشتیبانی از ماسک لایه|ویژگی|
|PSDNET-9|افزودن پشتیبانی از لایه تنظیم فیلتر عکس|ویژگی|
|PSDNET-8|افزودن پشتیبانی از لایه تنظیم میکسر کانال|ویژگی|
|PSDNET-7|افزودن پشتیبانی از لایه تنظیم اکسپرژر|ویژگی|
|PSDNET-6|افزودن پشتیبانی از لایه تنظیم روشنایی/کنتراست|ویژگی|
|PSDNET-5|افزودن پشتیبانی جزئی از لایه‌های تنظیمات|ویژگی|
|PSDNET-3|افزودن پشتیبانی از گزینه متن NoBreak در PSD|ویژگی|
|PSDNET-2|توانایی افزودن لایه متن در زمان اجرا|ویژگی|
|PSDNET-62|کدک TIFF قادر به ذخیره تصویر کانال 16 بیت نیست|بهبود|
|PSDNET-61|ذخیره‌کردن تصویر PSD با رنگ‌های نامعتبر|بهبود|
|PSDNET-60|مختصر کردن گوشه چپ بالای به‌روزرسانی را اشتباه محاسبه می‌کند|بهبود|
|PSDNET-59|استثناء در به‌روزرسانی لایه‌های متن|بهبود|
|PSDNET-58|آشکار کردن خاصیت کدک تصویر JPEG2000 به عموم|بهبود|
|PSDNET-57|اصلاح تنظیمات 24bpp برای صادرات به BMP|بهبود|
|PSDNET-46|لایه تنظیم در تبدیل PSD CMYK به TIFF یا JPG نادیده گرفته شد|بهبود|

## **مثال‌های استفاده:**
**PSDNET-68 پشتیبانی از خصوصیت LayerCreationDateTime** 

{{< highlight java >}}

 // مثال استفاده از خصوصیت LayerCreationDateTime

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // بررسی اینکه تاریخ ایجاد به‌روز شود یا لایه‌های جدید ایجاد شود

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 پشتیبانی از برجسته‌کردن رنگ شیت** 

{{< highlight java >}}

 // مثال استفاده از خصوصیت SheetColorHighlight

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

... (سایر مثال‌ها)**PSDNET-66 توانایی ادغام لایه‌ها با یکدیگر**

{{< highlight java >}}

 // مثال ادغام دو لایه

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

**PSDNET-65 افزودن پشتیبانی جزئی از خصوصیت Text Layer BoundBox**

{{< highlight java >}}

 // مثال باکس‌های Text

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // اندازه لایه، اندازه منطقی استاندارد برای کادر تصویر

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // یک TextBoundBox است که مساحت بیشتری برای Text Layer است

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 افزودن پشتیبانی از IopaResource**

{{< highlight java >}}

 // تغییر مشخصات Opacity توسط تغییر IopaResource

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

**PSDNET-56 پشتیبانی از اثرات لایه برای فرمت PSD**

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

**PSDNET-55 پشتیبانی از Monitor وقفه برای .Net**

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

                // تاخیر شود که کمتر از زمان مورد نیاز برای تبدیل تصویر کامل

                System.Threading.Thread.Sleep(3000);

                // وقفه را فراهم کنید

                monitor.Interrupt();

                System.Console.WriteLine("در حال وقفه نخ دفعه #{0} در {1}", thread.ManagedThreadId, System.DateTime.Now);

                // منتظر وقفه باشید...

                thread.Join();

            }

            finally

            {

                // اگر پرونده قابل حذف نباشد، هیچ استثناءی پرتاب نمی‌شود.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// آغاز کردن تبدیل تصویر و منتظر وقفه آن.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// مسیر به تصویر ورودی.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// مسیر به تصویر خروجی.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// وقفه نگهبان.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// گزینه‌های ذخیره.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// یک نمونه جدید از کلاس <see cref="SaveImageWorker" /> را مقدماتی می‌کند.

            /// </summary>

            /// <param name="inputPath">مسیر به تصویر ورودی.</param>

            /// <param name="outputPath">مسیر به تصویر خروجی.</param>

            /// <param name="saveOptions">گزینه‌های ذخیره.</param>

            /// <param name="monitor">وقفه نگهبان.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }



            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("وقفه مورد انتظار است.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("نخ ذخیره دفعه #{0} پایان می‌یابد در {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

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
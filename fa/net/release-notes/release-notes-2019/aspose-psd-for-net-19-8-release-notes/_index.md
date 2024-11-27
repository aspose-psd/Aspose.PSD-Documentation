---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 19.8
type: docs
weight: 50
url: /fa/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

این صفحه شامل یادداشت‌های انتشار Aspose.PSD برای .NET نسخه 19.8 می‌باشد.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-184|بارگذاری فایل‌های تصویری JPEG،PNG و سایر فرمت‌ها به PsdImage از جریان|ویژگی|
|PSDNET-134|پیاده‌سازی نمایش لایه پر کردن: گرادیان|ویژگی|
|PSDNET-166|ذخیره کردن PSD به عنوان PDF امکان متن قابل انتخاب را ارائه نمی‌دهد|ویژگی|
|PSDNET-158|پشتیبانی از ذخیره PSB به عنوان PDF|ویژگی|
|PSDNET-189|مصرف حافظه بالا در هنگام بارگذاری PSD با حالت فقط خواندن|بهبود|
|PSDNET-171|پس از ایجاد لایه متن جدید، پرونده PSD برای PS قابل خواندن نیست|اشکال|
|PSDNET-156|استثناء در هنگام بارگذاری PSD|اشکال|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **API‌های حذف شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **نمونه‌های استفاده:**

**PSDNET-184. بارگذاری فایل‌های تصویری JPEG،PNG و سایر فرمت‌ها به PsdImage از جریان**

{{< highlight java >}}

    // بارگذاری فایل‌های تصویری JPEG،PNG و سایر فرمت‌ها به PsdImage از جریان

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

**PSDNET-134. پیاده‌سازی نمایش لایه پر کردن: گرادیان**

{{< highlight java >}}

             // پیاده‌سازی نمایش لایه پر کردن: گرادیان

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

**PSDNET-166. ذخیره کردن PSD به عنوان PDF امکان متن قابل انتخاب را ارائه نمی‌دهد**

{{< highlight java >}}

  // ذخیره کردن PSD به عنوان PDF امکان متن قابل انتخاب را ارائه نمی‌دهد

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. پس از ایجاد لایه متن جدید، پرونده PSD برای PS قابل خواندن نیست**

{{< highlight java >}}

 // پس از ایجاد لایه متن جدید در سرور ساخت، فایل PSD برای PS قابل خواندن نیست

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("متنی", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. استثناء در هنگام بارگذاری PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. مصرف حافظه بالا در هنگام بارگذاری PSD با حالت فقط خواندن**

{{< highlight java >}}

 // مصرف حافظه بالا بر روی Aspose.PSD در هنگام بارگذاری PSD با حالت فقط خواندن

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // مصرف حافظه باید کمتر از ۱۰۰ مگابایت برای این نمونه باشد

            if (memoryUsed > 100)

            {

                throw new Exception("مصرف حافظه بیش از حد زیاد است");

            }

{{< /highlight >}}

**PSDNET-158. پشتیبانی از ذخیره PSB به عنوان PDF**

{{< highlight java >}}

 // پشتیبانی از ذخیره PSB به عنوان PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

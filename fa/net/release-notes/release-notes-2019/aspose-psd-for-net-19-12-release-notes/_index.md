---
title: فارسی
type: docs
weight: 10
url: /fa/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}} 

این صفحه شامل یادداشت‌های انتشار [Aspose.PSD for .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته بندی**|
| :- | :- | :- |
|PSDNET-11|[پشتیبانی از لایه متصل](/psd/fa/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|ویژگی|
|PSDNET-131|[پشتیبانی از SoCoResource](/psd/fa/net/support-of-socoresource/)|ویژگی|
|PSDNET-115|افزودن LineBreaks به LineBreaks موجود اگر TextLayer با یک رشته به روز شود|خطا|
|PSDNET-157|فریز کردن در حال ذخیره‌سازی PSB به عنوان PNG|خطا|
|PSDNET-250|استثناء در بارگذاری فایل CMYK PSD بدون لایه با فشرده‌سازی RLE|خطا|
|PSDNET-161|استثناء در به روز رسانی لایه‌های متنی|خطا|
|PSDNET-222|تغییر اندازه برخی از فایل‌های PSD با ماسک لایه به طرز نادرست عمل می‌کند|خطا|
|PSDNET-244|ذخیره کردن PSD با برخی از Globalization.CultureInfo.CurrentCulture منجر به استثنا در هنگام بارگذاری می‌شود|خطا|

## **تغییرات عمومی در API**
# **APIهای اضافه شده:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **APIهای حذف شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **نمونه‌های استفاده:**
**PSDNET-11. پشتیبانی از لایه متصل**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("example.psd"))

            {

                Layer[] layers = psd.Layers;

                // link all layers in one linked group

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // gets id for one layer

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId and linkGroupId are not equal.");

                }

                // gets all linked layers by link group id.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // unlink each layer from group

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // retrieves NULL for a link group ID that has no layers in the group.

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("The linkedLayers field is not NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. پشتیبانی از SoCoResource**

{{< highlight java >}}

      // Support of SoCoResource

    string sourceFileName = "ColorFillLayer.psd";

    string exportPath = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        foreach (var layer in im.Layers)

        {

            if (layer is FillLayer)

            {

                var fillLayer = (FillLayer)layer;

                foreach (var resource in fillLayer.Resources)

                {

                    if (resource is SoCoResource)

                    {

                        var socoResource = (SoCoResource)resource;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), socoResource.Color);

                        socoResource.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            im.Save(exportPath);

        }

    }

{{< /highlight >}}

**PSDNET-115. اضافه کردن LineBreaks به LineBreaks موجود اگر TextLayer با یک رشته به روز شود**

{{< highlight java >}}

           const string NewText = "abcdef\rzxcvbn";

        string sourceFilePath = "TestFileForAsianChars.psd");

        string outputFilePath = "result.psd";

        using (var image = (PsdImage)Image.Load(sourceFilePath))

        {

            var layer = (TextLayer)image.Layers[0];

            var imageOptions = new PsdOptions(image);

            layer.UpdateText(NewText);

            image.Save(outputFilePath, imageOptions);

        }

        using (var createdImage = (PsdImage)Image.Load(outputFilePath))

        {

            var createdLayer = (TextLayer)createdImage.Layers[0];

            if (NewText != createdLayer.Text)

            {

                throw new InvalidDataException("Updated text is invalid");

            }

        }

{{< /highlight >}}

**PSDNET-157. فریز کردن در حال ذخیره‌سازی PSB به عنوان PNG**

{{< highlight java >}}

       // Saving PSB as PNG 

    string sourceFileName = "sample.psb";

    string outFileName = "sample.png";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(outFileName, options);

    }

{{< /highlight >}}



` `**PSDNET-250. استثناء در بارگذاری فایل CMYK PSD بدون لایه با فشرده‌سازی RLE**

{{< highlight java >}}

     void LoadRawDataFromPsd()

        {

            string sourcePath = "CmykWithAlpha.psd";

            using (RasterImage image = (RasterImage)Image.Load(sourcePath))

            {

                var rawDataSettings = image.RawDataSettings;

                RawDataTester loader = new RawDataTester();

                image.LoadRawData(image.Bounds, rawDataSettings, loader);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end)

            {

            }

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions)

            {

            }

        }

{{< /highlight >}}


` `**PSDNET-161. استثناء در به روز رسانی لایه‌های متنی**

{{< highlight java >}}

      // Load a PSD file as an image and cast it into PsdImage

    using (PsdImage psdImage = (PsdImage)Image.Load("example.psd"))

    {

        foreach (var layer in psdImage.Layers)

        {

            if (layer is TextLayer)

            {

                TextLayer textLayer = layer as TextLayer;

                textLayer.UpdateText("test update", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        psdImage.Save("UpdateTextLayerInPSDFile_out.psd");

    }

{{< /highlight >}}



**PSDNET-222. تغییر اندازه برخی از فایل‌های PSD با ماسک لایه به طرز نادرست عمل می‌کند**

{{< highlight java >}}

     int scale = 2;

        string[] names = {

                             "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

                             "LevelsLayerWithLayerMaskRgb",

                             "LevelsLayerWithLayerMaskCmyk",

                             "ColorBalanceAdjustmentLayer"

                         };

        for (int i = 0; i < names.Length; i++)

        {

            string sourceFilePath = names[i] + ".psd";

            string outputFilePath = "output_" + sourceFilePath;

            string outputPngFilePath = "output_" + names[i] + ".png";

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, psdLoadOptions))

            {

                image.Resize(image.Width * scale, image.Height * scale);

                image.Save(outputFilePath, new PsdOptions());

                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}



**PSDNET-244. ذخیره کردن PSD با برخی از Globalization.CultureInfo.CurrentCulture منجر به استثنا در هنگام بارگذاری می‌شود**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string sourceFileName = string.Format("example-{0}.psd", i);

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            var psdSaveOptions = new PsdOptions();

            var culture = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            string outputFileName = "output-" + sourceFileName;

            // Load a PSD file as an image and cast it into PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image.Resize(160, 120);

                image.Save(outputFileName, psdSaveOptions);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            // Load a PSD file as an image and cast it into PsdImage

            using (PsdImage image2 = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image2.Resize(160, 120);

                image2.Save(outputFileName, psdSaveOptions);

            }

        }

{{< /highlight >}}

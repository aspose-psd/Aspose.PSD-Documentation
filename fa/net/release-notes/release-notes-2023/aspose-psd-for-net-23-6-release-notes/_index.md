---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 23.6
type: docs
weight: 70
url: /fa/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه [Aspose.PSD برای .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **کلید**   | **خلاصه**                                                                      | **دسته‌بندی** |
|:-----------|:-------------------------------------------------------------------------------|:--------------|
| PSDNET-1401 | بازسازی API TimeLine                                                        | بهبود         |
| PSDNET-1517 | حذف آرتیفکت‌ها در هنگام رندرینگ چیره                                       | بهبود         |
| PSDNET-1528 | بهینه‌سازی رندرینگ چیره                                                    | بهبود         |
| PSDNET-147  | پشتیبانی از لایه تنظیم آستانه                                                | قابلیت       |
| PSDNET-149  | پشتیبانی از لایه تنظیم رنگ انتخابی                                          | قابلیت       |
| PSDNET-801  | قابلیت صدور PSD TimeLine به فایل Gif متحرک                                    | قابلیت       |
| PSDNET-1555 | اضافه کردن پشتیبانی از TextLayer بدون حاشیه مستطیلی                        | قابلیت       |
| PSDNET-1582 | پشتیبانی از ShapeLayer                                                        | قابلیت       |
| PSDNET-864  | جایگزینی تصویر در Smart object بروز نمی‌شود                                 | باگ           |
| PSDNET-1404 | فایل PSD نمی‌تواند به عنوان PSD ذخیره شود با استثنای زیر: حالت‌های Rgb و Lab نمی‌توانند کمتر از 3 کانال و بیش از 4 کانال داشته باشند | باگ           |
| PSDNET-1546 | توجیه متن از بین می‌رود اگر لایه TextLayer را با حالت ویرایش فتوشاپ باز کنید | باگ           |
| PSDNET-1548 | استثنای مرجع خالی در زمان ذخیره فایل PSD                                      | باگ           |
| PSDNET-1578 | استثنا در بارگذاری ShapeLayer: نقاط برای محدوده مبدأ بردار پشتیبانی نمی‌شود هنوز | باگ           |
| PSDNET-1579 | استثنا در بارگذاری VogkResource: نقاط به عنوان DoubleStructures ذخیره شده‌اند، ما به عنوان UnitStructures می‌خوانیم | باگ           |
| PSDNET-1581 | LayerType لایه ShapeLayer خالی است                                          | باگ           |


## **تغییرات API عمومی**
# **API های اضافه شده:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **API های حذف شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **مثال‌های استفاده:**

**PSDNET-147. پشتیبانی از لایه تنظیم آستانه**

{{< highlight csharp >}}
string sourceFileWithThresholdLayer = "flowers_threshold_source.psd";
string outputPsdWithThresholdLayer = "flowers_threshold_output.psd";
string outputPngWithThresholdLayer = "flowers_threshold_output.png";

string sourceFileWithoutThresholdLayer = "flowers_source.psd";
string outputPsdWithoutThresholdLayer = "flowers_output.psd";
string outputPngWithoutThresholdLayer = "flowers_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("اشیا برابر نیستند.");
    }
}

// گرفتن، بررسی و تغییر لایه تنظیم آستانه از تصویر.
using (var image = (PsdImage)Image.Load(sourceFileWithThresholdLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // گرفتن لایه تنظیم آستانه.
            ThresholdLayer thrsLayer = (ThresholdLayer)layer;
            var level = thrsLayer.Level;

            // بررسی پارامترهای لایه.
            AssertAreEqual(level, (short)115);

            // تنظیم پارامترهای لایه.
            thrsLayer.Level = 50;

            image.Save(outputPsdWithThresholdLayer);
            image.Save(outputPngWithThresholdLayer, new PngOptions());
        }
    }
}

// افزودن و تنظیم لایه تنظیم آستانه به تصویر.
using (var image = (PsdImage)Image.Load(sourceFileWithoutThresholdLayer))
{
    // اضافه کردن لایه تنظیم آستانه.
    ThresholdLayer thresholdLayer = image.AddThresholdAdjustmentLayer();

    // تنظیم پارامترهای لایه.
    thresholdLayer.Level = 115;

    image.Save(outputPsdWithoutThresholdLayer);
    image.Save(outputPngWithoutThresholdLayer, new PngOptions());
}
{{< /highlight >}}
...

اینجا برخی از متن به دل منظور ترجمه نشده است.
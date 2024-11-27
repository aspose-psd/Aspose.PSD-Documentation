---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 23.5
type: docs
weight: 80
url: /fa/net/aspose-psd-for-net-23-5-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه [Aspose.PSD برای .NET 23.5](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

| **کلید**   | **خلاصه**                                                               | **دسته‌بندی** |
|:------------|:--------------------------------------------------------------------------|:--------------|
| PSDNET-343  | پشتیبانی از فیلتر: تیز کردن -> تیز                                      | ویژگی        |
| PSDNET-1179 | ذخیره پرونده PSD (RGB/8 بیت یا RGB/16 بیت) بدون لایه به 32 بیت        | ویژگی        |
| PSDNET-1408 | پیاده‌سازی مدیریت اشیاء مسیری از منابع vsms یا vmsk برای لایه شکل   | ویژگی        |
| PSDNET-1508 | افزودن تاثیر نقاط پوسته بر همدیگر                                      | ویژگی        |


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsDisabled
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.PathOperations
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor(Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord,Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ShapeIndex
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ToVectorPathRecords
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsInverted
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.DescriptorStructure)
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterId
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterType


# **API‌های حذف شده:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Save(Aspose.PSD.StreamContainer,System.Int32)


## **نمونه‌های استفاده:**

**PSDNET-343. پشتیبانی از فیلتر: تیز کردن -> تیز**

{{< highlight csharp >}}
string sourceFile = "sharpen_source.psd";
string outputPsd = "sharpen_output.psd";
string outputPng = "sharpen_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("اشیاء برابر نیستند.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

    // ویرایش فیلترهای هوشمند
    SharpenSmartFilter sharpen = (SharpenSmartFilter)smartObj.SmartFilters.Filters[0];

    // بررسی مقادیر فیلتر
    AssertAreEqual(BlendMode.Normal, sharpen.BlendMode);
    AssertAreEqual(100d, sharpen.Opacity);
    AssertAreEqual(true, sharpen.IsEnabled);

    // به‌روزرسانی مقادیر فیلتر
    sharpen.BlendMode = BlendMode.Divide;
    sharpen.Opacity = 75;
    sharpen.IsEnabled = false;

    // اضافه‌کردن موارد فیلتر جدید
    var filters = new List<SmartFilter>(smartObj.SmartFilters.Filters);
    filters.Add(new SharpenSmartFilter());
    smartObj.SmartFilters.Filters = filters.ToArray();

    // اعمال تغییرات
    smartObj.SmartFilters.UpdateResourceValues();
    smartObj.UpdateModifiedContent();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1179. ذخیره پرونده PSD (RGB/8 بیت یا RGB/16 بیت) بدون لایه به 32 بیت**

{{< highlight csharp >}}
string inputFile =  "input_8bit_rle.psd";
string outputPsdFile = "output_32bit.psd";
string outputImageFile32 = "output_from_32bit.png";

using (PsdImage srcImg = (PsdImage)Image.Load(inputFile))
{
    PsdOptions totalOptions = new PsdOptions() { ChannelBitsCount = 32, ColorMode = ColorModes.Rgb };
    srcImg.Save(outputPsdFile, totalOptions);

    using (var img32 = Image.Load(outputPsdFile))
    {
        img32.Save(outputImageFile32, new PngOptions() { ColorType = PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}

**PSDNET-1408. پیاده‌سازی مدیریت اشیاء مسیری از منابع vsms یا vmsk برای لایه شکل**

{{< highlight csharp >}}
string srcFile = "ShapeLayerTest.psd";
string outFile = "ShapeLayerTest-out.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer shapeLayer = image.Layers[1];
    VectorPathDataResource vectorPathDataResource = (VectorPathDataResource)shapeLayer.Resources[1];

    bool isFillStartsWithAllPixels;
    List<IPathShape> shapes = GetShapesFromResource(vectorPathDataResource, out isFillStartsWithAllPixels);

    // حذف یک شکل
    shapes.RemoveAt(1);

    // ذخیره داده‌های تغییر یافته به منبع
    List<VectorPathRecord> path = new List<VectorPathRecord>();
    path.Add(new PathFillRuleRecord(null));
    path.Add(new InitialFillRuleRecord(isFillStartsWithAllPixels));

    for (ushort i = 0; i < shapes.Count; i++)
    {
        PathShape shape = (PathShape)shapes[i];
        shape.ShapeIndex = i;
        path.AddRange(shape.ToVectorPathRecords());
    }

    vectorPathDataResource.Paths = path.ToArray();

    image.Save(outFile);
}

// بررسی مقادیر تغییر یافته در پرونده ذخیره شده
using (PsdImage image = (PsdImage)Image.Load(outFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer shapeLayer = image.Layers[1];
    VectorPathDataResource vectorPathDataResource = (VectorPathDataResource)shapeLayer.Resources[1];

    bool isFillStartsWithAllPixels;
    List<IPathShape> shapes = GetShapesFromResource(vectorPathDataResource, out isFillStartsWithAllPixels);

    // انتظار می‌رود پرونده ذخیره شده 1 شکل داشته باشد
    AssertAreEqual(1, shapes.Count);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "اشیاء برابر نیستند.");
    }
}

List<IPathShape> GetShapesFromResource(VectorPathDataResource vectorPathDataResource,out bool isFillStartsWithAllPixels)
{
    List<IPathShape> shapes = new List<IPathShape>();
    LengthRecord lengthRecord = null;
    isFillStartsWithAllPixels = false;
    List<BezierKnotRecord> bezierKnotRecords = new List<BezierKnotRecord>();

    foreach (var pathRecord in vectorPathDataResource.Paths)
    {
        if (pathRecord is LengthRecord)
        {
            if (bezierKnotRecords.Count > 0)
            {
                shapes.Add(new PathShape(lengthRecord, bezierKnotRecords.ToArray()));
                lengthRecord = null;
                bezierKnotRecords.Clear();
            }

            lengthRecord = (LengthRecord)pathRecord;
        }
        else if (pathRecord is BezierKnotRecord)
        {
            bezierKnotRecords.Add((BezierKnotRecord)pathRecord);
        }
        else if (pathRecord is InitialFillRuleRecord)
        {
            InitialFillRuleRecord initialFillRuleRecord = (InitialFillRuleRecord)pathRecord;
            isFillStartsWithAllPixels = initialFillRuleRecord.IsFillStartsWithAllPixels;
        }
    }

    if (bezierKnotRecords.Count > 0)
    {
        shapes.Add(new PathShape(lengthRecord, bezierKnotRecords.ToArray()));
        lengthRecord = null;
        bezierKnotRecords.Clear();
    }

    return shapes;
}
{{< /highlight >}}

**PSDNET-1508. اضافه کردن تأثیر نقاط شبکه بر هم**

{{< highlight csharp >}}
string sourceFile = "Bottom_Right.psd";
string outputFile = "output.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    image.Save(outputFile, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha});
}
{{< /highlight >}}
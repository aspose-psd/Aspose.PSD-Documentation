---
title: دفترچه ی انتشار Aspose.PSD برای Java 20.8
type: مستندات
weight: 50
url: /fa/java/aspose-psd-for-java-20-8-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.8/) می‌باشد. {{% /alert %}}

|**کلید**|**خلاصه**|**رده**|
| :- | :- | :- |
|PSDJAVA-264|پشتیبانی از SoLdResource (منبع داده لایه شیء هوشمند)|ویژگی|
|PSDJAVA-263|پشتیبانی از PlLdResource (منبع لایه قرار داده شده برای لایه شیء هوشمند)|ویژگی|
|PSDJAVA-262|افزودن پشتیبانی از ساختارهای آرایه شیء و آرایه واحد: امضاهای ObAr / UnFl|ویژگی|
|PSDJAVA-265|خط خورده و خط خورده از بین می‌روند پس از تمرکز روی متن در فایل ذخیره شده با Aspose.|اشکال|
|PSDJAVA-257|اصلاح ذخیره کردن تصویر PSD تغییر یافته با CMYK حالت رنگ 16 بیت بر کانال|اشکال|
|PSDJAVA-268|رگرسیون: Aspose.PSD 20.7.0 اندازه‌های قلم را برای فایل‌های قدیمی شکسته می‌کند|اشکال|

# **تغییرات عمومی API**
# **API های اضافه شده:**
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.TypeToolKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.ImageStack
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Raster
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Unknown
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Vector
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.AntiAliasPolicyKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.TypeToolKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ObjectArrayStructure.StructureKey
- F: com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.UnitArrayStructure.StructureKey
- M: com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.ClassID.#ctor(byte[],boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getAntiAliasPolicy
- و غیره.

# **مثال‌های استفاده:**

**PSDJAVA-264. پشتیبانی از SoLdResource (منبع داده لایه شیء هوشمند)**
{{< highlight java >}}
// در این مثال نشان‌داده شده است که چگونه از خصوصیات داده لایه شیء هوشمند در فایل PSD، داده گرفته یا تنظیم شود.

// تعریف یک کلاس محلی برای نگهداری کد‌های قابل استفاده (متد‌ها)
class LocalScopeExtension
{
    boolean equals(Object a, Object b)
    {
        return (a == b) || (a != null && a.equals(b));
    }

    void assertAreEqual(Object actual, Object expected)
    {
        boolean areEqual = equals(actual, expected);
        // مقایسه آرایه‌ها در صورت وجود
        // کاربرد دارد
        if (!areEqual &&
                (actual != null && actual.getClass().isArray()) &&
                (expected != null && expected.getClass().isArray()))
        {
            int length;
            // استفاده از Reflection برای دستیابی به آرایه‌ها جهت پشتیبانی از آرایه‌های پایه
            if ((length = Array.getLength(actual)) == Array.getLength(expected))
            {
                for (int i = 0; i < length; i++)
                {
                    if (!equals(Array.get(actual, i), Array.get(expected, i)))
                    {
                        break;
                    }
                }

                areEqual = true;
            }
        }

        if (!areEqual)
        {
            throw new FormatException(
                    String.format("مقدار واقعی %s با مورد انتظار %s برابر نیست.", actual, expected));
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();

String srcPsdPath = "LayeredSmartObjects8bit2.psd";
String dstPsdPath = "LayeredSmartObjects8bit2_output.psd";

Object[][] expectedValues = new Object[][]
        {
                // و غیره.
        };

// بارگیری یک فایل از پیش تعیین شده PSD حاوی SoLdResource
PsdImage image = (PsdImage)Image.load(srcPsdPath);
try
{
    SoLdResource resource = null;
    int index = 0;
    for (Layer imageLayer : image.getLayers())
    {
        for (LayerResource imageResource : imageLayer.getResources())
        {
            if (imageResource instanceof SoLdResource)
            {
                // اطمینان حاصل شود که منبع بارگیری شده همان چیزی است که ما انتظار داریم
                // در عین حال استفاده از API SoLdResource را نشان می‌دهد
                resource = (SoLdResource)imageResource;
                Object[] expectedValue = expectedValues[index++];
                $.assertAreEqual(expectedValue[0], resource.isCustom());
                $.assertAreEqual(expectedValue[1], resource.getUniqueId().toString());
                $.assertAreEqual(expectedValue[2], resource.getPageNumber());
                $.assertAreEqual(expectedValue[3], resource.getTotalPages());
                $.assertAreEqual(expectedValue[4], resource.getAntiAliasPolicy());
                $.assertAreEqual(expectedValue[5], resource.getPlacedLayerType());
                $.assertAreEqual(8, resource.getTransformMatrix().length);
                $.assertAreEqual(expectedValue[6], resource.getTransformMatrix());
                $.assertAreEqual(expectedValue[7], resource.getValue());
                $.assertAreEqual(expectedValue[8], resource.getPerspective());
                // و غیره.

                break;
            }
        }
    }

    $.assertAreEqual(true, resource != null);
    image.save(dstPsdPath, new PsdOptions(image));
}
finally
{
    image.dispose();
}
{{< /highlight >}}

و غیره.

**PSDJAVA-265. خط خورده و خط خورده از بین می‌روند پس از تمرکز روی متن در فایل ذخیره شده با Aspose.PSD**
{{< highlight java >}}
// در این مثال نشان داده شده است که فرمت خط خورده و خط‌خورده بر روی متن از بین نمی‌رود
// هنگام انتخاب متن با ابزار نوع افقی در فتوشاپ پس از ذخیره فایل PSD توسط کتابخانه.

String srcPsdPath = "source.psd";
String dstPsdPath = "output.psd";

// بارگیری یک فایل PSD حاوی لایه متنی
PsdImage image = (PsdImage)Image.load(srcPsdPath);
try
{
    Layer[] layers = image.getLayers();
    TextLayer textLayer = (TextLayer)layers[1];

    // سبک فرمت متن را تغییر دهید
    textLayer.getTextData().getItems()[0].getStyle().setUnderline(true);
    textLayer.getTextData().getItems()[1].getStyle().setStrikethrough(true);

    // تغییرات را در لایه متن اعمال کنید
    textLayer.getTextData().updateLayerData();

    image.save(dstPsdPath, new PsdOptions(image));
}
finally
{
    image.dispose();
}
{{< /highlight >}}**PSDJAVA-257. اصلاح ذخیره کردن تصویر PSD تغییر یافته با CMYK حالت رنگ 16 بیت بر کانال**
{{< highlight java >}}
// در این مثال نشان داده شده است که خطا در ذخیره سازی تصویر 16 بیتی PSD در حالت رنگ CMYK وجود ندارد.
// برنامه یک تصویر 16 بیتی در حالت CMYK بارگیری می‌کند، سپس آن را کمی تغییر داده و بعنوان یک سند فتوشاپ دیگر ذخیره می‌کند.

String srcPsdPath = "cub16bit_cmyk.psd";
String dstPngPath = "output.png";

// بارگیری یک تصویر 16 بیتی در حالت CMYK
PsdImage image = (PsdImage)Image.load(srcPsdPath);
try
{
    RasterCachedImage raster = image.getLayers()[0];

    // تغییر تصویر با اضافه کردن حاشیه داخلی
    Graphics graphics = new Graphics(raster);
    int width = raster.getWidth();
    int height = raster.getHeight();
    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1,
            height - (2 * (height / 3)) - 1);
    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // خط زیر باید بدون هیچ خطا اجرا شود
    image.save(dstPngPath, new PngOptions());
}
finally
{
    image.dispose();
}
{{< /highlight >}}

**PSDJAVA-268. رگرسیون: Aspose.PSD 20.7.0 اندازه‌های قلم را برای فایل‌های قدیمی شکسته می‌کند**
{{< highlight java >}}
// این مثال بازسازی خطا است که اندازه‌های قلم را برای فایل‌های PSD قدیمی شکسته می‌کند.

String srcPsdPath = "font_size_lost.psd";
String dstPngPath = "output.png";

PsdImage psdImage = (PsdImage)Image.load(srcPsdPath);
try
{
    TextLayer textLayer = (TextLayer)psdImage.getLayers()[0];
    // پردازش قدرتمند لایه متنی که تغییر نکرده است برای بازسازی خطا

    textLayer.getTextData().updateLayerData();

    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}
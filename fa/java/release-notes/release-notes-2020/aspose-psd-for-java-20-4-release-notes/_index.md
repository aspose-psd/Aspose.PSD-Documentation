---
title: یادداشت‌های نسخه Aspose.PSD برای جاوا 20.4
type: docs
weight: 30
url: /fa/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} این صفحه حاوی یادداشت‌های نسخه [Aspose.PSD برای جاوا 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) می‌باشد {{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDJAVA-156|پشتیبانی از منبع "داده‌های مبدأ بردار"|ویژگی|
|PSDJAVA-171|پشتیبانی از lclrResource (تنظیم رنگ برگه)|ویژگی|
|PSDJAVA-157|پشتیبانی از خصوصیت‌های داده LengthRecord. (عملیات‌های مسیر (عملیات‌های منطقی) ، ایندکس شکل در لایه ، تعداد شکل‌های بزرگ گره)|ویژگی|
|PSDJAVA-158|` `پشتیبانی از رنگ پس زمینه بخش منبع تصویر #1010|ویژگی|
|PSDJAVA-161|افزودن لایه‌های پر کننده به صورت زمان اجرا|ویژگی|
|PSDJAVA-168|پشتیبانی از اطلاعات مرز منبع تصویر #1009|ویژگی|
|PSDJAVA-169|پشتیبانی از لایه‌ها در فایل‌های فرمت AI|ویژگی|
|PSDJAVA-163|پشتیبانی از خواندن و ویرایش تاثیر لایه هم‌گرادیان روی|ویژگی|
|PSDJAVA-164|رندرینگ تاثیر لایه هم‌گرادیان روی|ویژگی|
|PSDJAVA-149|خطای Aspose.PSD برای جاوا هنگام دریافت خصوصیت textData.items از لایه متن|اشکال|
# **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **API‌های حذف شده:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **مثال‌های کاربرد:**

**PSDJAVA-156. پشتیبانی از منبع "داده‌های مبدأ بردار"**

{{< highlight java >}}

 /*

نمونه‌ای از خواندن و تغییر یک منبع داده "داده‌های مبدأ بردار".

*/

// متد‌ها را در دامنه محلی نگهداری کنید

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("VogkResource یافت نشد.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// یک فایل PSD را که شامل یک منبع VOGK تعریف شده است بارگذاری کنید

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // اولین VogkResource را در منابع لایه تعریف شده پیدا کنید

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // خصوصیات منابع پیش‌تعریف شده را تأیید کنید

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource با خطا خوانده شده است.");

    }

    // تغییراتی در برخی از خصوصیات VogkResource اعمال کنید

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // یک نسخه از فایل PSD بارگیری شده را بر روی مسیر ذخیره کنید

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. پشتیبانی از lclrResource (تنظیم رنگ برگه)**

{{< highlight java >}}

 /*

یک مثال از استفاده از رنگ برگه لایه برای برجسته کردن بصری لایه‌ها. به عنوان مثال می‌توان

چندین لایه در فایل PSD به‌روزرسانی کرد و سپس با ترکیب رنگ لایه مورد نظرتان را

برجسته کنید.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // منبع lcrl همیشه در لیست منابع فایل psd موجود است.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("رنگ برگه اشتباه خوانده شده است");

                }

                // برگرداندن رنگ لایه تایجه

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

}

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// در فایل، رنگ‌های برجسته لایه‌ها به این ترتیب هستند

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Red,

        SheetColorHighlightEnum.Orange,

        SheetColorHighlightEnum.Yellow,

        SheetColorHighlightEnum.Green,

        SheetColorHighlightEnum.Blue,

        SheetColorHighlightEnum.Violet,

        SheetColorHighlightEnum.Gray,

        SheetColorHighlightEnum.NoColor

};

// یک فایل PSD که شامل یک LclrResource پیش‌تعریف شده است بارگیری کنید

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// یک PSD فقط ذخیره شده را بارگذاری کنید

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // رنگ‌ها را برعکس کنید

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. پشتیبانی از خصوصیت‌های داده LengthRecord. (عملیات‌های مسیر (عملیات‌های منطقی) ، ایندکس شکل در لایه ، تعداد شکل‌های بزرگ گره)**

{{< highlight java >}}

 /*

نمونه‌ای از تغییر عملیات مسیر هنگام کار با اشکال. برنامه مسیرهای برداری پیش‌تعریف شده (LengthRecord) را می‌خواند

و عملیات‌های مسیر آن‌ها را تغییر می‌دهد و سپس یک نسخه اصلاح شده از سند را به عنوان یک فایل PSD جدید

ذخیره می‌کند.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// یک فایل PSD که شامل یک منبع vsms پیش‌تعریف شده است بارگیری کنید

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // وارد کردن اولین VsmsResource در منابع لایه پیش‌تعریف شده

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // تغییر روش ترکیب اشکال

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // یک نسخه اصلاح شده از فایل PSD بارگیری شده را بر روی مسیر ذخیره کنید

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. پشتیبانی از رنگ پس زمینه منبع تصویر #1010** 

{{< highlight java >}}

 /*

نمونه‌ای از خواندن و اصلاح یک منبع رنگ پس‌زمینه.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// یک فایل PSD که شامل یک منبع رنگ پس‌زمینه پیش‌تعریف شده است بارگیری کنید

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColor
---
title: دفترچه ی انتشار Aspose.PSD برای جاوا 20.6
type: مستندات
weight: 50
url: /fa/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل یادداشت‌های انتشار [Aspose.PSD برای جاوا 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) می‌باشد. {{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDJAVA-216|پشتیبانی از LnkEResource (منبع لایه Smart Object)|ویژگی|
|PSDJAVA-219|پشتیبانی از britResource (منبع لایه تنظیم روشنایی/کنتراست)|ویژگی|
|PSDJAVA-222|انتقال تنظیم DefaultReplacementFont به کلاس ImageOptionsBase|بهبود|
|PSDJAVA-217|اشکال در بازنویسی فایل‌های PSD در صورت وجود ماسک در لایه تنظیم که محدوده‌های خالی دارد|اشکال|
|PSDJAVA-218|تصویر Psd با حالت RGB 16 بیت/کانال فقط در پیش‌نمایش لایه‌ها را به‌روز می‌کند|اشکال|
|PSDJAVA-220|تغییرات ماسک لایه PSD در هنگام ذخیره نمی‌شوند|اشکال|
|PSDJAVA-221|ترتیب نادرست لایه پس از اضافه کردن گروه لایه به گروه لایه خالی|اشکال|
|PSDJAVA-223|استثناء در بارگیری فایل PSD خاص با منبع LnkE ترکیبی و ویژگی adobeStockLicenseState|اشکال|
|PSDJAVA-224|ذخیره فایل AI به فرمت Jpeg2000 کار نمی‌کند|اشکال|
|PSDJAVA-225|گروه لایه با حالت ادغام عبور نشده به درستی رندر نمی‌شود|اشکال|
|PSDJAVA-226|استثناء NullReference در هنگام تلاش برای تبدیل فایل خاص Psd به تصویر|اشکال|
|PSDJAVA-227|OverflowException در هنگام تلاش برای باز کردن فایل خاص Psd|اشکال|

# **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **API‌های حذف شده:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **مثال‌های استفاده:**

**PSDJAVA-216: پشتیبانی از LnkEResource (منبع لایه Smart Object)**

{{< highlight java >}}

 // یک مثال از لینک کردن انواع مختلف دارایی‌ها (تصاویر raster، کتابخانه‌های CC) به PSD.

// همچنین API‌ی LnkeResource مدنظر است.

// یک کلاس که متدها را در دامنه محلی نگهداری می‌کند

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport عملکرد اشتباهی دارد.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // این مثال نشان می‌دهد چگونه ویژگی‌های منبع Photoshop Psd LnkE

    // Resource را که اطلاعات درباره یک فایل دسترسی به بیرونی را دارد، بدست آورده و تنظیم ک

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,

            int length3,

            int length4,

            String fullPath,

            String date,

            double assetModTime,

            String childDocId,

            boolean locked,

            String uid,

            String name,

            String originalFileName,

            String fileType,

            long size)

    {

        String outputPath = "out_" + fileName;

        // یک PSD تعیین شده بارگیری کنید

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // جستجوی LnkeResource در میان منابع لایه جهانی

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // اعتبارسنجی ویژگی‌های LnkeResource

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), size);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.liFE);

                    // به‌روزرسانی ویژگی‌های LnkeResource

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), length2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), length3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), length4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    break;

                }

            }

            // مطمئن شوید که LnkeResource پشتیبانی می‌شود

            assertIsTrue(lnkeResource != null);

            // یک نسخه از PSD بارگیری شده را ذخیره کنید

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // فایل ذخیره‌شده را بارگیری کنید

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // PSD را به فرمت فایل PNG تبدیل کنید (با کانال آلفا برای شفافیت)

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            image1.save(Path.changeExtension(outputPath, "png"), pngOptions);

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// این مثال نشان می‌دهد چگونه ویژگی‌های منبع Psd LnkE را بدست آورید و تنظیم کنید

// که شامل اطلاعات درباره یک فایل خارجی لینک‌شده است.

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "05/09/2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// این مثال نشان می‌دهد چگونه ویژگی‌های منبع Psd LnkE را بدست آورید و تنظیم کنید

// که اطلاعات درباره یک فایل PNG خارجی لینک‌شده را دارد.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "04/14/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// این مثال نشان می‌دهد چگونه ویژگی‌های منبع Psd LnkE را بدست آورید و تنظیم کنید

// که اطلاعات درباره یک فایل لینک شده به کتابخانه CC دارد.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (قابلیت در دسترس است در Photoshop CC 2015)",

        "01/01/0001 00:00:00",

        1588890915488.0d,

        "",

        false,

        "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

        "rgb8_2x2_linked",

        "rgb8_2x2.png",

        "png",

        0);

{{< /highlight >}}


**PSDJAVA-219: پشتیبانی از britResource (منبع لایه تنظیم روشنایی/کنتراست)**

{{< highlight java >}}

 // این مثال نشان می‌دهد چگونه می‌توانید به صورت برنامه‌ریزی شده لایه تنظیم Brightness/Contrast تصویر PSD را تغییر دهید - BritResource. این یک API پایین‌سطح Aspose.PSD است. می‌توانید از لایه Brightness/Contrast از طریق API آن استفاده کنید، که بسیار آسانتر خواهد بود، اما ویرایش مستقیم منبع فتوشاپ بیشتر از محتوای فایل PSD برای شما کنترل بیشتری فراهم می‌کند.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// یک سند فتوشاپ را که شامل لایه تنظیم روشنایی/کنتراست است بارگیری کنید

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // جستجو برای BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // اعتبارسنجی ویژگی‌های منبع

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource به اشتباه خوانده شده است");

                    }

                    // به‌روزرسانی ویژگی‌های منبع

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // ذخیره یک نسخه از PSD به‌روزشده

                    psdImage.save(dstPath, new PsdOptions());

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-217: تغییر اندازه فایل‌های PSD اگر یک ماسک در لایه تنظیم وجود داشته باشد که محدوده‌های خالی دارد به طور نادرست کار نمی‌کند**

{{< highlight java >}}

 // یک مثال از تغییر اندازه تصویری که شامل یک ماسک لایه تنظیم با محدوده خالی است.

// برنامه فقط یک PSD پیش‌فرض بارگیری می‌کند تا اطمینان حاصل شود که هیچ استثناءی وجود ندارد.

final int scale = 2; // ضریب دلخواه

String[] names = {

        "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

        "LevelsLayerWithLayerMaskRgb",

        "LevelsLayerWithLayerMaskCmyk",

};

for (String name : names)

{

    String srcFilePath = name + ".psd";

    String dstFilePath = "output_" + srcFilePath;

    String dstPngFilePath = "output_" + name + ".png";

    // یک PSD پیش‌فرض که شامل ماسک لایه تنظیم با محدوده خالی است بارگیری کنید

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, psdLoadOptions);

    try

    {

        // تغییر اندازه تصویر

        image.resize(image.getWidth() * scale, image.getHeight() * scale);

        // یک نسخه از PSD بارگیری شده را ذخیره کنید

        image.save(dstFilePath, new PsdOptions());

        // صدور PSD به فایل PNG (با کانال آلفا برای شفافیت)

        PngOptions pngOptions = new PngOptions();

        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        image.save(dstPngFilePath, pngOptions);

    }

    finally

    {

        image.dispose();

    }

}

{{< /highlight >}}

**PSDJAVA-218: تصویر Psd با حالت RGB 16 بیت/کانال فقط در پیش‌نمایش لایه‌ها را به‌روز می‌کند**

{{< highlight java >}}

 

 // این مثال نشان می‌دهد چگونه لایه‌های معمولی برای تصویر 16 بیتی RGB به‌روز رسانی شود. برنامه چیزی را 

// بر روی هر لایه رسم می‌کند تا مطمئن شود که تمام لایه به درستی به‌روز شده است.

String sourceFilePath = "in.psd";

String outputFilePath = "output.psd";

// یک PSD پیش‌فرض در حالت RGB 16 بیت/کانال بارگیری کنید

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    for (Layer layer : image.getLayers())

    {

        // نام لایه و حاشیه داخلی برای لایه معمولی رسم می‌کند

        if (!(layer instanceof LayerGroup) && !(layer instanceof AdjustmentLayer) &&

                (layer.getWidth() > 100) && (layer.getHeight() > 100))

        {

            Graphics graphics = new Graphics(layer);

            graphics.drawString(layer.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            graphics.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // یک نسخه از PSD بارگیری شده را ذخیره کنید

    image.save(outputFilePath, new PsdOptions(image));

}

finally

{

    image.dispose();

}

{{< /highlight >}}
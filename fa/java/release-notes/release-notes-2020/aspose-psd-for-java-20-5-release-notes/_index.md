---
title: یادداشت های نسخه Aspose.PSD برای جاوا 20.5
type: docs
weight: 40
url: /fa/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل یادداشت های نسخه برای [Aspose.PSD برای جاوا 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) می‌باشد.{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDJAVA-188|پشتیبانی از پیشرفت تبدیل سند|ویژگی|
|PSDJAVA-197|پشتیبانی از ذخیره سازی تصویر حالت رنگ خاکستری PSD با 16 بیت بر کانال|ویژگی|
|PSDJAVA-198|پشتیبانی از منبع Nvrt (منبع لایه تنظیم متقارن)|ویژگی|
|PSDJAVA-200|پشتیبانی از ماسک های لایه برای گروه های لایه|ویژگی|
|PSDJAVA-195|رفع مشکل ذخیره سازی تصویر PSD با حالت رنگ خاکستری 16 بیت بر کانال به فرمت 16 بیت بر کانال RGB PSD|ایراد|
|PSDJAVA-196|رفع مشکل ذخیره سازی تصویر PSD با حالت رنگ خاکستری 16 بیت بر کانال به فرمت خاکستری 8 بیت بر کانال|ایراد|
|PSDJAVA-199|تنظیم متن از طریق ITextPortion برای زبان‌های راست به چپ کار نمی‌کند. فایل خروجی دچار آسیب می‌شود.|ایراد|
|PSDJAVA-201|خطا هنگام تلاش برای باز کردن فایل خاص Psd با رنگ Lab و 8 بیت/کانال|ایراد|
# **تغییرات API عمومی**
# **API های اضافه شده:**
- هیچکدام
## **API های حذف شده:**
- هیچکدام
# **نمونه های استفاده:**

**PSDJAVA-188. پشتیبانی از پیشرفت تبدیل سند**

{{< highlight java >}}

 // یک مثال از استفاده از دستگیره پیشرفت برای عملیات بارگذاری و ذخیره سازی.

// برنامه از گزینه های ذخیره سازی مختلف برای فعالیت های پیشرفته استفاده می‌کند.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// ایجاد یک دستگیره پیشرفت که اطلاعات پیشرفت را به کنسول مینویسد

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s از %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- بارگذاری Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// پیوستن دستگیره پیشرفت برای نشان دادن پیشرفت بارگذاری

loadOptions.setProgressEventHandler(localProgressEventHandler);

// بارگذاری PSD با استفاده از گزینه های بارگذاری خاص

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- ذخیره Apple.psd به فرمت PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // تغییر نوع تصویر به رنگی و غیر شفاف

    pngOptions.setColorType(PngColorType.Truecolor);

    // پیوستن دستگیره پیشرفت برای نشان دادن پیشرفت ذخیره سازی

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // تبدیل PSD به PNG با خصوصیات خاص

    image.save(outputStream, pngOptions);

    System.out.println("---------- ذخیره Apple.psd به فرمت PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // تغییر حالت رنگی خروجی به RGB

    psdOptions.setColorMode(ColorModes.Rgb);

    // تنظیم یک کانال برای هر رنگ (قرمز، سبز و آبی) به علاوه یک کانال ترکیبی

    psdOptions.setChannelsCount((short)4);

    // پیوستن دستگیره پیشرفت برای نشان دادن پیشرفت ذخیره سازی

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // ذخیره یک نسخه از PSD با خصوصیات خاص

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. پشتیبانی از ذخیره سازی تصویر حالت رنگ خاکستری PSD با 16 بیت بر کانال**

{{< highlight java >}}

 // یک مثال از اعمال ترکیبات مختلف حالات رنگ، بیت بر کانال، تعداد کانال ها و فشرده سازی ها برای لایه های خاص.

// ساخت یک متد قابل دسترس از دامنه محلی

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // بارگذاری یک PSD 16 بیتی خاکستری از پیش تعیین شده

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // نقشه کشیدن حاشیه خاکستری درونی دور قطر لایه

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // ذخیره یک کپی از PSD با خصوصیات خاص

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // بارگذاری PSD ذخیره شده

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // تبدیل PSD ذخیره شده به تصویر PNG خاکستری

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // اینجا نباید هیچ استثنا وجود داشته باشد

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. پشتیبانی از منبع Nvrt (منبع لایه تنظیم متقارن)**

{{< highlight java >}}

 // یک مثال از یافتن NvrtResource در یک لایه تنظیم معکوس.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// بارگذاری یک PSD قبلا تعریف شده حاوی یک لایه تنظیم معکوس

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // تلاش برای یافتن یک منبع از لایه تنظیم معکوس

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // منبع NvrtResource یافت شده است

                    nvrtResource = (NvrtResource)layerResource;

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

**PSDJAVA-200. پشتیبانی از ماسک های لایه برای گروه های لایه**

{{< highlight java >}}

 // یک مثال از پشتیبانی از ماسک های لایه برای گروه های لایه. برنامه PSD را بارگیری و ذخیره می‌کند

// به فرمت های خروجی مختلف بدون پرتاب استثنا.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// بارگذاری یک PSD قبلا تعریف شده حاوی ماسک های لایه برای گروه های لایه

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // تبدیل PSD بارگیری شده به PNG

    input.save(outputPng, new PngOptions());

    // ذخیره یک کپی از PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. رفع مشکل ذخیره سازی تصویر PSD با حالت رنگ خاکستری 16 بیت بر کانال به فرمت 16 بیت بر کانال RGB PSD**

{{< highlight java >}}

 // یک مثال از تبدیل یک PSD خاکستری 16 بیتی به یکی RGB 16 بیتی و سپس به 

// خاکستری 16 بیتی اما تصویر Raster.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// بارگذاری یک PSD 16 بیتی خاکستری از پیش تعریف شده

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // نقشه کشیدن حاشیه خاکستری درونی دور قطر لایه

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // ذخیره یک کپی از PSD با تغییر حالت رنگی به RBG

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// بارگذاری PSD ذخیره شده

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // تبدیل PSD ذخیره شده به تصویر PNG خاکستری

    image1.save(pngExportPath, pngOptions); // اینجا نباید هیچ استثنا وجود داشته باشد

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. رفع مشکل ذخیره سازی تصویر PSD با حالت رنگ خاکستری 16 بیت بر کانال به فرمت خاکستری 8 بیت بر کانال**

{{< highlight java >}}

 // یک مثال از تبدیل یک PSD خاکستری 16 بیتی به یکی خاکستری 8 بیتی و سپس به

// یک تصویر خاکستری 8 بیتی Raster.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// بارگذاری یک PSD 16 بیتی خاکستری از پیش تعریف شده

PsdImage image = (P
---
title: تعليمات إصدار Aspose.PSD لـ Java 20.5
type: docs
weight: 40
url: /ar/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} تحتوي هذه الصفحة على تعليمات الإصدار لـ [Aspose.PSD لـ Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDJAVA-188|دعم لتقدم تحويل المستند|ميزة|
|PSDJAVA-197|دعم لحفظ صورة PSD لوضع الألوان الرمادية بعمق 16 بت لكل قناة|ميزة|
|PSDJAVA-198|دعم لمرجع Nvrt (مرجع طبقة التكيفات المعكوس)|ميزة|
|PSDJAVA-200|دعم أقنعة الطبقة لمجموعات الطبقات|ميزة|
|PSDJAVA-195|إصلاح حفظ صورة PSD بوضع الألوان الرمادية بعمق 16 بت لكل قناة إلى تنسيق PSD RGB بـ 16 بت لكل قناة|خطأ|
|PSDJAVA-196|إصلاح حفظ صورة PSD بوضع الألوان الرمادية بعمق 16 بت لكل قناة إلى تنسيق PSD رمادي بـ 8 بت لكل قناة|خطأ|
|PSDJAVA-199|لا يعمل توجيه النص من خلال ITextPortion للغات من اليمين إلى اليسار. يتم تلف الملف الناتج.|خطأ|
|PSDJAVA-201|استثناء عند محاولة فتح ملف Psd مع لون Lab و 8 بت/قناة معين|خطأ|

# **تغيرات API العامة**
# **تمت إضافة APIs:**
- لا شيء
## **تمت إزالة APIs:**
- لا شيء
# **أمثلة الاستخدام:**

**PSDJAVA-188. دعم لتقدم تحويل المستند**

{{< highlight java >}}

 // مثال على استخدام معالج التقدم لعمليات التحميل والحفظ.

// يستخدم البرنامج خيارات حفظ مختلفة لإطلاق أحداث التقدم.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// إنشاء معالج تقدم يكتب معلومات التقدم إلى وحدة التحكم

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s من أصل %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- تحميل Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// ربط المعالج التقدم لإظهار تقدم التحميل

loadOptions.setProgressEventHandler(localProgressEventHandler);

// تحميل PSD باستخدام خيارات تحميل محددة

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- حفظ Apple.psd إلى تنسيق PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // جعل الصورة المُخرجة ملونة وغير شفافة

    pngOptions.setColorType(PngColorType.Truecolor);

    // ربط المعالج التقدم لإظهار تقدم الحفظ

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // تحويل PSD إلى PNG بخصائص محددة

    image.save(outputStream, pngOptions);

    System.out.println("---------- حفظ Apple.psd إلى تنسيق PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // جعل الصورة المُخرجة PSD ملونة

    psdOptions.setColorMode(ColorModes.Rgb);

    // تعيين قناة لكل لون (أحمر، أخضر، أزرق) بالإضافة إلى قناة مركبة

    psdOptions.setChannelsCount((short)4);

    // ربط المعالج التقدم لإظهار تقدم الحفظ

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // حفظ نسخة من PSD بخصائص محددة

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. دعم حفظ صورة PSD بوضع الألوان الرمادية بعمق 16 بت لكل قناة**

{{< highlight java >}}

 // مثال على تطبيق مختلف من تركيبات وضع الألوان وعمق البتات وعدد القنوات والضغوط للطبقات المحددة.

// جعل الطريق يكون متاحاً من النطاق المحلي

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

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" + channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // تحميل PSD محدد مسبقًا بعمق رمادي 16 بت

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // رسم حدود رمادية داخلية حول حافة الطبقة

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // حفظ نسخة من PSD بخصائص محددة

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

        // تحميل PSD المحفوظ

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // تحويل PSD المحفوظ إلى صورة PNG بدرجة رمادية

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // يجب أن لا تكون هناك استثناء

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

**PSDJAVA-198. دعم مرجع Nvrt (مرجع طبقة التكيفات المعكوس)**

{{< highlight java >}}

 // مثال على العثور على مرجع NvrtResource لطبقة التكيف المعكوس.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// تحميل PSD محدد مسبقًا الذي يتضمن طبقة تكييف معكوس

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // محاولة العثور على مورد طبقة التكييف المعكوس

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // تم العثور على NvrtResource

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

**PSDJAVA-200. دعم أقنعة الطبقة لمجموعات الطبقات**

{{< highlight java >}}

 // مثال على دعم أقنعة الطبقة لمجموعات الطبقات. يقوم البرنامج بتحميل وحفظ PSD

// في تنسيقات مخرجة مختلفة دون رمي استثناء.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// تحميل PSD محدد مسبقًا الذي يحتوي على أقنعة لمجموعات الطبقات

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // تحويل PSD المحملة إلى PNG

    input.save(outputPng, new PngOptions());

    // حفظ نسخة من PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. إصلاح حفظ صورة PSD بوضع الألوان الرمادية بعمق 16 بت لكل قناة إلى تنسيق PSD RGB بـ 16 بت لكل قناة**

{{< highlight java >}}

 // مثال على تحويل PSD رمادي 16 بت إلى PSD RGB 16 بت ثم إلى

// صورة بت رمادية 16 بت ولكن بصورة نقطية.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// تحميل PSD محدد مسبقًا بعمق رمادي 16 بت

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // رسم حدود رمادية داخلية حول حافة الطبقة

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // حفظ نسخة من PSD بتغيير وضع اللون إلى RBG

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

// تحميل PSD المحفوظ

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // تحويل PSD المحفوظ إلى صورة PNG رمادية

    image1.save(pngExportPath, pngOptions); // يجب أن لا تكون هناك استثناء

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. إصلاح حفظ صورة PSD بوضع الألوان الرمادية بعمق 16 بت لكل قناة إلى تنسيق PSD رمادي بـ 8 بت لكل قناة**

{{< highlight java >}}

 // مثال على تحويل PSD رمادي 16 بت إلى PSD رمادي بـ 8 بت ثم إلى

// صورة نقطية رمادية بـ 8 بت.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// تحميل PSD محدد مسبقًا بعمق رمادي 16 بت

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // رسم حدود رمادية داخلية حول حافة الطبقة

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // حفظ نسخة من PSD بتغيير عدد القنوات إلى 8 بت

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// تحميل PSD المحفوظ

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // تحويل PSD المحفوظ إلى ص
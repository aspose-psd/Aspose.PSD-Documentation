---
title: یادداشت‌های نسخه Aspose.PSD برای Java 23.7
type: docs
weight: 40
url: /fa/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل یادداشت‌های نسخه برای [Aspose.PSD برای Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) است. {{% /alert %}}

| **کلید**   | **خلاصه**                                                                                                                                       | **دسته** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | افزودن قابلیت صادر کردن هر لایه از فایل PSD به فایل Animated Gif               | ویژگی |
| PSDJAVA-503 | تعیین ویژگی پرکردن لایه شکل از منبع vscg                                                       | ویژگی |
| PSDJAVA-504 | افزودن انواع جدیدی از وارپ (arc و arch)                                                          | ویژگی |
| PSDJAVA-505 | تغییر برنامه‌ای که فایل PSD را ذخیره می‌کند به Aspose.PSD اگر خصوصیت UpdateMetadata به true تنظیم شده باشد | ویژگی |
| PSDJAVA-510 | افزایش محدوده محاسبات تصویر وارپ                                                               | ویژگی |
| PSDJAVA-511 | پردازش لایه تنظیم سیاه و سفید شفافیت نادرست است                                              | باگ     |
| PSDJAVA-512 | جایگزینی محتوای SmartObject (هنگامی که گزینه‌های AllowWarpRepaint فعال است) پس از ۲ دقیقه محاسبه افت می‌کند | باگ     |
| PSDJAVA-513 | افزودن قابلیت به دست آوردن موقعیت چپ و بالای واقعی لایه گروه                                             | باگ     |
| PSDJAVA-514 | تغییر اندازه لایه زمانی که فایل psd دارای VogkResource با ساختارها در امتیازهاست اشتباه کار می‌کند  | باگ     |
| PSDJAVA-515 | TextBound به عنوان انتظار کار نمی‌کند                                                          | باگ     |
| PSDJAVA-516 | اضافه کردن یک لایه‌ای که با سازنده پیش‌فرض ایجاد شده به تصویر PSD، منابع پیش‌فرض را به آن اضافه نمی‌کند  | باگ     |
| PSDJAVA-517 | تعداد لوپ‌های Timeline در هنگام صادر کردن به فایل GIF متحرک نادیده گرفته می‌شود  | باگ     |

## **تغییرات در API عمومی**
# **API‌های اضافه شده:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **API‌های حذف شده:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **مثال‌های استفاده:**

**PSDJAVA-502. افزودن قابلیت صادر کردن هر لایه از فایل PSD به فایل Animated Gif**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // ایجاد فریم برای هر لایه.
        int framesCount = psdImage.getLayers().length;
        Timeline timeline = psdImage.getTimeline();

        Frame[] frames = new Frame[framesCount];
        for (int i = 0; i < framesCount; i++) {
            frames[i] = new Frame();
            LayerState[] layerStates = new LayerState[framesCount];

            for (int j = 0; j < framesCount; j++) {
                layerStates[j] = new LayerState();
                layerStates[j].setEnabled(i == j);
            }

            frames[i].setLayerStates(layerStates);
        }

        timeline.setFrames(frames);

        // به‌روز کردن وضعیت‌های فعلی
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}} 

**PSDJAVA-503. تعیین ویژگی پرکردن لایه شکل از منبع vscg**

{{< highlight java >}}
        // مثال پرکردن جامد
        public static void main(String[] args) {
            String srcFile = "src/main/resources/ShapeInternalSolid.psd";
            String outFile = "src/main/resources/ShapeInternalSolid.psd.out.psd";

            PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
            psdLoadOptions.setLoadEffectsResource(true);

            try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
                 ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
                  ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
                 fillSettings.setColor(Color.getRed());

                 shapeLayer.update();

                 image.save(outFile);
            }

            // بررسی تغییرات ذخیره شده
            try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();

            assertAreEqual(Color.getRed(), fillSettings.getColor());

            image.save(outFile);
        }

        static void assertAreEqual(Object expected, Object actual, String message) {
            if (!expected.equals(actual)) {
                throw new IllegalArgumentException(message);
            }
        }

        static void assertAreEqual(Object expected, Object actual) {
            assertAreEqual(expected, actual, "موارد برابر نیستند.");
        }

        //مثال پرکردن گرادیانت:
    public static void main(String[] args) {
        String srcFile = "src/main/resources/ShapeInternalGradient.psd";
        String outFile = "src/main/resources/ShapeInternalGradient.psd.out.psd";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();
            fillSettings.setDither(true);
            fillSettings.setReverse(true);
            fillSettings.setAlignWithLayer(false);
            fillSettings.setAngle(20);
            fillSettings.setScale(50);
            fillSettings.getColorPoints()[0].setLocation(100);
            fillSettings.getColorPoints()[1].setLocation(4000);
            fillSettings.getTransparencyPoints()[0].setLocation(200);
            fillSettings.getTransparencyPoints()[1].setLocation(3800);
            fillSettings.getTransparencyPoints()[0].setOpacity(90);
            fillSettings.getTransparencyPoints()[1].setOpacity(10);

            shapeLayer.update();

            image.save(outFile);
        }

        // بررسی تغییرات ذخیره شده
        try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();

            assertAreEqual(true, fillSettings.getDither());
            assertAreEqual(true, fillSettings.getReverse());
            assertAreEqual(false, fillSettings.getAlignWithLayer());
            assertAreEqual((double) 20, fillSettings.getAngle());
            assertAreEqual(50, fillSettings.getScale());
            assertAreEqual(100, fillSettings.getColorPoints()[0].getLocation());
            assertAreEqual(4000, fillSettings.getColorPoints()[1].getLocation());
            assertAreEqual(200, fillSettings.getTransparencyPoints()[0].getLocation());
            assertAreEqual(3800, fillSettings.getTransparencyPoints()[1].getLocation());
            assertAreEqual((double) 90, fillSettings.getTransparencyPoints()[0].getOpacity());
            assertAreEqual((double) 10,
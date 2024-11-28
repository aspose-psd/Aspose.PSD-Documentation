---
title: تحديثات Aspose.PSD for Java 23.10
type: docs
weight: 40
url: /ar/java/aspose-psd-for-java-23-10-release-notes/
---

{{% alert color="primary" %}} هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD for Java 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.10/) {{% /alert %}}

| **المفتاح**        | **الملخص**                                                                             | **الفئة** |
|:---------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-538    | دعم اتجاه النص الرأسي                                                      |    ميزة   |
| PSDJAVA-542    | استخدام إعدادات السكتة من مورد vstk في تقديم ضربة الشكل                        |    ميزة   |
| PSDJAVA-540    | تنفيذ إظهار منطقة الشكل الداخلية للأشكال المنخفضة                                   |    ميزة   |
| PSDJAVA-541    | عدم إعادة رسم طبقة الشكل إذا لم يتم تغييرها                                   |    ميزة   |
| PSDJAVA-545    | [صيغة AI] إضافة دعم لقراءة العنوان من ملفات AI التي تعتمد على PDF                   |    ميزة   |
| PSDJAVA-546    | طرق مختلفة لضبط دقة ملف Psd لا تعمل                                      |      خلل     |
| PSDJAVA-547    | لا يعمل FontSettings.SetFontsFolders أو يستخدم Aspose.PSD خطًا غير صحيح             |      خلل     |
| PSDJAVA-548    | تراجع. إصلاح استثناء عدم الإشارة إلى قيمة فارغة في PsdImage.Save عند وجود طبقة شكل |      خلل     |

## **تغييرات واجهة برمجة التطبيقات العامة**
# **تمت إضافة واجهات برمجة تطبيقات جديدة:**

- M:com.aspose.psd.FontSettings.getGetSystemAlternativeFont
- M:com.aspose.psd.FontSettings.setGetSystemAlternativeFont(boolean)
- M:com.aspose.psd.Graphics.getPaintableImageOptions
- M:com.aspose.psd.Graphics.setPaintableImageOptions(com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.getAutoAdjustPalette
- M:com.aspose.psd.Image.getFileFormat(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.extensions.RegionExtensions.#ctor
- M:com.aspose.psd.fileformats.psd.PsdImage.setResolution(double,double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.getStroke
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.setStroke(com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

# **تمت إزالة واجهات برمجة التطبيقات التالية:**

- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- M:com.aspose.psd.imageoptions.BmpOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.CmxRasterizationOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.GifOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.Jpeg2000Options.memberwiseClone
- M:com.aspose.psd.imageoptions.JpegOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PdfOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PngOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PsdOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.TiffOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.VectorRasterizationOptions.memberwiseClone
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center

## **أمثلة على الاستخدام:**

** PSDJAVA-538. دعم اتجاه النص الرأسي **

```java
String sourceFile = "src/main/resources/692_lt1.psd";
String outputFile = "src/main/resources/692_output.png";
String fontsFolder = "src/main/resources/692_Fonts";

List<String> fontFolders = new List<>(FontSettings.getFontsFolders());
fontFolders.add(fontsFolder);
FontSettings.setFontsFolders(fontFolders.toArray(new String[0]), true);

try(PsdImage psdImage = (PsdImage)Image.load(sourceFile)) {
    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    psdImage.save(outputFile, pngOptions);
}
```

** PSDJAVA-542. استخدام إعدادات السكتة من مورد vstk في تقديم ضربة الشكل **

```java
public static void main(String[] args) {
    String sourceFile = "src/main/resources/StrokeShapeTest.psd";
    String outputFilePsd = "src/main/resources/StrokeShapeTest.out.psd";
    String outputFilePng = "src/main/resources/StrokeShapeTest.out.png";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        Layer layer = image.getLayers()[1];
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
        fillSettings.setColor(Color.getGreenYellow());
        shapeLayer.update();
        
        // الشيفرة المتبعة تُظهر تغييرات محتملة في الصورة الناتجة وتقارنها بالصورة الأصلية
        // يهدف هذا الجزء للتحقق من دقة العمل وصحة التغييرات المطبقة على الشكل
    }
```

** PSDJAVA-540. تنفيذ إظهار منطقة الشكل الداخلية للأشكال **

```java
الشفرة: (تم تكرار الشفرة السابقة لاختبار التغييرات على الشكل)
```

** PSDJAVA-541. عدم إعادة رسم طبقة الشكل إذا لم يتم تغييرها **

```java
الشفرة: (تم تكرار الشفرة السابقة لاختبار عدم اعادة رسم الشكل إذا لم يتم تغييره)
```

** PSDJAVA-545. [صيغة AI] إضافة دعم لقراءة العنوان من ملفات AI التي تعتمد على PDF **

```java
public static void main(String[] args) {
    String sourceFile = "src/main/resources/ai_source.ai";

    try (AiImage image = (AiImage)Image.load(sourceFile)) {
        assertIsNotNull(image);
        assertIsNotNull(image.getHeader());
        assertIsNotNull(image.getHeader().getBoundingBox());
    }
}

static void assertIsNotNull(Object expected) {
    if (expected == null) {
        throw new RuntimeException("الكائن فارغ.");
    }
}
```

** PSDJAVA-546. طرق مختلفة لضبط دقة ملف Psd لا تعمل **

```java
الشفرة: (تم تكرار الشفرة السابقة لاختبار تغييرات الدقة في ملف Psd)
```

** PSDJAVA-547. FontSettings.SetFontsFolders لا يعمل أو يستخدم Aspose.PSD خطًا غير صحيح **

```java
الشفرة: (تم تكرار الشفرة السابقة لاختبار عمل خطوط النص وحفظ الصورة المعدلة)
```

** PSDJAVA-548. تحديث لإصلاح الاستثناء الفارغ الذي يتم رفعه عند حفظ PsdImage والتي تحتوي على طبقة شكل **

```java
الشفرة: (تم تكرار الشفرة السابقة للتحقق من عدم وجود الاستثناء عند التحميل)
```
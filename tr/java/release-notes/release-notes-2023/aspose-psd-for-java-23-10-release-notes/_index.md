---
title: Aspose.PSD Java için 23.10 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-23-10-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD Java için 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.10/) sürümü için sürüm notlarını içerir. {{% /alert %}}

| **Anahtar**    | **Özet**                                                                                               | **Kategori** |
|:-------------- |:-------------------------------------------------------------------------------------------------------|:------------|
| PSDJAVA-538    | Dikey metin yönü desteği                                                                               |    Özellik   |
| PSDJAVA-542    | Şekil İçeriğindeki Vstk Kaynağından Varyasyonları Kullanma                                              |    Özellik   |
| PSDJAVA-540    | Stroke şekilleri için iç alanın render edilmesi uygulaması                                            |    Özellik   |
| PSDJAVA-541    |Şekil katmanı değiştirilmediyse tekrar boyama                                                       |    Özellik   |
| PSDJAVA-545    | [AI Format] PDF tabanlı AI Dosyalarındaki Başlığın okunması için destek ekleme                         |    Özellik   |
| PSDJAVA-546    | Çeşitli Psd Dosya Çözünürlüğü ayarlarının çalışmaması                                                  |      Hata    |
| PSDJAVA-547    | FontSettings.SetFontsFolders çalışmaz veya Aspose.PSD yanlış font kullanır                               |      Hata    |
| PSDJAVA-548    | Regresyon. Şekil katmanı bulunduğunda Null referansı istisnası düzeltildi                                |      Hata    |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**

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

# **Kaldırılan API'ler:**

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

## **Kullanım Örnekleri:**

** PSDJAVA-538. Dikey metin yönü desteği**

{{< highlight java >}}
    
    String kaynakDosya = "src/main/resources/692_lt1.psd";
    String çıktıDosyası = "src/main/resources/692_output.png";
    String fontKlasörü = "src/main/resources/692_Fonts";

        List<String> fontKlasörleri = new List<>(FontSettings.getFontsFolders());
        fontKlasörleri.add(fontKlasörü);
        FontSettings.setFontsFolders(fontKlasörleri.toArray(new String[0]), true);

        try(PsdImage psdResmi = (PsdImage)Image.load(kaynakDosya)) {
            PngOptions pngSeçenekleri = new PngOptions();
            pngSeçenekleri.setColorType(PngColorType.TruecolorWithAlpha);

            psdResmi.save(çıktıDosyası, pngSeçenekleri);
        }

{{< /highlight >}}

** PSDJAVA-542. Shape Stroke renderlama işlemi için vstk kaynağından Stroke ayarlarını kullanma**

{{< highlight java >}}

    public static void main(String[] args) {
        String kaynakDosya = "src/main/resources/StrokeShapeTest.psd";
        String çıktıDosyasıPsd = "src/main/resources/StrokeShapeTest.out.psd";
        String çıktıDosyasıPng = "src/main/resources/StrokeShapeTest.out.png";

        try (PsdImage görüntü = (PsdImage) Image.load(kaynakDosya)) {
            Layer katman = görüntü.getLayers()[1];
            ShapeLayer şekilKatmanı = (ShapeLayer) görüntü.getLayers()[1];
            ColorFillSettings dolumAyarları = (ColorFillSettings) şekilKatmanı.getFill();
            dolumAyarları.setColor(Color.getGreenYellow());
            şekilKatmanı.update();

            ShapeLayer şekilKatmanı2 = (ShapeLayer) görüntü.getLayers()[3];
            GradientFillSettings gradyanAyarları = (GradientFillSettings) şekilKatmanı2.getFill();
            gradyanAyarları.setDither(true);
            gradyanAyarları.setReverse(true);
            gradyanAyarları.setAlignWithLayer(false);
            gradyanAyarları.setAngle(20);
            gradyanAyarları.setScale(50);
            gradyanAyarları.getColorPoints()[0].setLocation(100);
            gradyanAyarları.getColorPoints()[1].setLocation(4000);
            gradyanAyarları.getTransparencyPoints()[0].setLocation(200);
            gradyanAyarları.getTransparencyPoints()[1].setLocation(3800);
            gradyanAyarları.getTransparencyPoints()[0].setOpacity(90);
            gradyanAyarları.getTransparencyPoints()[1].setOpacity(10);
            şekilKatmanı2.update();

            ShapeLayer şekilKatmanı3 = (ShapeLayer) görüntü.getLayers()[5];
            StrokeSettings strokeAyarları = (StrokeSettings) şekilKatmanı3.getStroke();
            strokeAyarları.setSize(15);
            ColorFillSettings strokeDolumAyarları = (ColorFillSettings) strokeAyarları.getFill();
            strokeDolumAyarları.setColor(Color.getGreenYellow());
            şekilKatmanı3.update();

            görüntü.save(çıktıDosyasıPsd);
            görüntü.save(çıktıDosyasıPng, new PngOptions());
        }

        // Değişiklik yapılan veriler kontrol ediliyor.
        try (PsdImage görüntü = (PsdImage) Image.load(çıktıDosyasıPsd)) {
            ShapeLayer şekilKatmanı = (ShapeLayer) görüntü.getLayers()[1];
            ColorFillSettings dolumAyarları = (ColorFillSettings) şekilKatmanı.getFill();
            assertAreEqual(Color.getGreenYellow(), dolumAyarları.getColor());

            ShapeLayer şekilKatmanı2 = (ShapeLayer) görüntü.getLayers()[3];
            GradientFillSettings gradyanAyarları = (GradientFillSettings) şekilKatmanı2.getFill();
            assertAreEqual(true, gradyanAyarları.getDither());
            assertAreEqual(true, gradyanAyarları.getReverse());
            assertAreEqual(false, gradyanAyarları.getAlignWithLayer());
            assertAreEqual(20.0, gradyanAyarları.getAngle());
            assertAreEqual(50, gradyanAyarları.getScale());
            assertAreEqual(100, gradyanAyarları.getColorPoints()[0].getLocation());
            assertAreEqual(4000, gradyanAyarları.getColorPoints()[1].getLocation());
            assertAreEqual(200, gradyanAyarları.getTransparencyPoints()[0].getLocation());
            assertAreEqual(3800, gradyanAyarları.getTransparencyPoints()[1].getLocation());
            assertAreEqual(90.0, gradyanAyarları.getTransparencyPoints()[0].getOpacity());
            assertAreEqual(10.0, gradyanAyarları.getTransparencyPoints()[1].getOpacity());

            ShapeLayer şekilKatmanı3 = (ShapeLayer) görüntü.getLayers()[5];
            StrokeSettings strokeAyarları = (StrokeSettings) şekilKatmanı3.getStroke();
            ColorFillSettings strokeDolumAyarları = (ColorFillSettings) strokeAyarları.getFill();
            assertAreEqual(15.0, strokeAyarları.getSize());
            assertAreEqual(Color.getGreenYellow(), strokeDolumAyarları.getColor());
        }
    }

    static void assertAreEqual(Object beklenen, Object gerçek) {
        assertAreEqual(beklenen, gerçek, "Nesneler eşit değil.");
    }

    static void assertAreEqual(Object beklenen, Object gerçek, String mesaj) {
        if (!beklenen.equals(gerçek)) {
            throw new IllegalArgumentException(mesaj);
        }
    }

{{< /highlight >}}


** PSDJAVA-540. Stroke şekillerinin iç alanını render etme uygulaması**

{{< highlight java >}}

    public static void main(String[] args) {
        String kaynakDosya = "src/main/resources/StrokeShapeTest.psd";
        String çıktıDosyasıPsd = "src/main/resources/StrokeShapeTest.out.psd";
        String çıktıDosyasıPng = "src/main/resources/StrokeShapeTest.out.png";

        try (PsdImage görüntü = (PsdImage) Image.load(kaynakDosya)) {
            Layer katman = görüntü.getLayers()[1];
            ShapeLayer şekilKatmanı = (ShapeLayer) görüntü.getLayers()[1];
            ColorFillSettings dolumAyarları = (ColorFillSettings) şekilKatmanı.getFill();
            dolumAyarları.setColor(Color.getGreenYellow());
            şekilKatmanı.update();

            ShapeLayer şekilKatmanı2 = (ShapeLayer) görüntü.getLayers()[3];
            GradientFillSettings gradyanAyarları = (GradientFillSettings) şekilKatmanı2.getFill();
            gradyanAyarları.setDither(true);
            gradyanAyarları.setReverse(true);
            gradyanAyarları.setAlignWithLayer(false);
            gradyanAyarları.setAngle(20);
            gradyanAyarları.setScale(50);
            gradyanAyarları.getColorPoints()[0].setLocation(100);
            gradyanAyarları.getColorPoints()[1].setLocation(4000);
            gradyanAyarları.getTransparencyPoints()[0].setLocation(200);
            gradyanAyarları.getTransparencyPoints()[1].setLocation(3800);
            gradyanAyarları.getTransparencyPoints()[0].setOpacity(90);
            gradyanAyarları.getTransparencyPoints()[1].setOpacity(10);
            şekilKatmanı2.update();

            ShapeLayer şekilKatmanı3 = (ShapeLayer) görüntü.getLayers()[5];
            StrokeSettings strokeAyarları = (StrokeSettings) şekilKatmanı3.getStroke();
            strokeAyarları.setSize(15);
            ColorFillSettings strokeDolumAyarları = (ColorFillSettings) strokeAyarları.getFill();
            strokeDolumAyarları.setColor(Color.getGreenYellow());
            şekilKatmanı3.update();

            görüntü.save(çıktıDosyasıPsd);
            görüntü.save(çıktıDosyasıPng, new PngOptions());
        }

        // Değişiklik yapılan veriler kontrol ediliyor.
        try (PsdImage görüntü = (PsdImage) Image.load(çıktıDosyasıPsd)) {
            ShapeLayer şekilKatmanı = (ShapeLayer) görüntü.getLayers()[1];
            ColorFillSettings dolumAyarları = (ColorFillSettings) şekilKatmanı.getFill();
            assertAreEqual(Color.getGreenYellow(), dolumAyarları.getColor());

            ShapeLayer şekilKatmanı2 = (ShapeLayer) görüntü.getLayers()[3];
            GradientFillSettings gradyanAyarları = (GradientFillSettings) şekilKatmanı2.getFill();
            assertAreEqual(true, gradyanAyarları.getDither());
            assertAreEqual(true, gradyanAyarları.getReverse());
            assertAreEqual(false, gradyanAyarları.getAlignWithLayer());
            assertAreEqual(20.0, gradyanAyarları.getAngle());
            assertAreEqual(50, gradyanAyarları.getScale());
            assertAreEqual(100, gradyanAyarları.getColorPoints()[0].getLocation());
            assertAreEqual(4000, gradyanAyarları.getColorPoints()[1].getLocation());
            assertAreEqual(200, gradyanAyarları
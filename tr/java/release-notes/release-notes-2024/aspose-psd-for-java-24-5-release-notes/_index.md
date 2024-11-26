---
title: Aspose.PSD for Java 24.5 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-24-5-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 24.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.5/) için sürüm notlarını içerir. {{% /alert %}}

| **Anahtar** | **Özet**                                                                                                                 | **Kategori**  |
|:------------|:------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-617 | [AI Format] AI dosyalarını EPSF başlığıyla işleme desteği ekleyin                                                         | Özellik       |
| PSDJAVA-620 | Psd dosyası önizlemesinde yarı şeffaflık yanlış işlenir                                                                   | Hata          |
| PSDJAVA-621 | Şekil Katmanının Kısmen Yanlış Düzenlenmesi                                                                               | Hata          |
| PSDJAVA-622 | Bellek kullanımıyla ilgili bir sorun var: 200 MB'dan büyük boyutlu ve büyük boyutlarda PSD dosyalarını kaydederken istisna      | Hata          |
| PSDJAVA-623 | 23.7'den 24.3'e güncellemeden sonra PDF'ye kaydederken görüntü kaydedilemedi istisnası                                  | Hata          |
| PSDJAVA-624 | Çin Yazı Tipleri için GetFontInfoRecords yöntemindeki sorunu düzeltin                                                    | Hata          |

## **Açık API Değişiklikleri**
# **Eklenen API'ler:**

- M:com.aspose.psd.fileformats.ai.AiLayerSection.getColorIndex
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setColorIndex(int)
- M:com.aspose.psd.fileformats.ai.AiLayerSection.hasMultiLayerMasks
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setMultiLayerMasks(boolean)
- M:com.aspose.psd.imageoptions.PsdOptions.getBackgroundContents
- M:com.aspose.psd.imageoptions.PsdOptions.setBackgroundContents(com.aspose.psd.fileformats.psd.rawcolor.RawColor)

# **Kaldırılan API'ler:**

- Hiçbiri

## **Kullanım Örnekleri:**

**PSDJAVA-617. [AI Format] AI dosyalarını EPSF başlığıyla işleme desteği ekleyin**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/örnek.ai";
        String outputFilePath = "src/main/resources/örnek.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            assertAreEqual(image.getLayers().length, 2);
            assertAreEqual(image.getLayers()[0].hasMultiLayerMasks(), false);
            assertAreEqual(image.getLayers()[0].getColorIndex(), -1);
            assertAreEqual(image.getLayers()[1].hasMultiLayerMasks(), false);
            assertAreEqual(image.getLayers()[1].getColorIndex(), -1);

            image.save(outputFilePath, new PngOptions());
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Nesneler eşit değil.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-620. Psd dosyası önizlemesinde yarı şeffaflık yanlış işlenir**

{{< highlight java >}}

        String sourceFile = "src/main/resources/frog_nosymb.psd";
        String outputFile = "src/main/resources/frog_nosymb_backgroundcontents_output.psd";

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
            RawColor backgroundColor = new RawColor(PixelDataFormat.getRgb32Bpp());
            int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
            backgroundColor.setAsInt(argbValue); // Beyaz

            PsdOptions psdOptions = new PsdOptions(psdImage);
            psdOptions.setColorMode(ColorModes.Rgb);
            psdOptions.setCompressionMethod(CompressionMethod.RLE);
            psdOptions.setChannelsCount((short) 4);
            psdOptions.setBackgroundContents(backgroundColor);

            psdImage.save(outputFile, psdOptions);
        }

{{< /highlight >}}

**PSDJAVA-621. Şekil Katmanının Kısmen Yanlış Düzenlenmesi**

{{< highlight java >}}

    private static final int ImgToPsdRatio = 256 * 65535;

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/ShapeLayerTest.psd";
        String outputFile = "src/main/resources/ShapeLayerTest_output.psd";
        
        try (PsdImage im = (PsdImage) Image.load(sourceFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) im.getLayers()[2];
            IPath path = shapeLayer.getPath();
            IPathShape[] pathShapes = path.getItems();
            List<BezierKnotRecord> knotsList = new ArrayList<>();
            for (IPathShape pathShape : pathShapes) {
                BezierKnotRecord[] knots = pathShape.getItems();
                Collections.addAll(knotsList, knots);
            }

            // Katman özelliklerini değiştir
            PathShape newShape = new PathShape();

            BezierKnotRecord firstBezierKnotRecord = new BezierKnotRecord();
            firstBezierKnotRecord.setLinked(true);
            firstBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize())});

            BezierKnotRecord secondBezierKnotRecord = new BezierKnotRecord();
            secondBezierKnotRecord.setLinked(true);
            secondBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(50, 490),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 490),
                            shapeLayer.getContainer().getSize()), // Sabit Nokta
                    pointFToResourcePoint(
                            new PointF(150, 490),
                            shapeLayer.getContainer().getSize())
            });

            BezierKnotRecord thirdBezierKnotRecord = new BezierKnotRecord();
            thirdBezierKnotRecord.setLinked(true);
            thirdBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(490, 150),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 50),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 20),
                            shapeLayer.getContainer().getSize()),
            });

            BezierKnotRecord[] bezierKnots = new BezierKnotRecord[]
                    {firstBezierKnotRecord, secondBezierKnotRecord, thirdBezierKnotRecord};

            newShape.setItems(bezierKnots);

            List<IPathShape> newShapes = new ArrayList<>(Arrays.asList(pathShapes));
            newShapes.add(newShape);

            IPathShape[] pathShapeNew = newShapes.toArray(new IPathShape[0]);
            path.setItems(pathShapeNew);

            shapeLayer.update();

            im.save(outputFile, new PsdOptions());
        }

        try (PsdImage im = (PsdImage) Image.load(outputFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) im.getLayers()[2];
            IPath path = shapeLayer.getPath();
            IPathShape[] pathShapes = path.getItems();
            List<BezierKnotRecord> knotsList = new ArrayList<>();
            for (IPathShape pathShape : pathShapes) {
                BezierKnotRecord[] knots = pathShape.getItems();
                knotsList.addAll(Arrays.asList(knots));
            }

            assertAreEqual(3, pathShapes.length);
            assertAreEqual(42, shapeLayer.getLeft());
            assertAreEqual(14, shapeLayer.getTop());
            assertAreEqual(1600, shapeLayer.getBounds().getWidth());
            assertAreEqual(1086, shapeLayer.getBounds().getHeight());
        }
    }

    static Point pointFToResourcePoint(PointF point, Size imageSize) {
        return new Point(
                (int) Math.round(point.getY() * (ImgToPsdRatio / imageSize.getHeight())),
                (int) Math.round(point.getX() * (ImgToPsdRatio / imageSize.getWidth())));
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Nesneler eşit değil.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-622. Bellek kullanımı ile ilgili bir sorun var: 200 MB'dan büyük boyutlu ve büyük boyutlarda PSD dosyalarını kaydederken istisna**

{{< highlight java >}}

    String kaynakDosya = "src/main/resources/büyükDosya.psd";
    String çıktıDosyası = "src/main/resources/çıktı_raw.psd";

    PsdLoadOptions yüklemeSeçenekleri = new PsdLoadOptions();
    yüklemeSeçenekleri.setLoadEffectsResource(true);
    yüklemeSeçenekleri.setUseDiskForLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(kaynakDosya, yüklemeSeçenekleri)) {
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setCompressionMethod(CompressionMethod.RLE);

        // Burada herhangi bir hata olmamalı
        psdImage.save(çıktıDosyası, psdOptions);
    }

{{< /highlight >}}

**PSDJAVA-623. 23.7'den 24.3'e güncellemeden sonra PDF'ye kaydederken görüntü kaydedilemedi istisnası**

{{< highlight java >}}

    String kaynakDosya = "src/main/resources/CVFlor.psd";
    String çıktıDosyası = "src/main/resources/_export.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(kaynakDosya)) {
        PdfOptions kaydetmeSeçenekleri = new PdfOptions();
        kaydetmeSeçenekleri.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(çıktıDosyası, kaydetmeSeçenekleri);
    }

{{< /highlight >}}

**PSDJAVA-624. Çin Yazı Tipleri için GetFontInfoRecords yöntemindeki sorunu düzeltin**

{{< highlight java >}}

    String fontKlasörü = "src/main/resources/Yazıtipi";
    String kaynakDosya = "src/main/resources/bd-worlds-best-pink.psd";

    PsdLoadOptions psdYüklemeSeçenekleri = new PsdLoadOptions();
    psdYüklemeSeçenekleri.setLoadEffectsResource(true);
    psdYüklemeSeçenekleri.setAllowWarpRepaint(true);

    try {
        FontSettings.setFontsFolders(new String[]{fontKlasörü}, true);

        try (PsdImage image = (PsdImage) PsdImage.load(kaynakDosya, psdYüklemeSeçenekleri)) {
            for (Layer katman : image.getLayers()) {
                if (katman instanceof TextLayer) {
                    TextLayer metinKatmanı = (TextLayer) katman;

                    if ("en iyi".equals(metinKatmanı.getText())) {
                        // Buraya bu onarım olmadan bir hata olacak çünkü Çin yazı tipi.
                        metinKatmanı.updateText("BAŞARI");
                    }
                }
            }
        }
    } finally {
        FontSettings.reset();
    }

{{< /highlight >}}
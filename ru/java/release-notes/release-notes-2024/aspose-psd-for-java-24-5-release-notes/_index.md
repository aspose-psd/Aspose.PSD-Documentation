---
title: Aspose.PSD для Java 24.5 - Примечания к выпуску
type: docs
weight: 40
url: /ru/java/aspose-psd-dlya-java-24-5-primechaniya-k-vypusku/
---

{{% alert color="primary" %}} Эта страница содержит примечания к выпуску для [Aspose.PSD для Java 24.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.5/) {{% /alert %}}

| **Ключ**     | **Описание**                                                                                                | **Категория** |
|:------------|:----------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-617 | [Формат AI] Добавлена поддержка обработки файлов AI с заголовком EPSF                                       | Функция      |
| PSDJAVA-620 | Неправильная обработка полупрозрачности при предварительном просмотре файла psd                            | Ошибка       |
| PSDJAVA-621 | Частично неверное отображение слоя формы                                                                      | Ошибка       |
| PSDJAVA-622 | Исключение при сохранении файлов PSD с размером более 200 МБ и большими размерами (проблема использования памяти) | Ошибка       |
| PSDJAVA-623 | Исключение при сохранении изображения в PDF после обновления с 23.7 до 24.3                                  | Ошибка       |
| PSDJAVA-624 | Исправлена проблема в методе GetFontInfoRecords для китайских шрифтов                                       | Ошибка       |

## **Изменения в публичном API**
# **Добавленные API:**

- M:com.aspose.psd.fileformats.ai.AiLayerSection.getColorIndex
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setColorIndex(int)
- M:com.aspose.psd.fileformats.ai.AiLayerSection.hasMultiLayerMasks
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setMultiLayerMasks(boolean)
- M:com.aspose.psd.imageoptions.PsdOptions.getBackgroundContents
- M:com.aspose.psd.imageoptions.PsdOptions.setBackgroundContents(com.aspose.psd.fileformats.psd.rawcolor.RawColor)

# **Удаленные API:**

- Нет

## **Примеры использования:**

**PSDJAVA-617. [Формат AI] Добавлена поддержка обработки файлов AI с заголовком EPSF**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/example.ai";
        String outputFilePath = "src/main/resources/example.png";

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
        assertAreEqual(expected, actual, "Объекты не равны.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-620. Неправильная обработка полупрозрачности при предварительном просмотре файла psd**

{{< highlight java >}}

        String sourceFile = "src/main/resources/frog_nosymb.psd";
        String outputFile = "src/main/resources/frog_nosymb_backgroundcontents_output.psd";

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
            RawColor backgroundColor = new RawColor(PixelDataFormat.getRgb32Bpp());
            int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
            backgroundColor.setAsInt(argbValue); // Белый

            PsdOptions psdOptions = new PsdOptions(psdImage);
            psdOptions.setColorMode(ColorModes.Rgb);
            psdOptions.setCompressionMethod(CompressionMethod.RLE);
            psdOptions.setChannelsCount((short) 4);
            psdOptions.setBackgroundContents(backgroundColor);

            psdImage.save(outputFile, psdOptions);
        }

{{< /highlight >}}

**PSDJAVA-621. Частично неверное отображение слоя формы**

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

            // Изменение свойств слоя
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
                            shapeLayer.getContainer().getSize()), // Точка крепления
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
        assertAreEqual(expected, actual, "Объекты не равны.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-622. Исключение при сохранении файлов PSD с размером более 200 МБ и большими размерами (проблема использования памяти)**

{{< highlight java >}}

    String sourceFile = "src/main/resources/bigfile.psd";
    String outputFile = "src/main/resources/output_raw.psd";

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setLoadEffectsResource(true);
    loadOptions.setUseDiskForLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, loadOptions)) {
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setCompressionMethod(CompressionMethod.RLE);

        // Здесь не должно быть ошибок
        psdImage.save(outputFile, psdOptions);
    }

{{< /highlight >}}

**PSDJAVA-623. Исключение при сохранении изображения в PDF после обновления с 23.7 до 24.3**

{{< highlight java >}}

    String sourceFile = "src/main/resources/CVFlor.psd";
    String outputFile = "src/main/resources/_export.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-624. Исправлена проблема в методе GetFontInfoRecords для китайских шрифтов**

{{< highlight java >}}

    String fontFolder = "src/main/resources/Font";
    String sourceFile = "src/main/resources/bd-worlds-best-pink.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    psdLoadOptions.setAllowWarpRepaint(true);

    try {
        FontSettings.setFontsFolders(new String[]{fontFolder}, true);

        try (PsdImage image = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
            for (Layer layer : image.getLayers()) {
                if (layer instanceof TextLayer) {
                    TextLayer textLayer = (TextLayer) layer;

                    if ("best".equals(textLayer.getText())) {
                        // Без этого исправления здесь будет исключение из-за китайского шрифта
                        textLayer.updateText("SUCCESS");
                    }
                }
            }
        }
    } finally {
        FontSettings.reset();
    }

{{< /highlight >}}
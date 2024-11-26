---
title: Релизные заметки Aspose.PSD для Java 24.4
type: docs
weight: 40
url: /ru/java/aspose-psd-for-java-24-4-release-notes/
---

{{% alert color="primary" %}} Эта страница содержит релизные заметки для [Aspose.PSD для Java 24.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.4/) {{% /alert %}}

| **Ключ**    | **Описание**                                                                                           | **Категория** |
|:------------|:------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-610 | Установка лицензии для Aspose.PSD для Java приводит к исключению, если это сделано более одного раза     | Ошибка        |
| PSDJAVA-611 | [Формат AI] Добавлена обработка ресурса XObjectForm                                                   | Функция       |
| PSDJAVA-612 | Добавлен конструктор для ShapeLayer                                                                    | Функция       |
| PSDJAVA-613 | Исправление конвертации файла Psd из RGB в CMYK                                                        | Ошибка        |
| PSDJAVA-614 | Определенный файл PSD не может быть экспортирован с использованием Aspose.PSD                          | Ошибка        |

## **Изменения в общедоступном API**
# **Добавленные API:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addShapeLayer

# **Удаленные API:**

- Нет

## **Примеры использования:**

**PSDJAVA-610. Установка лицензии для Aspose.PSD для Java приводит к исключению, если это сделано более одного раза**

{{< highlight java >}}

        License license = new License();
        String liccorrectJava = "Aspose.PSD.Java.lic";

        license.setLicense(liccorrectJava);
        license.setLicense(liccorrectJava);

{{< /highlight >}}

**PSDJAVA-611. [Формат AI] Добавлена обработка ресурса XObjectForm**

{{< highlight java >}}

        String sourceFile = "src/main/resources/example.ai";
        String outputFilePath = "src/main/resources/example.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-612. Добавлен конструктор для ShapeLayer**

{{< highlight java >}}

    private static final int IMG_TO_PSD_RATIO = 256 * 65535;

    public static void main(String[] args) {
        String outputFile = "src/main/resources/AddShapeLayer_output.psd";

        try (PsdImage newPsd = new PsdImage(600, 400)) {
            ShapeLayer layer = newPsd.addShapeLayer();

            PathShape newShape = generateNewShape(newPsd.getSize());
            List<IPathShape> newShapes = new List<>();
            newShapes.add(newShape);
            layer.getPath().setItems(newShapes.toArray(new IPathShape[0]));

            layer.update();

            newPsd.save(outputFile);
        }

        try (PsdImage image = (PsdImage) Image.load(outputFile)) {
            assertAreEqual(2, image.getLayers().length);

            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings internalFill = (ColorFillSettings) shapeLayer.getFill();
            IStrokeSettings strokeSettings = shapeLayer.getStroke();
            ColorFillSettings strokeFill = (ColorFillSettings) strokeSettings.getFill();

            assertAreEqual(1, shapeLayer.getPath().getItems().length); // 1 Форма
            assertAreEqual(3, shapeLayer.getPath().getItems()[0].getItems().length); // 3 узла в форме

            assertAreEqual(-16127182, internalFill.getColor().toArgb()); // ff09eb32

            assertAreEqual(7.41, strokeSettings.getSize());
            assertAreEqual(false, strokeSettings.getEnabled());
            assertAreEqual(StrokePosition.Center, strokeSettings.getLineAlignment());
            assertAreEqual(LineCapType.ButtCap, strokeSettings.getLineCap());
            assertAreEqual(LineJoinType.MiterJoin, strokeSettings.getLineJoin());
            assertAreEqual(-16777216, strokeFill.getColor().toArgb()); // ff000000
        }
    }

    static PathShape generateNewShape(Size imageSize) {
        PathShape newShape = new PathShape();

        PointF point1 = new PointF(20, 100);
        PointF point2 = new PointF(200, 100);
        PointF point3 = new PointF(300, 10);

        BezierKnotRecord firstBezierKnotRecord = new BezierKnotRecord();
        firstBezierKnotRecord.setLinked(true);
        firstBezierKnotRecord.setPoints(new Point[]{
                pointFToResourcePoint(point1, imageSize),
                pointFToResourcePoint(point1, imageSize),
                pointFToResourcePoint(point1, imageSize)
        });

        BezierKnotRecord secondBezierKnotRecord = new BezierKnotRecord();
        secondBezierKnotRecord.setLinked(true);
        secondBezierKnotRecord.setPoints(new Point[]{
                pointFToResourcePoint(point2, imageSize),
                pointFToResourcePoint(point2, imageSize),
                pointFToResourcePoint(point2, imageSize)
        });

        BezierKnotRecord thirdBezierKnotRecord = new BezierKnotRecord();
        thirdBezierKnotRecord.setLinked(true);
        thirdBezierKnotRecord.setPoints(new Point[]{
                pointFToResourcePoint(point3, imageSize),
                pointFToResourcePoint(point3, imageSize),
                pointFToResourcePoint(point3, imageSize)
        });

        BezierKnotRecord[] bezierKnots = new BezierKnotRecord[]{
                firstBezierKnotRecord,
                secondBezierKnotRecord,
                thirdBezierKnotRecord
        };

        newShape.setItems(bezierKnots);

        return newShape;
    }

    static Point pointFToResourcePoint(PointF point, Size imageSize) {
        return new Point(
                Math.round(point.getY() * (IMG_TO_PSD_RATIO / imageSize.getHeight())),
                Math.round(point.getX() * (IMG_TO_PSD_RATIO / imageSize.getWidth())));
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

**PSDJAVA-613. Исправление конвертации файла Psd из RGB в CMYK**

{{< highlight java >}}

    public static void main(String[] args) {
        // Проверить, что psd-файл, конвертированный из RGB в CMYK + RLE 4 канала из psd-файла в RGB + RLE 4 канала,
        // действительно имеет 4 канала и HasTransparencyData == false.
        String sourceFile = "src/main/resources/frog_nosymb.psd";
        String outputFile = "src/main/resources/frog_nosymb_output.psd";

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
            psdImage.setTransparencyData(false);

            PsdOptions psdOptions = new PsdOptions(psdImage);
            psdOptions.setColorMode(ColorModes.Cmyk);
            psdOptions.setCompressionMethod(CompressionMethod.RLE);
            psdOptions.setChannelsCount((short) 4);

            psdImage.save(outputFile, psdOptions);
        }

        try (PsdImage psdImage = (PsdImage) Image.load(outputFile)) {
            assertAreEqual(false, psdImage.hasTransparencyData());
            assertAreEqual(4, psdImage.getLayers()[0].getChannelsCount());
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

**PSDJAVA-614. Конкретный файл PSD не может быть экспортирован с использованием Aspose.PSD**

{{< highlight java >}}

        String sourceFile = "src/main/resources/1966source.psd";
        String outputPng = "src/main/resources/output.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            psdImage.save(outputPng, new PngOptions());
        }

{{< /highlight >}}

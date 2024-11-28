---
title: מסמכי שחרור Aspose.PSD עבור גרסה 24.4 של Java
type: מסמכים
weight: 40
url: /he/java/aspose-psd-for-java-24-4-release-notes/
---

{{% alert color="primary" %}} עמוד זה מכיל את רשימות השחרור עבור [Aspose.PSD עבור Java 24.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.4/) {{% /alert %}}

| **מפתח**   | **סיכום**                                                                                                | **קטגוריה** |
|:------------|:------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-610 | הגדרת הרישיון עבור Aspose.PSD עבור Java מובילה לחריגה אם היא מבוצעת יותר מפעם אחת               | באג            |
| PSDJAVA-611 | [תבנית AI] הוספת טיפוס XObjectForm                                                         | תכונה      |
| PSDJAVA-612 | הוספת בנאי עבור שכבת הצורה                                                                      | תכונה      |
| PSDJAVA-613 | תיקון המרת קובץ Psd מ-RGB ל-CMYK                                                            | באג            |
| PSDJAVA-614 | קובץ מסוים בתבנית PSD לא ניתן לייצוא באמצעות Aspose.PSD                                                     | באג            |

## **שינויים ב- API הציבוריים**
# **APIs שהוספו:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addShapeLayer

# **APIs שנמחקו:**

- אף אחד

## **דוגמאות לשימוש:**

**PSDJAVA-610. הגדרת הרישיון עבור Aspose.PSD עבור Java מובילה לחריגה אם היא מבוצעת יותר מפעם אחת**

{{< highlight java >}}


        License license = new License();
        String liccorrectJava = "Aspose.PSD.Java.lic";

        license.setLicense(liccorrectJava);
        license.setLicense(liccorrectJava);

{{< /highlight >}}

**PSDJAVA-611. [תבנית AI] הוספת טיפוס XObjectForm**

{{< highlight java >}}

        String sourceFile = "src/main/resources/example.ai";
        String outputFilePath = "src/main/resources/example.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-612. הוספת בנאי עבור שכבת הצורה**

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

            assertAreEqual(1, shapeLayer.getPath().getItems().length); // 1 Shape
            assertAreEqual(3, shapeLayer.getPath().getItems()[0].getItems().length); // 3 knots in a shape

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
        assertAreEqual(expected, actual, "Objects are not equal.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-613. תיקון המרת קובץ psd מ-RGB ל-CMYK**

{{< highlight java >}}

    public static void main(String[] args) {
        // בדיקה שהקובץ psd שהומיר ל-CMYK + RLE 4 ערוצים מקובץ psd ב-RGB + RLE 4 ערוצים, באמת מכיל 4 ערוצים
        // ו-HasTransparencyData == false.
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
        assertAreEqual(expected, actual, "Objects are not equal.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-614. קובץ PSD מסוים לא ניתן לייצוא באמצעות Aspose.PSD**

{{< highlight java >}}

        String sourceFile = "src/main/resources/1966source.psd";
        String outputPng = "src/main/resources/output.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            psdImage.save(outputPng, new PngOptions());
        }

{{< /highlight >}}

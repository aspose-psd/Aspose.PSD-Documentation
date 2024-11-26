---
title: Aspose.PSD dla Javy 24.4 - Notatki wydania
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-java-24-4-notatki-wydania/
---

{{% alert color="primary" %}} Ta strona zawiera notatki wydania dla [Aspose.PSD dla Javy 24.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.4/) {{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                      | **Kategoria** |
|:------------|:------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-610 | Ustawienie Licencji dla Aspose.PSD dla Javy skutkuje wyjątkiem, jeśli jest wykonane więcej niż jeden raz| Błąd         |
| PSDJAVA-611 | [Format AI] Dodanie obsługi zasobów XObjectForm                                                       | Funkcja      |
| PSDJAVA-612 | Dodanie Konstruktora dla Warstwy Kształtu                                                             | Funkcja      |
| PSDJAVA-613 | Naprawa konwersji pliku Psd z RGB na CMYK                                                           | Błąd         |
| PSDJAVA-614 | Określony plik PSD nie może być eksportowany przy użyciu Aspose.PSD                                   | Błąd         |

## **Zmiany w API publicznym**
# **Dodane API:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addShapeLayer

# **Usunięte API:**

- Brak

## **Przykłady użycia:**

**PSDJAVA-610. Ustawienie Licencji dla Aspose.PSD dla Javy skutkuje wyjątkiem, jeśli jest wykonane więcej niż jeden raz**

{{< highlight java >}}

        License license = new License();
        String liccorrectJava = "Aspose.PSD.Java.lic";

        license.setLicense(liccorrectJava);
        license.setLicense(liccorrectJava);

{{< /highlight >}}

**PSDJAVA-611. [Format AI] Dodanie obsługi zasobów XObjectForm**

{{< highlight java >}}

        String sourceFile = "src/main/resources/example.ai";
        String outputFilePath = "src/main/resources/example.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-612. Dodanie Konstruktora dla Warstwy Kształtu**

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

            assertAreEqual(1, shapeLayer.getPath().getItems().length); // 1 Kształt
            assertAreEqual(3, shapeLayer.getPath().getItems()[0].getItems().length); // 3 węzły w kształcie

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
        assertAreEqual(expected, actual, "Obiekty nie są równe.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-613. Naprawa konwersji pliku Psd z RGB na CMYK**

{{< highlight java >}}

    public static void main(String[] args) {
        // Sprawdź, czy plik psd przekonwertowany do CMYK + RLE 4 kanałów z pliku psd z RGB + RLE 4 kanały, faktycznie posiada 4 kanały
        // oraz HasTransparencyData == false.
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
        assertAreEqual(expected, actual, "Obiekty nie są równe.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-614. Określony plik PSD nie może być eksportowany przy użyciu Aspose.PSD**

{{< highlight java >}}

        String sourceFile = "src/main/resources/1966source.psd";
        String outputPng = "src/main/resources/output.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            psdImage.save(outputPng, new PngOptions());
        }

{{< /highlight >}}

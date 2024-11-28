---
title: Aspose.PSD für Java 24.4 - Versionshinweise
type: docs
weight: 40
url: /de/java/aspose-psd-fur-java-24-4-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält die Versionshinweise für [Aspose.PSD für Java 24.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.4/) {{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                   | **Kategorie** |
|:------------|:------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-610 | Einstellung der Lizenz für Aspose.PSD für Java führt zu einer Ausnahme, wenn sie mehr als einmal erfolgt | Fehler        |
| PSDJAVA-611 | [AI-Format] Hinzufügen der XObjectForm-Ressourcenverarbeitung                                           | Funktion      |
| PSDJAVA-612 | Konstruktor für die ShapeLayer hinzufügen                                                               | Funktion      |
| PSDJAVA-613 | Beheben der Konvertierung einer Psd-Datei von RGB nach CMYK                                             | Fehler        |
| PSDJAVA-614 | Bestimmte PSD-Datei kann nicht mit Aspose.PSD exportiert werden                                          | Fehler        |

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addShapeLayer

# **Entfernte APIs:**

- Keine

## **Beispiele für die Verwendung:**

**PSDJAVA-610. Einstellen der Lizenz für Aspose.PSD für Java führt zu einer Ausnahme, wenn sie mehr als einmal erfolgt**

{{< highlight java >}}

        Lizenz lizenz = new License();
        String lizenzKorrektJava = "Aspose.PSD.Java.lic";

        lizenz.setLicense(liccorrectJava);
        lizenz.setLicense(liccorrectJava);

{{< /highlight >}}

**PSDJAVA-611. [AI-Format] Hinzufügen der XObjectForm-Ressourcenverarbeitung**

{{< highlight java >}}

        String quelleDatei = "src/main/resources/beispiel.ai";
        String ausgabedateiPfad = "src/main/resources/beispiel.png";

        try (AiImage bild = (AiImage) Image.load(sourceFile)) {
            bild.save(ausgabedateiPfad, new PngOptions());
        }

{{< /highlight >}}

**PSDJAVA-612. Konstruktor für die ShapeLayer hinzufügen**

{{< highlight java >}}

    private static final int IMG_TO_PSD_RATIO = 256 * 65535;

    public static void main(String[] args) {
        String ausgabedatei = "src/main/resources/AddShapeLayer_output.psd";

        try (PsdImage neuePsd = new PsdImage(600, 400)) {
            ShapeLayer layer = newPsd.addShapeLayer();

            PathShape neueForm = generateNewShape(newPsd.getSize());
            List<IPathShape> neueFormen = new List<>();
            neueFormen.add(neueForm);
            layer.getPath().setItems(neueFormen.toArray(new IPathShape[0]));

            layer.update();

            newPsd.save(outputFile);
        }

        try (PsdImage bild = (PsdImage) Image.load(outputFile)) {
            assertAreEqual(2, bild.getLayer().length);

            ShapeLayer shapeLayer = (ShapeLayer) bild.getLayers()[1];
            ColorFillSettings interneFüllung = (ColorFillSettings) shapeLayer.getFill();
            IStrokeSettings strichEinstellungen = shapeLayer.getStroke();
            ColorFillSettings strichFüllung = (ColorFillSettings) strokeSettings.getFill();

            assertAreEqual(1, shapeLayer.getPath().getItems().length); // 1 Form
            assertAreEqual(3, shapeLayer.getPath().getItems()[0].getItems().length); // 3 Knoten in einer Form

            assertAreEqual(-16127182, interneFüllung.getColor().toArgb()); // ff09eb32

            assertAreEqual(7.41, strichEinstellungen.getSize());
            assertAreEqual(false, strichEinstellungen.getEnabled());
            assertAreEqual(StrokePosition.Center, strichEinstellungen.getLineAlignment());
            assertAreEqual(LineCapType.ButtCap, strokeSettings.getLineCap());
            assertAreEqual(LineJoinType.MiterJoin, strichEinstellungen.getLineJoin());
            assertAreEqual(-16777216, strichFüllung.getColor().toArgb()); // ff000000
        }
    }

    static PathShape generateNewShape(Size bildGröße) {
        PathShape neueForm = new PathShape();

        PointF punkt1 = new PointF(20, 100);
        PointF punkt2 = new PointF(200, 100);
        PointF punkt3 = new PointF(300, 10);

        BezierKnotRecord ersterBezierKnoten = new BezierKnotRecord();
        ersterBezierKnoten.setLinked(true);
        ersterBezierKnoten.setPoints(new Point[]{
                punktFZuRessourcePunkt(punkt1, bildGröße),
                punktFZuRessourcePunkt(punkt2, bildGröße),
                punktFZuRessourcePunkt(punkt3, bildGröße)
        });

        BezierKnotRecord zweiterBezierKnoten = new BezierKnotRecord();
        zweiterBezierKnoten.setLinked(true);
        zweiterBezierKnoten.setPoints(new Point[]{
                punktFZuRessourcePunkt(punkt2, bildGröße),
                punktFZuRessourcePunkt(punkt2, bildGröße),
                punktFZuRessourcePunkt(punkt2, bildGröße)
        });

        BezierKnotRecord dritterBezierKnoten = new BezierKnotRecord();
        dritterBezierKnoten.setLinked(true);
        dritterBezierKnoten.setPoints(new Point[]{
                punktFZuRessourcePunkt(punkt3, bildGröße),
                punktFZuRessourcePunkt(punkt3, bildGröße),
                punktFZuRessourcePunkt(punkt3, bildGröße)
        });

        BezierKnotRecord[] bezierKnoten = new BezierKnotRecord[]{
                ersterBezierKnoten,
                zweiterBezierKnoten,
                dritterBezierKnoten
        };

        neueForm.setItems(bezierKnoten);

        return neueForm;
    }

    static Point punktFZuRessourcePunkt(PointF punkt, Size bildGröße) {
        return new Point(
                Math.round(punkt.getY() * (IMG_TO_PSD_RATIO / bildGröße.getHeight())),
                Math.round(punkt.getX() * (IMG_TO_PSD_RATIO / bildGröße.getWidth())));
    }

    static void assertAreEqual(Object erwartet, Object tatsächlich) {
        assertAreEqual(erwartet, tatsächlich, "Objekte sind nicht gleich.");
    }

    static void assertAreEqual(Object erwartet, Object tatsächlich, String nachricht) {
        if (!erwartet.equals(tatsächlich)) {
            throw new IllegalArgumentException(nachricht);
        }
    }

{{< /highlight >}}

**PSDJAVA-613. Beheben der Konvertierung einer PSD-Datei von RGB nach CMYK**

{{< highlight java >}}

    public static void main(String[] args) {
        // Überprüfen, dass die PSD-Datei, die von RGB nach CMYK + RLE 4 Kanäle konvertiert wurde, tatsächlich 4 Kanäle hat
        // und HasTransparencyData == false.
        String quelleDatei = "src/main/resources/frog_nosymb.psd";
        String ausgabedatei = "src/main/resources/frog_nosymb_output.psd";

        try (PsdImage psdBild = (PsdImage) Image.load(sourceFile)) {
            psdBild.setTransparencyData(false);

            PsdOptions psdOptionen = new PsdOptions(psdBild);
            psdOptionen.setColorMode(ColorModes.Cmyk);
            psdOptionen.setCompressionMethod(CompressionMethod.RLE);
            psdOptionen.setChannelsCount((short) 4);

            psdBild.save(outputFile, psdOptionen);
        }

        try (PsdImage psdBild = (PsdImage) Image.load(outputFile)) {
            assertAreEqual(false, psdBild.hasTransparencyData());
            assertAreEqual(4, psdBild.getLayers()[0].getChannelsCount());
        }
    }

    static void assertAreEqual(Object erwartet, Object tatsächlich) {
        assertAreEqual(erwartet, tatsächlich, "Objekte sind nicht gleich.");
    }

    static void assertAreEqual(Object erwartet, Object tatsächlich, String nachricht) {
        if (!erwartet.equals(tatsächlich)) {
            throw new IllegalArgumentException(nachricht);
        }
    }

{{< /highlight >}}

**PSDJAVA-614. Bestimmte PSD-Datei kann nicht mit Aspose.PSD exportiert werden**

{{< highlight java >}}

        String quelleDatei = "src/main/resources/1966source.psd";
        String ausgabePng = "src/main/resources/ausgabe.png";

        PsdLoadOptions psdLadeOptionen = new PsdLoadOptions();
        psdLadeOptionen.setLoadEffectsResource(true);

        try (PsdImage psdBild = (PsdImage) Image.load(sourceFile, psdLadeOptionen)) {
            psdBild.save(outputPng, new PngOptions());
        }

{{< /highlight >}}

---
title: Versienotities van Aspose.PSD voor Java 24.5
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-24-5-versienotities/
---

{{% alert color="primary" %}} Deze pagina bevat versienotities voor [Aspose.PSD voor Java 24.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-voor-java-24.5/) {{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                                                        | **Categorie**  |
|:------------|:------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-617 | [AI-indeling] Ondersteuning toegevoegd voor het verwerken van AI-bestanden met EPSF-koptekst                     | Functie       |
| PSDJAVA-620 | Halftransparantie wordt verkeerd verwerkt in de psd-bestandsvoorbeeld                                                | Fout          |
| PSDJAVA-621 | Renderng van vormlaag gedeeltelijk incorrect                                                                           | Fout          |
| PSDJAVA-622 | Uitzondering bij het opslaan van PSD-bestanden met een formaat groter dan 200 MB en grote dimensies (Er is een probleem met geheugengebruik) | Fout          |
| PSDJAVA-623 | Fout bij het opslaan van afbeelding bij opslaan naar PDF na update van 23.7 naar 24.3                               | Fout          |
| PSDJAVA-624 | Los het probleem op in de GetFontInfoRecords-methode voor de Chinese lettertypen                                     | Fout          |

## **Wijzigingen in openbare API**

# **Toegevoegde API's:**

- M:com.aspose.psd.fileformats.ai.AiLayerSection.getColorIndex
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setColorIndex(int)
- M:com.aspose.psd.fileformats.ai.AiLayerSection.hasMultiLayerMasks
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setMultiLayerMasks(boolean)
- M:com.aspose.psd.imageoptions.PsdOptions.getBackgroundContents
- M:com.aspose.psd.imageoptions.PsdOptions.setBackgroundContents(com.aspose.psd.fileformats.psd.rawcolor.RawColor)

# **Verwijderde API's:**

- Geen

## **Gebruik voorbeelden:**

**PSDJAVA-617. [AI-indeling] Ondersteuning toegevoegd voor het verwerken van AI-bestanden met EPSF-koptekst**

{{< highlight java >}}

    public static void main(String[] args) {
        String bronbestand = "src/main/resources/example.ai";
        String uitvoerbestand = "src/main/resources/voorbeeld.png";

        try (AiImage afbeelding = (AiImage) Image.load(bronbestand)) {
            assertAreEqual(afbeelding.getLayers().length, 2);
            assertAreEqual(afbeelding.getLayers()[0].hasMultiLayerMasks(), false);
            assertAreEqual(afbeelding.getLayers()[0].getColorIndex(), -1);
            assertAreEqual(afbeelding.getLayers()[1].hasMultiLayerMasks(), false);
            assertAreEqual(afbeelding.getLayers()[1].getColorIndex(), -1);

            afbeelding.save(uitvoerbestand, new PngOptions());
        }
    }

    static void assertAreEqual(Object verwacht, Object werkelijk) {
        assertAreEqual(verwacht, werkelijk, "Objecten zijn niet gelijk.");
    }

    static void assertAreEqual(Object verwacht, Object werkelijk, String boodschap) {
        if (!verwacht.equals(werkelijk)) {
            throw new IllegalArgumentException(boodschap);
        }
    }

{{< /highlight >}}

**PSDJAVA-620. Halftransparantie wordt verkeerd verwerkt in het psd-bestandsvoorbeeld**

{{< highlight java >}}

        String bronbestand = "src/main/resources/frog_nosymb.psd";
        String uitvoerbestand = "src/main/resources/frog_nosymb_backgroundcontents_output.psd";

        try (PsdImage psdAfbeelding = (PsdImage) Image.load(bronbestand)) {
            RawColor achtergrondkleur = new RawColor(PixelDataFormat.getRgb32Bpp());
            int argbWaarde = 255 << 24 | 255 << 16 | 255 << 8 | 255;
            achtergrondkleur.setAsInt(argbWaarde); // Wit

            PsdOptions psdOpties = new PsdOptions(psdAfbeelding);
            psdOpties.setColorMode(ColorModes.Rgb);
            psdOpties.setCompressionMethod(CompressionMethod.RLE);
            psdOpties.setChannelsCount((short) 4);
            psdOpties.setBackgroundContents(achtergrondkleur);

            psdAfbeelding.save(uitvoerbestand, psdOpties);
        }

{{< /highlight >}}

**PSDJAVA-621. Renderng van vormlaag gedeeltelijk incorrect**

{{< highlight java >}}

    private static final int ImgToPsdRatio = 256 * 65535;

    public static void main(String[] args) {
        String bronbestand = "src/main/resources/ShapeLayerTest.psd";
        String uitvoerbestand = "src/main/resources/ShapeLayerTest_output.psd";
        
        try (PsdImage im = (PsdImage) Image.load(bronbestand)) {
            ShapeLayer vormlaag = (ShapeLayer) im.getLayers()[2];
            IPath-pad = vormlaag.getPath();
            IPathShape[] padVormen = pad.getItems();
            List<BezierKnotRecord> knopenLijst = new ArrayList<>();
            for (IPathShape padVorm : padVormen) {
                BezierKnotRecord[] knopen = padVorm.getItems();
                Collections.addAll(knopenLijst, knopen);
            }

            // Verander laageigenschappen
            PathShape nieuweVorm = new PathShape();

            BezierKnotRecord eersteBezierKnoopRecord = new BezierKnotRecord();
            eersteBezierKnoopRecord.setLinked(true);
            eersteBezierKnoopRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            vormlaag.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            vormlaag.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            vormlaag.getContainer().getSize())});

            BezierKnotRecord tweedeBezierKnoopRecord = new BezierKnotRecord();
            tweedeBezierKnoopRecord.setLinked(true);
            tweedeBezierKnoopRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(50, 490),
                            vormlaag.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 490),
                            vormlaag.getContainer().getSize()), // Ankerpunt
                    pointFToResourcePoint(
                            new PointF(150, 490),
                            vormlaag.getContainer().getSize())
            });

            BezierKnoopRecord derdeBezierKnoopRecord = new BezierKnoopRecord();
            derdeBezierKnoopRecord.setLinked(true);
            derdeBezierKnoopRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(490, 150),
                            vormlaag.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 50),
                            vormlaag.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 20),
                            vormlaag.getContainer().getSize()),
            });

            BezierKnosisRecord[] bezierKnopen = new BezierKnoopRecord[]
                    {eersteBezierKnoopRecord, tweedeBezierKnoopRecord, derdeBezierKnoopRecord};

            nieuweVorm.setItems(bezierKnopen);

            Lijst<IPathShape> nieuweVormen = nieuweLijst<>(Arrays.asList(padVormen));
            nieuweVormen.add(newShape);

            IPathShape[] padVormNieuw = nieuweVormen.toArray(new IPathShape[0]);
            pad.setItems(padVormNieuw);

            vormlaag.update();

            im.save(uitvoerbestand, nieuwe PsdOpties());
        }

        try (PsdImage im = (PsdImage) Image.load(uitvoerbestand)) {
            ShapeLayer vormlaag = (ShapeLayer) im.getLayers()[2];
            IPath pad = vormlaag.getPath();
            IPathShape[] padVormen = pad.getItems();
            List<BezierKnoweRecord> knopenLijst = new ArrayList<>();
            for (IPathShape padVorm : padVormen) {
                BezierKnoopRecord[] knopen = padVorm.getItems();
                knopenLijst.addAll(Arrays.asList(knopen));
            }

            assertAreEqual(3, padVormen.length);
            assertAreEqual(42, vormlaag.getLeft());
            assertAreEqual(14, vormlaag.getTop());
            assertAreEqual(1600, vormlaag.getBounds().getWidth());
            assertAreEqual(1086, vormlaag.getBounds().getHeight());
        }
    }

    static Point pointFToResourcePoint(PointF punt, Formaat afbeeldingsgrootte) {
        return new Point(
                (int) Math.round(punt.getY() * (ImgToPsdRatio / afbeeldingsgrootte.getHeight())),
                (int) Math.round(punt.getX() * (ImgToPsdRatio / afbeeldingsgrootte.getWidth())));
    }

    static void assertAreEqual(Object verwacht, Object werkelijk) {
        assertAreEqual(verwacht, werkelijk, "Objecten zijn niet gelijk.");
    }

    static void assertAreEqual(Object verwacht, Object werkelijk, String boodschap) {
        if (!verwacht.equals(werkelijk)) {
            throw new IllegalArgumentException(boodschap);
        }
    }

{{< /highlight >}}

**PSDJAVA-622. Uitzondering bij het opslaan van PSD-bestanden met een formaat groter dan 200 MB en grote dimensies(Er is een probleem met geheugengebruik)**

{{< highlight java >}}

    String bronbestand = "src/main/resources/grootbestand.psd";
    String uitvoerbestand = "src/main/resources/output_raw.psd";

    PsdLoadOptions laadOpties = new PsdLoadOptions();
    laadOpties.setLoadEffectsResource(true);
    laadOpties.setUseDiskForLoadEffectsResource(true);

    try (PsdImage psdAfbeelding = (PsdImage) Image.load(bronbestand, laadOpties)) {
        PsdOpties psdOpties = new PsdOptions();
        psdOpties.setCompressionMethod(CompressionMethod.RLE);

        // Hier mag geen fout zijn
        psdAfbeelding.save(uitvoerbestand, psdOpties);
    }

{{< /highlight >}}

**PSDJAVA-623. Fout bij het opslaan van afbeelding bij opslaan naar PDF na update van 23.7 naar 24.3**

{{< highlight java >}}

    String bronbestand = "src/main/resources/CVFlor.psd";
    String uitvoerbestand = "src/main/resources/_export.pdf";

    try (PsdImage psdAfbeelding = (PsdImage) Image.load(bronbestand)) {
        PdfOpties opslaanOpties = new PdfOptions();
        opslaanOpties.setPdfCoreOptions(new PdfCoreOptions());

        psdAfbeelding.save(uitvoerbestand, opslaanOpties);
    }

{{< /highlight >}}

**PSDJAVA-624. Los het probleem op in de GetFontInfoRecords-methode voor de Chinese lettertypen**

{{< highlight java >}}

    String lettertypenMap = "src/main/resources/Font";
    String bronbestand = "src/main/resources/bd-worlds-best-pink.psd";

    PsdLoadOptions psdLaadOpties = new PsdLoadOptions();
    psdLaadOpties.setLoadEffectsResource(true);
    psdLaadOpties.setAllowWarpRepaint(true);

    try {
        FontInstellingen.setFontsFolders(new String[]{fontsFolder}, true);

        try (PsdImage afbeelding = (PsdImage) PsdImage.load(bronbestand, psdLaadOpties)) {
            for (Laag laag : image.getLayers()) {
                if (laag instanceof TextLayer) {
                    TextLaag tekstLaag = (TextLayer) laag;

                    if ("best".equals(tekstLaag.getText())) {
                        // Zonder dit probleem te verhelpen, zou hier een uitzondering optreden vanwege het Chinese lettertype.
                        tekstLaag.updateText("SUCCES");
                    }
                }
            }
        }
    } finally {
        FontInstellingen.herstellen();
    }

{{< /highlight >}}
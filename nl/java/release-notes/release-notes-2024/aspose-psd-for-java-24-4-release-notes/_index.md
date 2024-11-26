---
title: Aspose.PSD voor Java 24.4 - Release-opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-24-4-release-opmerkingen/
---

{{% alert color = "primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 24.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.4/) {{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                                    | **Categorie** |
|:------------|:------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-610 | Het instellen van de licentie voor Aspose.PSD voor Java leidt tot een uitzondering als het meer dan één keer wordt gemaakt          | Fout          |
| PSDJAVA-611 | [AI-indeling] XObjectForm-bronverwerking toevoegen                                                      | Functie       |
| PSDJAVA-612 | Constructor toevoegen voor de ShapeLayer                                                               | Functie       |
| PSDJAVA-613 | Conversie van PSD-bestand van RGB naar CMYK repareren                                                  | Fout          |
| PSDJAVA-614 | Specifiek PSD-bestand kan niet worden geëxporteerd met behulp van Aspose.PSD                           | Fout          |

## **Openbare API-wijzigingen**
# **Toegevoegde API's:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addShapeLayer

# **Verwijderde API's:**

- Geen

## **Gebruik voorbeelden:**

**PSDJAVA-610. Het instellen van de licentie voor Aspose.PSD voor Java leidt tot een uitzondering als het meer dan één keer wordt gemaakt**

{{< highlight java >}}

        License licentie = nieuwe Licentie();
        String liccorrectJava = "Aspose.PSD.Java.lic";

        licentie.setLicentie(liccorrectJava);
        licentie.setLicentie(liccorrectJava);

{{< /highlight >}}

**PSDJAVA-611. [AI-indeling] XObjectForm-bronverwerking toevoegen**

{{< highlight java >}}

        String bronBestand = "src/main/resources/voorbeeld.ai";
        String uitvoerBestandPad = "src/main/resources/voorbeeld.png";

        probeer(AiImage afbeelding = (AiImage) Afbeelding.laden(bronBestand)) {
            afbeelding.opslaan(uitvoerBestandPad, nieuwe PngOpties());
        }

{{< /highlight >}}

**PSDJAVA-612. Constructor toevoegen voor de ShapeLayer**

{{< highlight java >}}

    private static final int IMG_TOT_PSD_RATIO = 256 * 65535;

    openbare statische leegte main(String[] args) {
        String uitvoerBestand = "src/main/resources/ToevoegenShapeLayer_uitvoer.psd";

        probeer(PsdImage nieuwPsd = nieuwe PsdImage(600, 400)) {
            ShapeLayer-laag = nieuwPsd.addShapeLayer();

            PathShape-nieuweVorm = genereerNieuweVorm(nieuwPsd.getGrootte());
            Lijst<IPathShape> nieuweVormen = nieuwe Lijst<>();
            nieuweVormen.toevoegen(nieuweVorm);
            laag.getPath().setItems(nieuweVormen.toArray(new IPathShape[0]));

            laag.update();

            nieuwPsd.save(uitvoerBestand);
        }

        probeer(PsdImage afbeelding = (PsdImage) Afbeelding.laden(uitvoerBestand)) {
            assertAreEqual(2, afbeelding.getLagen().length);

            ShapeLayer vormLaag = (ShapeLayer) afbeelding.getLagen()[1];
            InternalFill internalFill = (InternalFill) vormLaag.getVulling();
            IStrokeSettings lijnInstellingen = vormLaag.getLijn();
            InternalFill lijnVulling = (InternalFill) lijnInstellingen.getVulling();

            assertAreEqual(1, vormLaag.getPath().getItems().length); // 1 Vorm
            assertAreEqual(3, vormLaag.getPath().getItems()[0].getItems().length); // 3 knopen in een vorm

            assertAreEqual(-16127182, internalFill.getColor().toArgb()); // ff09eb32

            assertAreEqual(7.41, lijnInstellingen.getGrootte());
            assertAreEqual(false, lijnInstellingen.isEnabled());
            assertAreEqual(StrokePosition.Center, lijnInstellingen.getLineAlignment());
            assertAreEqual(LineCapType.ButtCap, lijnInstellingen.getLineCap());
            assertAreEqual(LineJoinType.MiterJoin, lijnInstellingen.getLineJoin());
            assertAreEqual(-16777216, lijnVulling.getColor().toArgb()); // ff000000
        }
    }

    statische PathShape genereerNieuweVorm(Grootte afbeeldingsGrootte) {
        PathShape nieuweVorm = nieuwe PathShape();

        PointF punt1 = nieuwe PointF(20, 100);
        PointF punt2 = nieuwe PointF(200, 100);
        PointF punt3 = nieuwe PointF(300, 10);

        BezierKnotRecord eersteBezierKnotRecord = nieuwe BezierKnotRecord();
        eersteBezierKnotRecord.setGekoppeld(true);
        eersteBezierKnotRecord.setPoints(new Point[]{
                pointFToResourcePoint(punt1, afbeeldingsGrootte),
                pointFToResourcePoint(punt1, afbeeldingsGrootte),
                pointFToResourcePoint(punt1, afbeeldingsGrootte)
        });

        BezierKnotRecord tweedeBezierKnotRecord = nieuwe BezierKnotRecord();
        tweedeBezierKnotRecord.setGekoppeld(true);
        tweedeBezierKnotRecord.setPoints(new Point[]{
                pointFToResourcePoint(punt2, afbeeldingsGrootte),
                pointFToResourcePoint(punt2, afbeeldingsGrootte),
                pointFToResourcePoint(punt2, afbeeldingsGrootte)
        });

        BezierKnotRecord derdeBezierKnotRecord = nieuwe BezierKnotRecord();
        derdeBezierKnotRecord.setGekoppeld(true);
        derdeBezierKnotRecord.setPoints(new Point[]{
                pointFToResourcePoint(punt3, afbeeldingsGrootte),
                pointFToResourcePoint(punt3, afbeeldingsGrootte),
                pointFToResourcePoint(punt3, afbeeldingsGrootte)
        });

        BezierKnotRecord[] bezierKnotsen = nieuwe BezierKnotRecord[]{
                eersteBezierKnotRecord,
                tweedeBezierKnotRecord,
                derdeBezierKnotRecord
        };

        nieuweVorm.setItems(bezierKnotsen);

        terug nieuweVorm;
    }

    statische Punt pointFToResourcePoint(PointF punt, Grootte afbeeldingsGrootte) {
        terug nieuwe Punt(
                Math.round(punt.getY() * (IMG_TOT_PSD_RATIO / afbeeldingsGrootte.getHoogte())),
                Math.round(punt.getX() * (IMG_TOT_PSD_RATIO / afbeeldingsGrootte.getBreedte())));
    }

    statische leegte assertZijnGelijk(Object verwacht, Object werkelijk) {
        assertZijnGelijk(verwacht, werkelijk, "Objecten zijn niet gelijk.");
    }

    statische leegte assertZijnGelijk(Object verwacht, Object werkelijk, String bericht) {
        als (!verwacht.equals(werkelijk)) {
            gooi nieuwe IllegalArgumentException(bericht);
        }
    }

{{< /highlight >}}

**PSDJAVA-613. Conversie van Psd-bestand van RGB naar CMYK repareren**

{{< highlight java >}}

    public static void main(String[] args) {
        // Controleer dat psd-bestand omgezet naar CMYK + RLE 4 kanalen van psd-bestand in RGB + RLE 4 kanalen, echt 4 kanalen heeft
        // en HasTransparencyData == false.
        String bronBestand = "src/main/resources/kikker_nosymb.psd";
        String uitvoerBestand = "src/main/resources/kikker_nosymb_output.psd";

        probeer(PsdImage psdAfbeelding = (PsdImage) Afbeelding.laden(bronBestand)) {
            psdAfbeelding.setTransparantieData(false);

            PsdOpties psdOpties = nieuwe PsdOpties(psdAfbeelding);
            psdOpties.setColorMode(ColorModes.Cmyk);
            psdOpties.setCompressieMethode(CompressieMethode.RLE);
            psdOpties.setAantalKanalen((korte) 4);

            psdAfbeelding.save(uitvoerBestand, psdOpties);
        }

        probeer(PsdImage psdAfbeelding = (PsdAfbeelding) Afbeelding.laden(uitvoerBestand)) {
            assertZijnGelijk(false, psdAfbeelding.hasTransparencyData());
            assertZijnGelijk(4, psdAfbeelding.getLagen()[0].getAantalKanalen());
        }
    }

    statische leegte assertZijnGelijk(Object verwacht, Object werkelijk) {
        assertZijnGelijk(verwacht, werkelijk, "Objecten zijn niet gelijk.");
    }

    statische leegte assertZijnGelijk(Object verwacht, Object werkelijk, String bericht) {
        als (!verwacht.equals(werkelijk)) {
            gooi nieuwe IllegalArgumentException(bericht);
        }
    }

{{< /highlight >}}

**PSDJAVA-614. Specifiek PSD-bestand kan niet worden geëxporteerd met behulp van Aspose.PSD**

{{< highlight java >}}

        String bronBestand = "src/main/resources/1966bron.psd";
        String uitvoerPng = "src/main/resources/uitvoer.png";

        PsdLaadOpties psdLaadOpties = nieuwe PsdLaadOpties();
        psdLaadOpties.setLaadEffectenBron(true);

        probeer(PsdImage psdAfbeelding = (PsdImage) Afbeelding.laden(bronBestand, psdLaadOpties)) {
            psdAfbeelding.save(uitvoerPng, nieuwe PngOpties());
        }

{{< /highlight >}}

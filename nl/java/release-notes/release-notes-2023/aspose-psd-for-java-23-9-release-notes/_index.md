---
title: Aspose.PSD voor Java 23.9 - Publicatie Opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-23-9-publicatie-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat publicatie-opmerkingen voor [Aspose.PSD voor Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                                                                                                    | **Categorie** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Implementatie van het maken van masker voor nieuwe aanpassingslagen                                                                                                   |    Functie   |
| PSDJAVA-528 | Toevoegen van ondersteuning voor samengevoegde lagen als Groep mengoptie                                                                                               |    Functie   |
| PSDJAVA-529 | PSD-bestand met 16-bits kleurenmodus past geen masker toe op aanpassingslagen                                                                                          |      Fout    |
| PSDJAVA-530 | Onjuiste weergave van haakjes in de tekstlaag                                                                                                                         |      Fout    |
| PSDJAVA-531 | Kan geen stijlen bijwerken in de tekstlagen                                                                                                                           |      Fout    |
| PSDJAVA-532 | Na exporteren van PSD-bestand met CMYK breken de kleuren in geëxporteerde PSD                                                                                            |      Fout    |
| PSDJAVA-533 | Specifiek PSB-bestand geeft uitzondering "Het rechthoek heeft geen gemeenschappelijk verwerkingsgebied"                                                              |      Fout    |
| PSDJAVA-534 | Laden van afbeelding mislukt. OverflowException: Rekenkundige bewerking resulteerde in een overloop.                                                             |      Fout    |

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **Verwijderde API's:**

- Geen

## **Gebruik voorbeelden:**

**PSDJAVA-527. Implementatie van het maken van masker voor nieuwe aanpassingslagen**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objecten zijn niet gelijk.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-528. Toevoegen van ondersteuning voor samengevoegde lagen als Groep mengoptie**

{{< highlight java >}}
    String bronBestand = "src/main/resources/voorbeeld_bron.psd";
    String uitvoerPsd = "src/main/resources/voorbeeld_uitvoer.psd";
    String uitvoerPng = "src/main/resources/voorbeeld_uitvoer.png";

    try (PsdImage afbeelding = (PsdImage)Image.load(bronBestand)) {
        afbeelding.getLayers()[1].setBlendClippedElements(false);
        afbeelding.save(uitvoerPsd);
        afbeelding.save(uitvoerPng, new PngOptions());
    }
{{< /highlight >}}


**PSDJAVA-529. PSD-bestand met 16-bits kleurenmodus past geen masker toe op aanpassingslagen**

{{< highlight java >}}
	String bronBestand = "src/main/resources/bron.psd";
    String uitvoerPng = "src/main/resources/huidig.png";

    try (PsdImage afbeelding = (PsdImage) Image.load(bronBestand)) {
        afbeelding.save(uitvoerPng, new PngOptions());
    }
{{< /highlight >}}


**PSDJAVA-530. Onjuiste weergave van haakjes in de tekstlaag**

{{< highlight java >}}
    String bestand = "src/main/resources/bestand1.psd";
    String uitvoer = "src/main/resources/uitvoer_1235.png";

    try (PsdImage psdAfbeelding = (PsdImage) Image.load(bestand)) {
        for (Layer laag : psdAfbeelding.getLayers()) {
            if (laag instanceof TextLayer) {
                TextLayer tekstLaag = (TextLayer) laag;
                tekstLaag.getTextData().updateLayerData();

                PsdOptions afbeeldingsopties = new PsdOptions(psdAfbeelding);
                psdAfbeelding.save(uitvoer, afbeeldingsopties);
            }
        }
    }
{{< /highlight >}}


**PSDJAVA-531. Kan geen stijlen bijwerken in de tekstlagen**

{{< highlight java >}}
    String bronBestand = "src/main/resources/Voorbeeld_Lettergrootte.psd";
    String uitvoerBestand = "src/main/resources/uitvoer_Voorbeeld_Lettergrootte.psd";

    PsdLoadOptions psdLaadopties = new PsdLoadOptions();
    psdLaadopties.setLoadEffectsResource(true);

    try (PsdImage psdAfbeelding = (PsdImage) Image.load(bronBestand, psdLaadopties)) {
        TextLayer l1 = (TextLayer) psdAfbeelding.getLayers()[4];
        TextLayer l2 = (TextLayer) psdAfbeelding.getLayers()[5];

        ITextPortion[] tekstItems1 = l1.getTextData().producePortions(new String[]{"tekst1", "tekst2"},
                l1.getTextData().getItems()[0].getStyle(), l1.getTextData().getItems()[0].getParagraph());

        l1.getTextData().removePortion(0);
        for (ITextPortion item : tekstItems1) {
            l1.getTextData().addPortion(item);
        }

        ITextPortion[] tekstItems2 = l2.getTextData().producePortions(new String[]{"tekstlaag 1", "tekstlaag 22"},
                l2.getTextData().getItems()[0].getStyle(), l2.getTextData().getItems()[0].getParagraph());

        for (ITextPortion item : tekstItems2) {
            l2.getTextData().addPortion(item);
        }

        l1.getTextData().updateLayerData();
        l2.getTextData().updateLayerData();

        psdAfbeelding.save(uitvoerBestand);
    }
{{< /highlight >}}


**PSDJAVA-532. Na exporteren van PSD-bestand met CMYK breken de kleuren in geëxporteerde PSD**

{{< highlight java >}}
    String bronBestand = "src/main/resources/canyon.psd";
    String uitvoerBestandPng = "src/main/resources/uitvoer_canyon.png";

    MemoryStream outputstroom = new MemoryStream();

    try (PsdImage psdAfbeelding = (PsdImage) Image.load(bronBestand)) {
        psdAfbeelding.save(outputstroom.toOutputStream());
    }

    outputstroom.setPosition(0);
    try (PsdImage psdAfbeelding = (PsdImage) Image.load(outputstroom.toInputStream())) {
        psdAfbeelding.save(uitvoerBestandPng, new PngOptions());
    }

    outputstroom.close();
{{< /highlight >}}


**PSDJAVA-533. Specifiek PSB-bestand geeft uitzondering "Het rechthoek heeft geen gemeenschappelijk verwerkingsgebied"**

{{< highlight java >}}
    String invoer = "src/main/resources/1619_src.psb";
    String uitvoer = "src/main/resources/1619_uitvoer.png";

    PsdLoadOptions psdLaadopties = new PsdLoadOptions();
    psdLaadopties.setLoadEffectsResource(true);
    try (PsdImage afb = (PsdImage) Image.load(invoer, psdLaadopties)) {
        PngOptions pngOpties = new PngOptions();
        pngOpties.setCompressionLevel(9);
        pngOpties.setColorType(PngColorType.TruecolorWithAlpha);
        afb.save(uitvoer, pngOpties);
    }
{{< /highlight >}}


**PSDJAVA-534. Laden van afbeelding mislukt. OverflowException: Rekenkundige bewerking resulteerde in een overloop.**

{{< highlight java >}}
public static void main(String[] args) {
    String bronBestand = "src/main/resources/9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

    try (PsdImage afbeelding = (PsdImage)PsdImage.load(bronBestand))
    {
        Layer laag = afbeelding.getLayers()[28];
        GrdmResource grdmResource = (GrdmResource)laag.getResources()[0];

        assertAreEqual("自定", grdmResource.getGradientName());
    }

}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objecten zijn niet gelijk.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

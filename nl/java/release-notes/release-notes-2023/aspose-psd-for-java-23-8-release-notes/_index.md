---
title: Aspose.PSD voor Java 23.8 - Notities bij uitgave
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-23-8-release-notes/
---

{{% alert color="primary" %}} Deze pagina bevat notities bij de uitgave van [Aspose.PSD voor Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) {{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                                                                                | **Categorie** |
|:------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Toevoegen van nieuw type warp (Vlag)                                                                                                           | Functie      |
| PSDJAVA-519 | Toevoegen van nieuwe types warp: boog omhoog, boog omlaag, bol                                                                                 | Functie      |
| PSDJAVA-520 | Implementeren van nieuwe methode PsdImage.AddPosterizeAdjustmentLayer voor het toevoegen van een nieuwe Posterize-laag                        | Functie      |
| PSDJAVA-521 | PSD-informatie gaat verloren bij alleen openen en opslaan                                                                                      | Fout        |
| PSDJAVA-522 | Laden van afbeelding mislukt                                                                                                                   | Fout        |
| PSDJAVA-523 | Laden van afbeelding mislukt: Kan object van het type UnknownStructure niet converteren naar het type DescriptorStructure                    | Fout        |
| PSDJAVA-524 | Bestand gewijzigd in de externe bibliotheek beschadigt PSD-bestand, maar kan geopend worden in Photoshop                                    | Fout        |

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **Verwijderde API's:**

- Geen

## **Gebruik voorbeelden:**

**PSDJAVA-518. Toevoegen van nieuw type warp (Vlag)**

{{< highlight java >}}
    String bronbestand = "src/main/resources/flag_warp.psd";
    String uitvoerBestand = "src/main/resources/flag_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(bronbestand, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(uitvoerBestand, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-519. Toevoegen van nieuwe types warp: boog omhoog, boog omlaag, bol**

{{< highlight java >}}
    String bronbestandBoogBoven = "src/main/resources/arc_upper_warp.psd";
    String bronbestandBoogOnder = "src/main/resources/arc_lower_warp.psd";
    String bronbestandBol = "src/main/resources/bulge_warp.psd";

    String uitvoerBestandBoogBoven = "src/main/resources/ArcUpper_export.png";
    String uitvoerBestandBoogOnder = "src/main/resources/ArcLower_export.png";
    String uitvoerBestandBol = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(bronbestandBoogBoven, psdLoadOptions)) {
        psdImage.save(uitvoerBestandBoogBoven, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(bronbestandBoogOnder, psdLoadOptions)) {
        psdImage.save(uitvoerBestandBoogOnder, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(bronbestandBol, psdLoadOptions)) {
        psdImage.save(uitvoerBestandBol, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-520. Implementeren van nieuwe methode PsdImage.AddPosterizeAdjustmentLayer voor het toevoegen van een nieuwe Posterize-laag**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya.psd";
    String outFile = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile)) {
        psdImage.addPosterizeAdjustmentLayer();
        psdImage.save(outFile);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // Controleer opgeslagen wijzigingen
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
    }
}

static void assertAreEqual(Object verwacht, Object daadwerkelijk) {
    assertAreEqual(verwacht, daadwerkelijk, "Objecten zijn niet gelijk.");
}

static void assertAreEqual(Object verwacht, Object daadwerkelijk, String boodschap) {
    if (!verwacht.equals(daadwerkelijk)) {
        throw new IllegalArgumentException(boodschap);
    }
}
{{< /highlight >}}

**PSDJAVA-521. PSD-informatie gaat verloren bij alleen openen en opslaan**

{{< highlight java >}}
    String bron = "src/main/resources/Oorspronkelijk bestand.psd";
    String uitvoerPsd = "src/main/resources/out_Oorspronkelijk bestand.psd";
    String uitvoerPng = "src/main/resources/out_Oorspronkelijk bestand.png";

    try (PsdImage psdImage = (PsdImage) Image.load(bron)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(uitvoerPsd);
        psdImage.save(uitvoerPng, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-522. Laden van afbeelding mislukt**

{{< highlight java >}}
    String bronBestand1 = "src/main/resources/test_text.psd";
    String bronBestand2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(bronBestand1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(bronBestand2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Laden van afbeelding mislukt: Kan object van het type UnknownStructure niet converteren naar het type DescriptorStructure**

{{< highlight java >}}
   try (PsdImage newPsd = new PsdImage(10, 10)) {
        newPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            newPsd.save(memStream.toOutputStream());

            memStream.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            memStream.write(new byte[1], 0, 0);
            memStream.setPosition(0);

            try (PsdImage psdImage = (PsdImage) Image.load(memStream.toInputStream())) {
                // Zou correct moeten laden
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Bestand gewijzigd in de externe bibliotheek beschadigt PSD-bestand, maar kan geopend worden in Photoshop**

{{< highlight java >}}
    String bronBestand = "src/main/resources/output.psd";
    String uitvoerBestand = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(bronBestand, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(uitvoerBestand, pngOptions);
    }
{{< /highlight >}}

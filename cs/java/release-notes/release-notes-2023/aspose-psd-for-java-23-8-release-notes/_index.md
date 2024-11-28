---
title: Aspose.PSD pro jazyk Java 23.8 - Poznámky k vydání
type: docs
weight: 40
url: /cs/java/aspose-psd-pro-javu-23-8-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Javu 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-pro-javu-23.8/) {{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                                                                      | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Přidán nový typ warp (Vlajka)                                                                                                                     |    Funkce   |
| PSDJAVA-519 | Přidány nové typy warpů: oblouk nahoru, oblouk dolů, sféra                                                                                       |    Funkce   |
| PSDJAVA-520 | Implementována nová metoda PsdImage.AddPosterizeAdjustmentLayer pro přidání nové vrstvy Posterize                                            |    Funkce   |
| PSDJAVA-521 | Ztráta informací PSD při pouhém otevření a uložení                                                                                                  |      Chyba     |
| PSDJAVA-522 | Načítání obrázku selhalo                                                                                                                        |      Chyba     |
| PSDJAVA-523 | Načítání obrázku selhalo: Nelze přetypovat objekt typu UnknownStructure na typ DescriptorStructure                                                 |      Chyba     |
| PSDJAVA-524 | Soubor změněný ve třetí straně knihovny poškodí soubor PSD, ale lze jej otevřít v aplikaci Photoshop                                             |      Chyba     |

## **Změny ve veřejném API**
# **Přidané API:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **Odebrané API:**

- žádné

## **Příklady použití:**

**PSDJAVA-518. Přidání nového typu warp (Vlajka)**

{{< highlight java >}}
    String zdrojovýSoubor = "src/main/resources/flag_warp.psd";
    String výstupníSoubor = "src/main/resources/flag_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(zdrojovýSoubor, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(výstupníSoubor, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-519. Přidány nové typy warpů: oblouk nahoru, oblouk dolů, sféra**

{{< highlight java >}}
    String zdrojSouborObloukNahoru = "src/main/resources/arc_upper_warp.psd";
    String zdrojSouborObloukDolů = "src/main/resources/arc_lower_warp.psd";
    String zdrojSouborBulge = "src/main/resources/bulge_warp.psd";

    String výstupníSouborObloukNahoru = "src/main/resources/ArcUpper_export.png";
    String výstupníSouborObloukDolů = "src/main/resources/ArcLower_export.png";
    String výstupníSouborBulge = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(zdrojSouborObloukNahoru, psdLoadOptions)) {
        psdImage.save(výstupníSouborObloukNahoru, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(zdrojSouborObloukDolů, psdLoadOptions)) {
        psdImage.save(výstupníSouborObloukDolů, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(zdrojSouborBulge, psdLoadOptions)) {
        psdImage.save(výstupníSouborBulge, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-520. Implementována nová metoda PsdImage.AddPosterizeAdjustmentLayer pro přidání nové vrstvy Posterize**

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

    // Ověření uložených změn
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objekty nejsou stejné.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-521. Ztráta informací PSD při pouhém otevření a uložení**

{{< highlight java >}}
    String src = "src/main/resources/Original file.psd";
    String outputPsd = "src/main/resources/out_Original file.psd";
    String outputPng = "src/main/resources/out_Original file.png";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputPsd);
        psdImage.save(outputPng, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-522. Načítání obrázku selhalo**

{{< highlight java >}}
    String srcFile1 = "src/main/resources/test_text.psd";
    String srcFile2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Načítání obrázku selhalo: Nelze přetypovat objekt typu UnknownStructure na typ DescriptorStructure**

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
                // Mělo by se načíst správně
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Soubor změněný ve třetí straně knihovny poškodí soubor PSD, ale lze jej otevřít v aplikaci Photoshop**

{{< highlight java >}}
    String zdrojovýSoubor = "src/main/resources/output.psd";
    String výstupníSoubor = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(zdrojovýSoubor, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(výstupníSoubor, pngOptions);
    }
{{< /highlight >}}

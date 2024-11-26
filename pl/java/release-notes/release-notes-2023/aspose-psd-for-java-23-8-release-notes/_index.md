---
title: Notatki wersji Aspose.PSD dla Javy 23.8
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-javy-23-8-notatki-wydania/
---

{{% alert color="primary" %}} Ta strona zawiera notatki wersji dla [Aspose.PSD dla Javy 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) {{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                                                                  | **Kategoria** |
|:------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-------------:|
| PSDJAVA-518  | Dodano nowy typ deformacji (Flaga)                                                                                                                |    Funkcja    |
| PSDJAVA-519  | Dodano nowe typy deformacji: łuk do góry, łuk w dół, sfera                                                                                       |    Funkcja    |
| PSDJAVA-520  | Implementacja nowej metody PsdImage.AddPosterizeAdjustmentLayer do dodawania nowej warstwy Posterize                                            |    Funkcja    |
| PSDJAVA-521  | Utrata informacji w pliku PSD po prostym otwarciu i zapisie                                                                                       |      Błąd     |
| PSDJAVA-522  | Błąd podczas ładowania obrazu                                                                                                                     |      Błąd     |
| PSDJAVA-523  | Błąd podczas ładowania obrazu: Nie można rzutować obiektu typu UnknownStructure na typ DescriptorStructure                                        |      Błąd     |
| PSDJAVA-524  | Zmieniony plik w bibliotece zewnętrznej psuje plik PSD, ale można go otworzyć w programie Photoshopu                                            |      Błąd     |

## Zmiany w interfejsie publicznym
# **Dodane interfejsy API:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **Usunięte interfejsy API:**

- Brak

## **Przykłady użycia:**

**PSDJAVA-518. Dodano nowy typ deformacji (Flaga)**

{{< highlight java >}}
    String plikZrodlowy = "src/main/resources/flag_warp.psd";
    String plikWyjsciowy = "src/main/resources/flag_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(plikZrodlowy, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(plikWyjsciowy, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-519. Dodano nowe typy deformacji: łuk do góry, łuk w dół, sfera**

{{< highlight java >}}
    String plikZrodlowyLukGora = "src/main/resources/arc_upper_warp.psd";
    String plikZrodlowyLukDol = "src/main/resources/arc_lower_warp.psd";
    String plikZrodlowyWypuklosc = "src/main/resources/bulge_warp.psd";

    String plikWyjsciowyLukGora = "src/main/resources/ArcUpper_export.png";
    String plikWyjsciowyLukDol = "src/main/resources/ArcLower_export.png";
    String plikWyjsciowyWypuklosc = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(plikZrodlowyLukGora, psdLoadOptions)) {
        psdImage.save(plikWyjsciowyLukGora, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(plikZrodlowyLukDol, psdLoadOptions)) {
        psdImage.save(plikWyjsciowyLukDol, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(plikZrodlowyWypuklosc, psdLoadOptions)) {
        psdImage.save(plikWyjsciowyWypuklosc, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-520. Implementacja nowej metody PsdImage.AddPosterizeAdjustmentLayer do dodawania nowej warstwy Posterize**

{{< highlight java >}}
public static void main(String[] args) {
    String plikZrodlowy = "src/main/resources/zendeya.psd";
    String plikWyjsciowy = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(plikZrodlowy)) {
        psdImage.addPosterizeAdjustmentLayer();
        psdImage.save(plikWyjsciowy);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // Sprawdzenie zapisanych zmian
    try (PsdImage image = (PsdImage) Image.load(plikWyjsciowy, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
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

**PSDJAVA-521. Utrata informacji w pliku PSD po prostym otwarciu i zapisie**

{{< highlight java >}}
    String plikZrodlowy = "src/main/resources/Oryginalny plik.psd";
    String outputPsd = "src/main/resources/out_Oryginalny plik.psd";
    String outputPng = "src/main/resources/out_Oryginalny plik.png";

    try (PsdImage psdImage = (PsdImage) Image.load(plikZrodlowy)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputPsd);
        psdImage.save(outputPng, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-522. Błąd podczas ładowania obrazu**

{{< highlight java >}}
    String plikTestowy1 = "src/main/resources/test_text.psd";
    String plikTestowy2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(plikTestowy1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(plikTestowy2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Błąd podczas ładowania obrazu: Nie można rzutować obiektu typu UnknownStructure na typ DescriptorStructure**

{{< highlight java >}}
   try (PsdImage nowaPsd = new PsdImage(10, 10)) {
        nowaPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            nowaPsd.save(memStream.toOutputStream());

            memStream.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            memStream.write(new byte[1], 0, 0);
            memStream.setPosition(0);

            try (PsdImage psdImage = (PsdImage) Image.load(memStream.toInputStream())) {
                // Powinno być wczytane poprawnie
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Zmieniony plik w bibliotece zewnętrznej psuje plik PSD, ale można go otworzyć w programie Photoshop**

{{< highlight java >}}
    String plikZrodlowy = "src/main/resources/output.psd";
    String plikWyjsciowy = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(plikZrodlowy, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(plikWyjsciowy, pngOptions);
    }
{{< /highlight >}}

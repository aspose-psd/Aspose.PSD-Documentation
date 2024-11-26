---
title: Aspose.PSD dla Javy 21.7 - Notatki wersji
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-java-21-7-notatki-wydania/
---

{{% alert color="primary" %}} Ta strona zawiera notatki wersji dla [Aspose.PSD dla Javy 21.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.7/) {{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDJAVA-362|Obsługa edycji czcionki przy użyciu TextPortions|Funkcja|
|PSDJAVA-363|Aspose.PSD 21.6: ImageSaveException podczas próby konwersji PSD do PNG|Błąd|

# **Zmiany w API publicznym**
# **Dodane interfejsy API:**
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontName
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontName(java.lang.String)
- M:com.aspose.psd.FontSettings.getAdobeFontName(java.lang.String)

# **Usunięte interfejsy API:**
- Brak

# **Przykłady użycia:**

**PSDJAVA-362. Obsługa edycji czcionki przy użyciu TextPortions**

{{< highlight java >}}
        String outputFilePng = "wynik_fontEditTest.png";
        String outputFilePsd = "fontEditTest.psd";

        PsdImage image = new PsdImage(500, 500);
        try {
            FillLayer backgroundFillLayer = FillLayer.createInstance(FillType.Color);
            ((IColorFillSettings) backgroundFillLayer.getFillSettings()).setColor(Color.getWhite());
            image.addLayer(backgroundFillLayer);

            TextLayer textLayer = image.addTextLayer("Tekst 1", new Rectangle(10, 35, image.getWidth(), 35));

            ITextPortion firstPortion = textLayer.getTextData().getItems()[0];
            firstPortion.getStyle().setFontName(FontSettings.getAdobeFontName("Comic Sans MS"));

            ITextPortion secondPortion = textLayer.getTextData().producePortion();
            secondPortion.setText("Tekst 2");
            secondPortion.getParagraph().apply(firstPortion.getParagraph());
            secondPortion.getStyle().apply(firstPortion.getStyle());
            secondPortion.getStyle().setFontName(FontSettings.getAdobeFontName("Arial"));

            textLayer.getTextData().addPortion(secondPortion);
            textLayer.getTextData().updateLayerData();

            image.save(outputFilePng, new PngOptions());
            image.save(outputFilePsd);
        } finally {
            image.dispose();
        }

        PsdImage imageOutput = (PsdImage) Image.load(outputFilePsd);
        try {
            TextLayer textLayer = (TextLayer) imageOutput.getLayers()[2];

            String adobeFontName1 = FontSettings.getAdobeFontName("Comic Sans MS");
            String adobeFontName2 = FontSettings.getAdobeFontName("Arial");

            AssertAreEqual(adobeFontName1, textLayer.getTextData().getItems()[0].getStyle().getFontName());
            AssertAreEqual(adobeFontName2, textLayer.getTextData().getItems()[1].getStyle().getFontName());
        } finally {
            imageOutput.dispose();
        }
{{< /highlight >}}

**PSDJAVA-363. Aspose.PSD 21.6: ImageSaveException podczas próby konwersji PSD do PNG**

{{< highlight java >}}
        String srcFile = "input.psd";
        String output = "output.png";
        Image image = Image.load(srcFile);
        try {
            image.save(output, new PngOptions());
        } finally {
            image.dispose();
        }
{{< /highlight >}}

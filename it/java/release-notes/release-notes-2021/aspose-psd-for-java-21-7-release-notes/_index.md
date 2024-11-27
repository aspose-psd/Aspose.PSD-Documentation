---
title: Note sulla versione di Aspose.PSD per Java 21.7
type: docs
weight: 40
url: /it/java/aspose-psd-for-java-21-7-release-notes/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 21.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.7/) {{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-362|Supporto dell'editing dei caratteri tramite TextPortions|Caratteristica|
|PSDJAVA-363|Aspose.PSD 21.6: ImageSaveException durante il tentativo di convertire PSD in PNG|Errore|

# **Modifiche all'API pubblica**
# **API aggiunte:**
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontName
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontName(java.lang.String)
- M:com.aspose.psd.FontSettings.getAdobeFontName(java.lang.String)

# **API rimosse:**
- Nessuna

# **Esempi di utilizzo:**

**PSDJAVA-362. Supporto dell'editing dei caratteri tramite TextPortions**

{{< highlight java >}}
        String outputFilePng = "risultato_fontEditTest.png";
        String outputFilePsd = "fontEditTest.psd";

        PsdImage image = new PsdImage(500, 500);
        try {
            FillLayer backgroundFillLayer = FillLayer.createInstance(FillType.Color);
            ((IColorFillSettings) backgroundFillLayer.getFillSettings()).setColor(Color.getWhite());
            image.addLayer(backgroundFillLayer);

            TextLayer textLayer = image.addTextLayer("Testo 1", new Rectangle(10, 35, image.getWidth(), 35));

            ITextPortion firstPortion = textLayer.getTextData().getItems()[0];
            firstPortion.getStyle().setFontName(FontSettings.getAdobeFontName("Comic Sans MS"));

            ITextPortion secondPortion = textLayer.getTextData().producePortion();
            secondPortion.setText("Testo 2");
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

**PSDJAVA-363. Aspose.PSD 21.6: ImageSaveException durante il tentativo di convertire PSD in PNG**

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

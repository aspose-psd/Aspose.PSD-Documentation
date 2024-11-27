---
title: Note sulla versione di Aspose.PSD per Java 23.10
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-23-10-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.10/) {{% /alert %}}

| **Chiave**     | **Sommario**                                                                 | **Categoria** |
|:--------------|:------------------------------------------------------------------------|:------------|
| PSDJAVA-538   | Supporto della direzione del testo verticale                          | Funzionalità |
| PSDJAVA-542   | Utilizzo delle impostazioni del contorno dal vstk risorsa nel rendering del contorno della forma | Funzionalità |
| PSDJAVA-540   | Implementare il rendering dell'area interna delle forme di contorno   | Funzionalità|
| PSDJAVA-541   | Non ridisegnare lo strato Forma se non è stato modificato            | Funzionalità|
| PSDJAVA-545   | [Formato AI] Aggiunta del supporto per la lettura dell'intestazione da file AI basati su PDF | Funzionalità |
| PSDJAVA-546   | Diversi modi per impostare la risoluzione del file Psd non funzionano | Bug |
| PSDJAVA-547   | FontSettings.SetFontsFolders non funziona o Aspose.PSD utilizza un font incorretto | Bug |
| PSDJAVA-548   | Regression. Risolvere l'eccezione di riferimento nullo su PsdImage.Save quando si ha uno strato Forma | Bug |

## **Modifiche all'API pubblica**
# **API Aggiunte:**

- M:com.aspose.psd.FontSettings.getGetSystemAlternativeFont
- M:com.aspose.psd.FontSettings.setGetSystemAlternativeFont(boolean)
- M:com.aspose.psd.Graphics.getPaintableImageOptions
- M:com.aspose.psd.Graphics.setPaintableImageOptions(com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.getAutoAdjustPalette
- M:com.aspose.psd.Image.getFileFormat(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.extensions.RegionExtensions.#ctor
- M:com.aspose.psd.fileformats.psd.PsdImage.setResolution(double,double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.getStroke
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.setStroke(com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

# **API Rimosse:**

- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- M:com.aspose.psd.imageoptions.BmpOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.CmxRasterizationOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.GifOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.Jpeg2000Options.memberwiseClone
- M:com.aspose.psd.imageoptions.JpegOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PdfOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PngOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PsdOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.TiffOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.VectorRasterizationOptions.memberwiseClone
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center

## **Esempi di utilizzo:**

** PSDJAVA-538. Supporto della direzione del testo verticale**

{{< highlight java >}}
    
    String fileSorgente = "src/main/resources/692_lt1.psd";
    String fileOutput = "src/main/resources/692_output.png";
    String cartelleFont = "src/main/resources/692_Fonts";

        List<String> cartelleFont = new List<>(FontSettings.getFontsFolders());
        cartelleFont.add(cartelleFont);
        FontSettings.setFontsFolders(cartelleFont.toArray(new String[0]), true);

        try(PsdImage immaginePsd = (PsdImage)Image.load(fileSorgente)) {
            PngOptions opzioniPng = new PngOptions();
            opzioniPng.setColorType(PngColorType.TruecolorWithAlpha);

            immaginePsd.save(fileOutput, opzioniPng);
        }

{{< /highlight >}}

** PSDJAVA-542. Utilizzo delle impostazioni del contorno dalla risorsa vstk nel rendering del contorno della forma**

{{< highlight java >}}

    public static void main(String[] args) {
        String fileSorgente = "src/main/resources/StrokeShapeTest.psd";
        String fileOutputPsd = "src/main/resources/StrokeShapeTest.out.psd";
        String fileOutputPng = "src/main/resources/StrokeShapeTest.out.png";

        try (PsdImage immagine = (PsdImage) Image.load(fileSorgente)) {
            Layer strato = immagine.getLayers()[1];
            ShapeLayer stratoForma = (ShapeLayer) immagine.getLayers()[1];
            ColorFillSettings impostazioniRiempimento = (ColorFillSettings) stratoForma.getFill();
            impostazioniRiempimento.setColor(Color.getGreenYellow());
            stratoForma.update();

            ShapeLayer stratoForma2 = (ShapeLayer) immagine.getLayers()[3];
            GradientFillSettings impostazioniGradiente = (GradientFillSettings) stratoForma2.getFill();
            impostazioniGradiente.setDither(true);
            impostazioniGradiente.setReverse(true);
            impostazioniGradiente.setAlignWithLayer(false);
            impostazioniGradiente.setAngle(20);
            impostazioniGradiente.setScale(50);
            impostazioniGradiente.getColorPoints()[0].setLocation(100);
            impostazioniGradiente.getColorPoints()[1].setLocation(4000);
            impostazioniGradiente.getTransparencyPoints()[0].setLocation(200);
            impostazioniGradiente.getTransparencyPoints()[1].setLocation(3800);
            impostazioniGradiente.getTransparencyPoints()[0].setOpacity(90);
            impostazioniGradiente.getTransparencyPoints()[1].setOpacity(10);
            stratoForma2.update();

            ShapeLayer stratoForma3 = (ShapeLayer) immagine.getLayers()[5];
            StrokeSettings impostazioniContorno = (StrokeSettings) stratoForma3.getStroke();
            impostazioniContorno.setSize(15);
            ColorFillSettings impostazioniRiempimentoContorno = (ColorFillSettings) impostazioniContorno.getFill();
            impostazioniRiempimentoContorno.setColor(Color.getGreenYellow());
            stratoForma3.update();

            immagine.save(fileOutputPsd);
            immagine.save(fileOutputPng, new PngOptions());
        }

        // Controlla i dati modificati.
        try (PsdImage immagine = (PsdImage) Image.load(fileOutputPsd)) {
            ShapeLayer stratoForma = (ShapeLayer) immagine.getLayers()[1];
            ColorFillSettings impostazioniRiempimento = (ColorFillSettings) stratoForma.getFill();
            assertSonoUguali(Color.getGreenYellow(), impostazioniRiempimento.getColor());

            ShapeLayer stratoForma2 = (ShapeLayer) immagine.getLayers()[3];
            GradientFillSettings impostazioniGradiente = (GradientFillSettings) stratoForma2.getFill();
            assertSonoUguali(true, impostazioniGradiente.getDither());
            assertSonoUguali(true, impostazioniGradiente.getReverse());
            assertSonoUguali(false, impostazioniGradiente.getAlignWithLayer());
            assertSonoUguali(20.0, impostazioniGradiente.getAngle());
            assertSonoUguali(50, impostazioniGradiente.getScale());
            assertSonoUguali(100, impostazioniGradiente.getColorPoints()[0].getLocation());
            assertSonoUguali(4000, impostazioniGradiente.getColorPoints()[1].getLocation());
            assertSonoUguali(200, impostazioniGradiente.getTransparencyPoints()[0].getLocation());
            assertSonoUguali(3800, impostazioniGradiente.getTransparencyPoints()[1].getLocation());
            assertSonoUguali(90.0, impostazioniGradiente.getTransparencyPoints()[0].getOpacity());
            assertSonoUguali(10.0, impostazioniGradiente.getTransparencyPoints()[1].getOpacity());

            ShapeLayer stratoForma3 = (ShapeLayer) immagine.getLayers()[5];
            StrokeSettings impostazioniContorno = (StrokeSettings) stratoForma3.getStroke();
            ColorFillSettings impostazioniRiempimentoContorno = (ColorFillSettings) impostazioniContorno.getFill();
            assertSonoUguali(15.0, impostazioniContorno.getSize());
            assertSonoUguali(Color.getGreenYellow(), impostazioniRiempimentoContorno.getColor());
        }
    }

    static void assertSonoUguali(Object previsto, Object effettivo) {
        assertSonoUguali(previsto, effettivo, "Gli oggetti non sono uguali.");
    }

    static void assertSonoUguali(Object previsto, Object effettivo, String messaggio) {
        if (!previsto.equals(effettivo)) {
            throw new IllegalArgumentException(messaggio);
        }
    }

{{< /highlight >}}


** PSDJAVA-540. Implementare il rendering dell'area interna delle forme di contorno**

{{< highlight java >}}

    public static void main(String[] args) {
        String fileSorgente = "src/main/resources/StrokeShapeTest.psd";
        String fileOutputPsd = "src/main/resources/StrokeShapeTest.out.psd";
        String fileOutputPng = "src/main/resources/StrokeShapeTest.out.png";

        try (PsdImage immagine = (PsdImage) Image.load(fileSorgente)) {
            Layer strato = immagine.getLayers()[1];
            ShapeLayer stratoForma = (ShapeLayer) immagine.getLayers()[1];
            ColorFillSettings impostazioniRiempimento = (ColorFillSettings) stratoForma.getFill();
            impostazioniRiempimento.setColor(Color.getGreenYellow());
            stratoForma.update();

            ShapeLayer stratoForma2 = (ShapeLayer) immagine.getLayers()[3];
            GradientFillSettings impostazioniGradiente = (GradientFillSettings) stratoForma2.getFill();
            impostazioniGradiente.setDither(true);
            impostazioniGradiente.setReverse(true);
            impostazioniGradiente.setAlignWithLayer(false);
            impostazioniGradiente.setAngle(20);
            impostazioniGradiente.setScale(50);
            impostazioniGradiente.getColorPoints()[0].setLocation(100);
            impostazioniGradiente.getColorPoints()[1].setLocation(4000);
            impostazioniGradiente.getTransparencyPoints()[0].setLocation(200);
            impostazioniGradiente.getTransparencyPoints()[1].setLocation(3800);
            impostazioniGradiente.getTransparencyPoints()[0].setOpacity(90);
            impostazioniGradiente.getTransparencyPoints()[1].setOpacity(10);
            stratoForma2.update();

            ShapeLayer stratoForma3 = (ShapeLayer) immagine.getLayers()[5];
            StrokeSettings impostazioniContorno = (StrokeSettings) stratoForma3.getStroke();
            impostazioniContorno.setSize(15);
            ColorFillSettings impostazioniRiempimentoContorno = (ColorFillSettings) impostazioniContorno.getFill();
            impostazioniRiempimentoContorno.setColor(Color.getGreenYellow());
            stratoForma3.update();

            immagine.save(fileOutputPsd);
            immagine.save(fileOutputPng, new PngOptions());
        }

        // Controlla i dati modificati.
        try (PsdImage immagine = (PsdImage) Image.load(fileOutputPsd)) {
            ShapeLayer stratoForma = (ShapeLayer) immagine.getLayers()[1];
            ColorFillSettings impostazioniRiempimento = (ColorFillSettings) stratoForma.getFill();
            assertSonoUguali(Color.getGreenYellow(), impostazioniRiempimento.getColor());

            ShapeLayer stratoForma2 = (ShapeLayer) immagine.getLayers()[3];
            GradientFillSettings impostazioniGradiente = (GradientFillSettings) stratoForma2.getFill();
            assertSonoUguali(true, impostazioniGradiente.getDither());
            assertSonoUguali(true, impostazioniGradiente.getReverse());
            assertSonoUguali(false, impostazioniGradiente.getAlignWithLayer());
            assertSonoUguali(20.0, impostazioniGradiente.getAngle());
            assertSonoUguali(50, impostazioniGradiente.getScale());
            assertSonoUguali(100, impostazioniGradiente.getColorPoints()[0].getLocation());
            assertSonoUguali(4000, impostazioniGradiente.getColorPoints()[1].getLocation());
            assertSonoUguali(200, impostazioniGradiente.getTransparencyPoints()[0].getLocation());
            assertSonoUguali(3800, impostazioniGradiente.getTransparencyPoints()[1].getLocation());
            assertSonoUguali(90.0, impostazioniGradiente.getTransparencyPoints()[0].getOpacity());
            assertSonoUguali(10.0, impostazioniGradiente.getTransparencyPoints()[1].getOpacity());

            ShapeLayer stratoForma3 = (ShapeLayer) immagine.getLayers()[5];
            StrokeSettings impostazioniContorno = (StrokeSettings) stratoForma3.getStroke();
            ColorFillSettings impostazioniRiempimentoContorno = (ColorFillSettings) impostazioniContorno.getFill();
            assertSonoUguali(15.0, impostazioniContorno.getSize());
            assertSonoUguali(Color.get
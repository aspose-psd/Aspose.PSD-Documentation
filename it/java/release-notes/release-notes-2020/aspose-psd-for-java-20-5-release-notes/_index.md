---
title: Note sulla versione di Aspose.PSD per Java 20.5
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-20-5-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-188|Supporto per il progresso della conversione del documento|Caratteristica|
|PSDJAVA-197|Supporto del salvataggio dell'immagine PSD del modo di colore scala di grigi con 16 bit per canale|Caratteristica|
|PSDJAVA-198|Supporto di Nvrt Resource (Risorsa livello di regolazione invertita)|Caratteristica|
|PSDJAVA-200|Supporto dei maschere di livello per i gruppi di livelli|Caratteristica|
|PSDJAVA-195|Risoluzione del salvataggio dell'immagine PSD con modo di colore scala di grigi a 16 bit per canale al formato PSD a 16 bit per canale RGB|Errore|
|PSDJAVA-196|Risoluzione del salvataggio dell'immagine PSD con modo di colore scala di grigi a 16 bit per canale al formato PSD scala di grigi a 8 bit per canale|Errore|
|PSDJAVA-199|L'allineamento del testo attraverso ITextPortion non funziona per le lingue da destra verso sinistra. Il file di output è danneggiato.|Errore|
|PSDJAVA-201|Eccezione nel tentativo di aprire un file Psd particolare con Colore Lab e 8 bit/canale|Errore|
# **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- Nessuna
## **API rimosse:**
- Nessuna
# **Esempi di utilizzo:**

**PSDJAVA-188. Supporto per il progresso della conversione del documento**

{{< highlight java >}}

 // Un esempio di utilizzo del gestore del progresso per operazioni di caricamento e salvataggio.

// Il programma utilizza diverse opzioni di salvataggio per triggerare eventi di progresso.

String sourceFilePath = "Mela.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Crea un gestore del progresso che scrive le informazioni di progresso nella console

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s su %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Caricamento Mela.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Lega il gestore del progresso per mostrare il progresso di caricamento

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Carica PSD utilizzando opzioni di caricamento specifiche

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Salvataggio Mela.psd nel formato PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Rendi l'immagine di output a colori e non trasparente

    pngOptions.setColorType(PngColorType.Truecolor);

    // Lega il gestore del progresso per mostrare il progresso di salvataggio

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Converti PSD in PNG con caratteristiche specifiche

    image.save(outputStream, pngOptions);

    System.out.println("---------- Salvataggio Mela.psd nel formato PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Rendi il PSD di output a colori

    psdOptions.setColorMode(ColorModes.Rgb);

    // Imposta un canale per ogni colore (rosso, verde e blu) più un canale composito

    psdOptions.setChannelsCount((short)4);

    // Lega il gestore del progresso per mostrare il progresso di salvataggio

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Salva una copia di PSD con caratteristiche specifiche

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Supporto del salvataggio dell'immagine PSD del modo di colore scala di grigi con 16 bit per canale**

{{< highlight java >}}

 // Un esempio di applicazione di diverse combinazioni di modi di colore, bit per canale, canali

// contare e compressioni per livelli specifici.

// Rendere un metodo accessibile dallo scope locale

class EstensioneScopeLocale

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // Carica un PSD in scala di grigi a 16 bit predefinito

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Disegna un bordo interno grigio intorno al perimetro del livello

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Salva una copia di PSD con caratteristiche specifiche

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // Carica il PSD salvato

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Converti il PSD salvato in un'immagine PNG in scala di grigi

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // qui non dovrebbe esserci alcuna eccezione

        }

        finally

        {

            image1.dispose();

        }

    }

}

EstensioneScopeLocale $ = new EstensioneScopeLocale();

$.saveToPsdThenLoadAndSaveToPng("scala_di_grigi5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_senza_livelli", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_senza_livelli", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_senza_livelli", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("indice8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Supporto di Nvrt Resource (Risorsa livello di regolazione invertita)**

{{< highlight java >}}

 // Un esempio di trovare NvrtResource di un livello di regolazione invertito.

String inPsdFilePath = "LivelloRegolazioneInvertito.psd";

NvrtResource nvrtResource = null;

// Carica un PSD predefinito contenente un livello di regolazione invertito

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Cerca una risorsa del livello di regolazione invertito

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // La risorsa NvrtResource è trovata

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Supporto dei maschere di livello per i gruppi di livelli**

{{< highlight java >}}

 // Un esempio di supporto delle maschere di livello per i gruppi di livelli. Il programma carica e salva PSD

// in diversi formati di output senza generare eccezioni.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Carica un PSD predefinito contenente maschere di livello per i gruppi di livelli

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Converti il PSD caricato in PNG

    input.save(outputPng, new PngOptions());

    // Salva una copia del PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Risoluzione del salvataggio dell'immagine PSD con modo di colore scala di grigi a 16 bit per canale al formato PSD a 16 bit per canale RGB**

{{< highlight java >}}

 // Un esempio di conversione di un PSD scala di grigi a 16 bit in uno RGB a 16 bit e poi di nuovo a

// un'immagine raster a 16 bit in scala di grigi.

String sourceFilePath = "scala_di_grigi5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Carica un PSD scala di grigi a 16 bit predefinito

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Disegna un bordo interno grigio intorno al perimetro del livello

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Salva una copia di PSD con il modo di colore cambiato in RBG

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Carica il PSD salvato

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Converti il PSD salvato in un'immagine PNG in scala di grigi

    image1.save(pngExportPath, pngOptions); // qui non dovrebbe esserci alcuna eccezione

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Risoluzione del salvataggio dell'immagine PSD con modo di colore scala di grigi a 16 bit per canale al formato PSD scala di grigi a 8 bit per canale**

{{< highlight java >}}

 // Un esempio di conversione di un PSD scala di grigi a 16 bit in uno scala di grigi a 8 bit e poi in

// un'immagine raster a 8 bit in scala di grigi.

String sourceFilePath = "scala_di_grigi16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Carica un PSD scala di grigi a 16 bit predefinito

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Disegna un bordo interno grigio intorno al perimetro del livello

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Salva una copia di PSD con il conteggio canali cambiato a 8-bit

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Carica il PSD salvato

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Converti il PSD salvato in un'immagine PNG in scala di grigi

    image1.save(pngExportPath, pngOptions); // qui non dovrebbe esserci alcuna eccezione

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. L'allineamento del testo attraverso ITextPortion non funziona per le lingue da destra verso sinistra. Il file di output è danneggiato.**

{{< highlight java >}}

 // Un esempio di allineamento di un livello di testo RTL attraverso ITextPortion. Il programma modifica

// un livello di testo RTL esistente in un PSD caricato e salva una copia del documento modificato.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// Carica un PSD predefinito contenente un livello di testo RTL

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // Ottieni porzioni di testo dal livello

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // Cambia l'allineamento del testo

    portions[0].getParagraph().setJustification(2);

    // Applica modifiche al livello

    layer.getTextData().updateLayerData();

    // Salva una copia modificata del PSD

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Eccezione nel tentativo di aprire un file Psd particolare con Colore Lab e 8 bit/canale**

{{< highlight java >}}

 // Un esempio del supporto di un documento Photoshop a 8 bit in modalità colore LAB.

String srcFile = "SenzaTitolo-1.psd";

String outputFilePsd = "output.psd";

// Carica un PSD predefinito a 8 bit in modalità colore LAB

PsdImage psdImage = (PsdImage)Image.load(srcFile);

try

{

    // Salva una copia del PSD caricato

    psdImage.save(outputFilePsd);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}
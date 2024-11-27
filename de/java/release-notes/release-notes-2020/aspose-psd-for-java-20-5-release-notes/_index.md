---
title: Aspose.PSD für Java 20.5 - Versionshinweise
type: docs
weight: 40
url: /de/java/aspose-psd-für-java-20-5-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-für-java-20.5/) {{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-188|Unterstützung für den Fortschritt bei der Dokumentkonvertierung|Feature|
|PSDJAVA-197|Unterstützung des Farbmodus Graustufen PSD-Bildspeicherung mit 16 Bit pro Kanal|Feature|
|PSDJAVA-198|Unterstützung des Nvrt-Ressourcen (Invert Adjustement Layer-Ressource)|Feature|
|PSDJAVA-200|Unterstützung von Ebenenmasken für Ebenengruppen|Feature|
|PSDJAVA-195|Behebung beim Speichern eines PSD-Bildes mit Farbmodus Graustufen 16 Bit pro Kanal im 16-Bit pro Kanal RGB-PSD-Format|Bug|
|PSDJAVA-196|Behebung beim Speichern eines PSD-Bildes mit Farbmodus Graustufen 16 Bit pro Kanal im 8-Bit pro Kanal Graustufen-PSD-Format|Bug|
|PSDJAVA-199|Textausrichtung durch ITextPortion funktioniert nicht für rechts-nach-links-Sprachen. Die Ausgabedatei ist beschädigt.|Bug|
|PSDJAVA-201|Ausnahme beim Versuch, eine bestimmte PSD-Datei mit Lab-Farbe und 8 bit/Kanal zu öffnen|Bug|
# **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- Keine
## **Entfernte APIs:**
- Keine
# **Verwendungsbeispiele:**

**PSDJAVA-188. Unterstützung für den Dokumentkonvertierungsfortschritt**

{{< highlight java >}}

 // Ein Beispiel für die Verwendung des Fortschrittshandlers für Lade- und Speicheroperationen.

// Das Programm verwendet verschiedene Speicheroptionen, um Fortschrittsereignisse auszulösen.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Erstelle einen Fortschritts-Handler, der Fortschrittsinformationen in die Konsole schreibt

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s von %s", 

                progressInfo.getDescription(), 

                Enum.getName(EventType.class, progressInfo.getEventType()), 

                progressInfo.getValue(), 

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Lade Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Binden Sie den Fortschritts-Handler, um den Ladevorgang anzuzeigen

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Laden Sie PSD unter Verwendung spezifischer Ladeoptionen

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Speichern von Apple.psd im PNG-Format ----------");

    PngOptions pngOptions = new PngOptions();

    // Mache das Ausgabebild farbig und nicht transparent

    pngOptions.setColorType(PngColorType.Truecolor);

    // Binden Sie den Fortschritts-Handler, um den Speicherfortschritt anzuzeigen

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Konvertiere PSD in PNG mit spezifischen Merkmalen

    image.save(outputStream, pngOptions);

    System.out.println("---------- Speichern von Apple.psd im PSD-Format ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Mache das Ausgabefarbe PSD farbig

    psdOptions.setColorMode(ColorModes.Rgb);

    // Setze einen Kanal für jede Farbe (Rot, Grün und Blau) plus einen Zusammensetzungskanal

    psdOptions.setChannelsCount((short)4);

    // Binden Sie den Fortschritts-Handler, um den Speicherfortschritt anzuzeigen

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Speichern Sie eine Kopie von PSD mit spezifischen Merkmalen

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Unterstützung der PSD-Bildspeicherung im Graustufen-Farbmodus mit 16 Bit pro Kanal**

{{< highlight java >}}

 // Ein Beispiel für die Anwendung verschiedener Kombinationen von Farbmodi, Bits pro Kanal, Kanälen

// Zählimpfen und Kompressionen für spezifische Ebenen.

// Mache eine Methode aus dem lokalen Bereich zugänglich

class LocalScopeExtension

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

        // Lade eine vordefinierte 16-Bit-Graustufen-PSD

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Zeichne einen grauen Innenrand um den Rand der Ebene

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3, 

                    height / 3, 

                    width - (2 * (width / 3)) - 1, 

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Speichern Sie eine Kopie von PSD mit spezifischen Merkmalen

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

        // Lade die gespeicherte PSD

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Konvertiere die gespeicherte PSD in ein Graustufen-PNG-Bild

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // hier sollte keine Ausnahme auftreten

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Unterstützung der Nvrt-Ressource (Invert Adjustement Layer-Ressource)**

{{< highlight java >}}

 // Ein Beispiel zum Auffinden der Nvrt-Ressource einer invertierten Anpassungsebenen-Ressource.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Lade eine vordefinierte PSD, die eine invertierte Anpassungsebene enthält

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Versuchen Sie, eine Ressource der invertierten Anpassungsebene zu finden

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Die Nvrt-Ressource wurde gefunden

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

**PSDJAVA-200. Unterstützung von Ebenenmasken für Ebenengruppen**

{{< highlight java >}}

 // Ein Beispiel zur Unterstützung von Ebenenmasken für Ebenengruppen. Das Programm lädt und speichert PSD

// in verschiedenen Ausgabeformaten, ohne Ausnahmen auszulösen.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Lade eine vordefinierte PSD, die Ebenenmasken für Ebenengruppen enthält

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Konvertiere die geladene PSD in PNG

    input.save(outputPng, new PngOptions());

    // Speichern Sie eine Kopie der PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Behebung beim Speichern eines PSD-Bildes mit Graustufen-Farbmodus 16 Bit pro Kanal in ein 16-Bit pro Kanal RGB-PSD-Format**

{{< highlight java >}}

 // Ein Beispiel für die Konvertierung einer 16-Bit-Graustufen-PSD in eine 16-Bit-RGB-PSD und dann zurück zu 

// 16-Bit-Graustufen, aber ein Rasterbild.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Lade eine vordefinierte 16-Bit-Graustufen-PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Zeichne einen grauen Innenrand um den Rand der Ebene

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Speichern Sie eine Kopie von PSD mit geänderter Farbmodus in RBG

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

// Lade die gespeicherte PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Konvertiere die gespeicherte PSD in ein Graustufen-PNG-Bild

    image1.save(pngExportPath, pngOptions); // hier sollte keine Ausnahme auftreten

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Behebung beim Speichern eines PSD-Bildes mit Graustufen-Farbmodus 16 Bit pro Kanal in ein 8-Bit pro Kanal Graustufen-PSD-Format**

{{< highlight java >}}

 // Ein Beispiel für die Umwandlung einer 16-Bit-Graustufen-PSD in eine 8-Bit-Graustufen-PSD und dann in 

// ein 8-Bit-Graustufen-Rasterbild.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Lade eine vordefinierte 16-Bit-Graustufen-PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Zeichne einen grauen Innenrand um den Rand der Ebene

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Speichern Sie eine Kopie von PSD mit einer Kanalanzahl von 8-Bit

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

// Lade die gespeicherte PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Konvertiere die gespeicherte PSD in ein Graustufen-PNG-Bild

    image1.save(pngExportPath, pngOptions); // hier sollte keine Ausnahme auftreten

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Textausrichtung durch ITextPortion funktioniert nicht für rechts-nach-links-Sprachen. Die Ausgabedatei ist beschädigt.**

{{< highlight java >}}

 // Ein Beispiel zum Ausrichten von RTL-Textebenen durch ITextPortion. Das Programm modifiziert

// eine vorhandene RTL-Textebene in der geladenen PSD und speichert eine Kopie des modifizierten Dokuments.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// Lade eine vordefinierte PSD, die eine RTL-Textebene enthält

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // Erhalte Textbereiche aus der Ebene

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // Ändere die Textausrichtung

    portions[0].getParagraph().setJustification(2);

    // Übertrage die Änderungen auf die Ebene

    layer.getTextData().updateLayerData();

    // Speichere eine modifizierte Kopie der PSD

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Ausnahme beim Versuch, eine bestimmte PSD-Datei mit Lab-Farbe und 8 bit/Kanal zu öffnen**

{{< highlight java >}}

 // Ein Beispiel zur Unterstützung von 8-Bit-Photoshop-Dokument im LAB-Farbmodus.

String srcFile = "Untitled-1.psd";

String outputFilePsd = "output.psd";

// Lade eine vordefinierte 8-Bit-PSD im LAB-Farbmodus

PsdImage psdImage = (PsdImage)Image.load(srcFile);

try

{

    // Speichere eine Kopie der geladenen PSD

    psdImage.save(outputFilePsd);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}
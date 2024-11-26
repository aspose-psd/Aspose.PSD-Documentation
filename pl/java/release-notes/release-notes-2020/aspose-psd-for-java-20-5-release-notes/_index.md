---
title: Aspose.PSD dla Java 20.5 - Notatki dotyczące wydania
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-java-20-5-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDJAVA-188|Wsparcie dla postępu konwersji dokumentu|Funkcja|
|PSDJAVA-197|Wsparcie zapisu obrazu PSD w trybie kolorów odcieni szarości z 16 bitami na kanał|Funkcja|
|PSDJAVA-198|Wsparcie zasobu Nvrt (Zasób warstwy regulacji odwrócenia)|Funkcja|
|PSDJAVA-200|` `Wsparcie masek warstw dla grup warstw|Funkcja|
|PSDJAVA-195|Naprawa zapisu obrazu PSD w trybie kolorów odcieni szarości z 16 bitami na kanał do formatu PSD RGB z 16 bitami na kanał|Błąd|
|PSDJAVA-196|Naprawa zapisu obrazu PSD w trybie kolorów odcieni szarości z 16 bitami na kanał do 8 bitów na kanał w skali szarości|Błąd|
|PSDJAVA-199|Wyrównywanie tekstu przez ITextPortion nie działa dla języków zapisywanych od prawej do lewej. Plik wynikowy jest uszkodzony.|Błąd|
|PSDJAVA-201|Wyjątek podczas próby otwarcia określonego pliku Psd z kolorem Lab i 8 bitów na kanał|Błąd|
# **Zmiany w API publicznym**
# **Dodane API:**
- Brak
## **Usunięte API:**
- Brak
# **Przykłady użycia:**

**PSDJAVA-188. Wsparcie dla postępu konwersji dokumentu**

{{< highlight java >}}

 // Przykład użycia obsługi postępu operacji ładowania i zapisu.

// Program wykorzystuje różne opcje zapisywania, aby wywołać zdarzenia postępu.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Utwórz obsługę postępu, która zapisuje informacje o postępie w konsoli

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s z %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Ładowanie Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Dołącz obsługę postępu, aby pokazać postęp ładowania

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Załaduj PSD z określonymi opcjami ładowania

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Zapisywanie Apple.psd do formatu PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Utwórz obraz kolorowy i nieprzeźroczysty

    pngOptions.setColorType(PngColorType.Truecolor);

    // Dołącz obsługę postępu, aby pokazać postęp zapisywania

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Konwertuj PSD na PNG o określonych cechach

    image.save(outputStream, pngOptions);

    System.out.println("---------- Zapisywanie Apple.psd do formatu PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Utwórz obraz PSD kolorowy

    psdOptions.setColorMode(ColorModes.Rgb);

    // Ustaw kanał dla każdego koloru (czerwony, zielony i niebieski) plus kanał złożony

    psdOptions.setChannelsCount((short)4);

    // Dołącz obsługę postępu, aby pokazać postęp zapisywania

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Zapisz kopię PSD o określonych cechach

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Wsparcie zapisu obrazu PSD w trybie kolorów odcieni szarości z 16 bitami na kanał**

{{< highlight java >}}

 // Przykład zastosowania różnych kombinacji trybów kolorów, bitów na kanał, liczby kanałów i kompresji dla określonych warstw.

// Umożliwia metodę dostępną z lokalnego zakresu

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

        // Załaduj predefiniowany 16-bitowy obraz w skali szarości PSD

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Narysuj szary wewnętrzny obramowanie wokół obwodu warstwy

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Zapisz kopię PSD o określonych cechach

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

        // Załaduj zapisany PSD

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Konwertuj zapisany PSD na obraz PNG w odcieniach szarości

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // tutaj nie powinno być wyjątku

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

**PSDJAVA-198. Wsparcie zasobu Nvrt (Zasób warstwy regulacji odwrócenia)**

{{< highlight java >}}

 // Przykład znajdowania zasobu NvrtResource warstwy regulacji odwrócenia.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Załaduj predefiniowany PSD zawierający warstwę regulacji odwrócenia

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Spróbuj znaleźć zasób warstwy regulacji odwrócenia

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Znaleziono zasób NvrtResource

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

**PSDJAVA-200. Wsparcie masek warstw dla grup warstw**

{{< highlight java >}}

 // Przykład wspierania masek warstw dla grup warstw. Program ładuje i zapisuje obraz PSD

// do różnych formatów wyjściowych bez rzucania wyjątków.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Załaduj predefiniowany PSD zawierający maski warstw dla grup warstw

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Konwertuj załadowany PSD na PNG

    input.save(outputPng, new PngOptions());

    // Zapisz kopię PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Naprawa zapisu obrazu PSD w trybie kolorów odcieni szarości z 16 bitami na kanał do formatu PSD RGB z 16 bitami na kanał**

{{< highlight java >}}

 // Przykład konwersji 16-bitowego obrazu w skali szarości PSD na 16-bitowy RGB, a następnie z powrotem do

// 16-bitowego obrazu w skali szarości, ale jako obraz rastrowy.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Załaduj predefiniowany 16-bitowy obraz w skali szarości PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Narysuj szary wewnętrzny obramowanie wokół obwodu warstwy

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Zapisz kopię PSD zmieniając tryb kolorów na RBG

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

// Załaduj zapisany PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Konwertuj zapisany PSD na obraz PNG w odcieniach szarości

    image1.save(pngExportPath, pngOptions); // tutaj nie powinno być wyjątek

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Naprawa zapisu obrazu PSD w trybie kolorów odcieni szarości z 16 bitami na kanał do 8 bitów na kanał w skali szarości**

{{< highlight java >}}

 // Przykład konwersji 16-bitowego obrazu w skali szarości PSD na 8-bitowy obraz w skali szarości, a następnie na

// obraz w skali szarości o 8 bitach na kanał..

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Załaduj predefiniowany 16-bitowy obraz w skali szarości PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Narysuj szary wewnętrzny obramowanie wokół obwodu warstwy

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Zapisz kopię PSD z liczbą kanałów zmienioną na 8-bitową

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

// Załaduj zapisany PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Konwertuj zapisany PSD na obraz PNG w odcieniach szarości

    image1.save(pngExportPath, pngOptions); // tutaj nie powinno być wyjątek

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Wyrównywanie tekstu przez ITextPortion nie działa dla języków zapisywanych cez prawej do lewej. Plik wynikowy jest uszkodzony.**

{{< highlight java >}}

 // Przykład wyrównywania warstwy tekstu RTL przez ITextPortion. Program modyfikuje

// istniejącą warstwę tekstu RTL w załadowanym PSD i zapisuje kopię zmodyfikowanego dokumentu.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// Załaduj predefiniowany PSD zawierający warstwę tekstu RTL

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // Pobierz fragmenty tekstu z warstwy

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // Zmień wyrównanie tekstu

    portions[0].getParagraph().setJustification(2);

    // Zastosuj zmiany do warstwy

    layer.getTextData().updateLayerData();

    // Zapisz zmodyfikowaną kopię PSD

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Wyjątek podczas próby otwarcia określonego pliku Psd z kolorem LAB i 8 bitami na kanał**

{{< highlight java >}}

 // Przykład obsługi 8-bitowego dokumentu Photoshopa w trybie kolorów LAB.

String srcFile = "Untitled-1.psd";

String
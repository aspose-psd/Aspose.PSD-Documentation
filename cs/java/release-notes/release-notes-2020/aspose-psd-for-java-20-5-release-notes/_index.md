---
title: Aspose.PSD pro Java 20.5 - Poznámky k vydání
type: docs
weight: 40
url: /cs/aspose-psd-pro-java-20-5-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-188|Podpora pro pokrok konverze dokumentu|Funkce|
|PSDJAVA-197|Podpora ukládání obrázků v režimu šedé stupnice s 16 bity na kanál|Funkce|
|PSDJAVA-198|Podpora zdroje Nvrt (Vrstva úprav invertování zdroje)|Funkce|
|PSDJAVA-200|Podpora maskování vrstev pro skupiny vrstev|Funkce|
|PSDJAVA-195|Oprava ukládání obrázku PSD ve šedé stupnici se 16 bity na kanál do formátu RGB PSD se 16 bity na kanál|Chyba|
|PSDJAVA-196|Oprava ukládání obrázku PSD ve šedé stupnici s 16 bity na kanál do šedé stupnice PSD s 8 bity na kanál|Chyba|
|PSDJAVA-199|Zarovnání textu pomocí ITextPortion nepracuje pro pravácké jazyky. Výstupní soubor je poškozen.|Chyba|
|PSDJAVA-201|Výjimka při pokusu o otevření konkrétního souboru Psd s Lab Color a 8 bit/kanál|Chyba|
# **Změny ve veřejném API**
# **Přidaná API:**
- žádné
## **Odstraněná API:**
- žádné
# **Příklady použití:**

**PSDJAVA-188. Podpora pro pokrok konverze dokumentu**

{{< highlight java >}}

 // Příklad použití pokročilého manipulátoru pro načítání a ukládání operací.

// Program používá různé možnosti ukládání pro spuštění pokrokových událostí.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Vytvoření pokrokového manipulátoru, který zapisuje informace o pokroku do konzole

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

System.out.println("---------- Načítání Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Přiřazení pokrokového manipulátoru k zobrazení pokroku načítání

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Načtěte PSD pomocí konkrétních možností načítání

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Ukládání Apple.psd do formátu PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Udělejte výstupní obrázek barevný a neprůhledný

    pngOptions.setColorType(PngColorType.Truecolor);

    // Přiřaďte pokrokový manipulátor k zobrazení pokroku ukládání

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Konvertujte PSD do PNG s konkrétními vlastnostmi

    image.save(outputStream, pngOptions);

    System.out.println("---------- Ukládání Apple.psd do formátu PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Udělejte výstupní PSD barevný

    psdOptions.setColorMode(ColorModes.Rgb);

    // Nastavte kanál pro každou barvu (červenou, zelenou a modrou) plus složený kanál

    psdOptions.setChannelsCount((short)4);

    // Přiřaďte pokrokový manipulátor k zobrazení pokroku ukládání

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Uložte kopii PSD s konkrétními vlastnostmi

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Podpora ukládání obrázků v režimu šedé stupnice s 16 bity na kanál**

{{< highlight java >}}

 // Příklad aplikace různých kombinací barevných režimů, bitů na kanál, počtů kanálů a kompresí pro určité vrstvy.

// Make a method be accessible from the local scope

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

        // Load a predefined 16-bit grayscale PSD

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Draw a gray inner border around the perimeter of the layer

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Save a copy of PSD with specific characteristics

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

        // Load the saved PSD

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Convert the saved PSD to a grayscale PNG image

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // here should be no exception

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

**PSDJAVA-198. Podpora zdroje Nvrt (Vrstva úprav invertování zdroje)**

{{< highlight java >}}

 // Příklad nalezení zdroje NvrtResource invertovací vrstvy úprav.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Načtěte předdefinované PSD obsahující invertovací vrstvu úprav

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Pokus o nalezení zdroje invertovací vrstvy úprav

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Zdroj NvrtResource je nalezen

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

**PSDJAVA-200. Podpora maskování vrstev pro skupiny vrstev**

{{< highlight java >}}

 // Příklad podpory maskování vrstev pro skupiny vrstev. Program načítá a ukládá PSD k různým výstupním formátům bez vyvolání výjimky.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Načtěte předdefinované PSD obsahující masky vrstev pro skupiny vrstev

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Konvertujte načtené PSD do PNG

    input.save(outputPng, new PngOptions());

    // Uložte kopii PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Oprava ukládání obrázku PSD ve šedé stupnici se 16 bity na kanál do formátu RGB PSD se 16 bity na kanál**

{{< highlight java >}}

 // Příklad převodu 16bitové šedé stupnice PSD na 16bitovou RGB a zpět na

// 16bitovou šedou, ale rastrový obrázek.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Načte předdefinovaný 16bitový šedý PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Vykreslení šedého vnitřního okraje kolem obvodu vrstvy

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Uložte kopii PSD s režimem barev změněným na RBG

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

// Načte uložené PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Převede uložený PSD na šedý obrázek PNG

    image1.save(pngExportPath, pngOptions); // zde by neměla být žádná výjimka

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Oprava ukládání obrázku PSD ve šedé stupnici s 16 bity na kanál do šedé stupnice PSD s 8 bity na kanál**

{{< highlight java >}}

 // Příklad převodu 16bitové šedé stupnice PSD na 8bitovou šedou a pak na

// 8bitový šedý rastrový obrázek.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Načtěte předdefinovaný 16bitový šedý PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Vykreslení šedého vnitřního okraje kolem obvodu vrstvy

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Uložte kopii PSD s počtem kanálů změněným na 8 bitů

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

// Načte uložené PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Převede uložený PSD na šedý obrázek PNG

    image1.save(pngExportPath, pngOptions); // zde by neměla být žádná výjimka

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Zarovnání textu pomocí ITextPortion nepodporuje pravácké jazyky. Výstupní soubor je poškozen.**

{{< highlight java >}}

 // Příklad zarovnání RTL textové vrstvy pomocí ITextPortion. Program modifikuje

// existující RTL textovou vrstvu v načteném PSD a uloží kopii upraveného dokumentu.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// Načte předdefinované PSD obsahující RTL textovou vrstvu

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // Získejte textové části z vrstvy

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // Změňte zarovnání textu

    portions[0].getParagraph().setJustification(2);

    // Aplikujte změny na vrstvu

    layer.getTextData().updateLayerData();

    // Uložte upravenou kopii PSD

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Výjimka při pokusu o otevření konkrétního souboru Psd s Lab Color a 8 bit/kanál**

{{< highlight java >}}

 // Příklad podpory 8bit
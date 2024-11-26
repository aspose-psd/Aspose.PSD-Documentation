---
title: Aspose.PSD voor Java 20.5 - Release-opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-20-5-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Belangrijk**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDJAVA-188|Ondersteuning voor voortgang van documentconversie|Functie|
|PSDJAVA-197|Ondersteuning van Grayscale ColorMode PSD-afbeelding opslaan met 16 bit per kanaal|Functie|
|PSDJAVA-198|Ondersteuning van Nvrt Resource (Invert Adjustment Layer Resource)|Functie|
|PSDJAVA-200|Ondersteuning van Laagemaskers voor Laaggroepen|Functie|
|PSDJAVA-195|Fout bij het opslaan van PSD-afbeelding met Grayscale ColorMode van 16 bit per kanaal naar 16-bits per kanaal RGB PSD-indeling|Fout|
|PSDJAVA-196|Fout bij het opslaan van PSD-afbeelding met Grayscale ColorMode van 16 bit per kanaal naar 8 bit per kanaal Grayscale PSD-indeling|Fout|
|PSDJAVA-199|Tekstuitlijning via ITextPortion werkt niet voor recht-naar-links talen. Het uitvoerbestand is beschadigd.|Fout|
|PSDJAVA-201|Uitzondering bij het proberen te openen van een specifiek Psd-bestand met Lab Color en 8 bit/kanaal|Fout|
# **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- Geen
## **Verwijderde API's:**
- Geen
# **Gebruik voorbeelden:**

**PSDJAVA-188. Ondersteuning voor documentconversievoortgang**

{{< highlight java >}}

 // Een voorbeeld van het gebruik van de voortgangshandler voor laad- en opslaagressies.

// Het programma gebruikt verschillende opslagopties om voortgangsgebeurtenissen te activeren.

String bronBestandspad = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Maak een voortgangshandler die voortgangsinformatie naar de console schrijft

ProgressEventHandler lokaleVoortgangsEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo voortgangsInfo)

    {

        String bericht = String.format(

                "%s %s: %s van %s",

                voortgangsInfo.getOmschrijving(),

                Enum.getName(EventType.class, voortgangsInfo.getGebeurtenisType()),

                voortgangsInfo.getWaarde(),

                voortgangsInfo.getMaximaleWaarde());

        System.out.println(bericht);

    }

};

System.out.println("---------- Laden Apple.psd ----------");

PsdLoadOptions laadOpties = new PsdLoadOptions();

// Koppel de voortgangshandler om de laadvoortgang te tonen

laadOpties.setProgressEventHandler(lokaleVoortgangsEventHandler);

// Laad PSD met specifieke laadopties

PsdImage afbeelding = (PsdImage)Image.load(bronBestandspad, laadOpties);

try

{

    System.out.println("---------- Opslaan Apple.psd naar PNG-indeling ----------");

    PngOptions pngOpties = new PngOptions();

    // Maak de uitvoerafbeelding gekleurd en niet-transparant

    pngOpties.setColorType(PngColorType.Truecolor);

    // Koppel de voortgangshandler om de opslagvoortgang te tonen

    pngOpties.setProgressEventHandler(lokaleVoortgangsEventHandler);

    // Converteer PSD naar PNG met specifieke kenmerken

    afbeelding.save(outputStream, pngOpties);

    System.out.println("---------- Opslaan Apple.psd naar PSD-indeling ----------");

    PsdOptions psdOpties = new PsdOptions();

    // Maak de uitvoer-PSD gekleurd

    psdOpties.setColorMode(ColorModes.Rgb);

    // Stel een kanaal in voor elke kleur (rood, groen en blauw) plus een samengesteld kanaal

    psdOpties.setChannelsCount((short)4);

    // Koppel de voortgangshandler om de opslagvoortgang te tonen

    psdOpties.setProgressEventHandler(lokaleVoortgangsEventHandler);

    // Sla een kopie van PSD op met specifieke kenmerken

    afbeelding.save(outputStream, psdOpties);

}

finally

{

    afbeelding.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Ondersteuning van Grayscale ColorMode PSD-afbeelding opslaan met 16 bit per kanaal**

{{< highlight java >}}

 // Een voorbeeld van het toepassen van verschillende combinaties van kleurmodi, bits per kanaal, kanalen

// telt en compressies voor specifieke lagen.

// Maak een methode toegankelijk vanuit de lokale scope

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String bestand,

            short kleurModus,

            short kanaalBitsTellen,

            short kanalenTellen,

            short compressie,

            int laagNummer)

    {

        String bestandsPad = bestand + ".psd";

        String postfix = Enum.getName(ColorModes.class, kleurModus) + kanaalBitsTellen + "_" +

                kanalenTellen + "_" + Enum.getName(CompressionMethod.class, compressie);

        String exportPad = bestand + postfix + ".psd";

        String pngExportPad = bestand + postfix + ".png";

        // Laad een vooraf gedefinieerde 16-bits grijstinten PSD

        PsdImage afbeelding = (PsdImage)Image.load(bestandsPad);

        try

        {

            RasterCachedImage raster = laagNummer >= 0 ? afbeelding.getLayers()[laagNummer] : afbeelding;

            // Teken een grijze binnenrand rond de omtrek van de laag

            Graphics graphics = new Graphics(raster);

            int breedte = raster.getWidth();

            int hoogte = raster.getHeight();

            Rechthoek rechthoek = nieuwe Rechthoek(

                    breedte / 3,

                    hoogte / 3,

                    breedte - (2 * (breedte / 3)) - 1,

                    hoogte - (2 * (hoogte / 3)) - 1);

            graphics.tekenRechthoek(new Pen(Color.getDarkGray(), 1), rechthoek);

            // Sla een kopie van PSD op met specifieke kenmerken

            PsdOpties psdOpties = new PsdOpties();

            psdOpties.setColorMode(kleurModus);

            psdOpties.setChannelBitsCount(kanaalBitsTellen);

            psdOpties.setChannelsCount(kanalenTellen);

            psdOpties.setCompressionMethod(compressie);

            afbeelding.save(exportPad, psdOpties);

        }

        finally

        {

            afbeelding.dispose();

        }

        // Laad de opgeslagen PSD

        PsdImage afbeelding1 = (PsdImage)Image.load(exportPad);

        try

        {

            // Converteer de opgeslagen PSD naar een grijstinten PNG-afbeelding

            PngOpties pngOpties = nieuwe PngOpties();

            pngOpties.setColorType(PngColorType.GrayscaleWithAlpha);

            afbeelding1.save(pngExportPad, pngOpties); // hier mag geen uitzondering zijn

        }

        finally

        {

            afbeelding1.dispose();

        }

    }

}

LocalScopeExtension $ = nieuwe LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grijstinten5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_geen_lagen", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_geen_lagen", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_geen_lagen", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Ondersteuning van Nvrt Resource (Invert Adjustment Layer Resource)**

{{< highlight java >}}

 // Een voorbeeld van het vinden van NvrtResource van een omgekeerde aanpassingslaag.

String inPsdBestandspad = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Laad een vooraf gedefinieerde PSD die een omgekeerde aanpassingslaag bevat

PsdImage psdAfbeelding = (PsdImage)Image.load(inPsdBestandspad);

try

{

    // Probeer een resource van de omgekeerde aanpassingslaag te vinden

    for (Laag laag : psdAfbeelding.getLayers())

    {

        als (laag instanceof InvertAdjustmentLayer)

        {

            voor (LaagResource laagResource : laag.getResources())

            {

                als (laagResource instanceof NvrtResource)

                {

                    // De NvrtResource is gevonden

                    nvrtResource = (NvrtResource)laagResource;

                    doorbreken;

                }

            }

        }

    }

}

finally

{

    psdAfbeelding.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Ondersteuning van Laagemaskers voor Laaggroepen**

{{< highlight java >}}

 // Een voorbeeld van ondersteuning van laagemaskers voor laaggroepen. Het programma laadt en slaat PSD op

// naar verschillende uitvoerindelingen zonder uitzonderingen te genereren.

String bronBestand = "psdnet595.psd";

String uitvoerPng = "uitvoer.png";

String uitvoerPsd = "uitvoer.psd";

// Laad een vooraf gedefinieerde PSD die laagemaskers bevat voor laaggroepen

PsdImage invoer = (PsdImage)Image.load(bronBestand);

try

{

    // Converteer geladen PSD naar PNG

    invoer.save(uitvoerPng, nieuwe PngOpties());

    // Sla een kopie van de PSD op

    invoer.save(uitvoerPsd);

}

finally

{

    invoer.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Fout bij het opslaan van PSD-afbeelding met Grayscale ColorMode 16bit per kanaal naar 16bit per kanaal RGB PSD-indeling**

{{< highlight java >}}

 // Een voorbeeld van het omzetten van een 16-bits grijsschaal PSD naar een 16-bits RGB PSD en vervolgens terug

// naar 16-bits grijsschaal maar een rasterafbeelding.

String bronBestandspad = "grijstinten5x5.psd";

String exportBestandspad = "rgb16bit5x5_output.psd";

String pngExportPad = "rgb16bit5x5_output.png";

// Laad een vooraf gedefinieerde 16-bits grijsschaal PSD

PsdImage afbeelding = (PsdImage)Image.load(bronBestandspad);

try

{

    RasterCachedImage raster = afbeelding.getLayers()[0];

    // Teken een grijze binnenrand rond de omtrek van de laag

    Graphics graphics = new Graphics(raster);

    int breedte = raster.getWidth();

    int hoogte = raster.getHeight();

    Rechthoek rechthoek = nieuwe Rechthoek(breedte / 3, hoogte / 3, breedte - (2 * (breedte / 3)) - 1, hoogte - (2 * (hoogte / 3)) - 1);

    graphics.tekenRechthoek(new Pen(Color.getDarkGray(), 1), rechthoek);

    // Sla een kopie van PSD op met de kleurmodus gewijzigd naar RBG

    PsdOpties psdOpties = nieuwe PsdOpties();

    psdOpties.setColorMode(ColorModes.Rgb);

    psdOpties.setChannelBitsCount((short)16);

    psdOpties.setChannelsCount((short)4);

    afbeelding.save(exportBestandspad, psdOpties);

}

finally

{

    afbeelding.dispose();

}

// Laad de opgeslagen PSD

PsdImage afbeelding1 = (PsdImage)Image.load(exportBestandspad);

try

{

    PngOpties pngOpties = nieuwe PngOpties();

    pngOpties.setColorType(PngColorType.GrayscaleWithAlpha);

    // Converteer de opgeslagen PSD naar een grijsschaal PNG-afbeelding

    afbeelding1.save(pngExportPad, pngOpties); // hier mag geen uitzondering zijn

}

finally

{

    afbeelding1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Fout bij het opslaan van PSD-afbeelding met Grayscale ColorMode 16bit per kanaal naar 8 bit per kanaal Grayscale PSD-indeling**

{{< highlight java >}}

 // Een voorbeeld van het omzetten van een 16-bits grijsschaal PSD naar een 8-bits grijsschaal en vervolgens naar

// een 8-bits grijsschaal rasterafbeelding.

String bronBestandspad = "grijsschaal16bit.psd";

String exportBestandspad = "grijsschaal16bit_output.psd";

String pngExportPad = "grijsschaal16bit_output.png";

// Laad een vooraf gedefinieerde 16-bits grijsschaal PSD

PsdImage afbeelding = (PsdImage)Image.load(bronBestandspad);

try

{

    RasterCachedImage raster = afbeelding.getLayers()[0];

    // Teken een grijze binnenrand rond de omtrek van de laag

    Graphics graphics = new Graphics(raster);

    int breedte = raster.getWidth();

    int hoogte = raster.getHeight();

    Rechthoek rechthoek = nieuwe Rechthoek(breedte / 3, hoogte / 3, breedte - (2 * (breedte / 3)) - 1, hoogte - (2 * (hoogte / 3)) - 1);

    graphics.tekenRechthoek(new Pen(Color.getDarkGray(), 1), rechthoek);

    // Sla een kopie van PSD op met het kanaalaantal gewijzigd naar 8-bits

    PsdOpties psdOpties = nieuwe PsdOpties();

    psdOpties.setColorMode(ColorModes.Grayscale);

    psdOpties.setChannelBitsCount((short)8);

    psdOpties.setChannelsCount((short)2);

    afbeelding.save(exportBestandspad, psdOpties);

}

finally

{

    afbeelding.dispose();

}

// Laad de opgeslagen PSD

PsdImage afbeelding1 = (PsdImage)Image.load(exportBestandspad);

try

{

    PngOpties pngOpties = nieuwe PngOpties();

    pngOpties.setColorType(PngColorType.GrayscaleWithAlpha);

    // Converteer de opgeslagen PSD naar een grijsschaal PNG-afbeelding

    afbeelding1.save(pngExportPad, pngOpties); // hier mag geen uitzondering zijn

}

finally

{

    afbeelding1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Tekstuitlijning via ITextPortion werkt niet voor recht-naar-links talen. Het uitvoerbestand is beschadigd.**

{{< highlight java >}}

 // Een voorbeeld van het uitlijnen van RTL-tekstlaag via ITextPortion. Het programma wijzigt

// een bestaande RTL-tekstlaag in geladen PSD en slaat een kopie van het gewijzigde document op.

String bronBestandsnaam = "bidi.psd";

String uitvoerBestandsnaam = "bidiOutput.psd";

// Laad een vooraf gedefinieerde PSD met een RTL-tekstlaag

PsdImage afbeelding = (PsdImage
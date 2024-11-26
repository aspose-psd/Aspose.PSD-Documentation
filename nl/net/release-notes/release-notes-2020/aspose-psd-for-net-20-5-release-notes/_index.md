---
title: Aspose.PSD voor .NET 20.5 - Release-opmerkingen
type: docs
weight: 80
url: /nl/net/aspose-psd-voor-net-20-5-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-595|Ondersteuning van laagmaskers voor laaggroepen|Functie|
|PSDNET-201|Ondersteuning voor voortgang van documentconversie|Functie|
|PSDNET-275|Ondersteuning van Nvrt Resource (Invert Adjustment Layer Resource)|Functie|
|PSDNET-124|Ondersteuning van het opslaan van PSD-afbeelding met Grayscale ColorMode met 16 bit per kanaal|Functie|
|PSDNET-589|Refactorisatie van voorbeelden op GitHub|Verbetering|
|PSDNET-587|Tekstuitlijning via ITextPortion werkt niet voor rechts-naar-links talen. Het uitvoerbestand is beschadigd.|Fout|
|PSDNET-604|Uitzondering bij het proberen te openen van een bepaald Psd-bestand met Lab Color en 8 bit/kanaal|Fout|
|PSDNET-598|Probleem opgelost bij het opslaan van PSD-afbeelding met Grayscale ColorMode 16 bit per kanaal naar 8 bit per kanaal Grayscale PSD-formaat|Fout|
|PSDNET-599|Probleem opgelost bij het opslaan van PSD-afbeelding met Grayscale ColorMode 16 bit per kanaal naar 16-bit per kanaal RGB PSD-formaat|Fout|

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- Geen
# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**
**PSDNET-595. Ondersteuning van laagmaskers voor laaggroepen**

{{< highlight java >}}

 string srcBestand = "psdnet595.psd";

string uitvoerPng = "uitvoer.png";

string uitvoerPsd = "uitvoer.psd";

using (var invoer = (PsdImage)Image.Load(srcBestand))

{

     invoer.Save(uitvoerPng, new PngOptions());

     invoer.Save(uitvoerPsd);

}

{{< /highlight >}}

**PSDNET-201. Ondersteuning voor voortgang van documentconversie**

{{< highlight java >}}

 string bronBestandsPad = "Apple.psd";

Stream uitvoerstroom = new MemoryStream();

ProgressEventHandler lokaleProgressEventHandler = delegate(ProgressEventHandlerInfo voortgangsInfo)

{

      string boodschap = string.Format(

           "{0} {1}: {2} van {3}",

           voortgangsInfo.Beschrijving,

           voortgangsInfo.GebeurtenisType,

           voortgangsInfo.Waarde,

           voortgangsInfo.MaxWaarde);

      Console.WriteLine(boodschap);

};

Console.WriteLine("---------- Laden van Apple.psd ----------");

var laadOpties = new PsdLoadOptions() { ProgressEventHandler = lokaleProgressEventHandler };

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsPad, laadOpties))

{

      Console.WriteLine("---------- Opslaan van Apple.psd naar PNG-formaat ----------");

      afbeelding.Save(

           uitvoerstroom,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = lokaleProgressEventHandler

           });

      Console.WriteLine("---------- Opslaan van Apple.psd naar PSD-formaat ----------");

      afbeelding.Save(

           uitvoerstroom,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = lokaleProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-275. Ondersteuning van Nvrt Resource (Invert Adjustment Layer Resource)**

{{< highlight java >}}

 using (var psdAfbeelding = (PsdImage)Image.Load("InvertAdjustmentLayer.psd"))

{

      foreach (var laag in psdAfbeelding.Layers)

      {

           if (laag is InvertAdjustmentLayer)

           {

                 foreach (var laagResource in laag.Resources)

                 {

                      if (laagResource is NvrtResource)

                      {

                           // De NvrtResource wordt ondersteund.

                           var resource = (NvrtResource)laagResource;

                           break;

                      }

                 }

           }

      }

}

{{< /highlight >}}

**PSDNET-124. Probleem opgelost bij het opslaan van PSD-afbeelding met Grayscale ColorMode 16 bit per kanaal naar 8 bit per kanaal Grayscale PSD-formaat**

{{< highlight java >}}

 void OpslaanNaarPsdDanLadenEnOpslaanNaarPng(

    string bestand,

    ColorModes kleurModus,

    korte kanaalBitsTelling,

    korte kanalenTelling,

    CompressieMethode compressie,

    int laagNummer)

{

    string bestandPad = bestand + ".psd";

    string achtervoegsel = kleurModus.ToString() + kanaalBitsTelling + "_" + kanalenTelling + "_" + compressie;

    string exportPad = @"Uitvoer\" + bestand + achtervoegsel + ".psd";

    PsdOptions psdOpties = new PsdOptions()

    {

        ColorMode = kleurModus,

        ChannelBitsCount = kanaalBitsTelling,

        ChannelsCount = kanalenTelling,

        CompressionMethod = compressie

    };

    using (PsdImage afbeelding = (PsdImage)Image.Load(bestandPad))

    {

        RasterCachedImage raster = laagNummer >= 0 ? (RasterCachedImage)afbeelding.Layers[laagNummer] : afbeelding;

        Aspose.PSD.Graphics graphics = new Graphics(raster);

        int breedte = raster.Breedte;

        int hoogte = raster.Hoogte;

        Rechthoek rechthoek = nieuwe Rechthoek(

            breedte / 3,

            hoogte / 3,

            breedte - (2 * (breedte / 3)) - 1,

            hoogte - (2 * (hoogte / 3)) - 1);

        graphics.TrekRechthoek(nieuwe Aspose.PSD.Pen(Kleur.DonkerGrijs, 1), rechthoek);

        afbeelding.Save(exportPad, psdOpties);

    }

    string pngExportPad = Path.ChangeExtension(exportPad, "png");

    using (PsdImage afbeelding = (PsdImage)Image.Load(exportPad))

    {

        // Hier mag geen uitzondering zijn.

        afbeelding.Save(pngExportPad, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

    }

}

OpslaanNaarPsdDanLadenEnOpslaanNaarPng("grayscale5x5", ColorModes.Cmyk, 16, 5, CompressionMethod.RLE, 0);

OpslaanNaarPsdDanLadenEnOpslaanNaarPng("argb16bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

OpslaanNaarPsdDanLadenEnOpslaanNaarPng("argb16bit_5x5_geen_lagen", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

OpslaanNaarPsdDanLadenEnOpslaanNaarPng("argb8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, 0);

OpslaanNaarPsdDanLadenEnOpslaanNaarPng("argb8bit_5x5_geen_lagen", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

OpslaanNaarPsdDanLadenEnOpslaanNaarPng("cmyk16bit_5x5_geen_lagen", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

OpslaanNaarPsdDanLadenEnOpslaanNaarPng("index8bit_5x5", ColorModes.Grayscale, 16, 2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDNET-587. Tekstuitlijning via ITextPortion werkt niet voor rechts-naar-links talen. Het uitvoerbestand is beschadigd.**

{{< highlight java >}}

 string bronBestandsNaam = "bidi.psd";

string uitvoerBestandsNaam = "bidiUitvoer.psd";

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsNaam))

{

    var laag = (TextLayer)afbeelding.Layers[2];

    var delen = laag.TextData.Items;

    delen[0].Paragraaf.Uitlijning = 2;

    laag.TextData.UpdateLayerData();

    afbeelding.Save(uitvoerBestandsNaam);

}

{{< /highlight >}}

` `**PSDNET-604. Uitzondering bij het proberen te openen van een bepaald Psd-bestand met Lab Color en 8 bit/kanaal**

{{< highlight java >}}

 string bronBestand = "Untitled-1.psd";

string uitvoerBestandPsd = "uitvoer.psd";

using (var psdAfbeelding = (PsdImage)Image.Load(bronBestand))

{

    psdAfbeelding.Save(uitvoerBestandPsd);

}

// LAB-bestand geladen en opgeslagen zonder uitzonderingen te gooien.

{{< /highlight >}}

**PSDNET-598. Probleem opgelost bij het opslaan van PSD-afbeelding met Grayscale ColorMode 16 bit per kanaal naar 8 bit per kanaal Grayscale PSD-formaat**

{{< highlight java >}}

 string bronBestandsNaam = "grayscale16bit.psd";

string exportBestandsNaam = "grayscale16bit_uitvoer.psd";

PsdOptions psdOpties = new PsdOptions()

{

    ColorMode = ColorModes.Grayscale,

    ChannelBitsCount = 8,

    ChannelsCount = 2

};

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsNaam))

{

    RasterCachedImage raster = afbeelding.Layers[0];

    Aspose.PSD.Graphics graphics = new Graphics(raster);

    int breedte = raster.Breedte;

    int hoogte = raster.Hoogte;

    Rechthoek rechthoek = nieuwe Rechthoek(breedte / 3, hoogte / 3, breedte - (2 * (breedte / 3)) - 1, hoogte - (2 * (hoogte / 3)) - 1);

    graphics.TrekRechthoek(nieuwe Aspose.PSD.Pen(Kleur.DonkerGrijs, 1), rechthoek);

    afbeelding.Save(exportBestandsNaam, psdOpties);

}

string pngExportPad = Path.ChangeExtension(exportBestandsNaam, "png");

using (PsdImage afbeelding = (PsdImage)Image.Load(exportBestandsNaam))

{

    // Hier mag geen uitzondering zijn.

    afbeelding.Save(pngExportPad, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}

**PSDNET-599. Probleem opgelost bij het opslaan van PSD-afbeelding met Grayscale ColorMode 16 bit per kanaal naar 16-bit per kanaal RGB PSD-formaat**

{{< highlight java >}}

 string bronBestandsNaam = "grayscale16bit.psd";

string exportBestandsNaam = "grayscale16bit_uitvoer.psd";

PsdOptions psdOpties = new PsdOptions()

{

    ColorMode = ColorModes.Rgb,

    ChannelBitsCount = 8,

    ChannelsCount = 4

};

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsNaam))

{

    RasterCachedImage raster = afbeelding.Layers[0];

    Aspose.PSD.Graphics graphics = new Graphics(raster);

    int breedte = raster.Breedte;

    int hoogte = raster.Hoogte;

    Rechthoek rechthoek = nieuwe Rechthoek(breedte / 3, hoogte / 3, breedte - (2 * (breedte / 3)) - 1, hoogte - (2 * (hoogte / 3)) - 1);

    graphics.TrekRechthoek(nieuwe Aspose.PSD.Pen(Kleur.DonkerGrijs, 1), rechthoek);

    afbeelding.Save(exportBestandsNaam, psdOpties);

}

string pngExportPad = Path.ChangeExtension(exportBestandsNaam, "png");

using (PsdImage afbeelding = (PsdImage)Image.Load(exportBestandsNaam))

{

    // Hier mag geen uitzondering zijn.

    afbeelding.Save(pngExportPad, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });

}

{{< /highlight >}}

---
title: Aspose.PSD voor .NET 19.4 - Release-opmerkingen
type: docs
weight: 90
url: /nl/net/aspose-psd-for-net-19-4-release-notes/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor Aspose.PSD voor .NET 19.4.

{{% /alert %}} 

|**Belangrijk**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-87|Voeg functie toe om JPEG/PNG/etc afbeeldingsbestanden naar PsdImage te laden zonder direct laden (wat niet ondersteund wordt in Aspose.PSD)|Functie|
|PSDNET-120|Ondersteuning van RGB-kleurmodus met 16 bits/kanaal (64 bits per kleur)|Functie|
|PSDNET-108|Ondersteuning van Laag Vectormaskers en Tekstlaag Aangepaste FlipRotate|Functie|
|PSDNET-99|Alle Aziatische tekens worden niet correct weergegeven|Fout|
|PSDNET-116|\r\n symbolen worden geïnterpreteerd als dubbele regelovergang, wat onjuist is|Fout|
|PSDNET-117|Als TextLayer wordt bijgewerkt met een tekenreeks die LineBreaks bevat, wordt het PSD-bestand onleesbaar|Fout|
|PSDNET-118|Als TextLayer wordt bijgewerkt met een tekenreeks die tab-symbolen bevat, mislukt de verwerking met een uitzondering|Fout|

## **Wijzigingen in Openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
# **Verwijderde API's:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.Bestandsformaat
- P:Aspose.PSD.FileFormats.Gif.GifImage.Xmp-gegevens
- P:Aspose.PSD.FileFormats.Gif.GifImage.HeeftTrailer
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsPaletGesorteerd
- P:Aspose.PSD.FileFormats.Gif.GifImage.PaletKleurresolutiebits
- P:Aspose.PSD.FileFormats.Gif.GifImage.Breedte
- P:Aspose.PSD.FileFormats.Gif.GifImage.Hoogte
- P:Aspose.PSD.FileFormats.Gif.GifImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Gif.GifImage.Blokken
- P:Aspose.PSD.FileFormats.Gif.GifImage.ActieveFrame
- P:Aspose.PSD.FileFormats.Gif.GifImage.AchtergrondKleur
- P:Aspose.PSD.FileFormats.Gif.GifImage.AchtergrondKleurIndex
- P:Aspose.PSD.FileFormats.Gif.GifImage.PixelAspectVerhouding
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsGecached
- P:Aspose.PSD.FileFormats.Gif.GifImage.HeeftTransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.TransparenteKleur
- P:Aspose.PSD.FileFormats.Gif.GifImage.HeeftAchtergrondKleur
- P:Aspose.PSD.FileFormats.Gif.GifImage.AfbeeldingDoorzichtigheid
- M:Aspose.PSD.FileFormats.Gif.GifImage.Vervager(Aspose.PSD.DitheringMethode,Systeem.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.CachedGegevens
- M:Aspose.PSD.FileFormats.Gif.GifImage.RoteerFlipAllemaal(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Blokvolgorde
- M:Aspose.PSD.FileFormats.Gif.GifImage.LeegBlokken
- M:Aspose.PSD.FileFormats.Gif.GifImage.VoegBlokIn(System.Int32,Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.VoegBlokToe(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.VerkrijgBlok(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RoteerFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Roteer(System.Float,System.Boolean,Aspose.PSD.Kleur)
- M:Aspose.PSD.FileFormats.Gif.GifImage.FormaatWijzigen(Systeem.Int32,Systeem.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.FormaatWijzigen(Systeem.Int32,Systeem.Int32,Aspose.PSD.ImageFormaatInstellingen)
- M:Aspose.PSD.FileFormats.Gif.GifImage.FormaatWijzigenProportioneel(Systeem.Int32,Systeem.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Uitsnede(Aspose.PSD.Rechthoek)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Grijsschaal
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinariseerVast(Systeem.Byte)
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinariseerOtsu
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinariseerBradley(Systeem.Dubbel)
- M:Aspose.PSD.FileFormats.Gif.GifImage.PasHelderheidAan(Systeem.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.PasContrastAan(Systeem.Enkelvoudig)
- M:Aspose.PSD.FileFormats.Gif.GifImage.PasGammaAan(Systeem.Enkelvoudig,Systeem.Enkelvoudig,Systeem.Enkelvoudig)
- M:Aspose.PSD.FileFormats.Gif.GifImage.PasGammaAan(Systeem.Enkelvoudig)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Filter(Aspose.PSD.Rechthoeksgebied,Aspose.PSD.Afbeeldingsfilters.FilterOpties.FilterOptiesBasis)
- M:Aspose.PSD.FileFormats.Gif.GifImage.VervangKleur(Systeem.Int32,Systeem.Byte,Systeem.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.VervangNietTransparanteKleuren(Systeem.Int32)
- T:Aspose.PSD.FileFormats.Tiff.TiffImage
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinariseerBradley(Systeem.Dubbel,Systeem.Int32)
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HeeftAlpha
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HeeftTransparentColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Bestandsformaat
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.VoormultipliceerComponenten
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Bytevolgorde
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HorizontaleResolutie
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.VerticaleResolutie
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.AchtergrondKleur
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BitsPerPiksel
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ActieveFrame
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Frames
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Hoogte
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Breedte
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.IsGecached
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Exif-gegevens
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.AfbeeldingDoorzichtigheid
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Xmp-gegevens
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResolutiesUitlijnen
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Vervager(Aspose.PSD.DitheringMethode,Systeem.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.StelResolutieIn(Systeem.Dubbel,Systeem.Dubbel)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.GecachteGegevens
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RoteerFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RoteerFlipAllemaal(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Roteer(System.Float,System.Boolean,Aspose.PSD.Kleur)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VoegFrameToe(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VoegToe(Aspose.PSD.FileFormats.Tiff.TiffImage)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VoegFramesToe(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VoegFrameIn(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VerwijderFrame(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VerwijderFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.FormaatWijzigen(Systeem.Int32,Systeem.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.FormaatWijzigen(Systeem.Int32,Systeem.Int32,Aspose.PSD.ImageFormaatInstellingen)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.FormaatWijzigenBreedteProportioneel(Systeem.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.FormaatWijzigenHoogteProportioneel(Systeem.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.FormaatWijzigenProportioneel(Systeem.Int32,Systeem.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Uitsnede(Aspose.PSD.Rechthoek)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Grijsschaal
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinariseerVast(Systeem.Byte)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinariseerOtsu
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinariseerBradley(Systeem.Dubbel)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Uitsnede(Systeem.Int32,Systeem.Int32,Systeem.Int32,Systeem.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.PasHelderheidAan(Systeem.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.PasContrastAan(Systeem.Enkelvoudig)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.PasGammaAan(Systeem.Enkelvoudig,Systeem.Enkelvoudig,Systeem.Enkelvoudig)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.PasGammaAan(Systeem.Enkelvoudig)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Filter(Aspose.PSD.Rechthoeksgebied,Aspose.PSD.Afbeeldingsfilters.FilterOpties.FilterOptiesBasis)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VervangKleur(Systeem.Int32,Systeem.Byte,Systeem.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VervangNietTransparanteKleuren(Systeem.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.VervangFrame(Systeem.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)

## **Gebruik voorbeelden:**
**PSDNET-87. Voeg functie toe om JPEG/PNG/etc afbeeldingsbestanden naar PsdImage te laden zonder direct laden (Wat niet ondersteund wordt in Aspose.PSD)**

{{< highlight java >}}

 string bestandsPad = "PsdVoorbeeld.psd";

string uitvoerBestandsPad = "PsdResultaat.psd";

using(var afbeelding = new PsdImage(200, 200)) {

 using(var afbeelding = Image.Load(bestandsPad)) {

  Laag laag = null;

  try {

   laag = new Laag((RasterAfbeelding) afbeelding);

   afbeelding.AddLaag(laag);

  } catch (Uitzondering e) {

   if (laag != null) {

    laag.Vrijgeven();

   }

   Gooi;
  }

 }

 afbeelding.Opslaan(uitvoerBestandsPad);

}  

{{< /highlight >}}

**PSDNET-120. Ondersteuning van RGB-kleurmodus met 16 bits/kanaal (64 bits per kleur)**

{{< highlight java >}}

  // Ondersteuning van RGB-kleurmodus met 16 bits/kanaal (64 bits per kleur)

string bronBestandsNaam = "inRgb16.psd.psd";

string uitvoerBestandsPadJpg = "uitRgb16.jpg";

string uitvoerBestandsPadPsd = "uitRgb16.psd";

var opties = nieuwe PsdLaadOpties();

using(PsdImage afbeelding = (PsdAfbeelding) Afbeelding.Laden(bronBestandsNaam, opties)) {

 afbeelding.Opslaan(uitvoerBestandsPadPsd, nieuwe PsdOpties(afbeelding));

 afbeelding.Opslaan(uitvoerBestandsPadJpg, nieuwe JpegOpties() {

  Kwaliteit = 100

 });

}

// Bestanden moeten worden geopend zonder uitzondering en leesbaar zijn voor Photoshop    

using(Afbeelding afbeelding = Afbeelding.Laden(uitvoerBestandsPadPsd)) {}  

{{< /highlight >}}

**PSDNET-108. Ondersteuning van Laag Vectormaskers en Tekstlaag Aangepaste FlipRotate**

{{< highlight java >}}

 // RoteerFlip-operatie werkt niet zoals verwacht met PSD

var bronBestand = "1.psd";

var pngPad = "RoteerFlipTest2617.png";

var psdPad = "RoteerFlipTest2617.psd";

var flipType = RoteerFlipType.Rotate270FlipXY;

using(var afbeelding = (PsdAfbeelding)(Afbeelding.Laden(bronBestand))) {

 afbeelding.RoteerFlip(flipType);

 afbeelding.Opslaan(pngPad, nieuwe PngOpties() {

  KleurType = PngKleurType.TruecolorWithAlpha

 });

 afbeelding.Opslaan(psdPad);

}

{{< /highlight >}}

**PSDNET-99. Alle Aziatische tekens worden niet correct weergegeven**

[**Controleer bijgevoegd voorbeeld**](bijlagen/86278147/86343681.cs)

**PSDNET-116. \r\n symbolen worden geïnterpreteerd als dubbele regelovergang, wat onjuist is**

{{< highlight java >}}

 // \r\n symbolen worden geïnterpreteerd als dubbele regelovergang, wat onjuist is

string bronBestandsNaam = "TekstTest.psd";

string exportPad = "Resultaat.psd";

using(Afbeelding afbeeld
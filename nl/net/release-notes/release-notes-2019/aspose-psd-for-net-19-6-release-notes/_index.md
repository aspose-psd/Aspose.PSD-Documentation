---
title: Aspose.PSD voor .NET 19.6 - Release-opmerkingen
type: docs
weight: 70
url: /nl/net/aspose-psd-voor-net-19-6-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-127|Mogelijkheid om een PSD-bestand naar PSB en vice versa te converteren|Functie|
|PSDNET-154|Overzetting van Aspose.Imaging 19.5 bronnen naar Aspose.PSD|Verbetering|
|PSDNET-155|Opruimen openbare API gerelateerd aan Aspose.PSD|Verbetering|
|PSDNET-159|Eigenschap IsLicensed verwijderen|Verbetering|
|PSDNET-102|Conversie PSB naar JPG blijft hangen|Fout|
|PSDNET-150|Nieuw toegevoegde tekstlaagpositie is verschoven bij bewerken in Photoshop|Fout|

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- T:Aspose.PSD.Bestandsindelingen.Psd.BestandsIndelingVersie
- F:Aspose.PSD.Bestandsformaten.Psd.BestandsIndelingVersie.Psd
- F:Aspose.PSD.Bestandsformaten.Psd.BestandsIndelingVersie.Psb
- P:Aspose.PSD.AfbeeldingsOpties.PsdOpties.BestandsIndelingVersie
- F:Aspose.PSD.BestandsFormaat.Cdr
- F:Aspose.PSD.BestandsFormaat.Cmx
- F:Aspose.PSD.Bestandsindelingen.Psd.Lagen.LaagResource.PsbResourceHandtekening
- F:Aspose.PSD.Bestandsindelingen.Psd.Lagen.LaagBronnen.LaagVergrendelType.AllesVergrendelen
- P:Aspose.PSD.Afbeeldings.BufferGrootteHint
- P:Aspose.PSD.AfbeeldingsOpties.JpegOpties.ResolutieEenheid
- P:Aspose.PSD.AfbeeldingsOpties.VectorRasterisatieOpties.TekstWeergaveHint
- M:Aspose.PSD.AfbeeldingsOpties.VectorRasterisatieOpties.KopiërenNaar(Aspose.PSD.AfbeeldingsOpties.VectorRasterisatieOpties)
- P:Aspose.PSD.LaadOpties.BufferGrootteHint
- T:Aspose.PSD.Geheugenbeheer.Configuratie
- P:Aspose.PSD.Geheugenbeheer.Configuratie.BufferGrootteHint
- T:Aspose.PSD.ResolutieEenheid
- F:Aspose.PSD.ResolutieEenheid.Geens
- F:Aspose.PSD.ResolutieEenheid.Inch
- F:Aspose.PSD.ResolutieEenheid.Cm
# **Verwijderde API's:**
- M:Aspose.PSD.Mengen.op_Gelijkheid(Aspose.PSD.Mengen,Aspose.PSD.Mengen)
- M:Aspose.PSD.Mengen.op_Verschil(Aspose.PSD.Mengen,Aspose.PSD.Mengen)
- M:Aspose.PSD.Kleurenmengen.op_Gelijkheid(Aspose.PSD.Kleurenmengen,Aspose.PSD.Kleurenmengen)
- M:Aspose.PSD.Kleurenmengen.op_Verschil(Aspose.PSD.Kleurenmengen,Aspose.PSD.Kleurenmengen)
- T:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader
- M:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.Kopgrootte
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapBreedte
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapHoogte
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapVliegtuigen
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitsPerPixel
- F:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapCoreHeaderGrootte
- F:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.Os22XBitmapKopGrootte
- F:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.Os22XBitmapKopVolledigeGrootte
- F:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapInfoKopGrootte
- F:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapInfoKopGrootteV2
- F:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapInfoKopGrootteV3
- F:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapInfoKopGrootteV4
- F:Aspose.PSD.Bestandsformaten.Bmp.BitmapCoreHeader.BitmapInfoKopGrootteV5
- T:Aspose.PSD.Bestandsformaten.Bmp.BitmapInfoHeader
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapInfoHeader.Bitcompressie
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapInfoHeader.BestandsBeeldGrootte
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapInfoHeader.BitmapsPerMeterX
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapInfoHeader.BitmapsPerMeterY
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapInfoHeader.GebruikteKleuren
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapInfoHeader.BelangrijkeKleuren
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapInfoHeader.ExtraBitMasks
- T:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.RoodMasker
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.GroenMasker
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.BlauwMasker
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.AlphaMasker
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.CSType
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.Eindpunten
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.GammaRood
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.GammaGroen
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV4Header.GammaBlauw
- T:Aspose.PSD.Bestandsformaten.Bmp.BitmapV5Header
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV5Header.Intentie
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV5Header.ProfielGegevens
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV5Header.ProfielGrootte
- P:Aspose.PSD.Bestandsformaten.Bmp.BitmapV5Header.Reserve
- T:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding
- M:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.#ctor(Systeem.Strings)
- M:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.#ctor(Systeem.Stroom)
- M:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.#ctor(Aspose.PSD.AfbeeldingsOpties.JpegOpties,Systeem.Int32,Systeem.Int32)
- P:Aspose.PSD.Bestandsformaat.BmpAfbeelding.BestandsIndeling
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.BitmapInfoKop
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.RawDataFormaat
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.RawLineGrootte
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.Compressie
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.Breedte
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.Hoogte
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.BitsPerPixel
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.HorizontaleResolutie
- P:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.VerticaleResolutie
- M:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.StelResolutieIn(Systeem.Dubbel,Systeem.Dubbel)
- M:Aspose.PSD.Bestandsformaten.Bmp.BmpAfbeelding.TeBitmap
- T:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop
- P:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop.Eenheden
- P:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop.Reserve
- P:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop.Opgenomen
- P:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop.Renderen
- P:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop.Grootte1
- P:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop.Grootte2
- P:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop.Kleurcodering
- P:Aspose.PSD.Bestandsformaten.Bmp.Os22XBitmapKop.Identificatie
- T:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinaten
- M:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinaten.#ctor(Systeem.Byte[])
- P:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinaten.CieCoördinatenX
- P:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinaten.CieCoördinatenY
- P:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinaten.CieCoördinatenZ
- T:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinatenTrio
- M:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinatenTrio.#ctor(Systeem.Byte[])
- P:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinatenTrio.CieXyzRood
- P:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinatenTrio.CieXyzGroen
- P:Aspose.PSD.Bestandsformaten.Bmp.Structuren.CieCoördinatenTrio.CieXyzBlauw
- T:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.#ctor
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.#ctor(Systeem.String,Systeem.Byte[],Systeem.Byte[])
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.ToepassingsAuthenticatieCode
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.ToepassingsIdentificatie
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.ToepassingsData
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.Opslaan(Systeem.Stroom)
- F:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.BlokKopGrootte
- F:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.UitbreidingsLabel
- F:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.BlokGrootte
- F:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.ToepassingsIdentificatieGrootte
- F:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifToepassingsUitbreidingsBlok.ToepassingsAuthenticatieCodeGrootte
- T:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifCommentaarBlok
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifCommentaarBlok.#ctor
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifCommentaarBlok.#ctor(Systeem.String)
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifCommentaarBlok.Commentaar
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifCommentaarBlok.Opslaan(Systeem.Stroom)
- F:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifCommentaarBlok.UitbreidingsLabel
- F:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifCommentaarBlok.BlokKopGrootte
- T:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.UInt16,Systeem.UInt16)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.UInt16,Systeem.UInt16,Systeem.UInt16,Systeem.UInt16)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.UInt16,Systeem.UInt16,Systeem.UInt16,Systeem.UInt16,Aspose.PSD.IColorPalet,Systeem.Boolean,Systeem.Boolean,Systeem.Byte)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Aspose.PSD.RasterAfbeelding)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Aspose.PSD.RasterAfbeelding,Systeem.UInt16,Systeem.UInt16)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Aspose.PSD.RasterAfbeelding,Systeem.UInt16,Systeem.UInt16,Systeem.Boolean,Systeem.Boolean,Systeem.Byte)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.Stroom)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.Stroom,Systeem.UInt16,Systeem.UInt16)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.Stroom,Systeem.UInt16,Systeem.UInt16,Systeem.Boolean,Systeem.Boolean,Systeem.Byte)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.String)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.String,Systeem.UInt16,Systeem.UInt16)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.#ctor(Systeem.String,Systeem.UInt16,Systeem.UInt16,Systeem.Boolean,Systeem.Boolean,Systeem.Byte)
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.BestandsIndeling
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.Breedte
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.Hoogte
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.BitsPerPixel
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.Gefaseerd
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.IsPaletGesorteerd
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.GifFrameBitsPerPixel
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.Links
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.Boven
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.Vlaggen
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.ControleBlok
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.HeeftTransparanteKleur
- P:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.TransparanteKleur
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.KleurenpaletOphalen(Aspose.PSD.IColorPalet,Aspose.PSD.IColorPalet)
- M:Aspose.PSD.Bestandsformaten.Gif.Blokken.GifFrameBlok.VlaggenM
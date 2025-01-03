---
title: Aspose.PSD voor .NET 19.2 - Release-opmerkingen
type: docs
weight: 110
url: /nl/net/aspose-psd-voor-net-19-2-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor Aspose.PSD voor .NET 19.2

{{% /alert %}} 

|**Belangrijkste**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-97|Ondersteuning toegevoegd voor Vul lagen: Kleur vullen|Functie|
|PSDNET-98|Ondersteuning toegevoegd voor Vul lagen: Gradiëntvulling|Functie|
|PSDNET-105|Ondersteuning van GdFlResource|Functie|
|PSDNET-106|Ondersteuning van VmskResource|Functie|
|PSDNET-109|Porting van feitelijke Aspose.Imaging-bronnen naar Aspose.PSD|Verbetering|
|PSDNET-92|Ondersteuning toegevoegd voor gedeeltelijk laden voor sommige methoden|Verbetering|
|PSDNET-110|PSD-prestatie daalde meerdere keren|Fout|

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.Lagen.VulLagen.VulLaag
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulLagen.VulLaag.VulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulLagen.VulLaag.VulType
- M:Aspose.PSD.FileFormats.Psd.Lagen.VulLagen.VulLaag.Bijwerken
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.GradiëntVulInstellingen.GradiëntNaam
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.GradiëntType
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen. GradiëntNaam
- T:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.VulType
- F:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.VulType.Kleur
- F:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.VulType.Gradiënt
- F:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.VulType.Patroon
- T:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IKleurVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IKleurVulInstellingen.Kleur
- T:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IVulInstellingen.VulType
- T:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.AfstemmenMetLaag
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.Neutraal
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.Omdraaien
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.Hoek
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.HorizontaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.VerticaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.KleurPunten
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntVulInstellingen.TransparantiePunten
- T:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntTransparantiePunt
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradatieTransparantiePunt.Ondoorzichtigheid
- P:Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradatieTransparantiePunt.Locatie
- P:Aspose.PSD.FileFormats.Psd.Lagen.IGradatieKleurPunt
- P:Aspose.PSD.FileFormats.Psd.Lagen.IGradatieKleurPunt.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.IGradatieKleurPunt.Locatie
- P:Aspose.PSD.FileFormats.Psd.Lagen.IGradatieKleurPunt.MedianePuntLocatie
- M:Aspose.PSD.Uitbreidingen.RectangleUitbreidingen.VerbindMet(Aspose.PSD.RectangleF,Aspose.PSD.RectangleF)
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.BezierKnoopRecord
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.BezierKnoopRecord.#ctor(Systeem.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.BezierKnoopRecord.Punten
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.BezierKnoopRecord.IsGesloten
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.BezierKnoopRecord. IsGekoppeld
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.BezierKnoopRecord.IsOpen
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.BezierKnoopRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.ClipboardRecord
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.ClipboardRecord.#ctor(Systeem.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.ClipboardRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden. InitiëleVulRegelRecord
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden. InitiëleVulRegelRecord.#ctor(Systeem.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden. InitiëleVulRegelRecord. VullenStartMetAllePixles
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden. InitiëleVulRegelRecord. Type
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.LengteRecord
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.LengteRecord.#ctor(Systeem.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.LengteRecord.IsGesloten
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.LengteRecord.IsOpen
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.LengteRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VulRegelRecord
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VulRegelRecord.#ctor(Systeem.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VulRegelRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadRecord
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadRecordFactory
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadRecordFactory.#ctor
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadRecordFactory.ProduceerPadRecord(Systeem.Byte[])
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.GeslotenSubpadLengteRecord
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.GeslotenSubpadBeziërKnooppuntGekoppeld
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.GeslotenSubpadBeziërKnooppuntOngekoppeld
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.OpenSubpadLengteRecord
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.OpenSubpadBeziërKnooppuntGekoppeld
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.OpenSubpadBeziërKnooppuntOngekoppeld
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.VulregelRecord
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.KlembordRecord
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VectorPaden.VectorPadType.InitiëleVulRegelRecord
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.#ctor(Systeem.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.Paden
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.Versie
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.IsUitgeschakeld
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.IsNietGekoppeld
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.IsInverteerd
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.Handtekening
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.Sleutel
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.Lengte
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.PsdVersie
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.Opslaan(Aspose.PSD.StroomContainer,Systeem.Int32)
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VmskResource.TypeGereedschapSleutel
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VulLaagHulpbron
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VulLaagHulpbron.#ctor
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.VulLaagHulpbron.Handtekening
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.Handtekening
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.Sleutel
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.Lengte
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.PsdVersie
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.Hoek
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.GradiëntType
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.KleurPunten
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.TransparantiePunten
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.GradiëntNaam
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.GradiëntInterval
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.Omdraaien
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.AfstemmenMetLaag
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.Opslaan(Aspose.PSD.StroomContainer,Systeem.Int32)
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.TypeGereedschapSleutel
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.HorizontaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.GdFlResource.VerticaleVerschuiving
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource.Sleutel
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource.Lengte
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource.PsdVersie
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource.Opslaan(Aspose.PSD.StroomContainer,Systeem.Int32)
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.SoCoResource.TypeGereedschapSleutel
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.BasisVulInstellingen
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.BasisVulInstellingen.#ctor
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.BasisVulInstellingen.VulType
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.KleurVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.KleurVulInstellingen.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.KleurVulInstellingen.VulType
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.KleurVulInstellingen.VulType
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntKleurPunt
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntKleurPunt.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntKleurPunt.Locatie
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntKleurPunt.MedianePuntLocatie
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.AfstemmenMetLaag
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.Neutraal
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.Hoek
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.GradiëntType
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.HorizontaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.VerticaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.VulType
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.KleurPunten
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.TransparantiePunten
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.VoegKleurPuntToe
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.VoegTransparantiePuntToe
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntTransparantiePunt
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntTransparantiePunt.Ondoorzichtigheid
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntTransparantiePunt.Locatie
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntTransparantiePunt.MedianePuntLocatie
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.VulType
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.Gekoppeld
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.Schaal
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.PuntType
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.PatroonNaam
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.PatroonId
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.HorizontaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.VerticaleVerschuiving
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntType
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntType.Lineair
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntType.Radiaal
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntType.Hoek
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntType.Weerspiegeld
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntType.Diamant
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntType.VormBurst
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntKleurPunt.#ctor
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.VerwijderTransparantiePunt(Aspose.PSD.FileFormats.Psd.Lagen.VulInstellingen.IGradiëntTransparantiePunt)
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.VerwijderKleurPunt(Aspose.PSD.FileFormats.Psd.Lagen.IGradiëntKleurPunt)
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntTransparantiePunt.#ctor
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.#ctor
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.GradiëntVulInstellingen.GenererenLfx2HulpbronNodes
- P:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.Kleur
- M:Aspose.PSD.FileFormats.Psd.Lagen.LaagInstellingen.PatroonVulInstellingen.GenererenLfx2HulpbronNodes(Systeem.String,Aspose.PSD.Kleur,Systeem.String,Systeem.String,Systeem.Double,Systeem.Boolean,Aspose.PSD.PointF)
- M:Aspose.PSD.FileFormats.Tiff.AfbeeldingVervangenKader(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FontInstellingen.WerkLettertypenBij
- T:Aspose.PSD.AfbeeldingOpties.CmxRasterisatieOpties
- M:Aspose.PSD.AfbeeldingOpties.CmxRasterisatieOpties.#ctor
- P:Aspose.PSD.AfbeeldingOpties.CmxRasterisatieOpties.Positionering
- T:Aspose.PSD.AfbeeldingOpties.Positioneringstypes
- F:Aspose.PSD.AfbeeldingOpties.Positioneringstypes.GedefinieerdDoorDocument
- F:Aspose.PSD.AfbeeldingOpties.Positioneringstypes.GedefinieerdDoorOpties
- F:Aspose.PSD.AfbeeldingOpties.Positioneringstypes.Relatief
- P:Aspose.PSD.AfbeeldingOpties.VectorRasterisatieOpties.VervagingsModus
- T:Aspose.PSD.Interfaces.IObjectMetSizeF
- P:Aspose.PSD.Interfaces.IObjectMetSizeF.SizeF
- P:Aspose.PSD.Interfaces.IObjectMetSizeF.BreedteF
- P:Aspose.PSD.Interfaces.IObjectMetSizeF.HoogteF
- T:Aspose.PSD.VectorAfbeelding
- M:Aspose.PSD.VectorAfbeelding.#ctor
- P:Aspose.PSD.VectorAfbeelding.SizeF
- P:Aspose.PSD.VectorAfbeelding.BreedteF
- P:Aspose.PSD.VectorAfbeelding.HoogteF
- P:Aspose.PSD.VectorAfbeelding.Breedte
- P:Aspose.PSD.VectorAfbeelding.Hoogte
# **Verwijderde API's:**
- T:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.BasisVulInstellingen
- M:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.BasisVulInstellingen.#ctor
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.BasisVulInstellingen.VulType
- T:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.KleurVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.KleurVulInstellingen.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.KleurVulInstellingen.VulType
- T:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.VulType
- F:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.VulType.Kleur
- F:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.VulType.Gradiënt
- F:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.VulType.Patroon
- T:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntKleurPunt
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntKleurPunt.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntKleurPunt.Locatie
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntKleurPunt.MedianePuntLocatie
- T:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.Kleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.AfstemmenMetLaag
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.Neutraal
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.Hoek
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.GradiëntType
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.HorizontaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.VerticaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.VulType
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.KleurPunten
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.TransparantiePunten
- M:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.VoegKleurPuntToe
- M:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.VoegTransparantiePuntToe
- M:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.VerwijderTransparantiePunt(Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntTransparantiePunt)
- M:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.VerwijderKleurPunt(Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntKleurPunt)
- T:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntTransparantiePunt
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntTransparantiePunt.Ondoorzichtigheid
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntTransparantiePunt.Locatie
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntTransparantiePunt.MedianePuntLocatie
- T:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.VulType
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.Gekoppeld
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.Schaal
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.PuntType
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.PatroonNaam
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.PatroonId
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.HorizontaleVerschuiving
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.VerticaleVerschuiving
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.Lfx2Hulpbronnen.GradiëntType
- T:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.Lfx2Hulpbronnen.GradiëntType
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.Lfx2Hulpbronnen.GradiëntType.Lineair
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.Lfx2Hulpbronnen.GradiëntType.Radiaal
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.Lfx2Hulpbronnen.GradiëntType.Hoek
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.Lfx2Hulpbronnen.GradiëntType.Weerspiegeld
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.Lfx2Hulpbronnen.GradiëntType.Diamant
- F:Aspose.PSD.FileFormats.Psd.Lagen.LaagHulpbronnen.Lfx2Hulpbronnen.GradiëntType.VormBurst
- M:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.#ctor
- M:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.GradiëntVulInstellingen.GenererenLfx2HulpbronNodes
- P:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.Kleur
- M:Aspose.PSD.FileFormats.Psd.Lagen.Laageffecten.PatroonVulInstellingen.GenererenLfx2HulpbronNodes(Systeem.String,Aspose.PSD.Kleur,Systeem.String,Systeem.String,Systeem.Double,Systeem.Boolean,Aspose.PSD.PointF)
---
title: Aspose.PSD voor .NET 20.9 - Release-opmerkingen
type: docs
weight: 40
url: /nl/net/aspose-psd-voor-net-20-9-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Belangrijkste**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-408|Ondersteuning van SoLEResource (Slim Objectlaag Externe bron)|Functie|
|PSDNET-614|Ondersteuning van Gekoppelde Slimme objecten|Functie|
|PSDNET-615|Ondersteuning van Ingesloten Slimme objecten|Functie|
|PSDNET-690|Het bijwerken van tekst in een gegeven PSD-bestand en het opslaan ervan verandert enkele laag- en tekstparameters|Fout|
|PSDNET-696|FillLayer wordt niet bijgewerkt na de creatie en kan niet correct worden weergegeven|Fout|
|PSDNET-712|Regressie: Aspose.PSD 20.8.0 kan het bestand niet openen|Fout|
|PSDNET-714|In een specifiek PSD-bestand verbreekt het wijzigen van TextLayer de locatiewaarde|Fout|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.VoegTextRecordToe(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoInterlinie
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandaardLigaturen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BelangrijkeLigaturen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextueleAlternatieven
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.TaalIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.VerticaleSchaal
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HorizontaleSchaal
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Breuken
- T:Aspose.PSD.FileFormats.Psd.AutoInterlinie
- F:Aspose.PSD.FileFormats.Psd.AutoInterlinie.Handmatig
- F:Aspose.PSD.FileFormats.Psd.AutoInterlinie.Metrisch
- F:Aspose.PSD.FileFormats.Psd.AutoInterlinie.Optisch
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.GeplaatsteId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Versie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.UniekeId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.IsAangepast
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.PaginaNummer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.TotaalPaginas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.AntiAliasBeleid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.GeplaatsteLaagType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Links
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Rechts
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Onder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Boven
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Grenzen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.TransformeerMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.HorizontaleMeshPunten
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.VerticaleMeshPunten
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.HorizontaleMeshPuntEenheid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.VerticaleMeshPuntEenheid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Handtekening
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Waarde
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Perspectief
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.AnderPerspectief
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.UVolgorde
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.VVolgorde
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron.Items
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.ComponentId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.OrigineelComponentId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.UniekeId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.GeplaatsteId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.PaginaNummer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.TotaalPaginas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.AntiAliasBeleid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.GeplaatsteLaagType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.TransformeerMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.NietAffineTransformatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Handtekening
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Lengte
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.PsdVersie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Uitsnede
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.FilmMetFrames
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Resolutie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.ResolutieEenheid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Comp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Breedte
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Hoogte
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.FilmstapTeller
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.FilmstapNoemer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.DuurTeller
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.DuurNoemer
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeObjectBron.Opslaan(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor(System.Guid,System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.Sleutel
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.TypeToolSleutel
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeBronMaker
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeBronMaker.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeBronMaker.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GeplaatsteBron)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeBronMaker.#ctor(System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeBronMaker.GenererenGeplaatsteBron
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeBronMaker.GenererenSlimmeIngeslotenBron
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SlimmeBronMaker.GenererenSlimmeExterneBron
- T:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag
- P:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.InhoudsGrenzen
- P:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.InhoudsBron
- P:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.Inhoud
- P:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.InhoudsType
- P:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.SlimmeObjectProvider
- M:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.ExporteerInhoud(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.LaadInhoud(Aspose.PSD.LaadOpties)
- M:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.VervangInhoud(Aspose.PSD.Afbeelding)
- M:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.VervangInhoud(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.EmbedGekoppeld
- M:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.ConverteerNaarGekoppeld(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.VernieuwNaarBestand(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SlimmeObjectLagen.SlimmeObjectLaag.WerkGewijzigdeInhoudBij
- T:Aspose.PSD.FileFormats.Psd.SlimmeObjectProvider
- M:Aspose.PSD.FileFormats.Psd.SlimmeObjectProvider.EmbedAlleGekoppelde
- M:Aspose.PSD.FileFormats.Psd.SlimmeObjectProvider.WerkAlleGewijzigdeInhoudBij
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SlimmeObjectType
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SlimmeObjectType.Ingesloten
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SlimmeObjectType.BeschikbaarGekoppeld
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SlimmeObjectType.NietBeschikbaarGekoppeld
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SlimmeObjectType.BibliotheekKoppeling
- P:Aspose.PSD.FileFormats.Psd.PsdAfbeelding.SlimmeObjectProvider

# **Verwijderde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.VoegTextRecordToe(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Versie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UniekeId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.IsAangepast
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PaginaNummer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TotaalPaginas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.AntiAliasBeleid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.GeplaatsteLaagType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Links
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Rechts
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Onder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Boven
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Grenzen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TransformeerMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontaleMeshPunten
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticaleMeshPunten
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontaleMeshPuntEenheid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticaleMeshPuntEenheid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Waarde
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UVolgorde
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VVolgorde
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.ComponentId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.OrigineelComponentId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Versie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UniekeId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.GeplaatsteId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.IsAangepast
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PaginaNummer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TotaalPaginas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.AntiAliasBeleid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.GeplaatsteLaagType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Links
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Rechts
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Onder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Boven
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Grenzen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TransformeerMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.NietAffineTransformatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.HorizontaleMeshPunten
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VerticaleMeshPunten
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.HorizontaleMeshPuntEenheid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VerticaleMeshPuntEenheid
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Handtekening
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Lengte
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PsdVersie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Waarde
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Perspectief
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.AnderPerspectief
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UVolgorde
- P
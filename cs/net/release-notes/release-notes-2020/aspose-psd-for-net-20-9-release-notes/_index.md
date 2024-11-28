---
title: Aspose.PSD pro .NET 20.9 - Poznámky k vydání
type: docs
weight: 40
url: /cs/net/aspose-psd-pro-net-20-9-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-408|Podpora SoLEResource (externí zdroj inteligentní vrstvy objektu)|Funkce|
|PSDNET-614|Podpora propojených inteligentních objektů|Funkce|
|PSDNET-615|Podpora vložených inteligentních objektů|Funkce|
|PSDNET-690|Aktualizace textu v daném souboru PSD a jeho uložení změní některé vrstvy a mnoho textových parametrů|Chyba|
|PSDNET-696|FillLayer nejsou aktualizovány po vytvoření a nemohou být správně renderovány|Chyba|
|PSDNET-712|Regrese: Aspose.PSD 20.8.0 nemůže otevřít soubor|Chyba|
|PSDNET-714|V konkrétním souboru PSD pokožení TextLayeru naruší hodnotu polohy|Chyba|

## **Změny veřejného API**
# **Přidaná API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DiscretionaryLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextualAlternates
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LanguageIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.VerticalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HorizontalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Fractions
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manual
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Metric
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Optical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Položka(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.PlacedId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Verze
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.JedinečnéId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.JeVlastní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.ČísloStránky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.CelkovýPočetStránek
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.AntiAliasPolitika
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TypVloženéVrstvy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Levo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Horní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Pravo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Dolní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Hranice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TransformačníMatice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.HorizontálníBodMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.VertikálníBodMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.JednotkaHorizontálníhoBoduMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.JednotkaVertikálníhoBoduMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Podpis
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Hodnota
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Perspektiva
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PerspektivaOstatní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Položky
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.UnikátníId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.ČísloStránky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.CelkovýPočetStránek
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.AntiAliasPolitika
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.TypVloženéVrstvy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.TransformačníMatice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.NeAffineTransformačníMatice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Podpis
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Délka
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PsdVerze
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Položky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Střih
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Obrok
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.RozsahSnímku
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.JednotkaRozsahuSnímku
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Komprese
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Šířka
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Výška
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.NásobekSnímkuČasu
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.DělitelSnímkuČasu
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Uložit(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor(System.Guid,System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.Klíč
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.#ctor(System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.GeneratePlacedResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.GenerateSmartEmbeddedResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.GenerateSmartExternalResource
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.HraniceObsahu
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.PůvodObsahu
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.Obsah
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.TypObsahu
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.PoskytovatelSmartObjektu
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ExportujObsah(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.NačtiObsah(Aspose.PSD.LoadOptions)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.NahraďObsah(Aspose.PSD.Image)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.NahraďObsah(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.VložPropojený
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.PřeveďNaPropojeno(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.PropojZnovuNaSoubor(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.AktualizujZměněnýObsah
- T:Aspose.PSD.FileFormats.Psd.SmartObjectProvider
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.VložVšePropojeno
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.AktualizujVšeZměněnýObsah
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType.Vložený
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType.DostupnéPropojeno
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType.NedostupnéPropojeno
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType.KnihovníPropojeno
- P:Aspose.PSD.FileFormats.Psd.PsdImage.PoskytovatelSmartObjektu

# **Odstraněná API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Verze
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.JedinečnéId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.JeVlastní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.ČísloStránky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.CelkovýPočetStránek
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.AntiAliasPolitika
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TypVloženéVrstvy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Levo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Horní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Pravo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Dolní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Hranice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TransformačníMatice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontálníBodMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VertikálníBodMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.JednotkaHorizontálníhoBoduMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.JednotkaVertikálníhoBoduMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Hodnota
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Položky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Verze
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.JeVlastní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.ČísloStránky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.CelkovýPočetStránek
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.AntiAliasPolitika
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TypVloženéVrstvy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Levo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Horní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Pravo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Dolní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Hranice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TransformačníMatice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.NeAffineTransformačníMatice
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.HorizontálníBodMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VertikálníBodMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.JednotkaHorizontálníhoBoduMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.JednotkaVertikálníhoBoduMřížky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Podpis
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Hodnota
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Perspektiva
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PerspektivaOstatní
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Položky
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Střih
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Obrok
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Rozs
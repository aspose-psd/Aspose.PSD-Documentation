---
title: Aspose.PSD voor .NET 23.6 - Release-opmerkingen
type: docs
weight: 70
url: /nl/net/aspose-psd-voor-net-23-6-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel**   | **Samenvatting**                                                                                                                                 | **Categorie** |
|:-------------|:------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Refactor TimeLine API                                                                                                                            | Verbetering  |
| PSDNET-1517 | Verwijder artefacten bij renderen warp                                                                                                          | Verbetering  |
| PSDNET-1528 | Warp-renderoptimalisatie                                                                                                                        | Verbetering  |
| PSDNET-147  | Ondersteuning van Threshold Adjustment Layer                                                                                                     | Functie       |
| PSDNET-149  | Ondersteuning van Selective Color Adjustment Layer                                                                                               | Functie       |
| PSDNET-801  | Mogelijkheid om PSD TimeLine naar Animated Gif-bestand te exporteren                                                                             | Functie       |
| PSDNET-1555 | Toevoegen van ondersteuning voor TextLayer zonder rechthoekige randen                                                                            | Functie       |
| PSDNET-1582 | Ondersteuning van ShapeLayer                                                                                                                     | Functie       |
| PSDNET-864  | Afbeelding vervangen in Smart object wordt niet bijgewerkt                                                                                       | Fout         |
| PSDNET-1404 | PSD-bestand kan niet worden opgeslagen als PSD met de volgende fout: Rgb en Lab-modi mogen niet minder dan 3 kanalen en meer dan 4 kanalen bevatten   | Fout         |
| PSDNET-1546 | Tekst uitlijning gaat verloren bij openen van TextLayer via de bewerkingsmodus van Photoshop                                                     | Fout         |
| PSDNET-1548 | Null-verwijzingsfout bij opslaan van PSD-bestand                                                                                                 | Fout         |
| PSDNET-1578 | Uitzondering bij het laden van de ShapeLayer: Punten voor vectorbegrenzing worden nog niet ondersteund                                              | Fout         |
| PSDNET-1579 | Uitzondering bij het laden van VogkResource: Punten worden opgeslagen als DoubleStructure, we lezen als UnitStructures                              | Fout         |
| PSDNET-1581 | LayerType van ShapeLayer is leeg                                                                                                                 | Fout         |


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.P
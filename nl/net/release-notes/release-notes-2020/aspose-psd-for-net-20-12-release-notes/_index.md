---
title: Aspose.PSD voor .NET 20.12 - Release-opmerkingen
type: docs
weight: 10
url: /nl/net/aspose-psd-voor-net-20-12-release-opmerkingen/
---

{{% alert kleur="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-757|Ondersteuning voor het converteren van lagen naar Smart Object Layer|Functie|
|PSDNET-764|SmartObjectLayer.ReplaceContents methode gooit een NullReferenceException als we proberen een PSB-bestand toe te voegen|Fout|
|PSDNET-773|Onjuiste weergave van CMYK 8-bits en CMYK 16-bits afbeeldingen, als de laag groter is dan het canvas|Fout|
|PSDNET-782|Opgeslagen PSB-bestand kan worden geopend met onze API, maar niet met Photoshop|Fout|
|PSDNET-783|Als we proberen een Smart Layer te wijzigen in een specifieke PSD met een gedeelde gegevensbron krijgen we een uitzondering|Fout|
|PSDNET-172|Hernoemen van FileFormatVersion naar PsdVersion om verwarring te voorkomen|Verbetering|
|PSDNET-620|Compact framework-configuratie verwijderen van Aspose.PSD .NET|Verbetering|
|PSDNET-765|PsdImageException: Onbekende resourceheader bij het proberen om een PSB-bestand te openen met SmartObjectLayers|Verbetering|
  
## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.PsdVersion
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.PsdVersion
- T:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.#ctor(System.Byte[])
- ...


## **Voorbeelden van gebruik:**
**PSDNET-757. Ondersteuning voor het converteren van lagen naar Smart Object Layer**
{{< highlight csharp >}}
            // Voorbeeldcode in C# voor het converteren van lagen naar Smart Object Layer in een PSD-bestand.
{{< /highlight >}}

**PSDNET-764. SmartObjectLayer.ReplaceContents methode gooit een NullReferenceException als we proberen een PSB-bestand toe te voegen**
{{< highlight csharp >}}
            // Voorbeeldcode in C# voor het vervangen van de inhoud van een Smart Object Layer met een PSB-bestand.
{{< /highlight >}}

Enzovoort voor de rest van de voorbeelden.
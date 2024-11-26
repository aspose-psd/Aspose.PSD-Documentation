---
title: Het Manipuleren van PNG-Afbeeldingen
type: docs
weight: 40
url: /nl/net/manipuleren-van-png-afbeeldingen/
---

## **Transparantie Specificeren voor PNG-Afbeeldingen**
Een van de voordelen van het opslaan van afbeeldingen in PNG-indeling is dat PNG een transparante achtergrond kan hebben. Aspose.PSD voor .NET biedt de mogelijkheid om transparantie te specificeren voor PNG-afbeeldingen en rasterafbeeldingen, zoals gedemonstreerd in de onderstaande sectie. Met behulp van de Aspose.PSD voor .NET API kan elk gewenste kleur als transparant worden ingesteld tijdens het maken van nieuwe PNG-afbeeldingen of het converteren van bestaande afbeeldingen naar PNG-indeling. Hiervoor heeft de Aspose.PSD voor .NET API de [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) eigenschap en de [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) enumeratie blootgelegd die kunnen worden ingesteld om aan te geven welke kleur als transparant moet worden weergegeven in de PNG-afbeelding. Het onderstaande codefragment toont hoe je een bestaande PSD-afbeelding naar een PNG-afbeelding kunt converteren door de gewenste kleur als transparant te specificeren.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-HetWijzigenEnConverterenVanAfbeeldingen-PNG-SpecificeerTransparantie-SpecificeerTransparantie.cs" >}}
## **Resolutie Instellen voor PNG-Afbeeldingen**
Aspose.PSD voor .NET onthult de ResolutionSetting klasse die kan worden gebruikt om de resolutie in te stellen voor alle afbeeldingsformaten, inclusief PNG. Dit artikel demonstreert het gebruik van de Aspose.PSD voor .NET API om de horizontale en verticale resolutieparameters in te stellen voor het PNG-afbeeldingsformaat. Het onderstaande codefragment laadt een bestaande PSD-afbeelding en converteert deze naar PNG-formaat, waarbij ook de resolutie wordt gewijzigd.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-HetWijzigenEnConverterenVanAfbeeldingen-PNG-ResolutieInstellen-ResolutieInstellen.cs" >}}
## **PNG-Bestanden Comprimeren**
Het Portable Network Graphic (PNG) is een verliesvrij compressieformaat voor het overbrengen van een bitmap over netwerken. Wanneer je een afbeelding als PNG-bestand opslaat in elk programma, kan het zijn dat je wordt gevraagd een compressieniveau te kiezen in een bereik van 0 tot een maximaal niveau. Het instellen van deze waarde comprimeert eigenlijk de bestandsgrootte en vermindert niet de kwaliteit van de afbeelding. Dit artikel beschrijft hoe Aspose.PSD API's je in staat stellen om de grootte van het PNG-bestand te beheren. Aspose.PSD API's kunnen worden gebruikt om de compressieniveaus voor het PNG-bestandsformaat in te stellen met behulp van de PngOptions klasse die een eigenschap van het type int [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) heeft. Deze eigenschap accepteert een waarde van 0 tot 9, waarbij 9 de maximale compressie is. Het onderstaande codefragment toont hoe je de compressieniveaus kunt instellen met behulp van de Aspose.PSD voor .NET API.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-HetWijzigenEnConverterenVanAfbeeldingen-PNG-BestandenComprimeren-BestandenComprimeren.cs" >}}
## **Bitdiepte Specificeren voor PNG-Afbeeldingen**
Bitdiepte in beeldvormgeving is het aantal bits dat wordt gebruikt om de kleur van een enkele pixel in een bitmapafbeelding aan te geven. Zoals alle andere bitmapindelingen, wordt de PNG-kleurdiepte ook weergegeven in bits, zoals 1-bit (2 kleuren), 2-bit (4 kleuren), 4-bit (16 kleuren) en 8-bit (256 kleuren). Aspose.PSD voor .NET API kan worden gebruikt om de bitdiepte in te stellen voor PNG-afbeeldingen met behulp van de [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) eigenschap blootgelegd door de PngOptions klasse. Op dit moment kan de BitDepth eigenschap worden ingesteld op 1, 2, 4 of 8 bits voor grijswaarden en geïndexeerde kleurentypen. Voor alle andere kleurtypes worden alleen 8 bits ondersteund. Het onderstaande codefragment toont hoe je de Bitdiepte kunt instellen voor een PNG-afbeelding.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-HetWijzigenEnConverterenVanAfbeeldingen-PNG-SpecificeerBitdiepte-SpecificeerBitdiepte.cs" >}}
## **Filtermethoden Toepassen op PNG-Afbeeldingen**
Bitdiepte in beeldvormgeving is het aantal bits dat wordt gebruikt om de kleur van een enkele pixel in een bitmapafbeelding aan te geven. Zoals alle andere bitmapindelingen, wordt de PNG-kleurdiepte ook weergegeven in bits, zoals 1-bit (2 kleuren), 2-bit (4 kleuren), 4-bit (16 kleuren) en 8-bit (256 kleuren). Aspose.PSD voor .NET API kan worden gebruikt om de bitdiepte in te stellen voor PNG-afbeeldingen met behulp van de BitDepth eigenschap blootgelegd door de PngOptions klasse. Op dit moment kan de BitDepth eigenschap worden ingesteld op 1, 2, 4 of 8 bits voor grijswaarden en geïndexeerde kleurentypen. Voor alle andere kleurtypes worden alleen 8 bits ondersteund. Het onderstaande codefragment toont hoe je de Bitdiepte kunt instellen voor een PNG-afbeelding.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-HetWijzigenEnConverterenVanAfbeeldingen-PNG-ToepassenFilterMethode-ToepassenFilterMethode.cs" >}}
## **Achtergrondkleur Wijzigen van een Transparante PNG-Afbeelding**
PNG-afbeeldingen in indeling kunnen een transparante achtergrond hebben. Aspose.PSD voor .NET biedt de mogelijkheid om de achtergrondkleur van een PNG-afbeelding met transparante achtergrond te veranderen. Aspose.PSD voor .NET API kan worden gebruikt om de kleur van een transparante PNG-afbeelding in te stellen/te veranderen. Het onderstaande codefragment toont hoe je de achtergrondkleur van een transparante PNG-afbeelding kunt instellen/veranderen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-HetWijzigenEnConverterenVanAfbeeldingen-PNG-AchtergrondkleurWijzigen-AchtergrondkleurWijzigen.cs" >}}

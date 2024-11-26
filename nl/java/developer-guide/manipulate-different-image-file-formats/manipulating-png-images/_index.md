---
title: Het manipuleren van PNG-afbeeldingen
type: docs
weight: 30
url: /nl/java/het-manipuleren-van-png-afbeeldingen/
---

## **Transparantie specificeren voor PNG-afbeeldingen**
Een van de voordelen van het opslaan van afbeeldingen in PNG-indeling is dat PNG een transparante achtergrond kan hebben. Aspose.PSD voor Java biedt de mogelijkheid om transparantie te specificeren voor de PngImage & RasterImage klassen, zoals gedemonstreerd in de onderstaande sectie. De Aspose.PSD voor Java API kan worden gebruikt om elke kleur als transparant in te stellen bij het maken van nieuwe PNG-afbeeldingen of bij het converteren van bestaande afbeeldingen naar PNG-indeling. Voor dit doel heeft de Aspose.PSD voor Java API de eigenschap TransparentColor en de enumeratie PngColorType blootgelegd die kan worden ingesteld om elke kleur te specificeren die als transparant moet worden gerenderd in de PNG-afbeelding. Het onderstaande codefragment toont hoe een bestaande PSD-afbeelding kan worden geconverteerd naar een PNG-afbeelding door gebruik te maken van de PngImage overloaded constructor en door de gewenste kleur als transparant te specificeren.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Resolutie instellen voor PNG-afbeeldingen**
Aspose.PSD voor Java blootgesteld de ResolutionSetting klasse die gebruikt kan worden om de resolutie in te stellen voor alle afbeeldingsindelingen, inclusief PNG. Dit artikel demonstreert het gebruik van de Aspose.PSD voor Java API om de horizontale en verticale resolutieparameters in te stellen voor het PNG-afbeeldingsformaat. Het volgende codefragment laadt een bestaande PSD-afbeelding en converteert deze naar PNG-formaat waarbij ook de resolutie wordt gewijzigd.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **PNG-bestanden comprimeren**
Het Portable Network Graphic (PNG) is een lossless compressieformaat voor het verzenden van een bitmap via netwerken. Wanneer u een afbeelding opslaat als PNG-bestand in elk programma, kunt u worden gevraagd om een compressieniveau te kiezen in een bereik van 0 tot elk maximaal niveau. Het instellen van deze waarde comprimeert eigenlijk de bestandsgrootte en verlaagt niet de kwaliteit van de afbeelding. Dit artikel beschrijft hoe Aspose.PSD API's u in staat stellen om de bestandsgrootte van het PNG-bestand te beheren. Aspose.PSD API's kunnen worden gebruikt om de compressieniveaus in te stellen voor het PNG-bestandsformaat met behulp van de PngOptions klasse die een eigenschap CompressionLevel van het type int heeft. Deze eigenschap accepteert een waarde van 0 tot 9, waarbij 9 de maximale compressie is. Het onderstaande codefragment toont hoe de compressieniveaus kunnen worden ingesteld met behulp van Aspose.PSD voor Java API.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Bitdiepte specificeren voor PNG-afbeeldingen**
Bitdiepte in beeldvorming is het aantal bits dat wordt gebruikt om de kleur van een enkele pixel in een bitmapafbeelding aan te geven. Net als alle andere bitmapformaten wordt ook de kleurdiepte van PNG uitgedrukt in bits zoals 1-bit (2 kleuren), 2-bit (4 kleuren), 4-bit (16 kleuren) en 8-bit (256 kleuren). Aspose.PSD voor Java API kan worden gebruikt om de bitdiepte voor PNG-afbeeldingen in te stellen met behulp van de BitDepth eigenschap blootgesteld door de PngOptions klasse. Op dit moment kan de BitDepth eigenschap ingesteld worden op 1, 2, 4 of 8 bits voor grijswaarden en geïndexeerde kleurtypes. Voor alle andere kleurtypes worden alleen 8 bits ondersteund. Het onderstaande codefragment toont hoe de bitdiepte kan worden ingesteld voor een PNG-afbeelding.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Filtermethoden toepassen op PNG-afbeeldingen**
Aspose.PSD voor Java blootgesteld de PngFilterType enumeratie die gebruikt kan worden om het filtertype in te stellen voor PNG-afbeelding. Het onderstaande codefragment demonstreert hoe een filter kan worden toegepast op een bestaand PSD-bestand om PNG-afbeelding door het gebruik van PngFilterType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Achtergrondkleur wijzigen van een transparante PNG-afbeelding**
Afbeeldingen in PNG-indeling kunnen een transparante achtergrond hebben. Aspose.PSD voor Java biedt de mogelijkheid om de achtergrondkleur van een PNG-afbeelding met transparante achtergrond te wijzigen. Aspose.PSD voor Java API kan worden gebruikt om de kleur van een transparante PNG-afbeelding in te stellen/te wijzigen. Het onderstaande codefragment toont hoe de achtergrondkleur van een transparante PNG-afbeelding kan worden ingesteld/gewijzigd.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}

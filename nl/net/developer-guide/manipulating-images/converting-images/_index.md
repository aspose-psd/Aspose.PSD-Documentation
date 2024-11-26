---
title: Afbeeldingen converteren
type: docs
weight: 20
url: /nl/afbeeldingen-converteren/
---

## **Afbeeldingen converteren naar zwart-wit en grijswaarden**
Soms moet u gekleurde afbeeldingen converteren naar zwart-wit of grijswaarden voor afdruk- of archiveringsdoeleinden. Dit artikel demonstreert het gebruik van de Aspose.PSD voor .NET API om dit te bereiken met behulp van twee methoden zoals hieronder beschreven.

- Binair maken
- Grijswaarden
### **Binair maken**
Om het concept van binarisatie te begrijpen, is het belangrijk om een binaire afbeelding te definiëren; dat is een digitale afbeelding die slechts twee mogelijke waarden kan hebben voor elk pixel. Normaal gesproken worden voor een binair beeld de twee kleuren zwart en wit gebruikt, hoewel elk van de twee kleuren kan worden gebruikt. Binarisatie is het proces om een afbeelding om te zetten in tweevoudig niveau, wat betekent dat elk pixel wordt opgeslagen als een enkel bit (0 of 1) waar 0 de afwezigheid van kleur aanduidt en 1 de aanwezigheid van kleur betekent. Aspose.PSD voor .NET API ondersteunt momenteel twee methoden voor binarisatie.
#### **Binarisatie met vast drempelwaarde**
Onderstaande codefragment toont hoe binarisatie met een vaste drempelwaarde kan worden toegepast op een afbeelding.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarisatie met Otsu-drempelwaarde**
Onderstaande codefragment toont hoe binarisatie met Otsu-drempelwaarde kan worden toegepast op een afbeelding.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Grijswaarden**
Grijswaarden is het proces van het omzetten van een continue toonafbeelding naar een afbeelding met onderbroken grijstinten. Onderstaand codefragment toont hoe grijswaarden kunnen worden gebruikt.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **Converteer GIF-afbeeldinglagen naar TIFF-afbeelding**
Soms is het nodig om lagen van een PSD-afbeelding te extraheren en converteren naar een ander rasterafbeeldingsformaat om aan een toepassingsbehoefte te voldoen. Aspose.PSD API ondersteunt de functie om lagen van een PSD-afbeelding te extraheren en converteren naar een ander rasterafbeeldingsformaat. Eerst zullen we een instantie van een afbeelding maken en de PSD-afbeelding vanaf de lokale schijf laden, daarna zullen we elke laag in de Eigenschap Layer doorlopen. Vervolgens zullen we het blok converteren naar een TIFF-afbeelding. Onderstaand codefragment toont hoe PSD-afbeeldingslagen kunnen worden geconverteerd naar TIFF-afbeeldingen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **PSD CMYK converteren naar CMYK TIFF**
Met Aspose.PSD voor .NET kunnen ontwikkelaars een CMYK PSD-bestand converteren naar het CMYK tiff-formaat. Dit artikel toont hoe u een CMYK PSD-bestand kunt exporteren/converteren naar het CMYK tiff-formaat met Aspose.PSD. Met Aspose.PSD voor .NET kunt u PSD-afbeeldingen laden en vervolgens verschillende eigenschappen instellen met behulp van [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) klasse en de afbeelding opslaan of exporteren. Onderstaand codefragment toont hoe u deze functie kunt realiseren.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **Afbeeldingen exporteren**
Naast een uitgebreide set van beeldverwerkingsroutines biedt Aspose.PSD gespecialiseerde klassen om PSD-bestandsindelingen naar andere indelingen te converteren. Door gebruik te maken van deze bibliotheek is PSD-afbeeldingsconversie zeer eenvoudig en intuïtief. Hier zijn enkele gespecialiseerde klassen hiervoor in de [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Het is eenvoudig om PSD-afbeeldingen te exporteren met de Aspose.PSD voor .NET API. Het enige wat je nodig hebt is een object van de juiste klasse uit de [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace. Door deze klassen te gebruiken, kunt u gemakkelijk elke afbeelding die is gemaakt, bewerkt of eenvoudigweg geladen met Aspose.PSD voor .NET exporteren naar elk ondersteund formaat.
## **Afbeeldingen combineren**
Dit voorbeeld gebruikt de Graphics-klasse en toont hoe twee of meer afbeeldingen kunnen worden gecombineerd tot één complete afbeelding. Om de bewerking te demonstreren, maakt het voorbeeld een nieuwe PsdImage en tekent afbeeldingen op het canvasoppervlak met behulp van de Draw Image-methode die wordt blootgesteld door de Graphics-klasse. Met behulp van de Graphics-klasse kunnen twee of meer afbeeldingen worden gecombineerd op zo'n manier dat de resulterende afbeelding eruit ziet als een volledige afbeelding zonder ruimte tussen de afbeeldingsdelen en zonder pagina's. De grootte van het canvas moet gelijk zijn aan de grootte van de resulterende afbeelding. Hieronder volgt de code-demonstratie die laat zien hoe de [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) methode van de [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) klasse kan worden gebruikt om afbeeldingen te combineren in één afbeelding.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **Afbeeldingen uitbreiden en bijsnijden**
Aspose.PSD API stelt u in staat om een afbeelding te vergroten of bij te snijden tijdens het conversieproces van de afbeelding. De ontwikkelaar moet een rechthoek maken met X- en Y-coördinaten en de breedte en hoogte van het rechthoekige vak specificeren. De X, Y en Breedte, Hoogte van de rechthoek zullen de vergroting of bijsnijden van de geladen afbeelding weerspiegelen. Als het nodig is om de afbeelding uit te breiden of bij te snijden tijdens de conversie van de afbeelding, voer dan de volgende stappen uit:

1. Maak een instantie van de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) klasse en laad de bestaande afbeelding.
1. Maak een instantie van de ImageOption-klasse.
1. Maak een instantie van de [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) klasse en initialiseer de X, Y en Breedte, Hoogte van de rechthoek
1. Roep de [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) methode van de RasterImage-klasse aan en geef de uitvoerbestandsnaam, de afbeeldingsopties en het rechthoekobject door als parameters.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **XMP-gegevens lezen en schrijven naar afbeeldingen**
XMP (Extensible Metadata Platform) is een ISO-standaard. XMP standaardiseert een gegevensmodel, een serialisatieformaat en kern-eigenschappen voor de definitie en verwerking van uitgebreide metagegevens. Het biedt ook richtlijnen voor het insluiten van XMP-informatie in een populaire afbeelding zoals JPEG, zonder de leesbaarheid te verbreken door applicaties die XMP niet ondersteunen. Met behulp van de Aspose.PSD voor .NET API kunnen ontwikkelaars XMP-metagegevens lezen of schrijven naar afbeeldingen. Dit artikel toont hoe XMP-metagegevens kunnen worden gelezen van een afbeelding en XMP-metagegevens naar afbeeldingen kunnen worden geschreven.
### **Maak XMP-metadata, schrijf deze en lees van bestand**
Met behulp van de Xmp-namespace kan de ontwikkelaar een XMP-metadata-object maken en deze schrijven naar een afbeelding. Het volgende codefragment toont hoe u de pakketten XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage en DublinCorePackage kunt gebruiken die zijn opgenomen in de [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp) namespace.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **Afbeeldingen exporteren in een multithread-omgeving**
Aspose.PSD voor .NET ondersteunt nu het converteren van afbeeldingen in een multithread-omgeving. Aspose.PSD voor .NET zorgt voor geoptimaliseerde prestaties van bewerkingen tijdens de uitvoering van code in een multithread-omgeving. Alle [beeldoptie](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) klassen (bijv. BmpOptions, TiffOptions, JpegOptions, enz.) in de Aspose.PSD voor .NET implementeren de IDisposable-interface. Daarom is het belangrijk dat de ontwikkelaar het beeldoptiesklasse-object correct verwijdert als de Source-eigenschap is ingesteld. Het volgende codefragment demonstreert deze functionaliteit.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD ondersteunt nu de SyncRoot-eigenschap bij het werken in een multithread-omgeving. Een ontwikkelaar kan deze eigenschap gebruiken om de toegang tot de bronstream te synchroniseren. Het volgende codefragment toont hoe de SyncRoot-eigenschap kan worden gebruikt.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}

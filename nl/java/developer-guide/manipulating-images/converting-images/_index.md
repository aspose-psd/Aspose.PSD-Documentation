---
title: Afbeeldingen converteren
type: docs
weight: 20
url: /nl/java/afbeeldingen-converteren/
---

## **Afbeeldingen converteren naar zwart-wit en grijswaarden**
Soms moet u gekleurde afbeeldingen converteren naar zwart-wit of grijswaarden voor afdruk- of archiveringsdoeleinden. Dit artikel toont het gebruik van de Aspose.PSD voor Java API om dit te bereiken met behulp van twee hieronder beschreven methoden.

- Binarisatie
- Grijswaarden
### **Binarisatie**
Om het concept van binarisatie te begrijpen, is het belangrijk om een binaire afbeelding te definiëren; dat is een digitale afbeelding die slechts twee mogelijke waarden kan hebben voor elk pixel. Normaal gesproken worden de twee kleuren die voor een binaire afbeelding worden gebruikt zwart en wit, hoewel elke twee kleuren kunnen worden gebruikt. Binarisatie is het proces van het omzetten van een afbeelding naar bi-niveau, wat betekent dat elk pixel wordt opgeslagen als een enkel bit (0 of 1) waarbij 0 de afwezigheid van kleur aangeeft en 1 de aanwezigheid van kleur betekent. De Aspose.PSD voor Java API ondersteunt momenteel twee binarisatiemethoden.
#### **Binarisatie met Vaste Drempelwaarde**
Het volgende codefragment toont hoe binarisatie met een vaste drempelwaarde kan worden toegepast op een afbeelding.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Binarisatie met Otsu-drempelwaarde**
Het volgende codefragment toont hoe binarisatie met Otsu-drempelwaarde kan worden toegepast op een afbeelding.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Grijswaarden**
Grijswaarden is het proces van het omzetten van een continue-afbeelding naar een afbeelding met onderbroken grijstinten. Het volgende codefragment toont hoe u grijswaarden kunt gebruiken.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Converteer GIF-afbeeldingslagen naar TIFF-afbeelding**
Soms is het nodig om lagen van een PSD-afbeelding te extraheren en converteren naar een ander rasterafbeeldingsformaat om aan de behoefte van een applicatie te voldoen. Aspose.PSD API ondersteunt de functie om lagen van een PSD-afbeelding te extraheren en om te zetten naar een ander rasterafbeeldingsformaat. Allereerst maken we een instantie van een afbeelding en laden we de PSD-afbeelding van de lokale schijf en daarna zullen we elke laag in de Layer-eigenschap doorlopen. Vervolgens zullen we het blok converteren naar een TIFF-afbeelding. Het onderstaande codefragment toont hoe u PSD-afbeeldingslagen naar TIFF-afbeeldingen kunt converteren.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **PSD naar CMYK TIFF converteren**
Met Aspose.PSD voor Java kunnen ontwikkelaars een CMYK PSD-bestand naar CMYK-tiff-indeling converteren. Dit artikel toont hoe u een CMYK PSD-bestand naar CMYK-tiff-indeling kunt exporteren/converteren met Aspose.PSD. Met Aspose.PSD voor Java kunt u PSD-afbeeldingen laden en vervolgens verschillende eigenschappen instellen met behulp van de TiffOptions-klasse en de afbeelding opslaan of exporteren. Het volgende codefragment toont hoe u deze functie kunt gebruiken.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Afbeeldingen exporteren**
Naast een uitgebreide reeks beeldverwerkingsroutines, biedt Aspose.PSD gespecialiseerde klassen om PSD-bestandsindelingen naar andere indelingen te converteren. Het omzetten van PSD-afbeeldingen is heel eenvoudig en intuïtief met behulp van deze library. Hieronder staan enkele gespecialiseerde klassen voor dit doel in de ImageOptions-namespace.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Het is eenvoudig om PSD-afbeeldingen te exporteren met de Aspose.PSD voor Java API. Het enige wat u nodig heeft is een object van de juiste klasse uit de ImageOptions-namespace. Door deze klassen te gebruiken, kunt u gemakkelijk elke afbeelding die is gemaakt, bewerkt of eenvoudigweg geladen met de Aspose.PSD voor Java exporteren naar een ondersteund formaat.
## **Afbeeldingen combineren**
Dit voorbeeld maakt gebruik van de Graphics-klasse en laat zien hoe u twee of meer afbeeldingen kunt combineren tot een enkele complete afbeelding. Om de bewerking te demonstreren, maakt het voorbeeld een nieuwe PsdImage en tekent afbeeldingen op het canvasscherm met behulp van de Draw Image-methode die wordt blootgesteld door de Graphics-klasse. Met de Graphics-klasse kunnen twee of meer afbeeldingen op zo'n manier worden gecombineerd dat de resulterende afbeelding eruit zal zien als een complete afbeelding zonder ruimte tussen de afbeeldingsdelen en zonder pagina's. De canvassize moet gelijk zijn aan de grootte van de resulterende afbeelding. Hieronder volgt de code die laat zien hoe u de Draw Image-methode van de Graphics-klasse kunt gebruiken om afbeeldingen te combineren in één afbeelding.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Afbeeldingen uitbreiden en bijsnijden**
Aspose.PSD API stelt u in staat om een afbeelding uit te breiden of bij te snijden tijdens het conversieproces van de afbeelding. De ontwikkelaar moet een rechthoek maken met X- en Y-coördinaten en de breedte en hoogte van het rechthoekvak specificeren. De X, Y en Breedte, Hoogte van de rechthoek geven de uitbreiding of bijsnijden van de geladen afbeelding aan. Als het nodig is om de afbeelding uit te breiden of bij te snijden tijdens de conversie van de afbeelding, voer dan de volgende stappen uit:

1. Maak een instantie van de klasse RasterImage en laad de bestaande afbeelding.
1. Maak een instantie van de ImageOption-klasse.
1. Maak een instantie van de klasse Rectangle en initialiseer de X, Y en Breedte, Hoogte van de rechthoek.
1. Roep de methode Save van de klasse RasterImage aan en geef de uitvoerbestandsnaam, afbeeldingsopties en het rechthoekobject als parameters door.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **XMP-gegevens lezen en schrijven naar afbeeldingen**
XMP (Extensible Metadata Platform) is een ISO-standaard. XMP standaardiseert een gegevensmodel, een serialisatieformaat en kernkenmerken voor de definitie en verwerking van uitbreidbare metadata. Het biedt ook richtlijnen voor het insluiten van XMP-informatie in populaire beeldformaten zoals JPEG, zonder de leesbaarheid te schaden door toepassingen die XMP niet ondersteunen. Met de Aspose.PSD voor Java API kunnen ontwikkelaars XMP-metadata naar afbeeldingen lezen of schrijven. Dit artikel toont hoe XMP-metadata van een afbeelding kunnen worden gelezen en XMP-metadata naar afbeeldingen kunnen worden geschreven.
### **Maak XMP-metadata, schrijf het en lees van bestand**
Met behulp van de XMP-namespace kan de ontwikkelaar een XMP-metadata-object maken en het naar een afbeelding schrijven. Het volgende codefragment toont hoe u de pakketten XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage en DublinCorePackage kunt gebruiken, die zijn opgenomen in de XMP-namespace.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Afbeeldingen exporteren in een meerdere-gewinde omgeving**
Aspose.PSD voor Java ondersteunt nu het converteren van afbeeldingen in een meerdere-gewinde omgeving. Aspose.PSD voor Java garandeert de geoptimaliseerde prestaties van operaties tijdens de uitvoering van code in een meerdere-gewinde omgeving. Alle klassen van afbeeldingsopties (bijv. BmpOptions, TiffOptions, JpegOptions, enz.) in de Aspose.PSD voor Java implementeren de IDisposable-interface. Daarom is het een must dat de ontwikkelaar het object van de afbeeldingsoptiesklasse op de juiste manier verwijdert als de Source-eigenschap is ingesteld. Het volgende codefragment toont de genoemde functionaliteit.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



Aspose.PSD ondersteunt nu de SyncRoot-eigenschap bij het werken in een meerdere-gewinde omgeving. Een ontwikkelaar kan deze eigenschap gebruiken om toegang tot de brondatabuffer te synchroniseren. Het volgende codefragment toont hoe de SyncRoot-eigenschap kan worden gebruikt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

---
title: Het maken, openen en opslaan van afbeeldingen
type: docs
weight: 30
url: /nl/java/het-maken-openen-en-opslaan-van-afbeeldingen/
---

## **Afbeeldingsbestanden maken**
Aspose.PSD voor Java stelt ontwikkelaars in staat om hun eigen afbeeldingen te maken. Gebruik de statische Create-methode die wordt blootgesteld door de Image-klasse om nieuwe afbeeldingen te maken. Het enige wat je hoeft te doen is het juiste object van een van de klassen uit de ImageOptions-naamruimte te leveren voor het gewenste uitvoerbeeldformaat. Om een ​​afbeeldingsbestand te maken, maak eerst een instantie van een van de klassen uit de ImageOptions-naamruimte. Deze klassen bepalen het uitvoerbeeldformaat. Hieronder staan enkele klassen uit de ImageOptions-naamruimte (let op dat op dit moment alleen bestandsindelingen van het PSD-bestandstype worden ondersteund voor creatie): 

PsdOptions stelt de opties in voor het maken van een PSD-bestand. Afbeeldingsbestanden kunnen worden aangemaakt door een uitvoerpad in te stellen of door een stream in te stellen.
### **Maken door Pad in te stellen**
Maak een PsdOptions van de ImageOptions-naamruimte en stel verschillende eigenschappen in. De belangrijkste eigenschap om in te stellen is de Source-eigenschap. Deze eigenschap geeft aan waar de afbeeldingsgegevens zich bevinden (in een bestand of een stream). In het onderstaande voorbeeld is de bron een bestand. Nadat de eigenschappen zijn ingesteld, geef je het object door aan een van de statische Create-methoden samen met de breedte- en hoogteparameter. De breedte en hoogte worden gedefinieerd in pixels.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Maken met behulp van Stream**
Het proces om een afbeelding te maken met behulp van een stream is hetzelfde als voor het gebruik van een pad. Het enige verschil is dat je een instantie van StreamSource moet maken door een Stream-object door te geven aan de constructor en dit toe te wijzen aan de Source-eigenschap.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Afbeeldingsbestanden openen**
Ontwikkelaars kunnen de Aspose.PSD voor Java API gebruiken om bestaande PSD-afbeeldingsbestanden te openen voor verschillende doeleinden, zoals het toevoegen van effecten aan de afbeelding of het converteren van een bestand naar een ander formaat. Wat het doel ook is, Aspose.PSD biedt twee standaard manieren om bestaande bestanden te openen: vanuit een bestand of vanuit een stream.
### **Openen vanuit Schijf**
Open een afbeeldingsbestand door het pad en de bestandsnaam als parameter door te gegeven aan de statische Load-methode die wordt blootgesteld door de Image-klasse.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Openen met behulp van een Stream**
Soms wordt de afbeelding die we willen openen opgeslagen als een stream. In dergelijke gevallen gebruik je de overbelaste versie van de Load-methode. Deze accepteert een Stream-object als argument om de afbeelding te openen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Afbeelding laden als laag**
Dit artikel demonstreert het gebruik van Aspose.PSD om een afbeelding als laag te laden. Aspose.PSD API's hebben efficiënte en gemakkelijk te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD heeft de AddLayer-methode van de PsdImage-klasse blootgelegd om een afbeelding toe te voegen aan een PSD-bestand als laag.

De stappen om een afbeelding in PSD als laag te laden zijn zo eenvoudig als hieronder:

- Maak een instantie van een afbeelding met de PsdImage-klasse met de opgegeven breedte en hoogte.
- Laad een PSD-bestand als een afbeelding door de fabrieksmethode Load blootgesteld door de Image-klasse.
- Maak een instantie van de Layer-klasse en wijs de PSD-afbeeldingslaag eraan toe.
- Voeg de gecreëerde laag toe met behulp van de AddLayer-methode blootgesteld door de PsdImage-klasse.
- Bewaar de resultaten.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Afbeeldingsbestanden opslaan**
Aspose.PSD stelt je in staat om afbeeldingsbestanden vanaf nul te maken. Het biedt ook de middelen om bestaande afbeeldingsbestanden te bewerken. Zodra de afbeelding is gemaakt of aangepast, wordt het bestand meestal opgeslagen op schijf. Aspose.PSD biedt methoden om afbeeldingen op te slaan op een schijf door een pad op te geven of door een Stream-object te gebruiken.
### **Opslaan op Schijf**
De Image-klasse vertegenwoordigt een beeldobject, dus deze klasse biedt alle benodigde tools om een afbeeldingsbestand te maken, te laden en op te slaan. Gebruik de Save-methode van de Image-klasse om afbeeldingen op te slaan. Een overbelaste versie van de Save-methode accepteert de bestandslocatie als een tekenreeks.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Opslaan naar een Stream**
Een andere overbelaste versie van de Save-methode accepteert het Stream-object als argument en slaat het afbeeldingsbestand op naar de stream.

Als de afbeelding is gemaakt door een van de CreateOptions te specificeren in de Image-constructor, wordt de afbeelding automatisch opgeslagen naar het opgegeven pad of de stream tijdens de initialisatie van de Image-klasse door de Save-methode aan te roepen die geen parameter accepteert.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Instellen voor Vervangen van Ontbrekende Lettertypen**
Ontwikkelaars kunnen de Aspose.PSD voor Java API gebruiken om bestaande PSD-afbeeldingsbestanden te laden voor verschillende doeleinden, bijvoorbeeld om standaard lettertypenaam in te stellen bij het opslaan van PSD-documenten als rasterafbeeldingen (in PNG, JPG en BMP-formaten). Dit standaardlettertype moet worden gebruikt als vervanging voor alle ontbrekende lettertypen (lettertypen die niet worden gevonden in het huidige besturingssysteem). Zodra de afbeelding is aangepast, wordt het bestand opgeslagen op schijf.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}


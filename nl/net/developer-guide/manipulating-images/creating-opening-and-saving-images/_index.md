---
title: Het maken, openen en opslaan van afbeeldingen
type: docs
weight: 30
url: /nl/het-maken-openen-en-opslaan-van-afbeeldingen/
---

## **Afbeeldingsbestanden maken**
Aspose.PSD voor .NET stelt ontwikkelaars in staat om hun eigen afbeeldingen te maken. Gebruik de statische Create-methode die wordt blootgesteld door de Image-klasse om nieuwe afbeeldingen te maken. Het enige wat je hoeft te doen is het juiste object van een van de klassen uit de ImageOptions-namespace te leveren voor het gewenste uitvoerformaat van de afbeelding. Om een afbeeldingsbestand te maken, maak eerst een instantie aan van een van de klassen uit de ImageOptions-namespace. Deze klassen bepalen het uitvoerformaat van de afbeelding. Hieronder staan enkele klassen uit de ImageOptions-namespace (let op dat op dit moment alleen bestanden van het PSD-bestandsformaat worden ondersteund voor creatie):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) stelt de opties in voor het maken van een PSD-bestand. Afbeeldingsbestanden kunnen worden gemaakt door een uitvoerpad in te stellen of door een stream in te stellen.
### **Maken door het instellen van een pad**
Maak PsdOptions uit de [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace en stel de verschillende eigenschappen in. De belangrijkste eigenschap om in te stellen is de Source-eigenschap. Deze eigenschap geeft aan waar de afbeeldingsgegevens zich bevinden (in een bestand of een stream). In het onderstaande voorbeeld is de bron een bestand. Nadat de eigenschappen zijn ingesteld, geef het object door aan een van de statische [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create)-methoden samen met de parameters voor breedte en hoogte. De breedte en hoogte worden in pixels gedefinieerd.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-AfbeeldingenMakenEnOpmaak-MakenDoorPadInTeStellen-MakenDoorPadInTeStellen.cs" >}}
### **Maken door gebruik te maken van een stream**
Het proces voor het maken van een afbeelding met behulp van een stream is hetzelfde als voor het gebruik van een pad. Het enige verschil is dat je een instantie van [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) moet maken door een Stream-object door te geven aan de constructor en dit toe te wijzen aan de Source-eigenschap.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-AfbeeldingenMakenEnOpmaak-MakenMetStream-MakenMetStream.cs" >}}
## **Afbeeldingsbestanden openen**
Ontwikkelaars kunnen de Aspose.PSD voor .NET API gebruiken om bestaande PSD-afbeeldingsbestanden te openen voor verschillende doeleinden, zoals het toevoegen van effecten aan de afbeelding of het converteren van een bestaand bestand naar een ander formaat. Wat het doel ook is, Aspose.PSD biedt twee standaardmanieren om bestaande bestanden te openen: vanuit een bestand of vanuit een stream.
### **Openen vanuit schijf**
Open een afbeeldingsbestand door het pad en de bestandsnaam als parameters door te gegeven aan de statische Load-methode die wordt blootgesteld door de Image-klasse.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversie-OpslaanOpSchijf-OpslaanOpSchijf.cs" >}}
### **Openen met behulp van een stream**
Soms is de afbeelding die we moeten openen opgeslagen als een stream. In dergelijke gevallen gebruik je de overloaded versie van de Load-methode. Dit accepteert een Stream-object als argument om de afbeelding te openen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversie-LadenVanStream-LadenVanStream.cs" >}}
### **Afbeelding laden als laag**
Dit artikel demonstreert het gebruik van Aspose.PSD om een afbeelding als een laag te laden. Aspose.PSD API's hebben efficiënte en gemakkelijk te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD heeft de AddLayer-methode van de PsdImage-klasse blootgesteld om een afbeelding aan een PSD-bestand toe te voegen als een laag.

De stappen om een afbeelding in PSD te laden als een laag zijn als volgt:

- Maak een instantie van een afbeelding met de PsdImage-klasse met een gespecificeerde breedte en hoogte.
- Laad een PSD-bestand als een afbeelding met de factory-methode Load die wordt blootgesteld door de Image-klasse.
- Maak een instantie van de Layer-klasse en wijs de PSD-afbeeldingslaag toe.
- Voeg de gecreëerde laag toe met de AddLayer-methode die beschikbaar is gesteld door de PsdImage-klasse.
- Sla de resultaten op.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-BewerkenEnConverterenAfbeeldingen-PSD-AfbeeldingLadenNaarPSD-AfbeeldingLadenNaarPSD.cs" >}}
### **Afbeelding laden als laag vanuit een stream**
Dit artikel demonstreert het gebruik van Aspose.PSD om een afbeelding als een laag vanuit een stream te laden. Om een afbeelding vanuit een stream te laden, geef eenvoudig een streamobject door dat een afbeelding bevat aan de constructor van de Layer-klasse. Voeg de gecreëerde laag toe met de AddLayer-methode die wordt blootgesteld door de PsdImage-klasse en sla de resultaten op.


Hier is de voorbeeldcode.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Openen-AfbeeldingLadenVanStream-AfbeeldingLadenVanStream.cs" >}}
## **Afbeeldingsbestanden opslaan**
Aspose.PSD stelt je in staat om afbeeldingsbestanden helemaal opnieuw te maken. Het biedt ook de middelen om bestaande afbeeldingsbestanden te bewerken. Zodra de afbeelding is gemaakt of aangepast, wordt het bestand meestal opgeslagen op de schijf. Aspose.PSD biedt methoden om afbeeldingen op te slaan naar een schijf door een pad op te geven of door het gebruik van een Stream-object.
### **Opslaan naar schijf**
De Image-klasse vertegenwoordigt een afbeeldingsobject, dus deze klasse biedt alle tools die nodig zijn om een afbeeldingsbestand te maken, laden en op te slaan. Gebruik de Image-klasse Save-methode om afbeeldingen op te slaan. Een overloaded versie van de Save-methode accepteert de bestandslocatie als een string.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversie-OpslaanOpSchijf-OpslaanOpSchijf.cs" >}}
### **Opslaan naar een stream**
Een andere overloaded versie van de Save-methode accepteert het Stream-object als argument en slaat het afbeeldingsbestand op naar de stream.

Als de afbeelding is gemaakt door een van de CreateOptions in de Image-constructor te specificeren, wordt de afbeelding automatisch opgeslagen op het pad of de stream die wordt opgegeven tijdens de initialisatie van de Image-klasse door de Save-methode te bellen die geen enkele parameter accepteert.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversie-OpslaanNaarStream-OpslaanNaarStream.cs" >}}
### **Instelling voor het vervangen van ontbrekende lettertypen**
Ontwikkelaars kunnen de Aspose.PSD voor .NET API gebruiken om bestaande PSD-afbeeldingsbestanden te laden voor verschillende doeleinden, bijvoorbeeld om standaard lettertype in te stellen wanneer PSD-documenten worden opgeslagen als een rasterafbeelding (in PNG, JPG en BMP formaten). Dit standaardlettertype moet worden gebruikt als vervanging voor alle ontbrekende lettertypen (lettertypen die niet worden gevonden in het huidige besturingssysteem). Zodra de afbeelding is aangepast, wordt het bestand opgeslagen op de schijf.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-Conversie-InstellingVoorVervangenOntbrekendeLettertypen-InstellingVervangingOntbrekendeLettertypen.cs" >}}

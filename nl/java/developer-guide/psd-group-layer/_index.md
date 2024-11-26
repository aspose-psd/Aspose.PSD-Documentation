---
title: Voorbeeld van het gebruik van groepslagen in Aspose.PSD voor Java
weight: 100
type: docs
description: Het gebruik van Groepslaag van het PSD-bestand via Java
keywords: [laaggroep, groepslaag, laag toevoegen aan groep, psd api, java, codevoorbeeld]
url: nl/java/psd-group-layer/
---

## **Overzicht**

Het gebruik van groepslagen in Aspose.PSD voor Java verbetert uw vermogen om lagen binnen een PSD-afbeelding effectief te beheren en te organiseren. Groepslagen, ook wel maplagen genoemd, stellen u in staat om meerdere lagen samen te voegen en transformaties of effecten gezamenlijk toe te passen.

Om te beginnen, maakt u een nieuwe PSD-afbeelding met behulp van de PsdImage.create() methode. Initialiseer vervolgens een nieuw LayerGroup object via de addLayerGroup methode van het PsdImage object. Geef de gewenste naam voor de groepslaag ("Map"), specificeer de invoegindex (0) en stel een boolean vlag in die de zichtbaarheid aangeeft (True).

Maak vervolgens twee Layer objecten aan en stel hun weergavenamen in met behulp van de setDisplayName methode. Voeg deze lagen toe aan de groepslaag met behulp van de addLayer methode.

Om toegang te krijgen tot de lagen binnen de groep, maak gebruik van de layers eigenschap van het LayerGroup object. Bevestig dat de weergavenamen van de eerste en tweede lagen in de groep respectievelijk "Laag 1" en "Laag 2" zijn.

Nadat u de groepslagen heeft gemanipuleerd, slaat u de gewijzigde PSD-afbeelding op met behulp van de save methode van het PsdImage object.

Dit dient als een fundamenteel voorbeeld om u vertrouwd te maken met het werken met groepslagen met behulp van Aspose.PSD voor Java. De bibliotheek biedt een overvloed aan geavanceerde functies voor laagmanipulatie en transformatie binnen PSD-afbeeldingen. Voor meer details en voorbeelden over het benutten van groepslagen en andere functionaliteiten van de bibliotheek, raadpleegt u de Aspose.PSD for Java documentatie.

Om met groepslagen in Aspose.PSD voor Java te werken, gebruikt u de LayerGroup klasse. Hieronder staat een codefragment dat illustreert hoe u een groepslaag maakt, lagen eraan toevoegt en de gewijzigde PSD-afbeelding opslaat.

Raadpleeg het volledige voorbeeld dat is verstrekt.

## **Voorbeeld**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}

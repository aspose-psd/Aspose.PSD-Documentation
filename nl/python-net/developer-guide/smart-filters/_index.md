---
title: Slimme Filter Manipulatie in Aspose.PSD voor Python
weight: 100
type: docs
description: Voorbeelden van het gebruik van Slimme Filters in een PSD bestand
keywords: [slimme filter, ruis toevoegen, gaussische vervaging, verscherpen, filter, psd filter, psd api, python, codevoorbeeld]
url: nl/python-net/smart-filters/
---

## **Overzicht**

Er zijn 3 manieren om slimme filters toe te passen in Aspose.PSD voor Python.

## **Directe Filter Toepassing**
In dit codevoorbeeld zien we een voorbeeld van hoe slimme filters direct kunnen worden toegepast in Aspose.PSD voor Python.

Eerst specificeert de code het bron-PSD bestand, het uitvoerbestand voor de originele afbeelding, en het uitvoerbestand voor de bijgewerkte afbeelding.

Vervolgens laadt de code de PSD-afbeelding met behulp van de Image.load() methode en zet deze om naar een PsdImage object.

De originele afbeelding wordt vervolgens opgeslagen met behulp van de save() methode, waarbij de uitvoerbestandsnaam wordt gespecificeerd.

Een SharpenSmartFilter object wordt aangemaakt, dat het slimme filter vertegenwoordigt dat moet worden toegepast.

Vervolgens haalt de code de reguliere laag op uit de PSD-afbeelding met behulp van im.layers[1].

Een lus wordt vervolgens gebruikt om het sharpenFilter drie keer toe te passen op de reguliere laag.

Tot slot wordt de bijgewerkte afbeelding opgeslagen met behulp van de save() methode en de uitvoerbestandsnaam gespecificeerd.

Deze code demonstreert hoe slimme filters direct kunnen worden toegepast in Aspose.PSD voor Python. Door de juiste filterobjecten te gebruiken en deze toe te passen op de gewenste lagen, kunt u de gewenste effecten op uw afbeeldingen bereiken.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentatie-Python-Aspose-psd-slimme-filter-direct-toepassen.py" >}}

## **Manipulatie van Slimme Filters in De Slimme Objecten**

Eerst specificeert de code het bron-PSD bestand, het uitvoerbestand voor de originele afbeelding, en het uitvoerbestand voor de bijgewerkte afbeelding.

De PSD-afbeelding wordt geladen met behulp van de Image.load() methode, en vervolgens omgezet naar een PsdImage object.

De originele afbeelding wordt opgeslagen met behulp van de save() methode, waarbij de uitvoerbestandsnaam wordt gespecificeerd.

Vervolgens zet de code de tweede laag van de PSD-afbeelding om naar een SmartObjectLayer object, dat de slimme objectlaag vertegenwoordigt.

De code gaat vervolgens verder met het bewerken van de slimme filters. In dit voorbeeld wordt gedemonstreerd hoe er wordt gewerkt met twee soorten slimme filters: GaussianBlurSmartFilter en AddNoiseSmartFilter.

Voor de GaussianBlurSmartFilter, update de code de filterwaarden, waaronder de straal, mengmodus, dekking, en of deze al dan niet is ingeschakeld.

Voor de AddNoiseSmartFilter, zet de code de ruisverdeling op NoiseDistribution.UNIFORM.

Vervolgens voegt de code twee nieuwe filteritems toe aan de slimme objectlaag: nog een GaussianBlurSmartFilter en een AddNoiseSmartFilter.

Na het toevoegen van de nieuwe filters, past de code de wijzigingen toe met behulp van de update_resource_values() methode.

Tot slot demonstreert de code hoe de filters direct kunnen worden toegepast op de laag en op de masker van de laag met behulp van de apply() en apply_to_mask() methoden, respectievelijk.

De bijgewerkte afbeelding wordt vervolgens opgeslagen met behulp van de save() methode en de uitvoerbestandsnaam gespecificeerd.

Door dit codevoorbeeld te volgen, kunt u leren hoe u kunt werken met slimme filters in Aspose.PSD voor Python. De bibliotheek biedt een breed scala aan slimme filters, elk met een eigen set eigenschappen en methoden die kunnen worden aangepast om de gewenste effecten op uw afbeeldingen te bereiken.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentatie-Python-Aspose-psd-slimme-filter-kenmerken.py" >}}

## **Het Toepassen van Slimme Filters op Laagmasker**

Slimme Filters toepassen op Maskers: Een Krachtige Techniek voor Beeldbewerking

Slimme filters zijn een populaire functie in beeldbewerkingssoftware waarmee gebruikers verschillende filters en effecten op hun afbeeldingen kunnen toepassen. Een interessante techniek die kan worden bereikt met behulp van slimme filters is het toepassen ervan op maskers. In dit artikel zullen we verkennen hoe slimme filters op maskers kunnen worden toegepast en hun gebruik bespreken in de wereld van beeldbewerking.

Wat is een Masker? Voordat we ingaan op het toepassen van slimme filters op maskers, laten we eerst begrijpen wat een masker is. In beeldbewerking is een masker een grijswaardebeeld dat de transparantie van bepaalde delen van een afbeelding bepaalt. Een masker kan worden gebruikt om selectief filters, aanpassingen of effecten op specifieke delen van een afbeelding toe te passen, terwijl andere gebieden ongewijzigd blijven.

Slimme Filters toepassen op Maskers: Bij het toepassen van slimme filters op maskers worden de filters alleen toegepast op de gebieden die zijn gespecificeerd door het masker. Dit biedt nauwkeurige controle over welke delen van de afbeelding worden beïnvloed door het filter. Door het masker te manipuleren, kunt u de intensiteit en de omvang van het effect van het filter bepalen.

Controleer alstublieft het vorige voorbeeld en de methode: [API Referentie Het Toepassen van Een Slim Filter op Een Masker](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

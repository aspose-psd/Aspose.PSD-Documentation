---
title: Smart Filter Manipulation in Aspose.PSD for Java
weight: 100
type: docs
description: Voorbeelden van het gebruik van Slimme Filters in PSD-bestand
keywords: [smart filter, ruis toevoegen, gauss vervagen, verscherpen, filter, psd-filter, psd-api, java, voorbeeldcode]
url: nl/java/smart-filters/
---

## **Overzicht**

Er zijn 3 methoden om slimme filters toe te passen in Aspose.PSD voor Java.

## **Directe Filtertoepassing**
Deze codevoorbeeld toont hoe je direct slimme filters kunt toepassen in Aspose.PSD voor Java.

In eerste instantie definieert de code het bron-PSD-bestand, het uitvoerbestand voor het originele beeld en het uitvoerbestand voor het bijgewerkte beeld.

Vervolgens laadt de code het PSD-beeld met behulp van de Image.load() methode en cast het naar een PsdImage object.

Het originele beeld wordt opgeslagen met de save() methode, waarbij de uitvoerbestandsnaam wordt opgegeven.

Een SharpenSmartFilter object wordt geïnstantieerd om het gewenste slimme filter te vertegenwoordigen.

Vervolgens haalt de code de reguliere laag op uit het PSD-beeld met behulp van psdImage.getLayers()[1].

Een lus wordt gebruikt om de sharpenFilter drie keer toe te passen op de reguliere laag.

Uiteindelijk wordt het bijgewerkte beeld opgeslagen met behulp van de save() methode met de opgegeven uitvoerbestandsnaam.

Deze code illustreert de directe toepassing van slimme filters in Aspose.PSD voor Java. Door het gebruik van passende filterobjecten en deze toe te passen op gewenste lagen, kunnen gewenste effecten worden bereikt op afbeeldingen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## **Manipulatie Slimme Filters in De Slimme Objecten**

Deze codefragment schetst hoe je slimme filters kunt manipuleren binnen slimme objecten in Aspose.PSD voor Java.

In eerste instantie definieert de code het bron-PSD-bestand, het uitvoerbestand voor het originele beeld en het uitvoerbestand voor het bijgewerkte beeld.

Het PSD-beeld wordt geladen met behulp van de Image.load() methode en vervolgens gecast naar een PsdImage object.

Het originele beeld wordt opgeslagen met de save() methode, waarbij de uitvoerbestandsnaam wordt opgegeven.

Vervolgens wordt de tweede laag van het PSD-beeld gecast naar een SmartObjectLayer object, dat de slimme objectlaag vertegenwoordigt.

Vervolgens demonstreert de code het bewerken van slimme filters, waarbij twee typen worden getoond: GaussianBlurSmartFilter en AddNoiseSmartFilter.

Voor de GaussianBlurSmartFilter werkt de code filterwaarden bij zoals straal, mengmodus, dekking en activeringsstatus.

Voor de AddNoiseSmartFilter stelt de code de ruisverdeling in op NoiseDistribution.Uniform.

Vervolgens voegt de code twee nieuwe filteritems toe aan de slimme objectlaag: nog een GaussianBlurSmartFilter en een AddNoiseSmartFilter.

Na het toevoegen van nieuwe filters past de code de wijzigingen toe met behulp van de updateResourceValues() methode.

Ten slotte demonstreert de code het direct toepassen van filters op de laag en de masker ervan met respectievelijk de apply() en applyToMask() methoden.

Het bijgewerkte beeld wordt vervolgens opgeslagen met behulp van de save() methode met de opgegeven uitvoerbestandsnaam.

Door dit codevoorbeeld te volgen, kunt u begrijpen hoe u slimme filters kunt manipuleren binnen slimme objecten in Aspose.PSD voor Java. De bibliotheek biedt een breed scala aan slimme filters, elk met zijn eigen reeks eigenschappen en methoden die kunnen worden aangepast om gewenste effecten op afbeeldingen te bereiken.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## **Toepassen van Slimme Filters op Laagmasker**

Slimme Filters toepassen op Maskers: Een Krachtige Beeldbewerkingstechniek

Slimme filters, veel voorkomend in beeldbewerkingssoftware, stellen gebruikers in staat diverse filters en effecten toe te passen op hun afbeeldingen. Een intrigerende techniek mogelijk gemaakt door slimme filters is hun toepassing op maskers. Dit artikel verkent het toepassen van slimme filters op maskers en bespreekt hun nut in het gebied van beeldbewerking.

Masks Begrijpen: Voordat we ingaan op het toepassen van slimme filters op maskers, is het essentieel om het concept van een masker te begrijpen. In beeldbewerking is een masker een grijswaardenbeeld dat de transparantie van specifieke gebieden binnen een afbeelding dicteert. Maskers maken selectieve toepassing van filters, aanpassingen of effecten op specifieke delen van een afbeelding mogelijk terwijl andere onaangetast blijven.

Slimme Filters toepassen op Maskers: Wanneer slimme filters op maskers worden toegepast, beïnvloeden ze alleen de gebieden gespecificeerd door het masker, waardoor nauwkeurige controle over de impact van het filter mogelijk is. Door het masker te manipuleren, kunnen gebruikers de intensiteit en omvang van het effect van het filter moduleren.

Raadpleeg alsjeblieft het vorige voorbeeld en de methode: [API Referentie Toepassen van Slimme Filter op Masker](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

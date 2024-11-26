---
title: PSD-, PSB- en AI-bestanden openen en exporteren naar PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Voorbeeld van het exporteren van PSD-, PSB- en AI-bestanden naar andere indelingen
keywords: [psd bestand openen, ai bestand openen, psb bestand openen, exporteren naar png, exporteren naar pdf, exporteren naar jpeg, exporteren naar tiff, psd api, python, voorbeeldcode]
url: nl/python-net/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Overzicht**
Om PSD-, PSB- en AI-bestanden naar verschillende indelingen om te zetten, kunt u de Aspose.PSD-bibliotheek in Python gebruiken. Deze bibliotheek biedt verschillende opties en instellingen om het conversieproces aan te passen.

Allereerst moet u de benodigde klassen en modules uit de Aspose.PSD-bibliotheek importeren. Zorg ervoor dat u de bibliotheek hebt geïnstalleerd voordat u de code uitvoert.

In deze code definiëren we diverse opties voor verschillende indelingen, zoals PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB en PSD. Met deze opties kunt u het uitvoerbestand aanpassen aan uw behoeften.

Vervolgens definiëren we een dictionary 'formats' die bestandsextensies koppelt aan de bijbehorende opslagopties.

Om een PSD-bestand naar andere indelingen om te zetten, moet u het PSD-bestand laden met PsdImage.load() en vervolgens door de 'formats'-dictionary itereren. Voor elke indeling geeft u de uitvoerbestandsnaam op en slaat u de afbeelding op met behulp van de image.save() methode.

Op dezelfde manier, om een AI-bestand naar andere indelingen om te zetten, laadt u het AI-bestand met AiImage.load() en itereert u door de 'formats'-dictionary. Geef de uitvoerbestandsnaam op en sla de afbeelding op met behulp van de image.save() methode.

Zorg ervoor dat u de juiste bestandspaden opgeeft voor de bron-PSD- en AI-bestanden.

Dat is alles! U kunt nu deze code gebruiken om PSD-, PSB- en AI-bestanden naar verschillende indelingen om te zetten met behulp van Aspose.PSD voor Python.

Bekijk het volledige voorbeeld hieronder.

## **Voorbeeld**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentatie-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}

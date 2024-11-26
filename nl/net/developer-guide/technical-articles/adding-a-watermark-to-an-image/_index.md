---
title: Het toevoegen van een watermerk aan een afbeelding
type: docs
weight: 30
url: /nl/het-toevoegen-van-een-watermerk-aan-een-afbeelding/
---

## **Het toevoegen van een watermerk aan een afbeelding**
Dit document legt uit hoe je een watermerk kunt toevoegen aan een afbeelding met behulp van Aspose.PSD. Het toevoegen van een watermerk aan een afbeelding is een veelvoorkomende eis voor beeldverwerkingsapplicaties. Dit voorbeeld gebruikt de Graphics-klasse om een tekenreeks op het oppervlak van de afbeelding te tekenen.
### **Watermerk toevoegen**
Om de werking te demonstreren, laden we een BMP-afbeelding van schijf en tekenen een tekenreeks als watermerk op het oppervlak van de afbeelding met behulp van de Graphics-klasse DrawString-methode. We slaan de afbeelding op in PNG-indeling met behulp van de PngOptions-klasse. Hieronder staat een codevoorbeeld dat laat zien hoe je een watermerk aan een afbeelding toevoegt. De broncode van het voorbeeld is opgesplitst in delen om de volgorde gemakkelijk te volgen. Stap voor stap tonen de voorbeelden hoe je:

1. [Laad](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) een afbeelding.
1. Maak en initialiseer een [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) object.
1. Maak en initialiseer Font- en [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush) objecten.
1. Teken een tekenreeks als watermerk met behulp van de Graphics-klasse [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) methode.
1. Sla de afbeelding op als PNG.

De volgende codefragment toont hoe je een watermerk aan de afbeelding toevoegt.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Een diagonaal watermerk toevoegen**
Een diagonaal watermerk toevoegen aan een afbeelding lijkt op het toevoegen van een horizontaal watermerk zoals hierboven besproken, met enkele verschillen. Om de werking te demonstreren, laden we een JPG-afbeelding van schijf, voegen we transformaties toe met behulp van een object van de [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix)-klasse en tekenen een tekenreeks als watermerk op het oppervlak van de afbeelding met behulp van de DrawString-methode van de Graphics-klasse. Hieronder staat een codevoorbeeld dat laat zien hoe je een diagonaal watermerk aan een afbeelding toevoegt. De broncode van het voorbeeld is opgesplitst in delen om de volgorde gemakkelijk te volgen. Stap voor stap tonen de voorbeelden hoe je:

1. Laad een afbeelding.
1. Maak en initialiseer een Graphics-object.
1. Maak en initialiseer [Font](https://reference.aspose.com/psd/net/aspose.psd/font)- en SolidBrush-objecten.
1. Vraag de grootte van de afbeelding op in een [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef)-object.
1. Maak een instantie van de Matrix-klasse en voer een samengestelde transformatie uit.
1. Wijs de transformatie toe aan het Graphics-object.
1. Maak en initialiseer een [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat)-object.
1. Teken een tekenreeks als watermerk met behulp van de DrawString-methode van de Graphics-klasse.
1. Sla het resulterende beeld op.

Het volgende codefragment toont hoe je een diagonaal watermerk toevoegt.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}

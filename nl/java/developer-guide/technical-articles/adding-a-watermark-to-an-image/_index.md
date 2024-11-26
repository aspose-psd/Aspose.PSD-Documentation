---
title: Het toevoegen van een watermerk aan een afbeelding
type: docs
weight: 20
url: /nl/het-toevoegen-van-een-watermerk-aan-een-afbeelding/
---

## **Het toevoegen van een watermerk aan een afbeelding**
Dit document legt uit hoe je een watermerk aan een afbeelding toevoegt met behulp van Aspose.PSD. Het toevoegen van een watermerk aan een afbeelding is een veelvoorkomende vereiste voor beeldverwerkingsapplicaties. Dit voorbeeld gebruikt de Graphics-klasse om een ​​tekst op het oppervlak van de afbeelding te tekenen.
### **Het toevoegen van een watermerk**
Om de bewerking te demonstreren, zullen we een BMP-afbeelding vanaf een schijf laden en een tekst als watermerk op het afbeeldingsoppervlak tekenen met behulp van de Graphics-klasse DrawString-methode. We zullen de afbeelding opslaan in PNG-indeling met behulp van de PngOptions-klasse. Hieronder staat een codevoorbeeld dat laat zien hoe je een watermerk aan een afbeelding toevoegt. De broncode van het voorbeeld is opgesplitst in delen om het gemakkelijk te volgen. Stap voor stap tonen de voorbeelden hoe je:

1. Een afbeelding laadt.
1. Een Graphics-object maakt en initialiseert.
1. Font- en SolidBrush-objecten maakt en initialiseert.
1. Een tekst als watermerk tekent met behulp van de Graphics-klasse DrawString-methode.
1. De afbeelding opslaat als PNG.

Het volgende codefragment laat zien hoe je een watermerk op de afbeelding toevoegt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Het toevoegen van een diagonaal watermerk**
Een diagonaal watermerk toevoegen aan een afbeelding is vergelijkbaar met het toevoegen van een horizontaal watermerk zoals hierboven besproken, met een paar verschillen. Om de bewerking te demonstreren, zullen we een JPG-afbeelding vanaf een schijf laden, transformaties toevoegen met behulp van een object van de Matrix-klasse en een tekst als watermerk op het afbeeldingsoppervlak tekenen met behulp van de Graphics-klasse DrawString-methode. Hieronder staat een codevoorbeeld dat laat zien hoe je een diagonaal watermerk aan een afbeelding toevoegt. De broncode van het voorbeeld is opgesplitst in delen om het gemakkelijk te volgen. Stap voor stap tonen de voorbeelden hoe je:

1. Een afbeelding laadt.
1. Een Graphics-object maakt en initialiseert.
1. Font- en SolidBrush-objecten maakt en initialiseert.
1. De grootte van de afbeelding in een SizeF-object krijgt.
1. Een instantie van de Matrix-klasse maakt en composiettransformatie uitvoert.
1. De transformatie toewijst aan het Graphics-object.
1. Een StringFormat-object maakt en initialiseert.
1. Een tekst als watermerk tekent met behulp van de Graphics-klasse DrawString-methode.
1. De resulterende afbeelding opslaat.

Het volgende codefragment laat zien hoe je een diagonaal watermerk toevoegt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}

---
title: Het tekenen van afbeeldingen
type: docs
weight: 10
url: /nl/java/het-tekenen-van-afbeeldingen/
---

## **Het tekenen van lijnen**
Dit voorbeeld maakt gebruik van de Graphics-klasse om lijnvormen op het afbeeldingsoppervlak te tekenen. Om de werking te demonstreren, maakt het voorbeeld een nieuwe afbeelding en tekent lijnen op het afbeeldingsoppervlak met de DrawLine-methode die wordt blootgesteld door de Graphics-klasse. Eerst zullen we een PsdImage maken waarbij de hoogte en breedte worden gespecificeerd.

Nadat de afbeelding is gemaakt, zullen we de Clear-methode gebruiken die wordt blootgesteld door de Graphics-klasse om de achtergrondkleur in te stellen. De DrawLine-methode van de Graphics-klasse wordt gebruikt om een ​​lijn op een afbeelding te tekenen die twee puntstructuren met elkaar verbindt. Deze methode heeft verschillende overbelastingen die de instantie van de Pen-klasse en coördinatenparen van punten of Point/PointF-structuren als argumenten accepteren. De Pen-klasse definieert een object dat wordt gebruikt om lijnen, krommen en figuren te tekenen. De Pen-klasse heeft verschillende overbelaste constructeurs om lijnen te tekenen met een gespecificeerde kleur, breedte en penseel. De SolidBrush-klasse wordt gebruikt om continu met een specifieke kleur te tekenen. Uiteindelijk wordt de afbeelding geëxporteerd naar het BMP-bestandsformaat. Het volgende codefragment laat zien hoe de lijnvormen op het afbeeldingsoppervlak kunnen worden getekend.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-HetTekenenvanAfbeeldingen-HetTekenenvanLijnen-HetTekenenvanLijnen.java" >}}

## **Het tekenen van een ellips**
Het voorbeeld van het tekenen van een ellips is het tweede artikel in de reeks vormen tekenen. We zullen de Graphics-klasse gebruiken om de ellipsvorm op het afbeeldingsoppervlak te tekenen. Om de werking te demonstreren, maakt het voorbeeld een nieuwe afbeelding en tekent de ellipsvorm op het afbeeldingsoppervlak met de DrawEllipse-methode die wordt blootgesteld door de Graphics-klasse. Eerst zullen we een PsdImage maken waarbij de hoogte en breedte worden gespecificeerd.

Nadat de afbeelding is gemaakt, zullen we een Graphics-klasse-object maken en initialiseren en de achtergrondkleur van de afbeelding instellen met behulp van de Clear-methode van de Graphics-klasse. De DrawEllipse-methode van de Graphics-klasse wordt gebruikt om de ellipsvorm op een afbeeldingsoppervlak te tekenen dat wordt gespecificeerd door de omgrenzende rechthoekstructuur. Deze methode heeft verschillende overbelastingen die de instanties van de Pen- en Rectangle/RectangleF-klassen accepteren of een paar coördinaten, een hoogte en een breedte als argumenten. De Pen-klasse definieert een object dat wordt gebruikt om lijnen, krommen en figuren te tekenen. De Pen-klasse heeft verschillende overbelaste constructeurs om lijnen te tekenen met een gespecificeerde kleur, breedte en penseel. De Rectangle-klasse slaat een reeks van vier gehele getallen op die de locatie en grootte van een rechthoek vertegenwoordigen. De Rectangle-klasse heeft verschillende overbelaste constructeurs om de rechthoekstructuur met gespecificeerde grootte en locatie te tekenen. De SolidBrush-klasse wordt gebruikt om continu met een specifieke kleur te tekenen. Uiteindelijk wordt de afbeelding geëxporteerd naar het BMP-bestandsformaat. Het volgende codefragment laat zien hoe de ellipsvorm op het afbeeldingsoppervlak kan worden getekend.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-HetTekenenvanAfbeeldingen-HetTekenenvanEllips-HetTekenenvanEllips.java" >}}

## **Het tekenen van een rechthoek**
In dit voorbeeld zullen we de rechthoekvorm op het afbeeldingsoppervlak tekenen. Om de werking te demonstreren, maakt het voorbeeld een nieuwe afbeelding en tekent de rechthoekvorm op het afbeeldingsoppervlak met de DrawRectangle-methode die wordt blootgesteld door de Graphics-klasse. Eerst zullen we een PsdImage maken waarbij de hoogte en breedte worden gespecificeerd. Vervolgens zullen we de achtergrondkleur van de afbeelding instellen met behulp van de Clear-methode van de Graphics-klasse.

De DrawRectangle-methode van de Graphics-klasse wordt gebruikt om de rechthoekvorm op een afbeeldingsoppervlak te tekenen dat wordt gespecificeerd door de rechthoekstructuur. Deze methode heeft verschillende overbelastingen die de instanties van de Pen- en Rectangle/RectangleF-klassen accepteren of een coördinaatpaar, een breedte en een hoogte als argumenten. De Rectangle-klasse slaat een reeks van vier gehele getallen op die de locatie en grootte van een rechthoek vertegenwoordigen. De Rectangle-klasse heeft verschillende overbelaste constructeurs om de rechthoekstructuur met gespecificeerde grootte en locatie te tekenen. Uiteindelijk wordt de afbeelding geëxporteerd naar het BMP-bestandsformaat. Het volgende codefragment laat zien hoe de rechthoekvorm op het afbeeldingsoppervlak kan worden getekend.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-HetTekenenvanAfbeeldingen-HetTekenenvanRechthoek-HetTekenenvanRechthoek.java" >}}

## **Het tekenen van een boog**
In deze sessie van de reeks vormen tekenen, zullen we de boogvorm op het afbeeldingsoppervlak tekenen. We zullen de DrawArc-methode van Graphics gebruiken om de werking op een BMP-afbeelding te demonstreren. Eerst zullen we een PsdImage maken waarbij de hoogte en breedte worden gespecificeerd. Nadat de afbeelding is gemaakt, zullen we de Clear-methode gebruiken die wordt blootgesteld door de Graphics-klasse om de achtergrondkleur in te stellen.

De DrawArc-methode van de Graphics-klasse wordt gebruikt om de boogvorm op een afbeeldingsoppervlak te tekenen. DrawArc representeert een deel van een ellips gespecificeerd door de rechthoekstructuur of paar coördinaten. Deze methode heeft verschillende overbelastingen die de instanties van de Pen-klassen en de Rectangle/RectangleF-structuur of een paar coördinaten, een breedte en een hoogte accepteren als argumenten. Uiteindelijk wordt de afbeelding geëxporteerd naar het BMP-bestandsformaat. Het volgende codefragment laat zien hoe de boogvorm op het afbeeldingsoppervlak kan worden getekend.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-HetTekenenvanAfbeeldingen-HetTekenenvanBoog-HetTekenenvanBoog.java" >}}

## **Het tekenen van een Bezier-kromme**
Dit voorbeeld maakt gebruik van de Graphics-klasse om de Bezier-vorm op het afbeeldingsoppervlak te tekenen. Om de werking te demonstreren, maakt het voorbeeld een nieuwe afbeelding en tekent de Bezier-vorm op het afbeeldingsoppervlak met behulp van de DrawBezier-methode die wordt blootgesteld door de Graphics-klasse. Eerst zullen we een PsdImage maken waarbij de hoogte en breedte worden gespecificeerd. Nadat de afbeelding is gemaakt, zullen we de Clear-methode gebruiken die wordt blootgesteld door de Graphics-klasse om de achtergrondkleur in te stellen.

De DrawBezier-methode van de Graphics-klasse wordt gebruikt om de Bezier-splinevorm op een afbeeldingsoppervlak te tekenen gedefinieerd door vier Point-structuren. Deze methode heeft verschillende overbelastingen die de instanties van de Pen-klasse en vier geordende coördinatenparen of vier Point/PointF-structuren of een array van Point/PointF-structuren accepteren. De Pen-klasse definieert een object dat wordt gebruikt om lijnen, krommen en figuren te tekenen. De Pen-klasse heeft verschillende overbelaste constructeurs om lijnen te tekenen met een gespecificeerde kleur, breedte en penseel. Uiteindelijk wordt de afbeelding geëxporteerd naar het BMP-bestandsformaat. Het volgende codefragment laat zien hoe de Bezier-vorm op het afbeeldingsoppervlak kan worden getekend.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-HetTekenenvanAfbeeldingen-HetTekenenvanBezier-HetTekenenvanBezier.java" >}}

## **Het tekenen van afbeeldingen met kernfunctionaliteit**
Aspose.PSD is een bibliotheek die veel waardevolle functies biedt, waaronder het maken van afbeeldingen vanaf nul. Teken met de kernfunctionaliteit zoals het manipuleren van bitmapinformatie van een afbeelding, of gebruik de geavanceerde functies zoals Graphics en GraphicsPath om vormen op het afbeeldingsoppervlak te tekenen met behulp van verschillende penselen en pennen. Met behulp van de RasterImage-klasse van Aspose.PSD kunt u de pixelinformatie van een afbeeldingsgebied ophalen en manipuleren. De RasterImage-klasse bevat de gehele kernfunctionaliteit van tekenen, zoals pixels ophalen en instellen en andere methoden voor het manipuleren van afbeeldingen. Maak een nieuwe afbeelding met een van de methoden die worden beschreven in het maken van bestanden en wijs het toe aan een instantie van de RasterImage-klasse. Gebruik de LoadPixels-methode van de RasterImage-klasse om de pixelinformatie van een deel van een afbeelding op te halen. Nadat u een array met pixels heeft, kunt u deze manipuleren door bijvoorbeeld de kleur van elke pixel te wijzigen. Nadat de pixelinformatie is gemanipuleerd, stelt u deze terug in het gewenste gebied in de afbeelding met behulp van de SavePixels-methode van de RasterImage-klasse. Het volgende codefragment laat zien hoe afbeeldingen kunnen worden getekend met behulp van kernfunctionaliteit.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-HetTekenenvanAfbeeldingen-KernTekenfunctionaliteiten-KernTekenfunctionaliteiten.java" >}}

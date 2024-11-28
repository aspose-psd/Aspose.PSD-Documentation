---
title: Ebenenanpassung in Schwarz-Weiß
type: docs
weight: 30
url: /de/java/layer-types/adjustment-layer/levels/
---

## Arbeiten mit der Photoshop Levels Ebenenanpassungsschicht in Java

In diesem Artikel werden wir lernen, wie man den Tonwertbereich und die Farbbalance eines Fotos im [PSD-Dateiformat](/psd/de/java/psd-format/) programmatisch in Java anpasst. Wir verwenden nicht den Foto-Editor Adobe® Photoshop® selbst. Stattdessen verwenden wir die Bibliothek Aspose.PSD für Java, die eigenständig funktioniert, um das Photoshop-Dokument zu manipulieren.

Obwohl Aspose.PSD für Java mehr als genug [Werkzeuge zur Bearbeitung von Fotos](/psd/de/java/manipulating-images/) unterstützt, entscheiden wir uns für die **API der Ebenenanpassungsschicht "Levels"**, die eine der einfachsten und schnellsten Möglichkeiten ist, die gewünschte Wirkung zu erzielen.

## API-Übersicht

Die aktuelle Implementierung (20.6 zum Zeitpunkt des Verfassens) der API der Ebenenanpassungsschicht "Levels" **unterstützt alle grundlegenden Funktionen von Photoshop Levels**, nämlich die Anpassung der Eingabe- und Ausgabewerte für den Kompositkanal (RGB) sowie für jeden primären Farbkanal (Rot, Grün und Blau).

Die API der Ebenenanpassungsschicht "Levels" ist unkompliziert. Die Klasse [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) ist der Einstiegspunkt für die Ebenenanpassung "Levels". Sie enthält ein paar Methoden zum Zugriff auf Farbkanäle: getMasterChannel und getChannel(int). Beide Methoden geben [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) zurück, der entsprechende Eigenschaften für die Manipulation der Eingabe- und Ausgabewerte hat. Der Unterschied besteht darin, dass getMasterChannel dazu dient, den Komposit-Farbkanaal (RGB) anzupassen, während getChannel auf einen bestimmten Farbkanal (Rot, Grün oder Blau) anhand seines Index zugreift.

## Kompatibilität mit Farbmodi

Es ist erwähnenswert, dass die Ebenenanpassungsschicht "Levels" **mit der überwiegenden Mehrheit der Farbmodi kompatibel ist**, gemäß den Photoshop Levels. Daher ist es möglich, Levels für Bilder in Graustufen (Grau-Kanal), RGB (RGB, Rot, Grün und Blau Kanäle), CMYK (CMYK, Cyan, Magenta, Gelb und Schwarz Kanäle), Duotone (Monoton-Kanal) und LAB (Helligkeit, a und b Kanäle) Farbmodi anzupassen.

## Anpassung des Tonwertbereichs

Einfach ausgedrückt werden Tonwertkorrekturen auf ein Bild angewendet, um die Schatten und Lichter für eine bessere Verteilung der mittleren Töne neu zu zuordnen. Im Allgemeinen **verleiht es dem Bild mehr Kontrast**, wenn es richtig gemacht wird. Beispielsweise nehmen wir ein Foto eines Hundes (b) und passen seinen Tonwertbereich an (a – der Screenshot stammt aus dem Photoshop Levels-Fenster für Klarheit), um das Bild kontrastreicher aussehen zu lassen (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Abbildung Levels-Ebene 1](levels-adjustment-figure-1.png)|

Um **den Gesamterkennungsbereich** eines Bildes anzupassen, sollten die Eingabe-Werte der Ebenenanpassungsschicht für den Hauptkanal festgelegt werden:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    levelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

Es ist wichtig zu beachten, dass die Eingabe-Werte im Bereich von 0 bis 253 für Schatten, von 9,99 bis 0,01 für mittlere Töne und von 2 bis 255 für Lichter liegen sollten. Der Bereich der Ausgabewerte muss zwischen 0 und 255 liegen.

Möchten Sie noch mehr Beispiele? Sie finden sie auf [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) und im [Wissensspeicher](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Fazit

Zusammenfassend hat Aspose.PSD für Java eine praktische und einfache API zur Änderung des Tonwertbereichs und der Farbbalance eines Bildes, die mit fast allen Farbmodi kompatibel ist. Die API der Ebenenanpassungsschicht "Levels" der Bibliothek ähnelt Photoshop Levels, daher ist es einfach, auch wenn Sie zuvor noch nie mit der Bibliothek gearbeitet haben.

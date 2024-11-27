---
title: Ebenenanpassungsebene für Helligkeit und Kontrast
type: docs
weight: 30
url: /de/java/layer-types/adjustment-layer/brightness-contrast/
---

# Arbeiten mit der Photoshop-Helligkeits/Kontrast-Anpassungsebene in Java

In diesem Artikel wenden wir eine Helligkeits-/Kontrastanpassung auf ein Adobe® Photoshop®-Dokument unter Verwendung der Aspose.PSD for Java®-Bibliothek an. Außerdem werden wir später mehr über die bibliotheksspezifischen Funktionen im Zusammenhang mit dieser Art von Anpassungsebene erfahren.

Aber zuerst etwas Theorie.

Die Helligkeits/Kontrast-Anpassungsebene ändert die Helligkeit und den Kontrast des Bildes. Aber Moment mal, was bedeutet das eigentlich? Eine Erhöhung der Helligkeit erhellt den Farbwert bis zu Weiß und eine Verringerung der Helligkeit verdunkelt den Farbwert bis zu Schwarz. Eine Erhöhung des Kontrasts wiederum erhöht den Unterschied zwischen hellen und dunklen Farben, und eine Verringerung des Kontrasts verringert diesen Unterschied entsprechend; das bedeutet, dass helle Farben heller und dunkle Farben dunkler werden.

## Die Farbmodusunterstützung

Die Bibliothek ermöglicht das Hinzufügen einer Helligkeits/Kontrast-Anpassungsebene zu Bildern im RGB-, CMYK- oder Lab-Farbmodus.

## Das aktuelle und das Legacy-Verhalten

Die aktuelle Implementierung der Bibliothek (v20.6 zum Zeitpunkt des Verfassens) verwendet den standardmäßigen Photoshop-Algorithmus, der den gesamten Tonwertbereich von den Schatten bis zu den Lichtern erhält, unterstützt jedoch noch nicht das Legacy-Verhalten. Das bedeutet, dass die Bibliothek die Helligkeits/Kontrast-Anpassungsebene in Dokumenten unterstützt, die in den neuesten Versionen von Photoshop (CS4 und höher) erstellt wurden. Wenn Sie es jedoch benötigen, können Sie die [Einführung des Legacy-Verhaltens der Helligkeits/Kontrast-Anpassungsebene auf unserem Forum anfordern](https://forum.aspose.com/c/psd).

## Helligkeit und Kontrast anpassen

Lassen Sie uns nun beschreiben, wie die High-Level-API der Helligkeits/Kontrast-Anpassungsebene funktioniert (vorausblickend ist die API unkompliziert). Die PsdImage-Klasse enthält eine Factory-Methode (addBrightnessContrastAdjustmentLayer) zur Instanziierung der BrightnessContrastLayer-Klasse, die das Tor für die Helligkeits- und Kontrastanpassung bildet. Die BrightnessContrastLayer-Klasse enthält lediglich ein paar Getter und Setter für den Zugriff auf die Helligkeits- und Kontrasteigenschaften sowie zum Ändern ihrer Werte.

![|Beispiel für eine Helligkeits/Kontrast-Anpassungsebene in PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

Nehmen wir also ein Bild eines Hundes (b) als Beispiel, um seine Helligkeit1 und seinen Kontrast2 (a) anzupassen, indem wir nur die Factory-Methode mit den entsprechenden Argumenten verwenden, um letztendlich ein Bild (c) zu erhalten, das lebendiger aussieht:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Hinweise:

1. Der Wert der Helligkeit muss im Bereich von -150 bis 150 liegen.
2. Der Wert des Kontrasts muss im Bereich von -50 bis 100 liegen.

Siehe die Dokumentation der [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) für weitere Details.

## Fazit

In diesem Artikel haben wir einen schnellen Überblick über die Helligkeits/Kontrast-Anpassungsebene bekommen und gelernt, wie man die Helligkeit und den Kontrast des Bildes mit der Factory-Methode anpasst.

Sehen Sie sich unsere Reihe von [Artikeln zu Anpassungsebenen-APIs](/de/java/layer-types/adjustment-layer/) von Aspose.PSD for Java an, um mehr zu erfahren.

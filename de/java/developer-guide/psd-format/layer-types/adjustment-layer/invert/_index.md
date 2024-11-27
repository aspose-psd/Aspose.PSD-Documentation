---
title: Ebenenanpassungsebene umkehren
type: docs
weight: 30
url: /de/java/ebenenarten/ebenanpassungsebene/umkehren/
---

# Arbeiten mit der Invertieren-Anpassungsebene in Photoshop in Java

In diesem Artikel zeigen wir, wie man ein Bild in einem Photoshop-Dokument programmgesteuert in ein negatives umwandelt. Hierfür verwenden wir die Bibliothek zur Manipulation von PSD-Dateiformaten namens Aspose.PSD für Java.

Die Farbinversions-API ermöglicht es, **einen Negativ-Effekt auf ein Bild anzuwenden**. Vielleicht haben Sie bereits gesehen, wie man die Farben eines Bildes mithilfe einer Kurven-Anpassungsebene [invertiert](/psd/de/java/ebenenarten/ebenanpassungsebene/kurven/). Heute betrachten wir jedoch einen schnelleren und einfacheren Weg, dies mit der Invertieren-Anpassungsebene zu erreichen.

## API-Übersicht

**Die API der Invertieren-Anpassungsebene** besteht aus der Ebenenklasse selbst, die [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer) heißt. Diese Klasse hat keine eigenen öffentlichen Elemente, da sie alle öffentlichen Elemente von der Elternklasse ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)) erbt. Dies vereinfacht die Verwendung, da alles, was Sie tun müssen, ist es zur PSD-Datei hinzuzufügen und das Bild wird negativ.

## Farben eines Bildes invertieren

Auch wenn es offensichtlich erscheint, wollen wir zur Klarheit demonstrieren, wie man der Abbildung eines Astronauten (a) den **Invertieren-Anpassungsebene-Effekt** hinzufügt, um für dieses Bild den negativen Effekt zu erzielen (b).

![Beispiel vor und nach der Invertieren-Anpassungsebene](invertieren-anpassungsebenen-abbildung-1.png)

Um die Farben des Bildes zu **invertieren**, fügen Sie einfach eine Invertieren-Anpassungsebene in die PSD ein:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

Das war's! Es gibt keine spezifischen Eigenschaften, die für diesen Typ von Anpassungsebene konfiguriert werden müssen.

## Fazit

In diesem Artikel haben wir die Invertieren-Anpassungsebene-API von Aspose.PSD für Java kennengelernt. Es ist ein müheloses Werkzeug, um negative Bilder zu erhalten, da die API dieser Anpassungsebene keine öffentlichen Elemente deklariert.

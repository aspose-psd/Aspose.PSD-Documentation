---
title: Pixel-Datenmanipulation mit Aspose.PSD für Python
weight: 100
type: docs
description: Beispiel, wie man schnell Rohpixel-Daten direkt und effektiv mit der PSD Python API aktualisiert
keywords: [Pixel bearbeiten, PSD bearbeiten, Ebene bearbeiten, Rohdatenmanipulation, PSD-Daten bearbeiten, PSD-API, Python, Codebeispiel]
url: de/python-net/pixel-datenmanipulation/
---

## **Einführung**
Aspose.PSD ist eine leistungsstarke Bibliothek, die es ermöglicht, mit Adobe Photoshop-Dateien (PSD) in Python zu arbeiten. In diesem Artikel werden wir erkunden, wie man Pixel-Daten in einer PSD-Datei mithilfe von Aspose.PSD manipuliert.

## **Überblick**
Der bereitgestellte Code demonstriert, wie man eine PSD-Datei erstellt, eine neue Ebene hinzufügt und dann die Pixel-Daten direkt manipuliert und das bearbeitete Bild speichert.

Importieren der erforderlichen Module: Der erste Schritt besteht darin, die notwendigen Module zu importieren. Wir importieren das BytesIO-Modul aus der io-Bibliothek sowie die Klassen PsdImage und Layer aus den Modulen aspose.psd.fileformats.psd bzw. aspose.psd.fileformats.psd.layers.

Als Nächstes definieren wir die Pfade zur Eingabe- und Ausgabedatei.

Öffnen der Eingabedatei als Stream: Wir öffnen die Eingabedatei als Stream mithilfe der open-Funktion und dem Modus "rb". Das Puffern-Argument wird auf 0 gesetzt, um das Puffern zu deaktivieren. Der Dateiinhalt wird in einen BytesIO-Stream gelesen und der Stream wird auf den Anfang gesetzt, indem stream.seek(0) aufgerufen wird.

Wir erstellen ein PSD-Ebenenobjekt, indem wir den Stream dem Konstruktor der Layer-Klasse übergeben.

Wir erstellen ein neues PSD-Bild, indem wir den Konstruktor der Klasse PsdImage aufrufen und die Breite und Höhe der Ebene als Argumente bereitstellen.

Wir weisen der layers-Eigenschaft des PSD-Bildes die Ebene mithilfe des Zuweisungsoperators (=) zu.

Um die Pixel-Daten zu manipulieren, laden wir zunächst die ARGB32-Pixel aus der Ebene mithilfe der Methode load_argb_32_pixels. Das Ergebnis wird in der Variable pixels gespeichert.

Als Nächstes definieren wir einen Bereich von Indizes (pixelsRange) basierend auf der Länge des arrays pixels. Wir iterieren über die Indizes und prüfen, ob ein Index durch 5 teilbar ist. Falls ja, setzen wir den Pixelwert an diesem Index auf 500000. So erstellen wir lediglich ein sich wiederholendes Muster. Sie können die Pixel-Daten nach Belieben ändern.

Dann speichern wir die modifizierten Pixel-Daten zurück in der Ebene mithilfe der Methode save_argb_32_pixels.

Schließlich speichern wir das PSD-Bild in der Ausgabedatei mithilfe der Methode save.

In diesem Artikel haben wir erkundet, wie man Pixel-Daten in einer PSD-Datei mithilfe von Aspose.PSD für Python manipuliert. Durch das Verständnis des bereitgestellten Codes können Sie verschiedene Operationen auf Pixel-Ebene durchführen, wie z. B. das Modifizieren von Pixeln basierend auf bestimmten Bedingungen. Aspose.PSD bietet eine umfassende Reihe von Funktionen zur programmgesteuerten Arbeit mit PSD-Dateien, wodurch es ein wertvolles Werkzeug für Bildmanipulationen in Python ist.

Bitte beachten Sie, dass der bereitgestellte Code davon ausgeht, dass Sie bereits die Aspose.PSD-Bibliothek und deren Abhängigkeiten installiert haben. Weitere Informationen zur Installation und Verwendung von Aspose.PSD für Python finden Sie in der offiziellen Dokumentation.

Bitte überprüfen Sie das vollständige Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentation-Python-Aspose-Pixel-Datenmanipulation.py" >}}

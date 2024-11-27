---
title: Aktualisierung der Füllebene in PSD unter Verwendung von Python
weight: 100
type: docs
description: Beispiele zur Verwendung aller Arten von Anpassungsebenen, einschließlich Farbfüllung, Gradientenfüllung und Musterfüllung
keywords: [Füllebene, Farbfüllung, Gradientenfüllung, Musterfüllung, psd api, Python, Codebeispiel]
url: de/python-net/psd-fill-layer-editing/
---

## **Übersicht**

Um eine reguläre Ebene zu erstellen, können Sie die bereitgestellte Funktion create_regular_layer im Code verwenden. Diese Funktion verwendet die Parameter links, oben, Breite und Höhe, um die Position und Größe der Ebene zu definieren. Sie erstellt eine neue Ebene, legt ihre Größe fest und füllt sie mit einer angegebenen Farbe.

Um eine Farbfüllebene zu erstellen, können Sie die Methode FillLayer.create_instance mit dem Parameter FillType.COLOR verwenden. Nachdem die Füllebene erstellt wurde, können Sie über die fill_settings-Eigenschaft auf ihre Einstellungen zugreifen und die Farbe über die color-Eigenschaft der Klasse ColorFillSettings festlegen. Im bereitgestellten Code wird die Farbe auf Color.coral gesetzt. Die clipping-Eigenschaft der Füllebene wird auf 1 gesetzt, wodurch die Ebene als Clipping-Maske fungiert.

Um eine Gradientenfüllschicht zu erstellen, können Sie die Methode FillLayer.create_instance mit dem Parameter FillType.GRADIENT verwenden. Ähnlich wie bei der Farbfüllebene können Sie über die fill_settings-Eigenschaft auf die Fülleinstellungen zugreifen und die Gradientenfarbpunkte sowie Transparenzpunkte festlegen. Im bereitgestellten Code werden die Gradientenfarbpunkte mit Hilfe der Klasse GradientColorPoint definiert und die Transparenzpunkte mit der Klasse GradientTransparencyPoint. Die clipping-Eigenschaft der Füllebene wird ebenfalls auf 1 gesetzt.

Um eine Musterfüllschicht zu erstellen, können Sie die Methode FillLayer.create_instance mit dem Parameter FillType.PATTERN verwenden. Erneut können Sie über die fill_settings-Eigenschaft auf die Fülleinstellungen zugreifen und die Mustereigenschaften und andere Eigenschaften festlegen. Im bereitgestellten Code wird die Mustereigenschaft mit der Klasse PatternFillSettings definiert und die clipping-Eigenschaft wird auf 1 gesetzt.

Nach Erstellung der Füllebenen können Sie sie mit der Methode add_layer dem PSD-Bild hinzufügen. Sie können auch den Anzeigenamen und andere Eigenschaften für jede Füllebene festlegen.

Abschließend können Sie das PSD-Bild und das entsprechende PNG-Bild mithilfe des bereitgestellten Codes speichern. Die PNG-Optionen sind auf die Verwendung von Truecolor mit Alpha für Transparenz eingestellt.

Bitte überprüfen Sie das vollständige Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentation-Python-Aspose-psd-fill-layer-editing.py" >}}

---
title: Beispiel zur Verwendung von Gruppenlayern in Aspose.PSD für Python
weight: 100
type: docs
description: Verwendung von Gruppenlayern einer PSD-Datei über Python
keywords: [Ebenengruppe, Gruppenlayer, Ebene zur Gruppe hinzufügen, PSD-API, Python, Codebeispiel]
url: de/python-net/psd-group-layer/
---

## **Überblick**

Die Arbeit mit Gruppenlayern in Aspose.PSD für Python ist eine leistungsstarke Funktion, die es ermöglicht, Ebenen innerhalb eines PSD-Bildes zu organisieren und zu manipulieren. Gruppenlayer, auch als Ordnerlayer bekannt, bieten eine Möglichkeit, mehrere Ebenen zusammenzufassen und Transformationen oder Effekte auf die gesamte Gruppe anzuwenden.

In diesem Beispiel erstellen wir zunächst ein neues PSD-Bild mit der Methode PsdImage.create. Anschließend erstellen wir ein neues LayerGroup-Objekt mit der Methode add_layer_group des PsdImage-Objekts. Wir geben den Namen des Gruppenlayers ("Folder"), den Index, an dem er eingefügt werden soll (0), und einen booleschen Wert an, der angibt, ob der Gruppenlayer sichtbar sein soll (True).

Als nächstes erstellen wir zwei Layer-Objekte und setzen ihre Anzeigenamen mit der Eigenschaft display_name. Diese Ebenen fügen wir dem Gruppenlayer mit der Methode add_layer hinzu.

Schließlich können wir auf die Ebenen innerhalb der Gruppe mit der Eigenschaft layers des LayerGroup-Objekts zugreifen. Im Beispiel wird überprüft, ob die Anzeigenamen der ersten und zweiten Ebenen in der Gruppe jeweils "Layer 1" und "Layer 2" sind.

Nach der Bearbeitung der Gruppenlayer können wir das modifizierte PSD-Bild mit der Methode save des PsdImage-Objekts speichern.

Dies ist nur ein grundlegendes Beispiel, um Sie beim Arbeiten mit Gruppenlayern in Aspose.PSD für Python zu unterstützen. Die Bibliothek bietet viele weitere fortgeschrittene Funktionen zum Manipulieren und Transformieren von Ebenen in PSD-Bildern. Für weitere Details und Beispiele zum Arbeiten mit Gruppenlayern und anderen Funktionen der Bibliothek können Sie die Aspose.PSD für Python-Dokumentation konsultieren.

Um mit Gruppenlayern in Aspose.PSD für Python zu arbeiten, können Sie die Klasse LayerGroup verwenden. Hier ist ein Beispielcode, der zeigt, wie ein Gruppenlayer erstellt, Ebenen hinzugefügt und das modifizierte PSD-Bild gespeichert wird.

Bitte überprüfen Sie das vollständige Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}

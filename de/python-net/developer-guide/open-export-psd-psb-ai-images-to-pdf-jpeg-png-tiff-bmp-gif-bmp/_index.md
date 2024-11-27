---
title: Öffnen Sie PSD-, PSB- und AI-Dateien und exportieren Sie sie in PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Beispiel PSD-, PSB- und AI-Dateiexport in andere Formate
keywords: [psd öffnen, ai öffnen, psb öffnen, in png exportieren, in pdf exportieren, in jpeg exportieren, in tiff exportieren, psd api, python, codebeispiel]
url: de/python-net/open-export-psd-psb-ai-bilder-in-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Übersicht**
Um PSD-, PSB- und AI-Dateien in verschiedene Formate zu konvertieren, können Sie die Aspose.PSD-Bibliothek in Python verwenden. Diese Bibliothek bietet verschiedene Optionen und Einstellungen, um den Konvertierungsprozess anzupassen.

Zunächst müssen Sie die erforderlichen Klassen und Module aus der Aspose.PSD-Bibliothek importieren. Stellen Sie sicher, dass Sie die Bibliothek installiert haben, bevor Sie den Code ausführen.

In diesem Code definieren wir verschiedene Optionen für verschiedene Formate wie PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB und PSD. Diese Optionen ermöglichen es Ihnen, die Ausgabedatei gemäß Ihren Anforderungen anzupassen.

Anschließend definieren wir ein Wörterbuch "formate", das Dateierweiterungen ihren jeweiligen Speicheroptionen zuordnet.

Um eine PSD-Datei in andere Formate zu konvertieren, laden Sie die PSD-Datei mit PsdImage.load() und durchlaufen Sie dann das Wörterbuch "formate". Geben Sie für jedes Format den Ausgabedateinamen an und speichern Sie das Bild mit der Methode image.save().

Ebenso laden Sie zum Konvertieren einer AI-Datei in andere Formate die AI-Datei mit AiImage.load() und durchlaufen Sie das Wörterbuch "formate". Geben Sie den Ausgabedateinamen an und speichern Sie das Bild mit der Methode image.save().

Stellen Sie sicher, dass Sie die korrekten Dateipfade für die Quell-PSD- und AI-Dateien angeben.

Das war's! Verwenden Sie diesen Code jetzt, um PSD-, PSB- und AI-Dateien mithilfe von Aspose.PSD für Python in verschiedene Formate zu konvertieren.

Bitte überprüfen Sie das vollständige Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentation-Python-Aspose-Psd-open-export-psd-psb-ai-bilder-zu-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}

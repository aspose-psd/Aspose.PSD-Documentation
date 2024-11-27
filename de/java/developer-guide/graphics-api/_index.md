---
title: Verwendung der Grafik-API zum Bearbeiten von Ebenen in PSD-Dateien
weight: 100
type: docs
description: Beispiel für die Verwendung der Grafik-API in Aspose.PSD für Java
keywords: [Ebenen aktualisieren, Kreis zeichnen, Ellipse zeichnen, Kreis mit Füllung zeichnen, Grafik, psd api, java, Codebeispiel]
url: de/java/graphics-api/
---

## **Übersicht**
Um zu beginnen, laden Sie die PSD-Datei mithilfe der Methode Image.load() oder erstellen Sie ein PSD-Bild von Grund auf. Verwenden Sie die Variable inputFile, um den Pfad zu Ihrer PSD-Datei darzustellen, und geben Sie ggf. Ladeoptionen mit loadOpt an.

Greifen Sie als nächstes auf die erste Ebene des PSD-Bildes zu, indem Sie die Syntax psdImage.getLayers()[0] verwenden, um einen Verweis auf das Ebenenobjekt für die Manipulation zu erhalten.

Um die Ebene zu bearbeiten, erstellen Sie ein Grafikobjekt, indem Sie die Ebene als Parameter übergeben. Dieses Objekt bietet verschiedene Methoden zum Zeichnen von Formen und zum Anwenden von Pinseln.

Ein Pen-Objekt wird verwendet, um die Farbe und Dicke des Umrisses von Formen zu definieren. Ebenso werden Pinsel wie LinearGradientBrush verwendet, um Füllfarben zu definieren.

Zeichnen Sie Formen auf der Ebene mit Methoden wie graphics.drawEllipse(), um Formen zu umreißen, und graphics.fillEllipse(), um sie zu füllen.

Nachdem Sie die gewünschten Änderungen an der Ebene vorgenommen haben, speichern Sie das modifizierte PSD-Bild mithilfe von psdImage.save().

Zusätzlich können Sie das modifizierte Bild in anderen Formaten wie PNG speichern, indem Sie geeignete Optionen verwenden.

Das war's! Sie haben erfolgreich die Grafik-API von Aspose.PSD für Java verwendet, um Ebenen in einer PSD-Datei zu bearbeiten. Entdecken Sie weitere Funktionen und Möglichkeiten der Aspose.PSD-Bibliothek, um Ihre Bildbearbeitungsfähigkeiten zu verbessern.

Bitte überprüfen Sie das vollständige Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentation-Java-Aspose-Psd-Grafik-API.java" >}}

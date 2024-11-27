---
title: Unterstützung großer Bilder
type: docs
weight: 60
url: /de/java/large-image-support/
---

## **Unterstützung großer Bilder**
Da die Standard-Java-Bibliothek einige Einschränkungen hinsichtlich der Bildgröße hat, haben wir einen neuen Mechanismus für die Unterstützung großer Bilder eingeführt. Der neue Ansatz überwindet die Einschränkungen, aber aufgrund von Datengrößenbeschränkungen betragen die maximal unterstützten Abmessungen für die Erstellung und das Laden 2.147.483.647 x 2.147.483.647 Pixel.
### **Arbeiten mit großen Bildern**
Aspose.PSD hat die Leistung und Unterstützung für große Bilder verbessert. Bilder, die Hunderte von Megabyte groß sind, sind nun kein Problem mehr, sodass Sie über diesen Bildern erstellen, laden und zeichnen können. Aufgrund der teilweisen Verarbeitung und Behandlung von OutOfMemoryException-Ausnahmen kann die Leistung bei sehr großen Bildern sehr niedrig sein. Dies liegt daran, dass Aspose.PSD versucht, eine geringere Datenmenge für die Verarbeitung neu zuzuweisen und jeder Neuzuweisungsschritt sehr kostspielig ist. Die Vorteile der neuen Architektur sind offensichtlich:

- Es gibt keine Begrenzung für die Bildgröße.
- Sie sind nicht auf den verfügbaren Speicher auf Ihrem PC beschränkt.

Wenn Sie eine langsame Verarbeitung feststellen, wird empfohlen, die Gesamtmenge an RAM zu erhöhen, um alle Ihre Pixel in den Speicher zu passen. Wenn Sie dies nicht tun, ist die Verarbeitung immer noch möglich, verläuft jedoch langsamer. Der Ansatz ist wie folgt:

- Rufen Sie die LoadPartialPixels-Methode mit dem gewünschten Rechteck auf und stellen Sie den delegierten Empfänger für die geladenen Pixel bereit.

Aspose.PSD versucht, das gesamte Rechteck zu laden.

- Wenn genügend Speicher vorhanden ist, um alle Pixel unterzubringen, werden alle Pixel einfach an den Aufrufer zurückgegeben.
- Wenn nicht genügend Speicher vorhanden ist, erhält der Aufrufer eine Teilmenge von Pixeln aus dem spezifizierten Rechteckinneren. Sobald diese Pixel verarbeitet wurden, erhält der Aufrufer das nächste Rechteck. Die Verarbeitung endet, wenn das gesamte Rechteck verarbeitet wurde.

Aspose.PSD versucht, so viele Zeilen wie möglich zu extrahieren. Wenn nicht genügend Speicher vorhanden ist, um eine einzelne Zeile von Pixeln unterzubringen, wird eine Zeile in Teile aufgeteilt, die den Rechtecken mit einer Höhe von 1 entsprechen. Sie können auch auf großen Bildern zeichnen. Der Zeichenprozess versucht, das gesamte gewünschte Rechteck zu beeinflussen. Wenn nicht genügend Speicher vorhanden ist, wird gezeichnet auf Teilrechtecken durchgeführt, bis der gesamte Bereich gezeichnet ist. Zusätzlich unterstützt Aspose.PSD das Speichern und Exportieren großer Bilder. Speichern Sie das Quellbild auf die Festplatte oder exportieren Sie es in ein anderes Dateiformat. Der Speicher- oder Exportprozess wird durch Verwendung von Teilrechtecken durchgeführt, wenn erforderlich.
### **Unterstützte Bildformate**
Die folgenden Formate werden für die Verarbeitung großer Bilder unterstützt:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Die oben genannten Formate können sicher durch Erstellung, Änderung, Anwendung von Zeichenoperationen, Speichern auf die Festplatte oder Exportieren in ungeachtet der Bildgröße verarbeitet werden.

---
title: Unterstützung Großer Bilder
type: docs
weight: 40
url: /de/net/large-image-support/
---

## **Unterstützung Großer Bilder**
Da die Standard-.NET-Bibliothek einige Einschränkungen hinsichtlich der Größe von Bildern hat, haben wir einen neuen Mechanismus zur Unterstützung großer Bilder eingeführt. Der neue Ansatz überwindet die Beschränkungen, aber aufgrund von Datengrößenbeschränkungen sind die maximal unterstützten Dimensionen für die Erstellung und das Laden 2.147.483.647 x 2.147.483.647 Pixel.
### **Arbeiten mit Großen Bildern**
Aspose.PSD hat die Leistung und Unterstützung für große Bilder verbessert. Bilder von Hunderten von Megabyte Größe sind kein Problem mehr, sodass Sie diese Bilder erstellen, laden und darüber zeichnen können. Aufgrund der teilweisen Verarbeitung und Handhabung von OutOfMemoryException-Ausnahmen kann die Leistung bei sehr großen Bildern sehr niedrig sein. Dies liegt daran, dass Aspose.PSD versucht, eine geringere Datenmenge für die Verarbeitung neu zuzuweisen und jeder Schritt der Neuverteiliung sehr kostspielig ist. Die Vorteile der neuen Architektur sind offensichtlich:

- Es gibt keine Beschränkung für die Bildgröße.
- Sie sind nicht auf den verfügbaren Speicherplatz auf Ihrem PC beschränkt.

Wenn Sie langsame Verarbeitung erleben, wird empfohlen, die Gesamtmenge an RAM zu erhöhen, um all Ihre Pixel in den Speicher passen zu können. Wenn Sie das nicht tun, ist die Verarbeitung dennoch möglich, aber langsamer. Der Ansatz ist wie folgt:

- Rufen Sie die Methode [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) mit dem gewünschten Rechteck auf und wählen Sie den Delegaten, um die geladenen Pixel anzugeben.

Aspose.PSD versucht, das gesamte Rechteck zu laden.

- Wenn genügend Speicher vorhanden ist, um alle Pixel unterzubringen, werden einfach alle Pixel dem Aufrufer zurückgegeben.
- Wenn nicht genügend Speicher vorhanden ist, erhält der Aufrufer eine Teilmenge von Pixeln innerhalb des angegebenen Rechtecks. Nachdem diese Pixel verarbeitet wurden, erhält der Aufrufer das nächste Rechteck. Die Verarbeitung endet, wenn das gesamte Rechteck verarbeitet wurde.

Aspose.PSD versucht, so viele Zeilen wie möglich zu extrahieren. Wenn nicht genügend Speicher vorhanden ist, um eine einzige Zeile von Pixeln aufzunehmen, wird eine Zeile in Teile aufgeteilt, die den Rechtecken mit einer Höhe von 1 entsprechen. Sie können auch auf großen Bildern zeichnen. Der Zeichenprozess versucht, das gesamte gewünschte Rechteck zu beeinflussen. Wenn nicht genügend Speicher vorhanden ist, wird die Zeichnung auf Teilrechtecken ausgeführt, bis der gesamte Bereich gezeichnet ist. Darüber hinaus unterstützt Aspose.PSD das Speichern und Exportieren großer Bilder. Speichern Sie das Quellbild auf der Festplatte oder exportieren Sie es in ein anderes Dateiformat. Der Speicher- oder Exportvorgang wird bei Bedarf durch Verwendung von Teilrechtecken durchgeführt.
### **Unterstützte Bildformate**
Die folgenden Formate werden für die Verarbeitung großer Bilder unterstützt:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Die oben genannten Formate können unabhängig von der Bildgröße sicher durch Erstellung, Modifikation, Anwendung von Zeichenoperationen, Speichern auf der Festplatte oder Export in ein anderes Format verarbeitet werden.

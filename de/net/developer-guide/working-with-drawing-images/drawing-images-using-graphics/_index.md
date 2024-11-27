---
title: Grafiken zeichnen mit Graphics
type: docs
weight: 20
url: /de/net/drawing-images-using-graphics/
---

## **Grafiken zeichnen mit Graphics**
Mit der Aspose.PSD-Bibliothek können Sie einfache Formen wie Linien, Rechtecke und Kreise sowie komplexe Formen wie Polygone, Kurven, Bögen und Bezierformen zeichnen. Die Aspose.PSD-Bibliothek erstellt solche Formen mithilfe der Klasse [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics), die im Namensraum Aspose.PSD enthalten ist. Grafikobjekte sind verantwortlich für verschiedene Zeichenoperationen auf einem Bild und ändern somit die Oberfläche des Bildes. Die [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-Klasse verwendet verschiedene Hilfsobjekte, um die Formen zu verbessern:

·         Stifte zum Zeichnen von Linien, Umrandungen von Formen oder Rendern anderer geometrischer Darstellungen.

·         Pinsel zum Definieren, wie Flächen gefüllt werden.

·         Schriftarten zur Definition der Form von Textzeichen.
### **Zeichnen mit der Graphics-Klasse**
Im Folgenden finden Sie ein Codebeispiel, das die Verwendung der [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-Klasse demonstriert. Der Beispielquellcode wurde in mehrere Teile aufgeteilt, um ihn einfach und leicht verständlich zu halten. Schritt für Schritt zeigen die Beispiele, wie Sie:

1. Ein Bild erstellen.
1. Ein Graphics-Objekt erstellen und initialisieren.
1. Die Oberfläche löschen.
1. Eine Ellipse zeichnen.
1. Ein gefülltes Polygon zeichnen und das Bild speichern.
### **Programmierbeispiele**
#### **Erstellen eines Bildes**
Beginnen Sie mit dem Erstellen eines Bildes mithilfe einer der Methoden, die in der Anleitung zur Erstellung von Dateien beschrieben sind.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Erstellen und Initialisieren eines Graphics-Objekts**
Erstellen und Initialisieren Sie dann ein Graphics-Objekt, indem Sie das Image-Objekt an seinen Konstruktor übergeben.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Die Oberfläche löschen**
Löschen Sie die Grafikoberfläche, indem Sie die Clear-Methode der [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-Klasse aufrufen und die Farbe als Parameter übergeben. Diese Methode füllt die Grafikoberfläche mit der übergebenen Farbe.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Eine Ellipse zeichnen**
Sie werden feststellen, dass die [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-Klasse viele Methoden zum Zeichnen und Füllen von Formen bereitstellt. Die vollständige Liste der Methoden finden Sie in der Aspose.PSD für .NET-API-Referenz. Die Graphics-Klasse hat mehrere überladene Versionen der DrawEllipse-Methode. All diese Methoden akzeptieren ein Pen-Objekt als ersten Argument. Die späteren Parameter werden übergeben, um das Begrenzungsrechteck um die Ellipse zu definieren. Verwenden Sie für dieses Beispiel die Version, die ein Rectangle-Objekt als zweiten Parameter akzeptiert, um eine Ellipse mit dem Pen-Objekt in Ihrer gewünschten Farbe zu zeichnen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Ein gefülltes Polygon zeichnen**
Zeichnen Sie als nächstes ein Polygon mit dem LinearGradientBrush und einem Array von Punkten. Die Graphics-Klasse bietet mehrere überladene Versionen der FillPolygon()-Methode. Alle akzeptieren ein Brush-Objekt als erstes Argument zur Definition der Fülleigenschaften. Der zweite Parameter ist ein Array von Punkten. Beachten Sie, dass jedes zweite aufeinanderfolgende Elemente im Array eine Seite des Polygons festlegen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Grafiken zeichnen mit Graphics: Vollständiger Quellcode**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Alle Klassen, die IDisposable implementieren und auf nicht verwaltete Ressourcen zugreifen, werden in einer Using-Anweisung instanziiert, um sicherzustellen, dass sie korrekt verworfen werden.

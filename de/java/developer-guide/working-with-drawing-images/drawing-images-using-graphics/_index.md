---
title: Zeichnen von Bildern mit Grafiken
type: docs
weight: 20
url: /de/java/drawing-images-using-graphics/
---

## **Zeichnen von Bildern mit Grafiken**

Mit der Aspose.PSD-Bibliothek können Sie einfache Formen wie Linien, Rechtecke und Kreise sowie komplexe Formen wie Polygone, Kurven, Bögen und Bézierformen zeichnen. Die Aspose.PSD-Bibliothek erstellt solche Formen mithilfe der Graphics-Klasse, die sich im Aspose.PSD-Namespace befindet. Graphics-Objekte sind für die Ausführung verschiedener Zeichenoperationen auf einem Bild verantwortlich und ändern somit die Oberfläche des Bildes. Die Graphics-Klasse verwendet eine Vielzahl von Hilfsobjekten, um die Formen zu verbessern:

- Pens, um Linien zu zeichnen, Umrisse von Formen zu ziehen oder andere geometrische Darstellungen zu rendern.
- Brushes, um zu definieren, wie Flächen gefüllt werden.
- Fonts, um die Form von Textzeichen zu definieren.

### **Zeichnen mit der Graphics-Klasse**

Im Folgenden finden Sie ein Codebeispiel, das die Verwendung der Graphics-Klasse demonstriert. Der Beispielquellcode wurde aufgeteilt, um ihn einfach und leicht verständlich zu halten. Schritt für Schritt zeigen die Beispiele, wie Sie:

1. Ein Bild erstellen.
1. Ein Graphics-Objekt erstellen und initialisieren.
1. Die Oberfläche löschen.
1. Eine Ellipse zeichnen.
1. Ein gefülltes Polygon zeichnen und das Bild speichern.

### **Programmierbeispiele**

#### **Erstellen eines Bildes**

Beginnen Sie mit der Erstellung eines Bildes mithilfe einer der in der Erstellung von Dateien beschriebenen Methoden.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenBilder-ZeichnenBezier-ZeichnenBezier.java" >}}

#### **Erstellen und Initialisieren eines Graphics-Objekts**

Erstellen und initialisieren Sie dann ein Graphics-Objekt, indem Sie das Image-Objekt an den Konstruktor übergeben.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenBilder-ZeichnenBogen-ZeichnenBogen.java" >}}

#### **Die Oberfläche löschen**

Löschen Sie die Grafikoberfläche, indem Sie die Clear-Methode der Graphics-Klasse aufrufen und eine Farbe als Parameter übergeben. Diese Methode füllt die Grafikoberfläche mit der übergebenen Farbe.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenBilder-ZeichnenMitGraphics-ZeichnenMitGraphics.java" >}}

#### **Eine Ellipse zeichnen**

Sie werden feststellen, dass die Graphics-Klasse viele Methoden zum Zeichnen und Füllen von Formen zur Verfügung stellt. Eine vollständige Liste der Methoden finden Sie im Aspose.PSD for Java-API-Referenz. Die Graphics-Klasse hat mehrere überladene Versionen der DrawEllipse-Methode. Alle diese Methoden akzeptieren ein Pen-Objekt als ersten Argument. Die späteren Parameter werden übergeben, um das umgebende Rechteck um die Ellipse zu definieren. Verwenden Sie für dieses Beispiel die Version, die ein Rectangle-Objekt als zweiten Parameter akzeptiert, um unter Verwendung des Pen-Objekts in Ihrer gewünschten Farbe eine Ellipse zu zeichnen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenBilder-ZeichnenEllipse-ZeichnenEllipse.java" >}}

#### **Ein gefülltes Polygon zeichnen**

Zeichnen Sie anschließend ein Polygon unter Verwendung des LinearGradientBrush und eines Arrays von Punkten. Die Graphics-Klasse hat mehrere überladene Versionen der FillPolygon-Methode. Alle diese akzeptieren ein Brush-Objekt als erstes Argument, das die Eigenschaften der Füllung definiert. Das zweite Argument ist ein Array von Punkten. Beachten Sie, dass zwei aufeinanderfolgende Punkte im Array eine Seite des Polygons definieren.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenBilder-ZeichnenMitGraphics-ZeichnenMitGraphics.java" >}}

### **Zeichnen von Bildern mit Grafiken: Vollständiger Quellcode**

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenBilder-ZeichnenMitGraphics-ZeichnenMitGraphics.java" >}}

Alle Klassen, die IDisposable implementieren und auf nicht verwaltete Ressourcen zugreifen, werden in einer Using-Anweisung instanziiert, um sicherzustellen, dass sie korrekt freigegeben werden.

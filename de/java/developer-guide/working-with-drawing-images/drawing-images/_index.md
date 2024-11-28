---
title: Bildzeichnen
type: docs
weight: 10
url: /de/java/bildzeichnen/
---

## **Zeichnen von Linien**
Dieses Beispiel verwendet die Graphics-Klasse, um Linienformen auf der Bildfläche zu zeichnen. Um den Vorgang zu demonstrieren, erstellt das Beispiel ein neues Bild und zeichnet Linien auf der Bildfläche mithilfe der durch die Graphics-Klasse bereitgestellten DrawLine-Methode. Zunächst erstellen wir ein PsdImage, indem wir seine Höhe und Breite festlegen.

Nachdem das Bild erstellt wurde, verwenden wir die Clear-Methode der Graphics-Klasse, um seine Hintergrundfarbe festzulegen. Die DrawLine-Methode der Graphics-Klasse wird verwendet, um eine Linie auf einem Bild zu zeichnen, die zwei Punktstrukturen verbindet. Diese Methode hat mehrere Überladungen, die die Instanz der Pen-Klasse und Koordinatenpaare von Punkten oder Point/PointF-Strukturen als Argumente akzeptieren. Die Pen-Klasse definiert ein Objekt, das zum Zeichnen von Linien, Kurven und Figuren verwendet wird. Die Pen-Klasse hat mehrere überladene Konstruktoren, um Linien mit angegebener Farbe, Breite und Pinsel zu zeichnen. Die SolidBrush-Klasse wird verwendet, um kontinuierlich mit einer bestimmten Farbe zu zeichnen. Schließlich wird das Bild im BMP-Dateiformat exportiert. Der folgende Code-Schnipsel zeigt Ihnen, wie Sie Linienformen auf der Bildfläche zeichnen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}

## **Zeichnen von Ellipsen**
Das Beispiel zum Zeichnen von Ellipsen ist der zweite Artikel in der Serie zum Zeichnen von Formen. Wir verwenden die Graphics-Klasse, um die Ellipsenform auf der Bildfläche zu zeichnen. Um den Vorgang zu demonstrieren, erstellt das Beispiel ein neues Bild und zeichnet die Ellipsenform auf der Bildfläche mithilfe der durch die Graphics-Klasse bereitgestellten DrawEllipse-Methode. Zunächst erstellen wir ein PsdImage, indem wir seine Höhe und Breite festlegen.

Nachdem das Bild erstellt wurde, erstellen und initialisieren wir ein Objekt der Graphics-Klasse und setzen die Hintergrundfarbe des Bildes mithilfe der Clear-Methode der Graphics-Klasse. Die DrawEllipse-Methode der Graphics-Klasse wird verwendet, um die Ellipsenform auf einer Bildfläche zu zeichnen, die durch die Bounding-Rectangle-Struktur angegeben ist. Diese Methode hat mehrere Überladungen, die die Instanzen der Pen- und Rectangle-/RectangleF-Klassen oder ein Koordinatenpaar, eine Höhe und eine Breite als Argumente akzeptieren. Die Pen-Klasse definiert ein Objekt, das zum Zeichnen von Linien, Kurven und Figuren verwendet wird. Die Pen-Klasse hat mehrere überladene Konstruktoren, um Linien mit angegebener Farbe, Breite und Pinsel zu zeichnen. Die Rectangle-Klasse speichert einen Satz von vier Ganzzahlen, die den Standort und die Größe eines Rechtecks darstellen. Die Rectangle-Klasse hat mehrere überladene Konstruktoren, um die Rechteckstruktur mit angegebener Größe und Lage zu zeichnen. Die SolidBrush-Klasse wird verwendet, um kontinuierlich mit einer bestimmten Farbe zu zeichnen. Schließlich wird das Bild im BMP-Dateiformat exportiert. Der folgende Code-Schnipsel zeigt Ihnen, wie Sie die Ellipsenform auf der Bildfläche zeichnen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

## **Zeichnen von Rechtecken**
In diesem Beispiel werden wir die Rechtecksform auf der Bildfläche zeichnen. Um den Vorgang zu demonstrieren, erstellt das Beispiel ein neues Bild und zeichnet die Rechtecksform auf der Bildfläche mithilfe der durch die Graphics-Klasse bereitgestellten DrawRectangle-Methode. Zunächst erstellen wir ein PsdImage, indem wir seine Höhe und Breite festlegen. Anschließend setzen wir die Hintergrundfarbe des Bildes mithilfe der Clear-Methode der Graphics-Klasse.

Die DrawRectangle-Methode der Graphics-Klasse wird verwendet, um die Rechtecksform auf einer Bildfläche zu zeichnen, die durch die Rechtecksstruktur angegeben ist. Diese Methode hat mehrere Überladungen, die die Instanzen der Pen- und Rectangle/RectangleF-Klassen oder Koordinatenpaare, eine Breite und eine Höhe als Argumente akzeptieren. Die Rectangle-Klasse speichert einen Satz von vier Ganzzahlen, die den Standort und die Größe eines Rechtecks darstellen. Die Rectangle-Klasse hat mehrere überladene Konstruktoren, um die Rechteckstruktur mit angegebener Größe und Lage zu zeichnen. Schließlich wird das Bild im BMP-Dateiformat exportiert. Der folgende Code-Schnipsel zeigt Ihnen, wie Sie die Rechtecksform auf der Bildfläche zeichnen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}

## **Zeichnen von Bögen**
In dieser Sitzung der Zeichenformen-Serie werden wir die Bogenform auf der Bildfläche zeichnen. Wir verwenden die DrawArc-Methode von Graphics, um den Vorgang an einem BMP-Bild zu demonstrieren. Zunächst erstellen wir ein PsdImage, in dem wir seine Höhe und Breite festlegen. Nachdem das Bild erstellt wurde, verwenden wir die Clear-Methode der Graphics-Klasse, um seine Hintergrundfarbe festzulegen.

Die DrawArc-Methode der Graphics-Klasse wird verwendet, um die Bogenform auf einer Bildfläche zu zeichnen. DrawArc stellt einen Teil einer Ellipse dar, der durch die Rechtecksstruktur oder das Koordinatenpaar angegeben ist. Diese Methode hat mehrere Überladungen, die die Instanzen der Pen-Klassen und Rectangle /RectangleF-Struktur oder ein Koordinatenpaar, eine Breite und eine Höhe als Argumente akzeptieren. Schließlich wird das Bild im BMP-Dateiformat exportiert. Der folgende Code-Schnipsel zeigt Ihnen, wie Sie die Bogenform auf der Bildfläche zeichnen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

## **Zeichnen von Bezierkurven**
Dieses Beispiel verwendet die Graphics-Klasse, um die Bezierkurvenform auf der Bildfläche zu zeichnen. Um den Vorgang zu demonstrieren, erstellt das Beispiel ein neues Bild und zeichnet die Bezierkurvenform auf der Bildfläche mithilfe der durch die Graphics-Klasse bereitgestellten DrawBezier-Methode. Zunächst erstellen wir ein PsdImage, indem wir seine Höhe und Breite festlegen. Sobald das Bild erstellt wurde, verwenden wir die Clear-Methode der Graphics-Klasse, um seine Hintergrundfarbe festzulegen.

Die DrawBezier-Methode der Graphics-Klasse wird verwendet, um die Bezier-Spline-Form auf einer Bildfläche zu zeichnen, die durch vier Point-Strukturen definiert ist. Diese Methode hat mehrere Überladungen, die die Instanzen der Pen-Klasse und vier geordnete Koordinatenpaare oder vier Point/PointF-Strukturen oder ein Array von Point/PointF-Strukturen als Argumente akzeptieren. Die Pen-Klasse definiert ein Objekt, das zum Zeichnen von Linien, Kurven und Figuren verwendet wird. Die Pen-Klasse hat mehrere überladene Konstruktoren, um Linien mit angegebener Farbe, Breite und Pinsel zu zeichnen. Schließlich wird das Bild im BMP-Dateiformat exportiert. Der folgende Code-Schnipsel zeigt Ihnen, wie Sie die Bezierkurve auf der Bildfläche zeichnen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

## **Zeichnen von Bildern mit Kernfunktionalität**
Aspose.PSD ist eine Bibliothek, die viele wertvolle Funktionen bietet, darunter das Erstellen von Bildern von Grund auf. Zeichnen Sie mithilfe der Kernfunktionalität wie der Manipulation von Bitmapinformationen eines Bildes oder verwenden Sie die erweiterten Funktionen wie Graphics und GraphicsPath, um Formen auf der Bildfläche mit Hilfe verschiedener Pinsel und Stifte zu zeichnen. Mit der RasterImage-Klasse von Aspose.PSD können Sie die Pixelinformationen eines Bildbereichs abrufen und manipulieren. Die RasterImage-Klasse enthält die gesamte Kern-Zeichenfunktionalität, wie das Abrufen und Setzen von Pixeln und andere Methoden zur Bildmanipulation. Erstellen Sie ein neues Bild mithilfe einer der in der Dokumentation "Dateien erstellen" beschriebenen Methoden und weisen Sie es einer Instanz der RasterImage-Klasse zu. Verwenden Sie die LoadPixels-Methode der RasterImage-Klasse, um die Pixelinformationen eines Bildbereichs abzurufen. Sobald Sie ein Pixelarray haben, können Sie es manipulieren, indem Sie beispielsweise die Farbe jedes Pixels ändern. Nach der Manipulation der Pixelinformationen setzen Sie sie an der gewünschten Stelle im Bild mit Hilfe der SavePixels-Methode der RasterImage-Klasse zurück. Der folgende Code-Schnipsel zeigt Ihnen, wie Sie Bilder mithilfe der Kernfunktionalität zeichnen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}

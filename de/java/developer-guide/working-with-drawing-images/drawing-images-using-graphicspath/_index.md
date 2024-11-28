---
title: Zeichnen von Bildern mit GraphicsPath
type: docs
weight: 30
url: /de/java/drawing-images-using-graphicspath/
---

## **Zeichnen von Bildern mit GraphicsPath**
Die GraphicsPath-Klasse ist dafür verantwortlich, einen Grafikpfad zu erstellen und zu pflegen. Der GraphicsPath hat keine Referenz zu einem Bild und ändert das Bild selbst nicht. Stattdessen kann er als ein Objekt betrachtet werden, das Metadaten enthält, die die Pfade beschreiben, die die Graphics-Klasse zeichnen kann. Die GraphicsPath-Klasse verwendet Figuren; jede Figur besteht entweder aus einer Sequenz von verbundenen Linien und Kurven oder einem geometrischen Formprimitive. Jede Form kann in Formsegmente unterteilt werden. Sie können verschiedene Figuren oder Formen einem GraphicsPath-Objekt hinzufügen, entfernen und ändern. Wenn der GraphicsPath vollständig beschrieben wurde, verwenden Sie die entsprechenden Methoden der Graphics-Klasse (DrawPath und Fill Paths), um die Pfade zu zeichnen oder zu füllen. Die Graphics-Klasse nimmt jedes Formsegment und zeichnet es, um das endgültige Bild zu erzeugen.

### **Zeichnen mit der GraphicsPath-Klasse**
Im Folgenden finden Sie ein Beispiel, das die Verwendung der GraphicsPath-Klasse demonstriert. Der Beispielquellcode wurde in mehrere Teile unterteilt, um ihn einfach und verständlich zu gestalten. Schritt für Schritt zeigen Ihnen die Beispiele, wie Sie:

- Ein Bild erstellen.
- Initialisieren eines Graphics-Objekts.
- Die Oberfläche löschen.
- Eine Instanz von GraphicsPath erstellen.
- Eine Figur erstellen.
- Formen zur Figur hinzufügen.
- Ein Figurenarray erstellen.
- Pfade zeichnen.
- Pfade füllen.

### **Zeichnen von Bildern mit GraphicsPath: Programmbeispiele**
#### **GraphicsPath: Ein Bild erstellen**
Beginnen Sie mit der Erstellung eines Bildes mithilfe einer der in der Erstellung von Dateien beschriebenen Methoden.
#### **GraphicsPath: Initialisieren eines Graphics-Objekts**
Erstellen und initialisieren Sie ein Graphics-Objekt, indem Sie dem Konstruktor das Image-Objekt übergeben.
#### **GraphicsPath: Die Oberfläche löschen**
Löschen Sie die Grafikoberfläche, indem Sie die Clear-Methode der Graphics-Klasse aufrufen und eine Farbe als Parameter übergeben. Diese Methode füllt die Grafikoberfläche mit der übergebenen Farbe.
#### **GraphicsPath: Eine Instanz von GraphicsPath erstellen**
Erstellen Sie eine Instanz von GraphicsPath mit GraphicsPath standardmäßig auf Alternate festgelegt. Diese Einstellung bestimmt, wie der Innenraum einer geschlossenen Figur gefüllt werden soll. Der andere mögliche Wert von GraphicsPath ist Winding.
#### **GraphicsPath: Eine Figur erstellen**
Erstellen Sie eine Instanz der Figure-Klasse. Wie bereits erwähnt, kann eine Figur Formen enthalten, und Formen befinden sich im Aspose.PSD.Shapes-Namespace.
#### **GraphicsPath: Formen zur Figur hinzufügen**
Die von der Figure-Klasse bereitgestellte Add Shapes-Methode ermöglicht das Hinzufügen von Formen zur Figur. In den untenstehenden Codebeispielen werden mehrere Formen zu einem Figure-Objekt hinzugefügt.
#### **GraphicsPath: Figuren zu einem Array hinzufügen**
Mehrere Figuren können einem GraphicsPath-Objekt mit der AddFigures-Methode der GraphicsPath-Klasse hinzugefügt werden. Diese Methode akzeptiert ein Array von Figuren als Parameter.
#### **GraphicsPath: Die Pfade zeichnen**
Zeichnen Sie den GraphicsPath mithilfe der DrawPath-Methode der Graphics-Klasse. Die Methode akzeptiert zwei Parameter. Der erste Parameter ist ein Objekt der Pen-Klasse, das die Farbe, Breite und den Stil des Pfads bestimmt. Der zweite Parameter ist das Objekt der GraphicsPath-Klasse, das den Pfad selbst darstellt.
#### **GraphicsPath: Pfade füllen**

Sie können einen Pfad füllen, indem Sie ein GraphicsPath-Objekt an die von der Graphics-Klasse bereitgestellte Fill Paths-Methode übergeben. Die Fill Paths-Methode füllt den Pfad gemäß dem für den Pfad eingestellten Füllmodus (Alternate oder Winding). Wenn der Pfad offene Figuren enthält, wird der Pfad so gefüllt, als wären diese Figuren geschlossen.

Die Fill Paths-Methode akzeptiert zwei Parameter. Der erste Parameter ist ein Objekt einer beliebigen Brush-Klasse aus dem Aspose.PSD.Brushes-Namespace. Der zweite Parameter ist der Pfad selbst. Verwenden Sie zum Beispiel für dieses Beispiel den HatchBrush, der eine rechteckige Bürste mit einem Schraffurmuster, einer Vordergrundfarbe und einer Hintergrundfarbe ist. Legen Sie vor dem Übergeben des HatchBrush-Objekts an die Fill Paths-Methode seine Eigenschaften fest.
### **GraphicsPath: Vollständiger Quellcode**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



Alle Klassen, die IDisposable implementieren, werden in einer Using-Anweisung instanziiert, um sicherzustellen, dass sie ordnungsgemäß entsorgt werden.

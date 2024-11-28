---
title: Zeichnen von Bildern mit GraphicsPath
type: docs
weight: 30
url: /de/net/zeichnen-von-bildern-mit-graphicspath/
---

## **Zeichnen von Bildern mit GraphicsPath**
Die [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath)-Klasse ist dafür verantwortlich, einen Grafikpfad zu erstellen und zu pflegen. GraphicsPath enthält keine Referenz zu einem Bild und ändert das Bild selbst nicht. Stattdessen kann es als ein Objekt betrachtet werden, das Metadaten enthält, die die Pfade beschreiben, die die Graphics-Klasse zeichnen kann. Die GraphicsPath-Klasse verwendet Figuren; jede Figur besteht entweder aus einer Abfolge von verbundenen Linien und Kurven oder aus einer geometrischen Formprimitive. Jede Form kann in Formsegmente unterteilt werden. Sie können verschiedene Figuren oder Formen in einem GraphicsPath-Objekt hinzufügen, entfernen und ändern. Wenn der GraphicsPath vollständig beschrieben wurde, verwenden Sie die entsprechenden Methoden der Graphics-Klasse (DrawPath und Fill Paths), um über die Pfade zu zeichnen oder sie zu füllen. Die Graphics-Klasse nimmt jedes Formsegment und zeichnet es, um das endgültige Bild zu erstellen.
### **Zeichnen mit der GraphicsPath-Klasse**
Im Folgenden wird ein Beispiel gezeigt, das die Verwendung der [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath)-Klasse demonstriert. Der Beispielquellcode wurde in mehrere Teile aufgeteilt, um ihn einfach und leicht verständlich zu halten. Schritt für Schritt zeigen die Beispiele, wie Sie:

- Ein Bild erstellen.
- Ein Graphics-Objekt initialisieren.
- Die Oberfläche löschen.
- Eine Instanz von [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) erstellen.
- Eine Figur erstellen.
- Formen zur Figur hinzufügen.
- Ein Array von Figuren erstellen.
- Pfade zeichnen.
- Pfade füllen.


### **Zeichnen von Bildern mit GraphicsPath: Programmbeispiele**
#### **GraphicsPath: Ein Bild erstellen**
Beginnen Sie damit, ein Bild zu erstellen, indem Sie eine der in Erstellen von Dateien beschriebenen Methoden verwenden.
#### **GraphicsPath: Initialisieren eines Graphics-Objekts**
Erstellen und initialisieren Sie ein Graphics-Objekt, indem Sie das Image-Objekt an seinen Konstruktor übergeben.
#### **GraphicsPath: Die Oberfläche löschen**
Löschen Sie die Graphics-Oberfläche, indem Sie die Clear-Methode der Graphics-Klasse aufrufen und eine Farbe als Parameter übergeben. Diese Methode füllt die Graphics-Oberfläche mit der übergebenen Farbe.
#### **GraphicsPath: Eine Instanz von GraphicsPath erstellen**
Erstellen Sie eine Instanz von GraphicsPath mit dem standardmäßig auf Alternative gesetzten GraphicsPath. Dieser Modus bestimmt, wie der Innenraum einer geschlossenen Figur gefüllt wird. Der andere mögliche GraphicsPath-Wert ist Winding.
#### **GraphicsPath: Eine Figur erstellen**
Erstellen Sie eine Instanz der Figure-Klasse. Wie bereits erwähnt, kann eine Figur Formen enthalten, und Formen befinden sich im Aspose.PSD.Shapes-Namespace.
#### **GraphicsPath: Formen zur Figur hinzufügen**
Die von der Figure-Klasse bereitgestellte Methode Add Shapes ermöglicht es, Formen zur Figur hinzuzufügen. In den unten stehenden Codebeispielen werden mehrere Formen zu einem Figure-Objekt hinzugefügt.
#### **GraphicsPath: Figuren einem Array hinzufügen**
Mehrere Figuren können einem GraphicsPath-Objekt mit der von der GraphicsPath-Klasse bereitgestellten AddFigures-Methode hinzugefügt werden. Diese Methode akzeptiert ein Array von Figuren als Parameter.
#### **GraphicsPath: Die Pfade zeichnen**
Zeichnen Sie den GraphicsPath mit der von der Graphics-Klasse bereitgestellten DrawPath-Methode. Die Methode akzeptiert zwei Parameter. Der erste Parameter ist ein Objekt der Pen-Klasse, das die Farbe, Breite und den Stil des Pfads bestimmt. Der zweite Parameter ist das Objekt der GraphicsPath-Klasse, das den Pfad selbst darstellt.
#### **GraphicsPath: Pfade füllen**


Ein Pfad kann gefüllt werden, indem ein GraphicsPath-Objekt an die von der Graphics-Klasse bereitgestellte Fill Paths-Methode übergeben wird. Die Fill Paths-Methode füllt den Pfad gemäß dem aktuellen Füllmodus (Alternate oder Winding), der für den Pfad festgelegt ist. Wenn der Pfad offene Figuren enthält, wird der Pfad gefüllt, als ob diese Figuren geschlossen wären.

Die Fill Paths-Methode akzeptiert zwei Parameter. Der erste Parameter ist ein Objekt einer beliebigen Pinselklasse aus dem Aspose.PSD.Brushes-Namespace. Der zweite Parameter ist der Pfad selbst. Verwenden Sie für dieses Beispiel den HatchBrush, der ein rechteckiger Pinsel mit einem Schraffurstil, einer Vordergrundfarbe und einer Hintergrundfarbe ist. Legen Sie vor dem Übergeben des HatchBrush-Objekts an die Fill Paths-Methode dessen Eigenschaften fest.
### **GraphicsPath: Vollständiger Quellcode**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Alle Klassen, die IDisposable implementieren, werden in einer Using-Anweisung instanziiert, um sicherzustellen, dass sie ordnungsgemäß entsorgt werden.

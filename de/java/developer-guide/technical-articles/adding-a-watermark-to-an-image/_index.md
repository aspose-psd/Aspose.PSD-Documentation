---
title: Hinzufügen eines Wasserzeichens zu einem Bild
type: docs
weight: 20
url: /de/java/hinzufügen-eines-wasserzeichens-zu-einem-bild/
---

## **Hinzufügen eines Wasserzeichens zu einem Bild**
Dieses Dokument erklärt, wie man mithilfe von Aspose.PSD ein Wasserzeichen zu einem Bild hinzufügt. Das Hinzufügen eines Wasserzeichens zu einem Bild ist eine häufige Anforderung in Bildverarbeitungsanwendungen. In diesem Beispiel wird die Graphics-Klasse verwendet, um einen Text auf der Oberfläche des Bildes zu zeichnen.
### **Hinzufügen eines Wasserzeichens**
Um die Operation zu demonstrieren, laden wir ein BMP-Bild von der Festplatte und zeichnen einen Text als Wasserzeichen auf die Oberfläche des Bildes mithilfe der DrawString-Methode der Graphics-Klasse. Wir speichern das Bild im PNG-Format mithilfe der PngOptions-Klasse. Unten finden Sie ein Codebeispiel, das zeigt, wie man einem Bild ein Wasserzeichen hinzufügt. Der Beispielquellcode wurde in Teile aufgeteilt, um die Nachverfolgung zu erleichtern. Schritt für Schritt zeigen die Beispiele, wie man:

1. Ein Bild laden.
1. Ein Graphics-Objekt erstellen und initialisieren.
1. Font- und SolidBrush-Objekte erstellen und initialisieren.
1. Einen Text als Wasserzeichen mit der DrawString-Methode der Graphics-Klasse zeichnen.
1. Das Bild im PNG-Format speichern.

Der folgende Codeausschnitt zeigt Ihnen, wie Sie ein Wasserzeichen auf das Bild hinzufügen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Hinzufügen eines diagonalen Wasserzeichens**
Das Hinzufügen eines diagonalen Wasserzeichens zu einem Bild ist ähnlich wie das Hinzufügen eines horizontalen Wasserzeichens, wie oben besprochen, mit einigen Unterschieden. Um die Operation zu demonstrieren, laden wir ein JPG-Bild von der Festplatte, fügen Transformationen mit einem Objekt der Matrix-Klasse hinzu und zeichnen einen Text als Wasserzeichen auf die Oberfläche des Bildes mithilfe der DrawString-Methode der Graphics-Klasse. Unten finden Sie ein Codebeispiel, das zeigt, wie man einem Bild ein diagonales Wasserzeichen hinzufügt. Der Beispielquellcode wurde in Teile aufgeteilt, um die Nachverfolgung zu erleichtern. Schritt für Schritt zeigen die Beispiele, wie man:

1. Ein Bild laden.
1. Ein Graphics-Objekt erstellen und initialisieren.
1. Font- und SolidBrush-Objekte erstellen und initialisieren.
1. Die Größe des Bildes in ein SizeF-Objekt erhalten.
1. Eine Instanz der Matrix-Klasse erstellen und Composite-Transformation durchführen.
1. Die Transformation dem Graphics-Objekt zuweisen.
1. Ein StringFormat-Objekt erstellen und initialisieren.
1. Einen Text als Wasserzeichen mit der DrawString-Methode der Graphics-Klasse zeichnen.
1. Das resultierende Bild speichern.

Der folgende Codeausschnitt zeigt Ihnen, wie Sie ein diagonales Wasserzeichen hinzufügen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}

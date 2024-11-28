---
title: Hinzufügen eines Wasserzeichens zu einem Bild
type: docs
weight: 30
url: /de/net/hinzufuegen-eines-wasserzeichens-zu-einem-bild/
---

## **Hinzufügen eines Wasserzeichens zu einem Bild**
Dieses Dokument erklärt, wie man mithilfe von Aspose.PSD ein Wasserzeichen zu einem Bild hinzufügt. Das Hinzufügen eines Wasserzeichens zu einem Bild ist eine häufige Anforderung für Bildverarbeitungsanwendungen. Dieses Beispiel verwendet die Graphics-Klasse, um einen Text auf der Bildebene zu zeichnen.
### **Hinzufügen eines Wasserzeichens**
Um die Operation zu demonstrieren, laden wir ein BMP-Bild von der Festplatte und zeichnen einen Text als Wasserzeichen auf der Bildebene mithilfe der Graphics-Klasse DrawString-Methode. Wir speichern das Bild im PNG-Format mithilfe der PngOptions-Klasse. Im Folgenden finden Sie einen Code, der zeigt, wie man einem Bild ein Wasserzeichen hinzufügt. Der Beispielquellcode wurde in Teile aufgeteilt, um das Verständnis zu erleichtern. Schritt für Schritt zeigen die Beispiele, wie man:

1. Ein Bild [laden](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2).
1. Ein [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-Objekt erstellen und initialisieren.
1. Schriftart- und [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush)-Objekte erstellen und initialisieren.
1. Einen Text als Wasserzeichen mithilfe der Graphics-Klasse [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring)-Methode zeichnen.
1. Bild im PNG-Format speichern.

Der folgende Code zeigt Ihnen, wie Sie ein Wasserzeichen auf dem Bild hinzufügen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Hinzufügen eines diagonalen Wasserzeichens**
Das Hinzufügen eines diagonalen Wasserzeichens zu einem Bild ist ähnlich wie das Hinzufügen eines horizontalen Wasserzeichens, wie oben besprochen, mit einigen Unterschieden. Um die Operation zu demonstrieren, laden wir ein JPG-Bild von der Festplatte, fügen Transformationen mithilfe eines Objekts der [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix)-Klasse hinzu und zeichnen einen Text als Wasserzeichen auf der Bildebene mithilfe der Graphics-Klasse DrawString-Methode. Im Folgenden finden Sie einen Code, der zeigt, wie man einem Bild ein diagonales Wasserzeichen hinzufügt. Der Beispielquellcode wurde in Teile aufgeteilt, um das Verständnis zu erleichtern. Schritt für Schritt zeigen die Beispiele, wie man:

1. Ein Bild laden.
1. Ein Graphics-Objekt erstellen und initialisieren.
1. [Font](https://reference.aspose.com/psd/net/aspose.psd/font)- und SolidBrush-Objekte erstellen und initialisieren.
1. Größe des Bildes im [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef)-Objekt abrufen.
1. Eine Instanz der Matrix-Klasse erstellen und eine zusammengesetzte Transformation durchführen.
1. Transformation dem Graphics-Objekt zuweisen.
1. Ein [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat)-Objekt erstellen und initialisieren.
1. Einen Text als Wasserzeichen mithilfe der Graphics-Klasse DrawString-Methode zeichnen.
1. Resultierendes Bild speichern.

Der folgende Code zeigt Ihnen, wie Sie ein diagonales Wasserzeichen hinzufügen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}

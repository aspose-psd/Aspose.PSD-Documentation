---
title: Hinzufügen einer Signatur zu einem Bild
type: docs
weight: 70
url: /de/net/hinzufugen-einer-signatur-zu-einem-bild/
---

## **Hinzufügen einer Signatur**

Das Hinzufügen einer Signatur zu einem Bild ist manchmal erforderlich, um die Bilder digital zu signieren und Fälschungen zu vermeiden. Ein anderer Gedanke könnte sein, das Bild mehr wie in einer Galerie gezeigt zu behandeln. Was auch immer der Grund ist, die Aspose.PSD APIs bieten die Möglichkeit, eine Signatur auf einem Bild hinzuzufügen, indem sie den einfachsten Mechanismus verwenden, wie unten erklärt. Bitte beachten Sie, dass dieses Beispiel die [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-Klasse verwendet, um ein anderes Bild mit einer Signatur auf die Oberfläche des Originalbildes zu zeichnen. Zur Demonstration werden wir ein PSD-Bild von der Festplatte laden und ein anderes Bild als Signatur auf die Oberfläche des Originalbildes mit der Graphics-Klasse [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage)-Methode zeichnen. Wir speichern das resultierende Bild im PNG-Format mit der [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)-Klasse. Hier ist ein Codebeispiel, das zeigt, wie man eine Signatur zu einem Bild hinzufügt. Der Beispiel-Quellcode wurde in Teile aufgeteilt, um die Nachverfolgung zu erleichtern. Schritt für Schritt zeigt das Beispiel, wie man:

- Die primären und sekundären (Signatur-)Bilder laden.
- Ein Graphics-Objekt erstellen und initialisieren.
- Ein Bild unter Verwendung der Graphics-Klasse DrawImage-Methode zeichnen.
- Das Ergebnis im PNG-Format speichern.

### **Programmbeispiele**
#### **Bilder laden**
Zunächst erstellen Sie Instanzen der Image-Klasse, um die Beispielfotos von der Festplatte zu laden.

#### **Erstellen und Initialisieren eines Grafikobjekts**
Nach dem Laden der Bilder erstellen und initialisieren Sie ein Graphics-Objekt, während Sie das Objekt des primären Bildes verwenden.

#### **Zeichnen des sekundären Bildes auf das primäre Bild**
Verwenden Sie dann die Graphics-Klasse DrawImage-Methode, um das sekundäre Bild auf das primäre Bild zu setzen. Es gibt mehrere Überladungen der DrawImage-Methode, die ein Objekt des Bildes als ersten Parameter akzeptieren, während alle anderen Parameter dem Ort entsprechen, an dem das Bild gezeichnet werden soll. Zu Demonstrationszwecken verwendet der folgende Code die Überladungsversion von DrawImage, die ein Objekt des Point als zweiten Parameter akzeptiert und versucht, die Signatur in die untere rechte Ecke des primären Bildes zu zeichnen.

#### **Speichern des Bildes**
Speichern Sie das Bild schließlich als PNG-Datei zurück auf der lokalen Festplatte unter Verwendung der PngOptions-Klasse.

#### **Vollständiger Quelltext**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}


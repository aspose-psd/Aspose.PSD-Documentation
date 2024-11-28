---
title: Hinzufügen einer Signatur zu einem Bild
type: docs
weight: 10
url: /de/java/hinzufuegen-einer-signatur-zu-einem-bild/
---

## **Hinzufügen einer Signatur**

Das Hinzufügen einer Signatur zu einem Bild ist manchmal erforderlich, um die Bilder digital zu signieren und Fälschungen zu vermeiden. Ein anderer Gedanke könnte sein, das Bild eher so zu behandeln, als ob es in einer Galerie gezeigt wird. Aus welchem ​​Grund auch immer, die Aspose.PSD APIs bieten die Möglichkeit, eine Signatur auf ein Bild hinzuzufügen, indem sie den einfachsten Mechanismus wie unten erklärt verwenden. Bitte beachten Sie, dass dieses Beispiel die Graphics-Klasse verwendet, um ein anderes Bild mit einer Signatur auf die Oberfläche des Originalbilds zu zeichnen. Um den Vorgang zu demonstrieren, laden wir ein PSD-Bild von der Festplatte und zeichnen ein anderes Bild als Signatur auf die Oberfläche des Originalbilds unter Verwendung der Graphics-Klasse DrawImage-Methode. Wir speichern das resultierende Bild im PNG-Format unter Verwendung der PngOptions-Klasse. Im Folgenden finden Sie ein Codebeispiel, das zeigt, wie Sie eine Signatur zu einem Bild hinzufügen. Der Beispielquellcode wurde in Teile aufgeteilt, um das Verständnis zu erleichtern. Schritt für Schritt zeigt das Beispiel, wie Sie vorgehen:

- Laden Sie die primären und sekundären (Signatur-)Bilder.
- Erstellen und Initialisieren eines Grafikobjekts.
- Zeichnen Sie das Bild unter Verwendung der DrawImage-Methode der Graphics-Klasse.
- Ergebnis im PNG-Format speichern.
### **Programmbeispiele**
#### **Bilder laden**
Erstellen Sie zunächst Instanzen der Image-Klasse, um die Beispielsbilder von der Festplatte zu laden.
#### **Erstellen und Initialisieren eines Grafikobjekts**
Nach dem Laden der Bilder erstellen und initialisieren Sie ein Grafikobjekt, während Sie das Objekt des primären Bildes verwenden.
#### **Sekundäres Bild auf das Primärbild zeichnen**
Verwenden Sie dann die DrawImage-Methode der Graphics-Klasse, um das sekundäre Bild auf das primäre Bild zu setzen. Es gibt mehrere Überlastungen der DrawImage-Methode, die ein Objekt des Bildes als ersten Parameter akzeptieren, während alle anderen Parameter den Ort angeben, an dem das Bild gezeichnet werden soll. Zu Demonstrationszwecken verwendet der folgende Code die Überladungsversion von DrawImage, die ein Objekt von Point als zweiten Parameter akzeptiert und versucht, die Signatur in die untere rechte Ecke des primären Bildes zu zeichnen.
#### **Speichern des Bildes**
Speichern Sie das Bild schließlich wieder auf der lokalen Festplatte als PNG-Datei unter Verwendung der PngOptions-Klasse.
#### **Vollständiger Quellcode**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}


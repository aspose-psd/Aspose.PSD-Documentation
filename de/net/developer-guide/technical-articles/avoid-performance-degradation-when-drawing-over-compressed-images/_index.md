---
title: Vermeiden Sie Leistungsverluste beim Zeichnen über komprimierten Bildern
type: docs
weight: 10
url: /de/net/vermeiden-sie-leistungsverluste-beim-zeichnen-ueber-komprimierten-bildern/
---

## **Vermeiden Sie Leistungsverluste, wenn Sie über komprimierten Bildern zeichnen**
Es gibt Momente, in denen Sie sehr umfangreiche Grafikoperationen auf einem komprimierten Bild durchführen möchten. Wenn Aspose.PSD Bilder auf die Schnelle komprimieren und dekomprimieren muss, kann es zu Leistungsverlusten kommen. Das Zeichnen über komprimierten Bildern kann ebenfalls mit einer Leistungseinbuße einhergehen.
### **Lösung**
Um Leistungsverluste zu vermeiden, empfehlen wir, das Bild in ein unkomprimiertes oder Rohformat zu konvertieren, bevor Grafikoperationen durchgeführt werden.
### **Verwendung von Dateipfaden**
Im folgenden Beispiel wird ein PSD-Bild in das Rohformat konvertiert (ohne Kompression) und auf der Festplatte gespeichert. Das unkomprimierte Bild wird dann geladen, bevor darauf Grafikoperationen durchgeführt werden. Die gleiche Technik gilt für BMP- und GIF-Dateien.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **Verwendung eines Stream-Objekts**
Der folgende Codeausschnitt zeigt Ihnen, wie ein PSD-Bild in das Rohformat konvertiert wird (ohne Kompression) und unter Verwendung von MemoryStream auf der Festplatte gespeichert wird.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}

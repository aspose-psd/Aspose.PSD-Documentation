---
title: Vermeiden Sie Leistungsverschlechterung beim Zeichnen über komprimierten Bildern
type: docs
weight: 40
url: /de/java/vermeiden-sie-leistungsverschlechterung-beim-zeichnen-über-komprimierten-bildern/
---

## **Vermeiden Sie Leistungsverschlechterung beim Zeichnen über komprimierten Bildern**
Es gibt Zeiten, in denen Sie extrem umfangreiche Grafikoperationen auf einem komprimierten Bild durchführen möchten. Wenn Aspose.PSD Bilder on-the-fly komprimieren und dekomprimieren muss, kann es zu Leistungsverschlechterung kommen. Das Zeichnen über komprimierten Bildern kann ebenfalls eine Leistungsstrafe nach sich ziehen.
### **Lösung**
Um Leistungsverschlechterung zu vermeiden, empfehlen wir, das Bild in ein nicht komprimiertes oder Rohformat zu konvertieren, bevor Grafikoperationen durchgeführt werden.
### **Verwendung eines Dateipfads**
Im folgenden Beispiel wird ein PSD-Bild in ein Rohformat (ohne Kompression) umgewandelt und auf der Festplatte gespeichert. Das unkomprimierte Bild wird dann geladen, bevor Grafikoperationen durchgeführt werden. Die gleiche Technik gilt für BMP- und GIF-Dateien.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Verwendung eines Stream-Objekts**
Der folgende Codeausschnitt zeigt Ihnen, wie ein PSD-Bild in ein Rohformat (ohne Kompression) umgewandelt und mit einem Stream auf der Festplatte gespeichert wird.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}

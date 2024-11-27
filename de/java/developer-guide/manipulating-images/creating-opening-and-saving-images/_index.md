---
title: Erstellen, Öffnen und Speichern von Bildern
type: docs
weight: 30
url: /de/java/erstellen-öffnen-und-speichern-von-bildern/
---

## **Bilddateien erstellen**
Aspose.PSD für Java ermöglicht es Entwicklern, eigene Bilder zu erstellen. Verwenden Sie die statische Create-Methode der Image-Klasse, um neue Bilder zu erstellen. Alles, was Sie tun müssen, ist ein geeignetes Objekt einer Klasse aus dem ImageOptions-Namespace für das gewünschte Ausgabeformat bereitzustellen. Um eine Bilddatei zu erstellen, erstellen Sie zunächst eine Instanz einer Klasse aus dem ImageOptions-Namespace. Diese Klassen bestimmen das Ausgabeformat des Bildes. Nachfolgend finden Sie einige Klassen aus dem ImageOptions-Namespace (beachten Sie, dass derzeit nur die PSD-Dateiformate-Familie für die Erstellung unterstützt wird):

PsdOptions legt die Optionen für das Erstellen einer PSD-Datei fest. Bilddateien können erstellt werden, indem Sie einen Ausgabepfad festlegen oder indem Sie einen Stream festlegen.
### **Erstellen durch Festlegen des Pfades**
Erstellen Sie PsdOptions aus dem ImageOptions-Namespace und legen Sie die verschiedenen Eigenschaften fest. Die wichtigste Eigenschaft, die festgelegt werden muss, ist die Source-Eigenschaft. Diese Eigenschaft gibt an, wo die Bilddaten gespeichert sind (in einer Datei oder einem Stream). Im folgenden Beispiel ist die Quelle eine Datei. Nachdem die Eigenschaften festgelegt wurden, übergeben Sie das Objekt zusammen mit Breite und Höhe-Parametern an eine der statischen Create-Methoden. Die Breite und Höhe sind in Pixel definiert.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Erstellen unter Verwendung eines Streams**
Der Prozess zum Erstellen eines Bildes unter Verwendung eines Streams ist identisch mit dem für die Verwendung eines Pfads. Der einzige Unterschied besteht darin, dass Sie eine Instanz von StreamSource erstellen müssen, indem Sie einem Stream-Objekt in seinem Konstruktor übergeben und es der Source-Eigenschaft zuweisen.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Bilddateien öffnen**
Entwickler können die Aspose.PSD für Java-API verwenden, um vorhandene PSD-Bilddateien für verschiedene Zwecke zu öffnen, z. B. um Effekte auf das Bild hinzuzufügen oder eine vorhandene Datei in ein anderes Format zu konvertieren. Unabhängig vom Zweck bietet Aspose.PSD zwei Standardmethoden zum Öffnen vorhandener Dateien: aus einer Datei oder aus einem Stream.
### **Öffnen von der Festplatte**
Öffnen Sie eine Bilddatei, indem Sie den Pfad und den Dateinamen als Parameter an die statische Methode Load übergeben, die von der Image-Klasse bereitgestellt wird.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Öffnen mit einem Stream**
Manchmal ist das Bild, das geöffnet werden soll, als Stream gespeichert. In solchen Fällen verwenden Sie die überladene Version der Load-Methode. Diese akzeptiert ein Stream-Objekt als Argument zum Öffnen des Bildes.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Bild als Ebene laden**
Dieser Artikel zeigt die Verwendung von Aspose.PSD zum Laden eines Bildes als Ebene. Aspose.PSD-APIs haben effiziente und benutzerfreundliche Methoden freigelegt, um dieses Ziel zu erreichen. Aspose.PSD hat die AddLayer-Methode der PsdImage-Klasse freigelegt, um ein Bild als Ebene in eine PSD-Datei hinzuzufügen.

Die Schritte zum Laden eines Bildes in PSD als Ebene sind so einfach wie unten beschrieben:

- Erstellen Sie eine Instanz eines Bildes mit der PsdImage-Klasse mit angegebener Breite und Höhe.
- Laden Sie eine PSD-Datei als Bild mit der von der Image-Klasse bereitgestellten Factory-Methode Load.
- Erstellen Sie eine Instanz der Layer-Klasse und weisen Sie die PSD-Bildebene zu.
- Fügen Sie die erstellte Ebene mit der von der PsdImage-Klasse freigelegten AddLayer-Methode hinzu.
- Speichern Sie die Ergebnisse.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Bilddateien speichern**
Mit Aspose.PSD können Sie Bilddateien von Grund auf erstellen. Es bietet auch die Möglichkeit, vorhandene Bilddateien zu bearbeiten. Sobald das Bild erstellt oder geändert wurde, wird die Datei normalerweise auf der Festplatte gespeichert. Aspose.PSD bietet Ihnen Methoden zum Speichern von Bildern auf der Festplatte, indem Sie einen Pfad angeben oder ein Stream-Objekt verwenden.
### **Speichern auf der Festplatte**
Die Image-Klasse stellt ein Bildobjekt dar, daher bietet diese Klasse alle Werkzeuge, die zum Erstellen, Laden und Speichern einer Bilddatei benötigt werden. Verwenden Sie die Image-Klasse Save-Methode, um Bilder zu speichern. Eine überladene Version der Save-Methode akzeptiert den Dateispeicherort als Zeichenfolge.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Speichern in einem Stream**
Eine weitere überladene Version der Save-Methode akzeptiert das Stream-Objekt als Argument und speichert die Bilddatei im Stream.

Wenn das Bild durch Festlegung eines der CreateOptions im Image-Konstruktor erstellt wird, wird das Bild automatisch auf dem Pfad oder im Stream gespeichert, der während der Initialisierung der Image-Klasse bereitgestellt wurde, indem die Save-Methode aufgerufen wird, die keinen Parameter akzeptiert.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Einstellung zum Ersetzen fehlender Schriftarten**
Entwickler können die Aspose.PSD für Java-API verwenden, um vorhandene PSD-Bilddateien für verschiedene Zwecke zu laden, z. B. um den Standard-Schriftnamen festzulegen, wenn PSD-Dokumente als Rasterbild (in PNG, JPG und BMP Formaten) gespeichert werden. Diese Standardschrift sollte als Ersatz für alle fehlenden Schriftarten (Schriftarten, die im aktuellen Betriebssystem nicht gefunden werden) verwendet werden. Sobald das Bild geändert wurde, wird die Datei auf der Festplatte gespeichert.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}

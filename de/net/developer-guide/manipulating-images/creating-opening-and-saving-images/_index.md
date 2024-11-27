---
title: Erstellen, Öffnen und Speichern von Bildern
type: docs
weight: 30
url: /de/net/erstellen-öffnen-und-speichern-von-bildern/
---

## **Erstellen von Bilddateien**
Aspose.PSD für .NET ermöglicht es Entwicklern, eigene Bilder zu erstellen. Verwenden Sie die von der Image-Klasse bereitgestellte statische Create-Methode, um neue Bilder zu erstellen. Alles, was Sie tun müssen, ist, ein geeignetes Objekt einer der Klassen aus dem ImageOptions-Namespace für das gewünschte Ausgabeformat des Bildes zu übergeben. Um eine Bilddatei zu erstellen, erstellen Sie zunächst eine Instanz einer der Klassen aus dem ImageOptions-Namespace. Diese Klassen bestimmen das Ausgabeformat des Bildes. Im Folgenden sind einige Klassen aus dem ImageOptions-Namespace aufgeführt (beachten Sie, dass derzeit nur die PSD-Dateiformate-Familie für die Erstellung unterstützt wird):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) legt die Optionen für das Erstellen einer PSD-Datei fest. Bilddateien können erstellt werden, indem ein Ausgabepfad festgelegt wird oder indem ein Stream festgelegt wird.
### **Erstellen durch Festlegen des Pfades**
Erstellen Sie PsdOptions aus dem [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) -Namespace und legen Sie die verschiedenen Eigenschaften fest. Die wichtigste Eigenschaft, die festgelegt werden muss, ist die Source-Eigenschaft. Diese Eigenschaft gibt an, wo die Bilddaten gespeichert sind (in einer Datei oder einem Stream). Im folgenden Beispiel stammt die Quelle aus einer Datei. Nach dem Festlegen der Eigenschaften übergeben Sie das Objekt zusammen mit Breite und Höhe-Parametern an eine der statischen [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) -Methoden. Die Breite und Höhe sind in Pixeln definiert.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Erstellen unter Verwendung eines Streams**
Der Prozess zum Erstellen eines Bildes mithilfe eines Streams ist derselbe wie beim Verwenden eines Pfads. Der einzige Unterschied besteht darin, dass Sie eine Instanz von [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) erstellen, indem Sie einem Streamobjekt an seinen Konstruktor übergeben und es der Source-Eigenschaft zuweisen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Öffnen von Bilddateien**
Entwickler können die Aspose.PSD für .NET-API verwenden, um vorhandene PSD-Bilddateien für verschiedene Zwecke zu öffnen, z.B. um Effekte zum Bild hinzuzufügen oder eine vorhandene Datei in ein anderes Format zu konvertieren. Was auch immer der Zweck ist, Aspose.PSD bietet zwei Standardwege, um vorhandene Dateien zu öffnen: von einer Datei oder von einem Stream.
### **Öffnen von der Festplatte**
Öffnen einer Bilddatei, indem Sie den Pfad und den Dateinamen als Parameter an die statische Methode Load übergeben, die von der Image-Klasse freigegeben wird.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Öffnen unter Verwendung eines Streams**
Manchmal ist das Bild, das wir öffnen müssen, in einem Stream gespeichert. In solchen Fällen verwenden Sie die überladene Version der Load-Methode. Diese akzeptiert ein Streamobjekt als Argument, um das Bild zu öffnen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Bild als Ebene laden**
Dieser Artikel demonstriert die Verwendung von Aspose.PSD, um ein Bild als Ebene zu laden. Aspose.PSD-APIs haben effiziente und benutzerfreundliche Methoden bereitgestellt, um dieses Ziel zu erreichen. Aspose.PSD hat die AddLayer-Methode der PsdImage-Klasse freigegeben, um ein Bild in eine PSD-Datei als Ebene hinzuzufügen.

Die Schritte zum Laden eines Bildes in PSD als Ebene sind so einfach wie folgt:

- Erstellen Sie eine Instanz eines Bildes mit der PsdImage-Klasse mit einer angegebenen Breite und Höhe.
- Laden Sie eine PSD-Datei als Bild mit der von der Image-Klasse freigegebenen Factory-Methode Load.
- Erstellen Sie eine Instanz der Layer-Klasse und weisen Sie das PSD-Bild der Ebene zu.
- Fügen Sie die erstellte Ebene mit der von der PsdImage-Klasse freigegebenen AddLayer-Methode hinzu.
- Speichern Sie die Ergebnisse.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Bild als Ebene aus einem Stream laden**
Dieser Artikel demonstriert die Verwendung von Aspose.PSD, um ein Bild als Ebene aus einem Stream zu laden. Um ein Bild aus einem Stream zu laden, übergeben Sie einfach ein Streamobjekt, das ein Bild enthält, an den Konstruktor der Layer-Klasse. Fügen Sie die erstellte Ebene mit der von der PsdImage-Klasse freigegebenen AddLayer-Methode hinzu und speichern Sie die Ergebnisse.


Hier ist der Beispielcode.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Speichern von Bilddateien**
Mit Aspose.PSD können Sie Bilddateien von Grund auf erstellen. Es bietet auch Mittel zur Bearbeitung vorhandener Bilddateien. Sobald das Bild erstellt oder geändert wurde, wird die Datei normalerweise auf der Festplatte gespeichert. Aspose.PSD bietet Ihnen Methoden zum Speichern von Bildern auf der Festplatte, indem Sie einen Pfad angeben oder ein Stream-Objekt verwenden.
### **Speichern auf der Festplatte**
Die Image-Klasse stellt ein Bildobjekt dar, daher bietet diese Klasse alle Werkzeuge, die benötigt werden, um ein Bild zu erstellen, zu laden und zu speichern. Verwenden Sie die Save-Methode der Image-Klasse, um Bilder zu speichern. Eine überladene Version der Save-Methode akzeptiert den Dateispeicherort als Zeichenfolge.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Speichern in einen Stream**
Eine weitere überladene Version der Save-Methode akzeptiert das Stream-Objekt als Argument und speichert die Bilddatei im Stream.

Wenn das Bild durch Angabe einer der CreateOptions im Image-Konstruktor erstellt wird, wird das Bild automatisch auf dem beim Initialisieren der Image-Klasse bereitgestellten Pfad oder Stream gespeichert, indem die Save-Methode aufgerufen wird, die keinen Parameter akzeptiert.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Einstellungen zum Ersetzen fehlender Schriftarten**
Entwickler können die Aspose.PSD für .NET-API verwenden, um vorhandene PSD-Bilddateien für verschiedene Zwecke zu laden, z.B. um den Standard-Schriftartnamen festzulegen, wenn PSD-Dokumente als Rasterbild (in PNG-, JPG- und BMP-Formaten) gespeichert werden. Diese Standard-Schriftart sollte als Ersatz für alle fehlenden Schriftarten (Schriftarten, die im aktuellen Betriebssystem nicht gefunden werden) verwendet werden. Sobald das Bild geändert wurde, wird die Datei auf der Festplatte gespeichert.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}

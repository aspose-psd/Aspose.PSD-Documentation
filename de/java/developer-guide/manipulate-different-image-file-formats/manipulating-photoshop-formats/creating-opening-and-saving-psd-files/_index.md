---
title: Erstellen, Öffnen und Speichern von PSD-Dateien
type: docs
weight: 10
url: /de/erstellen-öffnen-und-speichern-von-psd-dateien/
---

## **Bildexport nach PSD**
PSD (PhotoShop-Dokument) ist das Standarddateiformat, das von Adobe PhotoShop zum Arbeiten mit Bildern verwendet wird. Aspose.PSD ermöglicht es Ihnen, Dateien in PSD zu laden, zu bearbeiten und zu speichern, damit sie in PhotoShop geöffnet und bearbeitet werden können. Dieser Artikel zeigt, wie eine Datei mit Aspose.PSD in PSD gespeichert werden kann, und er erörtert auch einige der Einstellungen, die beim Speichern in diesem Format verwendet werden können. PsdOptions ist eine spezialisierte Klasse im Namespace ImageOptions, die zum Exportieren von Bildern nach PSD verwendet wird. Um in PSD zu exportieren, erstellen Sie eine Instanz der Klasse Image, entweder aus einer vorhandenen Bilddatei (z. B. Vorschaubilder) oder von Grund auf neu erstellt. Dieser Artikel erklärt, wie das geht. In den folgenden Beispielen wird ein Bild von Grund auf neu erstellt. Sobald es erstellt und die Pixeldaten bevölkert sind, speichern Sie das Bild mit der Save-Methode der Klasse Image und übergeben Sie ein PsdOptions-Objekt als zweites Argument. Mehrere Eigenschaften der Klasse PsdOptions können für eine erweiterte Konvertierung festgelegt werden. Einige der Eigenschaften sind ColorMode, CompressionMethod und Version. Aspose.PSD unterstützt die folgenden Komprimierungsmethoden durch die Enumeration CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Die folgenden Farbmodi werden durch die Enumeration ColorModes unterstützt:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Zusätzliche Ressourcen können hinzugefügt werden, wie z. B. Miniaturressourcen für PSD v4.0, v5.0 und höher oder Raster- und Hilfslinienressourcen für PSD v4.0 und höher. Der folgende Code erstellt eine BMP-Datei von Grund auf neu, bevölkert die Pixel und speichert sie in PSD mit RLE-Komprimierung und Graustufen-Farbmodus. Der folgende Codeausschnitt zeigt Ihnen, wie ein Bild nach PSD exportiert wird.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Importieren von Bildern in eine PSD-Schicht**
In diesem Artikel wird die Verwendung von Aspose.PSD demonstriert, um ein Bild zu einer PSD-Schicht hinzuzufügen oder zu importieren. Aspose.PSD-APIs haben effiziente und benutzerfreundliche Methoden freigelegt, um dieses Ziel zu erreichen. Aspose.PSD hat die Methode DrawImage der Klasse Layer freigelegt, um ein Bild in eine PSD-Datei hinzuzufügen/importieren. Die Methode DrawImage benötigt Ort- und Bildwerte, um ein Bild in eine PSD-Datei hinzuzufügen/importieren. Die Schritte zum Importieren eines Bildes in eine PSD-Schicht sind so einfach wie unten beschrieben:

- Laden Sie eine PSD-Datei als Bild mit der Factory-Methode Load der Klasse Image.
- Erstellen Sie eine Instanz der Klasse Layer und weisen Sie die PSD-Bildschicht dazu zu.
- Laden Sie das Bild, das hinzugefügt werden muss, oder erstellen Sie eines von Grund auf neu.
- Rufen Sie die Methode Layer.DrawImage auf und geben Sie den Ort und die Bildinstanz an.
- Speichern Sie die Ergebnisse.



Der folgende Codeausschnitt zeigt Ihnen, wie ein Bild in eine PSD-Schicht importiert wird.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Erstellen von Miniaturansichten aus PSD-Dateien**
PSD ist das native Dokumentenformat der Anwendung Adobe Photoshop. Adobe Photoshop (Version 5.0 und höher) speichert Miniaturinformationen für die Vorschauanzeige in einem Bildressourcenblock, der aus einem anfänglichen 28-Byte-Header besteht, gefolgt von einer JFIF-Miniaturansicht in RGB (Rot, Grün, Blau) Reihenfolge. Die Aspose.PSD-API bietet einen einfach zu bedienenden Mechanismus, um auf die Ressourcen einer PSD-Datei zuzugreifen. Diese Ressourcen umfassen auch die Miniaturressource, die ihrerseits abgerufen und je nach Anwendungsbedarf auf die Festplatte gespeichert werden kann. Der folgende Codeausschnitt zeigt Ihnen, wie Miniaturansichten aus PSD-Dateien erstellt werden können.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Erstellen von indizierten PSD-Dateien**
Die Aspose.PSD for Java API kann indizierte PSD-Dateien von Grund auf neu erstellen. In diesem Artikel wird die Verwendung der Klassen PsdOptions und PsdImage zur Erstellung eines indizierten PSD beim Zeichnen einiger Formen über die neu erstellte Leinwand demonstriert. Die folgenden einfachen Schritte sind erforderlich, um eine indizierte PSD-Datei zu erstellen.

- Erstellen Sie eine Instanz von PsdOptions und setzen Sie deren Quelle.
- Setzen Sie die Eigenschaft ColorMode der PsdOptions auf ColorModes.Indexed.
- Erstellen Sie eine neue Palette von Farben aus dem RGB-Raum und setzen Sie sie als Eigenschaft Palette von PsdOptions.
- Setzen Sie die Eigenschaft CompressionMethod auf den erforderlichen Komprimierungsalgorithmus.
- Erstellen Sie ein neues PSD-Bild, indem Sie die Methode PsdImage.Create aufrufen.
- Zeichnen Sie Grafiken oder führen Sie andere Operationen nach Bedarf aus.
- Rufen Sie die Methode PsdImage.Save auf, um alle Änderungen zu bestätigen.



Der folgende Codeausschnitt zeigt Ihnen, wie indizierte PSD-Dateien erstellt werden können.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **Exportieren von PSD-Schicht in Rasterbild**
Aspose.PSD for Java ermöglicht es Ihnen, Ebenen in einer PSD-Datei in Rasterbilder zu exportieren. Verwenden Sie bitte die Methode Aspose.PSD.FileFormats.Psd.Layers.Layer.Save, um die Ebene in ein Bild zu exportieren. Der folgende Beispielcode lädt eine PSD-Datei und exportiert jede ihrer Schichten in ein PNG-Bild mit Hilfe von Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Nachdem alle Schichten in PNG-Bilder exportiert wurden, können Sie sie mit Ihrem bevorzugten Bildbetrachter öffnen. Der folgende Codeausschnitt zeigt Ihnen, wie eine PSD-Schicht in ein Rasterbild exportiert wird.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}

---
title: Bearbeitung von Adobe Photoshop-Formaten
type: docs
weight: 20
url: /de/net/manipulating-adobe-photoshop-formats/
---

## **Verschmelzen von PSD-Ebenen mit anderen Ebenen**

## **Bildexport in PSD**
PSD, Photoshop-Dokument, ist das Standarddateiformat, das von Adobe Photoshop zum Arbeiten mit Bildern verwendet wird. Aspose.PSD ermöglicht es Ihnen, Dateien im PSD-Format zu laden, zu bearbeiten und zu speichern, damit sie in Photoshop geöffnet und bearbeitet werden können. In diesem Artikel wird gezeigt, wie eine Datei als PSD mit Aspose.PSD gespeichert wird, und es werden auch einige der Einstellungen erläutert, die beim Speichern in diesem Format verwendet werden können. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) ist eine spezialisierte Klasse im [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)-Namespace, die zum Exportieren von Bildern in PSD verwendet wird. Um in PSD zu exportieren, erstellen Sie eine Instanz der Image-Klasse, entweder geladen aus einer vorhandenen Bilddatei (zum Beispiel Miniaturansichten) oder von Grund auf erstellt. Dieser Artikel erklärt wie. In den folgenden Beispielen wird ein Bild von Grund auf erstellt. Nachdem es erstellt und die Pixeldaten bevölkert wurden, speichern Sie das Bild unter Verwendung der Save-Methode der Image-Klasse und geben ein PsdOptions-Objekt als zweites Argument an. Einige der Eigenschaften der PsdOptions-Klasse können für eine erweiterte Konvertierung eingestellt werden. Einige der Eigenschaften sind ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) und Version. Aspose.PSD unterstützt die folgenden Komprimierungsmethoden durch die Aufzählung CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Die folgenden Farbmodi werden durch die [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes)-Aufzählung unterstützt:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

Zusätzliche Ressourcen können hinzugefügt werden, wie Miniaturressourcen für PSD v4.0, v5.0 und höher, oder Raster- und Hilfe-Ressourcen für PSD v4.0 und höher. Der folgende Code erstellt eine Bilddatei von Grund auf, bevölkert die Pixel und speichert sie als PSD mit RLE-Komprimierung und Graustufen-Farbmodus. Der folgende Codeausschnitt zeigt, wie man ein Bild in PSD exportiert.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-BildexportNachPSD-BildexportNachPSD.cs" >}}

## **Importieren eines Bildes in eine PSD-Ebene**
Dieser Artikel demonstriert die Verwendung von Aspose.PSD, um ein Bild zu einer PSD-Ebene hinzuzufügen oder zu importieren. Aspose.PSD-APIs haben effiziente und benutzerfreundliche Methoden bereitgestellt, um dieses Ziel zu erreichen. Aspose.PSD hat die Methode [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) der Layer-Klasse freigelegt, um ein Bild in eine PSD-Datei hinzuzufügen/importieren. Die DrawImage-Methode benötigt Standort- und Bildwerte, um ein Bild in eine PSD-Datei hinzuzufügen/importieren. Die Schritte zum Importieren eines Bildes in eine PSD-Ebene sind ganz einfach:

- Laden Sie eine PSD-Datei als Bild mit der von der Image-Klasse freigegebenen Factory-Methode Load.
- Erstellen Sie eine Instanz der Layer-Klasse aus dem Stream mit der Datei Png, Jpeg, Tiff, Gif, Bmp, Psd oder j2k.
- Fügen Sie die Ebene mit der AddLayer-Methode zum Psd hinzu.
- Speichern Sie die Ergebnisse.

Der folgende Codeausschnitt zeigt Ihnen, wie Sie das Bild in die PSD-Ebene importieren.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-Öffnen-LadenBildVonStream-LadenBildVonStream.cs" >}}

## **Farbersetzung in PSD-Ebenen**
Dieser Artikel demonstriert die Verwendung von Aspose.PSD, um ein Bild zu einer PSD-Ebene hinzuzufügen oder zu importieren. Aspose.PSD-APIs haben effiziente und benutzerfreundliche Methoden bereitgestellt, um dieses Ziel zu erreichen. Aspose.PSD hat die DrawImage-Methode der Layer-Klasse freigelegt, um ein Bild in eine PSD-Datei hinzuzufügen/importieren. Die DrawImage-Methode benötigt Standort- und Bildwerte, um ein Bild in eine PSD-Datei hinzuzufügen/importieren. Die Schritte zum Importieren eines Bildes in eine PSD-Ebene sind ganz einfach:

- Laden Sie eine PSD-Datei als Bild mit der von der Image-Klasse freigegebenen Factory-Methode Load.
- Erstellen Sie eine Instanz der Layer-Klasse und weisen Sie ihr die PSD-Bildebene zu.
- Laden Sie das Bild, das hinzugefügt werden soll, oder erstellen Sie es von Grund auf neu.
- Rufen Sie die Methode Layer.DrawImage auf und geben Sie Standort und Bildinstanz an.
- Speichern Sie die Ergebnisse.

Der folgende Codeausschnitt zeigt Ihnen, wie Sie ein Bild in eine PSD-Ebene importieren.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-FarbersetzungInPSD-FarbersetzungInPSD.cs" >}}

## **Erstellen von Miniaturansichten aus PSD-Dateien**
PSD ist das native Dokumentenformat der Adobe Photoshop-Anwendung. Adobe Photoshop (Version 5.0 und höher) speichert Miniaturinformationen für die Vorschauanzeige in einem Bildressourcenblock, der aus einem ersten 28-Byte-Header besteht, gefolgt von einer JFIF-Miniaturansicht in RGB (Rot, Grün, Blau) Reihenfolge. Aspose.PSD-API bietet einen einfach zu bedienenden Mechanismus zum Zugriff auf die Ressourcen der PSD-Datei. Diese Ressourcen enthalten auch die Miniaturansichtsressource, die wiederum abgerufen und bei Bedarf auf Datenträger gespeichert werden kann. Der folgende Codeausschnitt zeigt Ihnen, wie Sie Miniaturansichten aus PSD-Dateien erstellen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-ErstellenVonMiniaturansichtenAusPSD-Dateien-ErstellenVonMiniaturansichtenAusPSD-Dateien.cs" >}}

## **Erstellen von indizierten PSD-Dateien**
Aspose.PSD für .NET API kann indizierte PSD-Dateien von Grund auf erstellen. Dieser Artikel demonstriert die Verwendung von PsdOptions und [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage)-Klassen zum Erstellen einer indizierten PSD beim Zeichnen einiger Formen über die neu erstellte Leinwand. Es sind die folgenden einfachen Schritte erforderlich, um eine indizierte PSD-Datei zu erstellen.

- Erstellen Sie eine Instanz von PsdOptions und setzen Sie ihre Quelle.
- Setzen Sie die ColorMode-Eigenschaft der PsdOptions auf ColorModes.Indexed.
- Erstellen Sie eine neue Palette von Farben aus dem RGB-Raum und setzen Sie sie als Palette-Eigenschaft der PsdOptions.
- Setzen Sie die CompressionMethod-Eigenschaft auf den gewünschten Komprimierungsalgorithmus.
- Erstellen Sie ein neues PSD-Bild, indem Sie die PsdImage.[Erstellen](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create)-Methode aufrufen.
- Zeichnen Sie Grafiken oder führen Sie andere Operationen nach Bedarf durch.
- Rufen Sie die PsdImage.Save-Methode auf, um alle Änderungen zu übernehmen.

Der folgende Codeausschnitt zeigt Ihnen, wie Sie indizierte PSD-Dateien erstellen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-ErstellenIndiziertePSD-Dateien-ErstellenIndiziertePSD-Dateien.cs" >}}

## **Exportieren von PSD-Ebene in Rasterbild**
Aspose.PSD für .NET ermöglicht es Ihnen, Ebenen in einer PSD-Datei in Rasterbilder zu exportieren. Bitte verwenden Sie die [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index)-Methode, um die Ebene in das Bild zu exportieren. Der folgende Beispielscode lädt eine PSD-Datei und exportiert jede ihrer Ebenen in ein PNG-Bild unter Verwendung der Aspose.PSD.FileFormats.Psd.Layers.Layer.Save-Methode. Sobald alle Ebenen in PNG-Bilder exportiert sind, können Sie diese in Ihrem bevorzugten Bildbetrachter öffnen. Der folgende Codeausschnitt zeigt Ihnen, wie Sie eine PSD-Ebene in ein Rasterbild exportieren.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-ExportierenPSDEbeneInRasterbild-ExportierenPSDEbeneInRasterbild.cs" >}}

## **Aktualisieren der Textebene in einer PSD-Datei**
Aspose.PSD für .NET ermöglicht es Ihnen, den Text in der Textebene einer PSD-Datei zu bearbeiten. Bitte verwenden Sie die [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)-Klasse, um den Text in der PSD-Ebene zu aktualisieren. Der folgende Codeausschnitt lädt eine PSD-Datei, greift auf die Textebene zu, aktualisiert den Text und speichert die PSD-Datei unter einem neuen Namen mit der Methode [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-AktualisierenDerTextebeneInPSD-Datei-AktualisierenDerTextebeneInPSD-Datei.cs" >}}

## **Erkennen einer flachen PSD**
Aspose.PSD für .NET ermöglicht es Ihnen zu erkennen, ob eine angegebene PSD-Datei flach ist oder nicht. Die Eigenschaft IsFlatten wurde in die Klasse Aspose.PSD.FileFormats.Psd.PsdImage eingeführt, um diese Funktionalität zu erreichen. Der folgende Codeausschnitt lädt eine PSD-Datei und greift auf die Eigenschaft [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten) zu.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-ErkennenFlacherPSD-ErkennenFlacherPSD.cs" >}}

## **Verschmelzen von PSD-Ebenen**
In diesem Artikel wird gezeigt, wie man Ebenen in einer PSD-Datei verschmilzt, während eine PSD-Datei in JPG mit Aspose.PSD konvertiert wird. Im folgenden Beispiel wird eine vorhandene PSD-Datei geladen, indem der Dateipfad an die statische Load-Methode der Image-Klasse übergeben wird. Nachdem sie geladen wurde, konvertiert/kastiert das Bild zum PsdImage. Erstellen Sie eine Instanz der JpegOptions-Klasse und setzen Sie verschiedene Eigenschaften. Rufen Sie nun die Save-Methode der PsdImage-Instanz auf. Der folgende Codeausschnitt zeigt Ihnen, wie Sie PSD-Ebenen verschmelzen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-VerschmelzenVonPSDEbenen-VerschmelzenVonPSDEbenen.cs" >}}

## **Graustufenunterstützung mit Alpha für PSD**
In diesem Artikel wird gezeigt, wie man Graustufen mit Alpha für eine PSD-Datei unterstützt, während eine PSD-Datei in PNG mit Aspose.PSD konvertiert wird. Im folgenden Beispiel wird eine vorhandene PSD-Datei durch Übergeben des Dateipfads an die statische Load-Methode der Image-Klasse geladen. Nachdem sie geladen wurde, wird das Bild zum PsdImage umgewandelt/konvertiert. Erstellen Sie eine Instanz der PngOptions-Klasse und setzen Sie ihre verschiedenen Eigenschaften. Setzen Sie die [ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype)-Eigenschaft auf TruecolorWithAlpha. Rufen Sie nun die Save-Methode der PngOptions-Instanz auf. Der folgende Codeausschnitt zeigt Ihnen, wie Sie in Graustufen mit Alpha konvertieren.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-GraustufenunterstützungMitAlpha-GraustufenunterstützungMitAlpha.cs" >}}

## **Unterstützung von Ebeneneffekten für PSD**
Dieser Artikel zeigt, wie man verschiedene Effekte wie **Unschärfe**, **Inneren** **Glanz**, **Nach außen** **Glanz** für PSD-Ebenen unterstützt. Der folgende Codeausschnitt zeigt Ihnen, wie man Ebeneneffekte unterstützt.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-UnterstützungFürEbenenInPSD-UnterstützungFürEbenenInPSD.cs" >}}

## **Unterstützung für Erstellungsdatum- und Uhrzeit-Ebene**
Dieser Artikel zeigt, wie man das Datums- und Uhrzeit-Ebenerstellungsdatum für PSD-Ebenen unterstützt. Der folgende Codeausschnitt zeigt Ihnen, wie man Ebenen erstellt.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-ModifizierenUndKonvertierenBilder-PSD-Ebenenerstellungsdatum-und-zeit-Ebenenerstellungsdatum-und-zeit.cs" >}}
---
title: Bilder bearbeiten
type: docs
weight: 50
url: /de/net/modifying-images/
---

## **Dithering für Rasterbilder**
Dithering ist eine Technik zur Erzeugung der Illusion neuer Farben und Schattierungen durch Variation des Punktmusters, das tatsächlich ein Bild erzeugt. Es ist das häufigste Mittel, um den Farbbereich von Bildern auf 256 (oder weniger) Farben zu reduzieren. Aspose.PSD bietet die Unterstützung für Dithering für die Klasse [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), indem die Methode Dither eingeführt wird, die zwei Parameter akzeptiert. Der erste ist vom Typ DitheringMethod, der mit zwei möglichen Optionen angewendet werden soll: FloydSteinbergDithering und ThresholdDithering. Der zweite Parameter für die Methode [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) ist die Bit-Anzahl als Ganzzahl. BitCount definiert die Abtastgröße für das Dithering-Ergebnis. Der Standardwert ist 1, der Schwarz und Weiß darstellt, während die erlaubten Werte 1, 4, 8 sind, die Paletten mit 2, 4 und 256 Farben generieren, bzw.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}
## **Helligkeit, Kontrast und Gamma anpassen**
Farbanpassungen in digitalen Bildern sind eine der wichtigsten Funktionen, die die meisten Bildverarbeitungsbibliotheken bereitstellen. Farbanpassungen können in folgende Kategorien eingeteilt werden.

1. Helligkeit bezieht sich auf die Helligkeit oder Dunkelheit einer Farbe. Durch Erhöhen der Helligkeit eines Bildes werden alle Farben aufgehellt, während durch Verringern der Helligkeit alle Farben verdunkelt werden.
1. Kontrast steht für die Hervorhebung von Objekten oder Details innerhalb eines Bildes. Durch Erhöhen des Kontrasts eines Bildes wird der Unterschied zwischen hellen und dunklen Bereichen erhöht, sodass die hellen Bereiche heller und die dunklen Bereiche dunkler werden. Durch Verringern des Kontrasts bleiben die helleren und dunkleren Bereiche etwa gleich, aber das Gesamtbild wird homogener.
1. Gamma optimiert den Kontrast und die Helligkeit der indirekten Beleuchtung, die ein Objekt im Bild beleuchtet.
### **Helligkeit anpassen**
Die Aspose.PSD für .NET API bietet die Methode [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) für die Klasse [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), die verwendet werden kann, um die Helligkeit des Bildes durch Übergabe eines Ganzzahlwerts als Parameter anzupassen. Der höchste Parameterwert steht für ein helleres Bild. Hier ist das Originalbild und das resultierende Bild zum Vergleich.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}


### **Kontrast anpassen**
Die von der Klasse [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) bereitgestellte Methode [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) kann verwendet werden, um den Kontrast eines Bildes durch Übergabe eines Gleitkommawerts als Parameter anzupassen.

Der höchste Parameterwert steht für einen höheren Kontrast im gegebenen Bild. Hier ist das Originalbild und das resultierende Bild zum Vergleich.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}
### **Gamma anpassen**
Die von der Klasse [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) bereitgestellte Methode [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) hat zwei Versionen. Eine der Überladungen akzeptiert einen Gleitkommawert und führt die Gammakorrektur für die Koeffizienten der Rot-, Blau- und Grünkanäle durch. Die andere Überladung akzeptiert drei Gleitkommawerte, die jeweils einen Farbkoeffizienten separat darstellen. Das folgende Codebeispiel zeigt, wie die Gamma-Anpassung an einem Bild durchgeführt wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}
## **Ein Bild verwischen**
Dieser Artikel zeigt die Verwendung von Aspose.PSD für .NET, um einen Weichzeichnungseffekt auf einem Bild durchzuführen. Aspose.PSD APIs haben effiziente und benutzerfreundliche Methoden zur Erzielung dieses Ziels freigelegt. Aspose.PSD für .NET hat die Klasse [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) bereitgestellt, um einen Weichzeichnungseffekt in Echtzeit zu erzeugen. Die [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions)-Klasse benötigt Radius- und Sigma-Werte, um einen Weichzeichnungseffekt auf einem Bild zu erzeugen. Die Schritte zum Durchführen einer Skalierung sind so einfach wie unten aufgeführt:

1. Laden Sie ein Bild mit der von der Image-Klasse freigelegten Load-Fabrikmethode.
1. Konvertieren Sie das Bild in ein [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Erstellen Sie eine Instanz der [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions)-Klasse mit dem Standardkonstruktor oder geben Sie Radius- und Sigma-Werte im Konstruktor an.
1. Rufen Sie die Methode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter auf und geben Sie das Rechteck als Bildgrenzen und die Instanz der [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions)-Klasse an.
1. Speichern Sie die Ergebnisse.

Das folgende Codebeispiel zeigt, wie ein Weichzeichnungseffekt auf einem Bild erzeugt wird.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}
## **Transparenz eines Bildes überprüfen**
Dieser Artikel zeigt die Verwendung von Aspose.PSD für .NET, um die Transparenz eines Bildes zu überprüfen. Die Schritte zur Überprüfung der Bildtransparenz sind so einfach wie unten aufgeführt:

1. Laden Sie ein Bild mit der von der [Image](https://reference.aspose.com/psd/net/aspose.psd/image)-Klasse freigelegten Fabrikmethode [Load](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2).
1. Überprüfen Sie die Bilddeckkraft. Wenn die Deckkraft null ist, ist das Bild transparent.
1. Das folgende Codebeispiel zeigt, wie überprüft wird, ob das Bild transparent ist oder nicht.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}
## **Implementieren eines verlustbehafteten GIF-Komprimierers**
Mit Aspose.PSD für .NET können Entwickler einen Pixelunterschied festlegen. Die Kompression von GIF basiert auf einem "Wörterbuch" von Zeichenfolgen von gesehenen Pixeln. Der normale Encoder sucht im Wörterbuch nach der längsten Zeichenfolge von Pixeln, die genau den Pixeln im Bild entsprechen. Der verlustbehaftete Encoder wählt die längste Zeichenfolge von Pixeln aus, die "ähnlich genug" zu Pixeln im Bild sind. Unten finden Sie die Code-Demonstration dieser Funktionalität.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}
## **Implementieren der Bicubic-Neubemusterung**
Neubemusterung bedeutet, dass Sie die Pixelabmessungen eines Bildes ändern. Beim Herunterskalieren werden Pixel eliminiert und somit Informationen und Details aus Ihrem Bild gelöscht. Beim Hochskalieren werden Pixel hinzugefügt. Photoshop fügt diese Pixel durch Interpolation hinzu. Dieser Artikel zeigt, wie Sie die Bicubic-Neubemusterung mithilfe von Aspose.PSD für .NET durchführen können.

Unten finden Sie die Code-Demonstration dieser Funktionalität.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}
## **Farbbalance-Anpassungsebene**
Dieser Artikel zeigt die Verwendung von Aspose.PSD für .NET, um die **Farbbalance-Anpassungsebene** auf einem Bild durchzuführen. Die Farbbalance-Anpassungsebene ermöglicht es Ihnen, Anpassungen an der Farbgebung ihrer Bilder vorzunehmen. Sie präsentiert die drei Farbkanäle und ihre Komplementärfarben, und Sie können das Gleichgewicht dieser Paare anpassen, um das Erscheinungsbild eines Fotos zu ändern.

Unten finden Sie die Code-Demonstration dieser Funktionalität.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}
## **Invertieren der Anpassungsebene**
Dieser Artikel zeigt, wie Sie die **Invertieren-Anpassungsebene** mithilfe von Aspose.PSD für .NET durchführen können. Eine Anpassungsebene ist eine spezielle Art von Ebene, die hauptsächlich zur Farbkorrektur verwendet wird. Anstatt einen eigenen Inhalt zu haben, passt sie die Informationen auf den darunter liegenden Ebenen an. Die Invertieren-Anpassungsebene erzeugt einen Negativ-Effekt, indem sie die Farben eines Bildes umkehrt.

Unten finden Sie die Code-Demonstration dieser Funktionalität.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}

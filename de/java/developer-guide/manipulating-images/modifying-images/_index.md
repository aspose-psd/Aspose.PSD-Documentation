---
title: Bilder bearbeiten
type: docs
weight: 50
url: /de/java/bilder-bearbeiten/
---

## **Dithering für Rasterbilder**
Dithering ist eine Technik, die die Illusion neuer Farben und Schattierungen erzeugt, indem das Muster von Punkten variiert wird, die tatsächlich ein Bild erstellen. Es ist das häufigste Mittel, um den Farbumfang von Bildern auf 256 (oder weniger) Farben zu reduzieren. Aspose.PSD bietet die Dithering-Unterstützung für die RasterImage-Klasse, indem die Dither-Methode eingeführt wird, die zwei Parameter akzeptiert. Der erste ist vom Typ DitheringMethod, der mit zwei möglichen Optionen FloydSteinbergDithering und ThresholdDithering angewendet werden kann. Der zweite Parameter der Dither-Methode ist der BitCount in Ganzzahl. BitCount definiert die Probenahmegröße für das Dithering-Ergebnis. Der Standardwert ist 1, der Schwarz und Weiß repräsentiert, während zulässige Werte 1, 4, 8 sind, die Paletten mit jeweils 2, 4 und 256 Farben generieren.

## **Helligkeit, Kontrast und Gamma anpassen**

Farbanpassungen in digitalen Bildern sind eine der Hauptfunktionen, die die meisten Bildverarbeitungsbibliotheken bieten. Farbanpassungen können wie folgt kategorisiert werden.

1. Helligkeit bezieht sich auf die Helligkeit oder Dunkelheit der Farbe. Durch Erhöhen der Helligkeit eines Bildes werden alle Farben aufgehellt, während durch Verringern der Helligkeit alle Farben verdunkelt werden.
1. Kontrast bezieht sich darauf, Objekte oder Details innerhalb eines Bildes deutlicher zu machen. Durch Erhöhen des Kontrasts eines Bildes wird der Unterschied zwischen hellen und dunklen Bereichen erhöht, sodass die hellen Bereiche heller und die dunklen Bereiche dunkler werden. Durch Verringern des Kontrasts bleiben hellere und dunklere Bereiche ungefähr gleich, aber das Gesamtbild wird homogener.
1. Gamma optimiert den Kontrast und die Helligkeit des indirekten Lichts, das ein Objekt im Bild beleuchtet.

### **Helligkeit anpassen**
Aspose.PSD für Java API bietet die AdjustBrightness-Methode für die RasterImage-Klasse, die verwendet werden kann, um die Bildhelligkeit durch Übergabe eines Ganzzahlwerts als Parameter anzupassen. Der höchste Parameterwert steht für ein helleres Bild. Hier ist das Originalbild und das resultierende Bild zum Vergleich.

### **Kontrast anpassen**
Die von der RasterImage-Klasse freigegebene AdjustContrast-Methode kann verwendet werden, um den Kontrast eines Bildes durch Übergeben eines Float-Werts als Parameter anzupassen.

Der höchste Parameterwert steht für einen höheren Kontrast im gegebenen Bild. Hier ist das Originalbild und das resultierende Bild zum Vergleich.

### **Gamma anpassen**
Die von der RasterImage-Klasse freigegebene AdjustGamma-Methode hat zwei Versionen. Eine der Überlastungen akzeptiert einen Float-Wert und führt die Gammakorrektur für die Rot-, Blau- und Grünkanal-Koeffizienten durch. Während die andere Überlastung drei Float-Parameter akzeptiert, die jeden Farbkoeffizienten separat darstellen. Das folgende Codebeispiel zeigt, wie die Gamma-Anpassung auf einem Bild durchgeführt wird.

## **Ein Bild verwischen**
In diesem Artikel wird die Verwendung von Aspose.PSD für Java demonstriert, um einen Weichzeichnungseffekt auf einem Bild zu erzeugen. Aspose.PSD APIs haben effiziente und benutzerfreundliche Methoden zur Erzielung dieses Ziels freigelegt. Aspose.PSD für Java hat die Klasse GaussianBlurFilterOptions freigegeben, um einen Weichzeichnungseffekt zu erzeugen. Die Klasse GaussianBlurFilterOptions benötigt Radius- und Sigma-Werte, um einen Weichzeichnungseffekt auf einem Bild zu erzeugen. Die Schritte zum Ausführen der Größenänderung sind so einfach wie unten aufgeführt:

1. Laden Sie ein Bild mithilfe der von der Image-Klasse freigegebenen Load-Factory-Methode.
1. Konvertieren Sie das Bild in ein RasterImage.
1. Erstellen Sie eine Instanz der Klasse GaussianBlurFilterOptions mit dem Standardkonstruktor oder geben Sie Radius- und Sigma-Werte im Konstruktor an.
1. Rufen Sie die RasterImage.Filter-Methode auf, während Sie das Rechteck als Bildgrenzen und die Instanz der Klasse GaussianBlurFilterOptions angeben.
1. Speichern Sie die Ergebnisse.

Das folgende Codebeispiel zeigt, wie man einen Weichzeichnungseffekt auf einem Bild erzeugt.

## **Bildtransparenz überprüfen**
In diesem Artikel wird die Verwendung von Aspose.PSD für Java zur Überprüfung der Bildtransparenz demonstriert. Die Schritte zum Überprüfen der Bildtransparenz sind so einfach wie unten aufgeführt:

1. Laden Sie ein Bild mithilfe der von der Image-Klasse freigegebenen Load-Factory-Methode.
1. Überprüfen Sie die Bilddeckkraft, wenn die Deckkraft null ist, ist das Bild transparent.
1. Das folgende Codebeispiel zeigt, wie überprüft wird, ob das Bild transparent ist oder nicht.

## **Implementierung eines verlustbehafteten GIF-Komprimierungsverfahrens**
Mit Aspose.PSD für Java können Entwickler den Pixelunterschied einstellen. Die Kompression von GIF basiert auf einem "Wörterbuch" von Zeichenfolgen von Pixeln, die gesehen wurden. Der normale Encoder durchsucht das Wörterbuch nach der längsten Zeichenfolge von Pixeln, die genau den Pixeln im Bild entsprechen. Der verlustbehaftete Encoder wählt die längste Zeichenfolge von Pixeln aus, die "hinreichend ähnlich" zu den Pixeln im Bild sind. Unten finden Sie die Code-Demonstration dieser Funktionalität.

## **Implementieren von Bicubic Resampling**
Resampling bedeutet, dass Sie die Pixelmaße eines Bildes ändern. Beim Downsampling werden Pixel eliminiert und somit Informationen und Details aus Ihrem Bild gelöscht. Beim Upsampling werden Pixel hinzugefügt. Photoshop fügt diese Pixel durch Interpolation hinzu. Dieser Artikel zeigt, wie Sie das Bicubic-Resampling mit Aspose.PSD für Java durchführen können.

Unten finden Sie die Code-Demonstration dieser Funktionalität.

## **Ebenenanpassung umkehren**
In diesem Artikel wird gezeigt, wie Sie die **Invert-Anpassungsebene** mithilfe von Aspose.PSD für Java durchführen können. Eine Anpassungsebene ist eine spezielle Art von Ebene, die hauptsächlich zur Farbkorrektur verwendet wird. Anstatt einen eigenen Inhalt zu haben, passen sie die Informationen auf den darunter liegenden Ebenen an. Die Umkehrung der Anpassungsebene erzeugt einen negativen Effekt auf ein Bild, indem die Farben eines Bildes invertiert werden.

Unten finden Sie die Code-Demonstration dieser Funktionalität.


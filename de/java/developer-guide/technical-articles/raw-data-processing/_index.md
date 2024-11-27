---
title: Rohdatenverarbeitung
type: docs
weight: 70
url: /de/java/rohdatenverarbeitung/
---

## **Rohdatenverarbeitung**
Um die Leistung der Aspose.PSD-API zu verbessern, haben wir mit der Version 2.4.0 eine Methode zur Rohdatenverarbeitung eingeführt. Die Rohdatenverarbeitung wird jetzt intern verwendet und verfügt über eine externe API, damit sie von außerhalb der Bibliothek genutzt werden kann, um die Gesamtleistung zu verbessern. Manchmal gestaltet sich die Verarbeitung etwas kompliziert und erfordert eine Erklärung. Die Rohdatenverarbeitung ist derzeit nur für das BMP-Format verfügbar.

Um Entwicklern zu helfen, die beste Leistung zu erzielen, bietet die Aspose.PSD-API ein System zur Rohdatenverarbeitung, das eine externe API für die Anpassung bereitstellt. Entwickler rufen die Methoden LoadRawData und SaveRawData auf, um die Rohdatenverarbeitung zu nutzen. Diese Methoden erfordern auch die Festlegung des gewünschten Rohdatenformats unter Verwendung der Klasse RawDataSettings. Die Klasse RawDataSettings ermöglicht es Entwicklern, jedes Rohdatenformat anzugeben. Um jedoch die beste Leistung zu erzielen, muss das Rohdatenformat verwendet werden, in dem die Daten gespeichert sind. Die in der Klasse RasterImage definierten RawDataSettings helfen dabei, das Rohdatenformat des Bildes zu bestimmen. Wenn Sie die Instanz von RawDataSettings an die LoadRawData-Methode übergeben, werden die Daten so zurückgegeben, wie sie sind, ohne dass eine Konvertierung erfolgt, was die Leistung verbessern kann. Andererseits müssen Sie sich um alle möglichen Rohdatenformatslayouts kümmern, was manchmal etwas kompliziert sein kann.

Um den Bearbeitungsprozess zu vereinfachen, können Sie auf Kosten einiger Leistungseinbußen die gewünschten RawDataSettings angeben, indem Sie die Klasse mit den gewünschten Rohdateneinstellungen instanziieren und initialisieren. In einigen Fällen kann es nicht möglich sein, die Rohdaten im angegebenen Format zurückzugeben (zum Beispiel ist die Konvertierung von CMYK-Farbräumen in RGB in der Version 2.4.0 nicht verfügbar). Darüber hinaus kann es Szenarien geben, in denen die Rohdatenverarbeitung für ein Bildformat überhaupt nicht verfügbar ist. Um festzustellen, ob Sie die Methoden LoadRawData und SaveRawData verwenden können, müssen Sie die Eigenschaft IsRawDataAvailable abfragen.

### **Einblick**
Für das RGB-Pixeldatenformat sind indizierte (palettenbasierte) und RGB-basierte Rohdatenformate verfügbar. Indizierte Rohdatenformate enthalten Paletten-Eintragsindizes im Bereich von 0 bis (2^bis Anzahl - 1). Die indizierten Rohdatenformate sind 1, 2, 4 und 8 Bits pro Pixel. Der Rest sind RGB-basierte Rohdatenformate. Beim Laden von Rohdaten sollten Sie darauf achten, dass genügend Bytes verfügbar sind, um die Daten zu laden, da andernfalls eine entsprechende Ausnahme ausgelöst wird. Sie können die Größe des Byte-Arrays einfach schätzen, indem Sie die Zeilengröße mit den erforderlichen Zeilen multiplizieren. Die Zeilengröße kann variieren und hängt vom Speicherformat der Rohdaten ab.

Um die beste Leistung zu erzielen, verwenden Sie immer eine Rohdaten-Zeilenlänge, die dem Wert der RasterImage.RawLineSize-Eigenschaft entspricht. Manchmal müssen Sie jedoch zusätzliche Polsterung zu den Rohdatenzeilen hinzufügen oder reduzieren, und in diesem Fall kann eine andere Zeilenlänge verwendet werden. Wenn ein Ausschnitt eines Bildbegrenzungsrechtecks erforderlich ist, sollten Sie auch die Bitverschiebungen berücksichtigen, die für indizierte RGB-Pixelformate auftreten können. Wenn beispielsweise ein Bild mit den Abmessungen 100x100 Pixel und einem Rohdatenformat von 1 Bit pro Pixel vorliegt und Sie ein Rechteck mit den Abmessungen (7,0) und (2,1) laden möchten, benötigen Sie 2 Pixel ab x=7 und y=0. In diesem Fall erhalten Sie folgendes Datenlayout:







![todo:image_alt_text](raw-data-processing_1.png)

Das bedeutet, dass Sie 2 Bytes erhalten, wobei das erste Byte 7 unerwünschte Pixel und 1 gewünschtes Pixel enthält, und das zweite Byte 1 gewünschtes Pixel und dann 7 unerwünschte enthält. Sie könnten sich fragen, warum wir keine Datenverschiebung durchgeführt haben und diese 2 Pixel in ein einzelnes Byte gesteckt haben. Die Antwort ist einfach: um die Leistung hoch zu halten. Die gesamte interne Verarbeitung erfolgt typischerweise mit allen Daten, beginnend beim ersten Pixel und endend mit dem letzten verfügbaren Pixel. Es gibt seltene Situationen, in denen ein Pixelsubset erforderlich ist. Darüber hinaus wissen wir nicht, wie diese Pixel anschließend verarbeitet werden sollen, daher würde eine Verschiebung die Leistung beeinträchtigen und den Code unnötig komplex machen. Schätzen Sie immer das richtige Bit (es ist nicht erforderlich, das richtige Byte zu bestimmen, da die Daten immer mit dem ersten gefüllten Byte kommen), an dem die geforderten Pixel beginnen. Zur Berechnung des richtigen Bits kann eine einfache Formel verwendet werden: (rect.Left * bitsCount) % 8.

### **Konvertierung von indizierten RGB-Farben**
Um die bestmögliche Leistung zu erzielen, verwenden Sie immer die gleichen Quell- und Ziel-Rohdateneinstellungen, Pixelformate und Zeilengrößen. Manchmal müssen Sie jedoch eine Datenkonvertierung durchführen. Zum Beispiel können Sie ein 1-Bit-pro-Pixel-RGB-Bild laden und mit 2 Bits pro Pixel speichern oder ein 4-Bit-RGB-Bild laden und seinen Farbbereich auf 2 Bits pro Pixel reduzieren. In jedem Fall sollte eine Farbkonvertierung angewendet werden. Die Konvertierung von indizierten RGB-Bildern kann manchmal knifflig sein und kann nicht ohne einige Einstellungen erfolgen. Wir müssen feststellen, wie der Quellfarbbereich auf den Ziel-Farbraum abgebildet wird. Um diese Aufgabe zu erfüllen, haben wir verschiedene Modi:

- Palettenzuordnung (DitheringMethods.PaletteConversion)
- Rohdatenzuordnung (DitheringMethods.PaletteIgnore)
- Benutzerdefinierte Konvertierung (DitheringMethods.CustomConverter)

Wenn die Palettenkonvertierung verwendet wird, versucht der Quellfarbraum, dem Ziel-Farbraum so nahe wie möglich zu kommen. Angenommen, wir haben ein 4-Bit-Bild mit den folgenden Farben:
[0] RGB = 0, 0, 0
[1] RGB = 17, 17, 17
[2] RGB = 34, 34, 34
[3] RGB = 51, 51, 51
[4] RGB = 68, 68, 68
[5] RGB = 85, 85, 85
[6] RGB = 102, 102, 102
[7] RGB = 119, 119, 119
[8] RGB = 136, 136, 136
[9] RGB = 153, 153, 153
[10] RGB = 170, 170, 170
[11] RGB = 187, 187, 187
[12] RGB = 204, 204, 204
[13] RGB = 221, 221, 221
[14] RGB = 238, 238, 238
[15] RGB = 255, 255, 255

Das Quellbild sieht wie folgt aus:




![todo:image_alt_text](raw-data-processing_2.png)

Und wir konvertieren das 4-Bit-Bild in ein 1-Bit-Bild mit den folgenden definierten Palettenfarben:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Im Palettenkonvertierungsmodus liest der Konverter die Quellfarbe und bestimmt den Zielindex unter Verwendung der Methode GetNearestColorIndex der Ziel-Palette. Der Wert der RasterImage.RawFallbackIndex-Eigenschaft wird verwendet, falls die Methode GetNearestColorIndex der Palette einen Index außerhalb des Bereichs ergibt. Dies konvertiert die Quellfarben in die dem Zielbild am nächsten liegenden Farben in Bezug auf Intensitätswerte. Das Zielbild entspricht dem Quellbild so nahe wie möglich. Sie können das folgende Ergebnis sehen:




![todo:image_alt_text](raw-data-processing_3.png)

Im Rohdatenzuordnungsmodus wird ein anderes Szenario verwendet. Die Quell- und Ziel-Farbpakete werden einfach ignoriert und die Quellindizes werden auf Zielindizes abgebildet. Wenn ein Wert gefunden wird, der nicht in den Zielbereich abgebildet werden kann (beim Verringern der Bitanzahl), wird der Wert der RasterImage.RawFallbackIndex-Eigenschaft verwendet. Der Wert ist standardmäßig 0 und wird in die erste Farbe der Ziel-Palette abgebildet. Wenn der Wert dieser Eigenschaft außerhalb des Zielbereichs liegt, wird eine entsprechende Ausnahme ausgelöst. Dies führt zu weniger vorhersehbaren Ergebnissen, die auf dem folgenden Bild gezeigt werden können:




![todo:image_alt_text](raw-data-processing_4.png)

Der Palettenkonvertierungsmodus ist eine genauere Lösung für das Farbzuordnungsproblem, benötigt jedoch etwas mehr Zeit zur Fertigstellung, da Berechnungen durchgeführt werden müssen, um die korrekten Paletteneinstellungen zu schätzen. (Typischerweise gibt es nur einen sehr geringen Leistungsunterschied zwischen den beiden Methoden.) Andererseits führt der Rohzuordnungsmodus etwas schneller aus und kann für eine grobe Farbkonvertierung verwendet werden, wenn die genaue Farbzuordnung nicht so wichtig ist. Es gibt beispielsweise Fälle, in denen die Quellfarbpalette abgeschnitten werden kann und sicher auf eine geringere Bitanzahl konvertiert werden kann, da die zusätzlichen Bits sowieso nicht verwendet wurden.

Um eine dieser Herangehensweisen zu verwenden, verwenden Sie die RasterImage-Klasse RawDitheringMethod-Eigenschaft. Standardmäßig ist sie auf die Palettenkonvertierungsmethode eingestellt, um die bestmöglichen Ergebnisse zu erzielen. Sie können diese Eigenschaft ändern, bevor eine Konvertierung stattfindet (beispielsweise beim Speichern eines Bildes in einen Stream). Bitte beachten Sie, dass die Palettenignorieren- und Palettenkonvertierungs-Dithering-Methoden nicht durchgeführt werden, wenn ein Bild geladen und einige der ursprünglichen Pixeldaten überschrieben wurden, da die neuen Daten in den Cache gelangen und der Cache die Daten im maximal verfügbaren Format 32ARGB speichert (ab Version 2.4.0, Änderungen vorbehalten). Dieses Format wird verwendet, um Probleme mit möglicherweise unterschiedlichen Farbbereichen für geladene und gespeicherte Bilder zu überwinden. Darüber hinaus werden die Methoden der Palettenignorierung und der Palettenkonvertierung nicht durchgeführt, wenn ein Bild im RGB-Modus geladen und in den indizierten Modus oder umgekehrt konvertiert wird.

### **Benutzerdefinierte Farbkonverter**
Manchmal genügt es nicht, den Standardansatz für die Farbkonvertierung zu verwenden. Möglicherweise möchten Sie einen benutzerdefinierten Algorithmus verwenden, um vollständige Freiheit bei der Verwendung von Farbkonvertierungsroutinen zu haben. Wenn die Pixelformate der Quell- und Zielbilder beide indizierte RGB-Formate sind, kann eine einfachere Schnittstelle, IIndexedColorConverter, verwendet werden. Sie müssen die RasterImage.RawIndexedColorConverter-Eigenschaft auf eine Instanz des IIndexedColorConverter-Interfaces setzen und den Wert DitheringMethods.CustomConverter für die RawDitheringMethod-Eigenschaft festlegen. Wenn diese Kombination verwendet wird, wird jede indizierte Farbkonvertierung über die spezifizierte IIndexedColorConverter-Instanz ausgeführt. Der benutzerdefinierte indizierte Farbkonverter hat die folgende Methode definiert:
 
{{< highlight java >}}
 
 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);
 
{{< /highlight >}}
 
Die FillIndexedtoIndexedMap-Methode wird aufgerufen, wenn eine Konvertierung von einem indizierten RGB-Bild in ein anderes indiziertes RGB-Bildformat erforderlich ist (wenn eine der 1,2,4 oder 8 Bitanzahlen ineinander umgewandelt wird). Das Karten-Array hat die Länge aller möglichen Quellformat-Einträge. Sie müssen dieses Array füllen, um die Zuordnung vom Quellfarbpalette-Eintrag zum Ziel-Farbpalette-Eintrag vorzunehmen. Achten Sie darauf, dass der Wert des Zielindex im Bereich von 0 bis (Bitanzahl - 1) liegt, ansonsten wird eine entsprechende Ausnahme ausgelöst.
 
Wenn die Anforderung besteht, ein anspruchsvolleres Farbkonversionsszenario durchzuführen, sollte die RasterImage.RawCustomColorConverter-Eigenschaft auf eine Instanz des IColorConverter-Interfaces gesetzt werden. Die RawCustomColorConverter-Eigenschaft überschreibt immer die RawIndexedColorConverter-Eigenschaft, wenn beide festgelegt sind, und in einem solchen Fall wird kein indizierter Farbkonverter verwendet. Das IColorConverter hat eine einzige Methode definiert:
 
{{< highlight java >}}
 
 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}
 
Die Convert-Methode wird jedes Mal aufgerufen, wenn eine Farbkonvertierung erforderlich ist. Die Methode empfängt die Quellrohdaten im Quellformat und verwendet einen Ausgabe-Puffer zur Aufnahme des in das Zielformat konvertierten Farbformats. Der Zielpuffer sollte ausreichend sein, um die konvertierten Daten zu empfangen (wenn der Schnittstellenaufruf intern von der Aspose.PSD-Bibliothek erfolgt) und sollte die konvertierten Rohdaten beim Rückgabewert der Methode enthalten. Die Convert-Methode kann mehrmals aufgerufen werden, bis alle Quelldaten abgedeckt sind.
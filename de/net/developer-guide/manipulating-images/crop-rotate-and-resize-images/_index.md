---
title: Bilder zuschneiden, drehen und skalieren
type: docs
weight: 40
url: /de/net/bilder-zuschneiden-drehen-und-skalieren/
---

## **Bilder zuschneiden**
Das Zuschneiden von Bildern bezieht sich normalerweise auf das Entfernen der äußeren Teile eines Bildes, um die Rahmung zu verbessern. Das Zuschneiden kann auch verwendet werden, um einen bestimmten Bereich eines Bildes auszuschneiden, um den Fokus auf einen bestimmten Bereich zu erhöhen. Die Aspose.PSD-API unterstützt zwei verschiedene Ansätze zum zuschneiden von Bildern: durch Verschiebungen und Rechteck.
### **Zuschneiden durch Verschiebungen**
Die Klasse [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) bietet eine überladene Version der Crop-Methode, die 4 Ganzzahlwerte akzeptiert, die links, rechts, oben und unten bezeichnen. Basierend auf diesen vier Werten verschiebt die Crop-Methode die Bildgrenzen in Richtung der Bildmitte, während der äußere Teil verworfen wird. Der folgende Codeausschnitt zeigt, wie ein Bild durch Verschiebungen zugeschnitten wird.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-DrawingAndFormattingImages-ZuschneidenMitVerschiebungen-ZuschneidenMitVerschiebungen.cs" >}}
### **Zuschneiden durch Rechteck**
Die Klasse [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) bietet eine weitere überladene Version der Crop-Methode, die eine Instanz der Rectangle-Klasse akzeptiert. Sie können jeden beliebigen Ausschnitt eines Bildes ausschneiden, indem Sie die gewünschten Begrenzungen dem Rectangle-Objekt übergeben. Der folgende Codeausschnitt zeigt, wie ein beliebiges Bild durch ein Rechteck zugeschnitten wird.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-DrawingAndFormattingImages-ZuschneidenDurchRechteck-ZuschneidenDurchRechteck.cs" >}}
## **Bild drehen und spiegeln**
Aspose.PSD für .NET ist eine benutzerfreundliche Bibliothek, da sie einfache Methoden bietet, um komplexe Operationen durchzuführen. Zum Beispiel hat Aspose.PSD für .NET die Methode RotateFlip für die Basisklasse Image bereitgestellt, wenn eine Anwendung das Drehen eines Bildes erfordert. Unabhängig vom Bildformat kann die Bibliothek spezifische Dreh- und Spiegelverfahren anwenden.
### **Ein Bild drehen**
Die Methode Image.RotateFlip kann verwendet werden, um das Bild um 90/180/270 Grad zu drehen und das Bild horizontal oder vertikal zu spiegeln. Die Methode Image.RotateFlip akzeptiert einen Parameter vom Typ RotateFlipType, der den zu verwendenden Rotations- und Spiegeltyp für das Bild angibt. Die Schritte zum Durchführen der Drehung und des Spiegelns sind wie folgt,

1. Laden Sie das Bild mit der von der Image-Klasse bereitgestellten Factory-Methode Load.
1. Rufen Sie die Methode Image.RotateFlip auf und geben Sie den entsprechenden RotateFlipType an.
1. Speichern Sie die Ergebnisse.

Das folgende Codebeispiel zeigt, wie man die RotateFlip-Eigenschaft eines Bildes und die Aufzählung RotateFlipType setzt.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-DrawingAndFormattingImages-BildDrehen-BildDrehen.cs" >}}
## **Ein Bild in einem bestimmten Winkel drehen**
Aspose.PSD für .NET API bietet die [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate-Methode, um Benutzern, die ein Bild um einen bestimmten Winkel drehen möchten, zu unterstützen. Im Gegensatz zur [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip-Methode akzeptiert die [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate-Methode drei Parameter:

1. Rotationswinkel: Ein Parameter vom Typ Float, der den Rotationswinkel angibt, um den das Bild gedreht werden soll. Ein positiver Wert dreht das Bild im Uhrzeigersinn; ein negativer Wert führt eine gegen den Uhrzeigersinn gerichtete Drehung durch.
1. Proportional skalieren: Ein Parameter vom Typ Boolean, der angibt, ob die Bildgröße gemäß den Projektionen des rotierten Rechtecks (Eckpunkte) geändert werden muss. Wenn es auf false gesetzt ist, bleiben die Bildabmessungen unverändert und nur der interne Bildinhalt wird gedreht.
1. Hintergrundfarbe: Ein Parameter vom Typ Color, der die Farbe angibt, die im Hintergrund des gedrehten Bildes gefüllt werden soll.

Der folgende Codeausschnitt zeigt die Verwendung der [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate-Methode.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-DrawingAndFormattingImages-BildDrehenUnterEinemBestimmtenWinkel-BildDrehenUnterEinemBestimmtenWinkel.cs" >}}
## **Bilder skalieren**
Dieser Artikel zeigt die Verwendung von Aspose.PSD für .NET zur Durchführung einer Skalierungsoperation an einem Bild. Aspose.PSD-APIs haben effiziente und benutzerfreundliche Methoden zur Erreichung dieses Ziels bereitgestellt. Aspose.PSD für .NET hat die Resize-Methode für die Image-Klasse freigelegt, die dazu verwendet werden kann, vorhandene Bilder on-the-fly zu skalieren. Es gibt zwei Überladungen der Resize-Methode, um den Anforderungen der Anwendung gerecht zu werden.
### **Einfache Skalierung**
Die Schritte zur Durchführung der Skalierung sind wie folgt:

1. Laden Sie das Bild mit der von der Image-Klasse bereitgestellten Factory-Methode Load.
1. Rufen Sie die Methode Image.Resize auf und geben Sie neue Höhe & Breite an.
1. Speichern Sie die Ergebnisse.

Das folgende Codebeispiel zeigt, wie man ein Bild skalieren kann.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-DrawingAndFormattingImages-EinfacheSkalierung-EinfacheSkalierung.cs" >}}
### **Skalierung mit ResizeType-Aufzählung**
Die Aspose.PSD-API hat die ResizeType-Aufzählung freigelegt, die mit Image.Resize verwendet werden kann, um die gewünschten Ergebnisse zu erzielen. Der unten bereitgestellte Codeausschnitt zeigt die Verwendung der ResizeType-Aufzählung, während die Details der Mitglieder der ResizeType-Aufzählung am Ende dieser Seite gefunden werden können.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-DrawingAndFormattingImages-SkalierungMitResizeTypeAufzählung-SkalierungMitResizeTypeAufzählung.cs" >}}



Wenn Sie ein qualitativ hochwertiges Ergebnis nach der Anwendung der Skalierung erhalten möchten, wird empfohlen, dass Sie immer ResizeType.LanczosResample verwenden, da dies hochwertige Ergebnisse liefert, aber langsamer arbeiten kann als ResizeType.NearestNeighbourResample. Andererseits wird der Algorithmus ResizeType.NearestNeighbourResample speziell für schnelle Skalierung verwendet, wobei die Bildqualität beeinträchtigt wird. Diese Methode kann nützlich sein für die Erstellung von Miniaturbildern in Echtzeit oder ähnlichen Prozessen, bei denen die Leistung erforderlich ist.
## **Bild proportional skalieren**
Sie können Bilder skalieren, indem Sie neue Höhen- & Breitenwerte als Parameter an die Image.Resize-Methode übergeben, aber in diesem Fall müssen Sie das Seitenverhältnis selbst berechnen. Dies liegt daran, dass, wenn die Breite oder Höhe eines Bildes verändert wird, das Bild entweder skaliert oder verkleinert wird, um die neue Größe zu füllen. Wenn die Änderungen an der Breite und Höhe eines Bildes nicht im Verhältnis stehen, kann dies zu gestreckten und verzerrten Ergebnissen führen. Dieser Artikel zeigt die Verwendung der Aspose.PSD für .NET-API zum Skalieren von Bildern, indem entweder neue Höhe oder Breite übergeben wird, wobei die API automatisch den anderen proportionalen Wert berechnen darf.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Beispiele-CSharp-Aspose-DrawingAndFormattingImages-BildProportionalSkalieren-BildProportionalSkalieren.cs" >}}
### **Aufzählung ResizeType**
ResizeType bestimmt den Typ der Umwandlung, die auf dem Bild basierend auf dem ausgewählten Filter durchgeführt werden soll.

Mitglieder der [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype) Aufzählung

|**Mitgliedsname**|**Wert**|**Beschreibung**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Der linke obere Punkt des neuen Bildes wird mit dem linken oberen Punkt des Originalbildes zusammenfallen. Ein Beschnitt erfolgt bei Bedarf.|
|RightTopToRightTop|1|Der rechte obere Punkt des neuen Bildes wird mit dem rechten oberen Punkt des Originalbildes zusammenfallen. Ein Beschnitt erfolgt bei Bedarf.|
|RightBottomToRightBottom|2|Der rechte untere Punkt des neuen Bildes wird mit dem rechten unteren Punkt des Originalbildes zusammenfallen. Ein Beschnitt erfolgt bei Bedarf.|
|LeftBottomToLeftBottom|3|Der linke untere Punkt des neuen Bildes wird mit dem linken unteren Punkt des Originalbildes zusammenfallen. Ein Beschnitt erfolgt bei Bedarf.|
|CenterToCenter|4|Das Zentrum des neuen Bildes wird mit dem Zentrum des Originalbildes zusammenfallen. Ein Beschnitt erfolgt bei Bedarf.|
|LanczosResample|5|Neuabtastung mit Lanczos-Algorithmus unter Verwendung einer Maske von 7x7.|
|NearestNeighbourResample|6|Neuabtastung unter Verwendung des Nachbarn-Algorithmus.|

---
title: Bilder zuschneiden, drehen und skalieren
type: docs
weight: 40
url: /de/java/bilder-zuschneiden-drehen-und-skalieren/
---

## **Bilder zuschneiden**
Das Zuschneiden von Bildern bezieht sich in der Regel auf das Entfernen der äußeren Teile eines Bildes, um die Rahmung zu verbessern. Das Zuschneiden kann auch verwendet werden, um einen bestimmten Bereich eines Bildes auszuschneiden und den Fokus auf diesen Bereich zu erhöhen. Die Aspose.PSD-API unterstützt zwei verschiedene Ansätze zum Zuschneiden von Bildern: durch Verschiebungen und Rechteck.
### **Zuschneiden durch Verschiebungen**
Die Klasse RasterImage bietet eine überladene Version der Crop-Methode, die 4 Ganzzahlwerte akzeptiert, die links, rechts, oben & unten bedeuten. Basierend auf diesen vier Werten verschiebt die Crop-Methode die Bildgrenzen in Richtung Mitte des Bildes, wobei der äußere Teil verworfen wird. Der folgende Codeausschnitt zeigt, wie man ein Bild durch Verschiebungen zuschneidet.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Zuschneiden durch Rechteck**
Die Klasse RasterImage bietet eine weitere überladene Version der Crop-Methode, die eine Instanz der Rechteckklasse akzeptiert. Sie können jeden beliebigen Bereich eines Bildes ausschneiden, indem Sie die gewünschten Grenzen dem Rechteckobjekt mitteilen. Der folgende Codeausschnitt zeigt, wie man ein Bild durch ein Rechteck zuschneidet.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Bild drehen und spiegeln**
Aspose.PSD für Java ist eine einfach zu bedienende Bibliothek, da sie einfache Methoden bereitstellt, um komplexe Operationen durchzuführen. Zum Beispiel hat Aspose.PSD für Java für seine Basisklasse Image die RotateFlip-Methode bereitgestellt, wenn eine Anwendung eine Bildrotation benötigt. Unabhängig vom Bildformat kann die Bibliothek eine spezifische Dreh- und Spiegelungsvorgänge ausführen.
### **Bild drehen**
Die Image.RotateFlip-Methode kann verwendet werden, um das Bild um 90/180/270 Grad zu drehen und das Bild horizontal oder vertikal zu spiegeln. Die Image.RotateFlip-Methode akzeptiert einen Parameter von RotateFlipType, der den Typ der durchzuführenden Drehung und Spiegelung angibt. Die Schritte zur Durchführung der Rotation & Spiegelung sind wie folgt einfach:

1. Laden Sie das Bild mit der von der Image-Klasse bereitgestellten Factory-Methode Load ein.
1. Rufen Sie die Image.RotateFlip-Methode auf und geben Sie den entsprechenden RotateFlipType an.
1. Speichern Sie die Ergebnisse.

Das folgende Codebeispiel zeigt, wie man die RotateFlip-Eigenschaft eines Bildes und die RotateFlipType-Aufzählung setzt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Bild in einem bestimmten Winkel drehen**
Aspose.PSD für Java API bietet die Methode RasterImage.Rotate, um Benutzern zu ermöglichen, ein Bild in einem bestimmten Winkel zu drehen. Im Gegensatz zur Methode RasterImage.RotateFlip akzeptiert die Methode RasterImage.Rotate drei Parameter:

1. Drehwinkel: Ein Parameter vom Typ Float, der den Drehwinkel angibt, um den das Bild gedreht werden soll. Ein positiver Wert dreht das Bild im Uhrzeigersinn; ein negativer Wert führt eine gegen den Uhrzeigersinn Drehung durch.
1. Proportional ändern: Ein Boolean-Parameter gibt an, ob die Bildgröße entsprechend den Projektionen des gedrehten Rechtecks (Eckpunkte) geändert werden muss. Wenn auf false gesetzt, bleiben die Bildabmessungen unverändert und nur der interne Bildinhalt wird gedreht.
1. Hintergrundfarbe: Ein Color-Parameter gibt die Farbe an, die im Hintergrund des gedrehten Bildes gefüllt werden soll.

Der folgende Codeausschnitt zeigt die Verwendung der RasterImage.Rotate-Methode.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Bilder skalieren**
Dieser Artikel zeigt die Verwendung von Aspose.PSD für Java, um eine Skalierungsoperation auf einem Bild durchzuführen. Die Aspose.PSD-APIs haben effiziente und einfach zu bedienende Methoden bereitgestellt, um dieses Ziel zu erreichen. Aspose.PSD für Java hat die Resize-Methode für die Image-Klasse bereitgestellt, die verwendet werden kann, um vorhandene Bilder dynamisch umzuskalieren. Es gibt zwei Überlastungen der Resize-Methode, um den Anwendungsbedarf zu erfüllen.
### **Einfache Skalierung**
Die Schritte zur Durchführung einer Skalierung sind wie folgt einfach:

1. Laden Sie das Bild mit der von der Image-Klasse bereitgestellten Factory-Methode Load ein.
1. Rufen Sie die Image.Resize-Methode auf und geben Sie neue Höhe & Breite an.
1. Speichern Sie die Ergebnisse.

Das folgende Codebeispiel zeigt, wie man ein Bild skalieren kann.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Skalieren mit ResizeType-Aufzählung**
Aspose.PSD-API hat die ResizeType-Aufzählung freigegeben, die zusammen mit Image.Resize verwendet werden kann, um die gewünschten Ergebnisse zu erzielen. Der untenstehende Codeausschnitt zeigt die Verwendung der ResizeType-Aufzählung, wobei die Details der Mitglieder der ResizeType-Aufzählung am unteren Rand dieser Seite zu finden sind.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



Wenn Sie nach dem Anwenden der Skalierung ein qualitativ hochwertiges Ergebnis erhalten möchten, wird empfohlen, immer ResizeType.LanczosResample zu verwenden, da so hochwertige Ergebnisse erzielt werden können, dies jedoch möglicherweise langsamer funktioniert als ResizeType.NearestNeighbourResample. Andererseits wird der Algorithmus ResizeType.NearestNeighbourResample speziell für schnelles Skalieren verwendet, wobei die Bildqualität beeinträchtigt wird. Diese Methode kann für die Echtzeit-Erstellung von Miniaturansichten oder ähnlichen Prozessen verwendet werden, bei denen die Leistung erforderlich ist.
## **Bild proportional skalieren**
Sie können Bilder verkleinern, indem Sie neue Höhe- und Breitenwerte als Parameter an die Image.Resize-Methode übergeben, in diesem Fall müssen Sie jedoch das Seitenverhältnis selbst berechnen. Dies liegt daran, dass, wenn die Breite oder Höhe eines Bildes geändert wird, das Bild entweder skaliert oder verkleinert wird, um die neue Größe zu füllen. Wenn die Änderungen an der Breite und Höhe eines Bildes nicht proportional sind, kann dies zu gestreckten und verzerrten Ergebnissen führen. Dieser Artikel zeigt die Verwendung der Aspose.PSD für Java-API, um Bilder zu verkleinern, indem entweder die neue Höhe oder Breite übergeben wird, wobei der API ermöglicht wird, den anderen proportionalen Wert automatisch zu berechnen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **ResizeType-Aufzählung**
ResizeType bestimmt den Typ des Skalierungsvorgangs, der basierend auf dem ausgewählten Filter auf das Bild angewendet wird.

Mitglieder der ResizeType-Aufzählung

|**Mitgliedsname**|**Wert**|**Beschreibung**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Der linke obere Punkt des neuen Bildes wird mit dem linken oberen Punkt des Originalbildes übereinstimmen. Es erfolgt ein Beschnitt, wenn erforderlich.|
|RightTopToRightTop|1|Der rechte obere Punkt des neuen Bildes wird mit dem rechten oberen Punkt des Originalbildes übereinstimmen. Es erfolgt ein Beschnitt, wenn erforderlich.|
|RightBottomToRightBottom|2|Der rechte untere Punkt des neuen Bildes wird mit dem rechten unteren Punkt des Originalbildes übereinstimmen. Es erfolgt ein Beschnitt, wenn erforderlich.|
|LeftBottomToLeftBottom|3|Der linke untere Punkt des neuen Bildes wird mit dem linken unteren Punkt des Originalbildes übereinstimmen. Es erfolgt ein Beschnitt, wenn erforderlich.|
|CenterToCenter|4|Das Zentrum des neuen Bildes wird mit dem Zentrum des Originalbildes übereinstimmen. Es erfolgt ein Beschnitt, wenn erforderlich.|
|LanczosResample|5|Neubemusterung mit Lanczos-Algorithmus unter Verwendung einer 7x7-Maske.|
|NearestNeighbourResample|6|Neubemusterung mit dem nächsten Nachbaralgorithmus.|



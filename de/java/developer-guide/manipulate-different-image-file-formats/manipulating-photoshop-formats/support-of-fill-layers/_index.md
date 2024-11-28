---
title: Unterstützung von Füllungsebenen
type: docs
weight: 50
url: /de/java/unterstutzung-von-fullungsebenen/
---


## **Unterstützung von Füllungsebenen mit Farbfüllung**
Dieser Artikel zeigt, wie eine PSD-Ebene mit Farbe gefüllt werden kann. Verwenden Sie die Aspose.PSD.FileFormats.Psd.Layers.FillLayer, um Farbe in eine PSD-Ebene hinzuzufügen. Die folgenden Code-Snippets laden eine PSD-Datei, greifen auf die Filllayer-Klasse zu und setzen die Farbe mit der FillLayer.FillSettings-Eigenschaft.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Unterstützung von Füllungsebenen mit Farbverlaufsfüllung**
Dieser Artikel zeigt die Verwendung von Farbverlaufsfüllung zum Füllen einer PSD-Ebene. Aspose.PSD APIs haben effiziente und einfach zu verwendende Methoden bereitgestellt, um dieses Ziel zu erreichen. Aspose.PSD hat die Klassen GradientColorPoint und GradientTransparencyPoint verfügbar gemacht, um einen Verlaufs­effekt in eine Ebene hinzuzufügen.

` `Der Prozess, eine PSD-Ebene mit Farbverlaufsfüllung zu füllen, ist so einfach wie folgt:

- Laden Sie eine PSD-Datei als Bild mithilfe der von der Image-Klasse bereitgestellten Factory-Methode Load.
- Setzen Sie die Einstellungen der Eigenschaften des FillLayer-Objekts.
- Erstellen Sie eine Liste von ColorPoints mit den erforderlichen Farben und Positionen der Farben.
- Erstellen Sie eine Liste von TransparencyPoints mit der erforderlichen Deckkraft und Position des Transparenzpunkts.
- Rufen Sie die FillLayer.Update-Methode auf.
- Speichern Sie die Ergebnisse.



Der folgende Code-Schnipsel zeigt Ihnen, wie Sie einen Farbverlauf zur Füllung einer PSD-Ebene hinzufügen können.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Kontureffekt mit Farbverlaufsfüllung**
Dieser Artikel zeigt, wie ein Kontureffekt mit Farbverlaufsfüllung gerendert werden kann. Der Kontureffekt wird verwendet, um Striche und Rahmen zu Ebenen und Formen hinzuzufügen. Er kann verwendet werden, um einfarbige Linien, bunte Farbverläufe sowie gemusterte Rahmen zu erstellen.

Die Schritte zur Darstellung des Kontureffekts mit Farbverlaufsfüllung sind so einfach wie folgt:

- Setzen Sie die Eigenschaft LoadEffectsResource.
- Laden Sie eine PSD-Datei als Bild mithilfe der von der Image-Klasse bereitgestellten Factory-Methode Load und definieren Sie PsdLoadOptions.
- Setzen Sie die Einstellungen der Eigenschaften von **ColorFillSetting**.
- Speichern Sie die Ergebnisse.

Der folgende Code-Schnipsel zeigt Ihnen, wie Sie den Kontureffekt mit Farbverlaufsfüllung rendern können.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}




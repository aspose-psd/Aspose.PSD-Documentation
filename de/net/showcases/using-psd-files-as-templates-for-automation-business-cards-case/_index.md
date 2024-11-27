---
title: Verwendung von PSD-Dateien als Vorlagen für die Automatisierung - Fallstudie Visitenkarten
type: docs
weight: 10
url: /de/verwendung-von-psd-dateien-als-vorlagen-fur-die-automatisierung-fallstudie-visitenkarten/
---

### **Überblick**
Dieser Artikel beschreibt häufig verwendete Fälle, wenn Sie programmgesteuert einige Ebenen in einer [PSD-Datei](https://wiki.fileformat.com/image/psd/) aktualisieren müssen, in der die PSD/PSB-Datei über eine bekannte vorlagenähnliche Struktur verfügt. Dies kann verwendet werden, um eine große Anzahl von Visitenkarten für verschiedene Personen zu erstellen (Fallstudie Visitenkarten). Oder Sie müssen eine Übersetzung der PSD-Datei in verschiedene Sprachen mit dem Austausch von grafischem Material darin durchführen.

Nach dem Lesen dieses Artikels werden Sie wissen, wie Sie dies erreichen können:

![todo:image_alt_text](using-psd-dateien-als-vorlagen-fur-die-automatisierung-fallstudie-visitenkarten_1.png)
## **Einfacher Fall**
Beispielsweise haben Sie eine PSD-Vorlage mit bekannten Ebenennamen. Daher müssen Sie eine PSD-Ebene über C# ändern, aktualisieren oder ersetzen. Zunächst müssen Sie die Vorlagendatei mit Aspose.PSD öffnen.

Wie öffnet man eine PSD-Datei über C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-CSharp-Aspose-PsdDateiAlsVorlage-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-dateien-als-vorlagen-fur-die-automatisierung-fallstudie-visitenkarten_2.png)



Dann müssen wir eine Ebene finden, die wir durch ihren Namen ersetzen möchten. Hier ist eine einfache Implementierung dafür.

Wie man die Ebene in einer PSD-Datei nach ihrem Namen findet

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-CSharp-Aspose-PsdDateiAlsVorlage-Snippet-2.cs" >}}



Wenn die Ebene gefunden wurde, können wir sie auf übliche Weise aktualisieren, indem wir [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) verwenden:

Wie man auf die Grafiken der PSD-Ebene zeichnet

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-CSharp-Aspose-PsdDateiAlsVorlage-Snippet-3.cs" >}}

In diesem Fall zeichnen wir ein neu geladenes [PNG-Bild](https://wiki.fileformat.com/image/png/) auf die vorhandene PSD-Ebene, sodass die alten Daten in der neuen Datei verloren gehen.

Aber was ist, wenn wir auch Text aktualisieren müssen? Der Prozess wird ähnlich sein. Finden Sie [Textebene](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) nach ihrem Namen und aktualisieren Sie sie programmgesteuert [Textebene der Photoshop-Datei](/psd/de/net/render-text-with-different-colors-in-text-layer/).

Wie man die Textebene in Photoshop über C# aktualisiert

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-CSharp-Aspose-PsdDateiAlsVorlage-Snippet-4.cs" >}}



Am Ende müssen wir unsere Änderungen speichern:

Wie man geänderte PSD-Datei speichert unter Verwendung von [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-CSharp-Aspose-PsdDateiAlsVorlage-Snippet-5.cs" >}}



Das resultierende Bild:

![todo:image_alt_text](using-psd-dateien-als-vorlagen-fur-die-automatisierung-fallstudie-visitenkarten_3.png)


## **Ein komplexer Fall mit zusätzlichen Funktionen**
Oben haben wir die einfachste Möglichkeit gezeigt, ein Bild in einer Ebene einer PSD-Datei zu ersetzen.

Aber Aspose.PSD kann fortschrittlichere zusätzliche Funktionen wie das Hinzufügen einer neuen Ebene, das Entfernen alter Ebenen und das Aktualisieren der Textebene mit verschiedenen Stilen in mehrzeiligem Text bieten.

Wir können die [Ebene](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) finden, die wir ersetzen möchten, dann finden wir ihren Index in der Ebenenliste, entfernen sie und fügen eine neue Ebene ein, nachdem sie aus der [Jpeg-Datei](https://wiki.fileformat.com/image/jpeg/) erstellt wurde, an derselben Stelle.

Erstellen Sie eine neue Ebene aus einer Datei und fügen Sie sie als PSD-Bild mit [Aspose.PSD](https://products.aspose.com/psd/net) hinzu

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-CSharp-Aspose-PsdDateiAlsVorlage-Snippet-6.cs" >}}



Am Ende dieses Datei-Codeschnipsels korrigieren wir die Ebenenposition und speichern das neue Ebenenarray im Psd-Bild.

Wie man [PsdImage ](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)-Eigenschaften der Ebene kopiert

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-CSharp-Aspose-PsdDateiAlsVorlage-Snippet-7.cs" >}}



Und schließlich müssen wir Textebenen im vorhandenen PSD-Bild über C# aktualisieren. Aspose.PSD unterstützt die [Aktualisierung von Textebenen portionsweise](/psd/de/net/working-with-text-layers/). Jede [Textportion](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) hat eine eindeutige Kombination aus Stil- und Absatzeigenschaften.

Wie man [PsdImage ](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)-Ebeneneigenschaften kopiert

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentation-CSharp-Aspose-PsdDateiAlsVorlage-Snippet-8.cs" >}}



Als Ergebnis haben wir die PSD-Vorlage über den Code mit einer neuen Ebene aus Jpeg-, Png-, J2k-, Bmp-, Gif- oder Tiff-Datei und mehrzeiligen [Texten mit verschiedenen Stilen](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) in jedem Abschnitt geändert.

![todo:image_alt_text](using-psd-dateien-als-vorlagen-fur-die-automatisierung-fallstudie-visitenkarten_4.png)


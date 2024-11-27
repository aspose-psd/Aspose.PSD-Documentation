---
title: Erstellen Sie PSD- oder PSB-Bilder von Grund auf mit Python
weight: 100
type: docs
description: Beispiel dafür, wie Aspose.PSD für Python ein PSD-Bild von Grund auf erstellen kann
keywords: [psd erstellen, psb erstellen, neu erstellen, ebene erstellen, textebene erstellen, psd api, python, codebeispiel]
url: de/python-net/create-psd-psb-images-from-scratch/
---

## **Überblick**
Um eine PSD- oder PSB-Datei von Grund auf mit Aspose.PSD für Python zu erstellen, können Sie die folgenden Schritte befolgen:

Importieren Sie die erforderlichen Module und Klassen aus der Aspose.PSD-Bibliothek:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Geben Sie den Ausgabedateinamen und den Pfad an:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

Erstellen Sie ein PSD-Bild mit den gewünschten Abmessungen:

```python 
with PsdImage(500, 500) as img:
```

Fügen Sie eine reguläre PSD-Ebene hinzu und aktualisieren Sie sie mithilfe der Grafik-API:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Erstellen Sie eine Textebene:
```python 
textLayer = img.add_text_layer("Beispieltext", Rectangle(200, 200, 100, 100))
```

Fügen Sie der Textebene einen Schlagschatteneffekt hinzu:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Speichern Sie die PSD-Datei:
```python 
img.save(outputFile)
```

Dieser Code erstellt ein PSD-Bild mit den Abmessungen 500x500 Pixel. Es fügt eine reguläre Ebene hinzu und zeichnet mit einem Stift und einem Pinsel eine Ellipse darauf. Anschließend fügt es eine Textebene mit dem Text "Beispieltext" hinzu und wendet einen Schlagschatteneffekt darauf an. Schließlich speichert es die PSD-Datei mit dem angegebenen Ausgabedateinamen.

Bitte beachten Sie, dass Sie die Aspose.PSD-Bibliothek installiert und korrekt in Ihrer Python-Umgebung eingerichtet haben müssen, damit dieser Code funktioniert. Sie können sich an die offizielle Aspose.PSD-Dokumentation wenden, um weitere Informationen zur Installation und Verwendung der Bibliothek zu erhalten.

Bitte prüfen Sie das vollständige Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}

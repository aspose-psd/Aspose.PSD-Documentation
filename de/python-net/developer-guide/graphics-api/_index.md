---
title: Verwendung der Graphics-API zum Bearbeiten von Ebenen in PSD-Dateien
weight: 100
type: docs
description: Beispiel zur Verwendung der Graphics-API in Aspose.PSD für Python
keywords: [Ebene aktualisieren, Kreis zeichnen, Ellipse zeichnen, mit gefülltem Kreis zeichnen, Grafiken, PSD API, Python, Codebeispiel]
url: de/python-net/graphics-api/
---

## **Überblick**
Zunächst müssen Sie die PSD-Datei mithilfe der Image.load() Methode laden oder ein Psd-Bild von Grund auf erstellen. Im Beispiel stellt die Variable inputFile den Pfad zu Ihrer PSD-Datei dar und loadOpt stellt die Ladeoptionen dar (falls vorhanden).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Als nächstes können Sie auf die erste Ebene des PSD-Bildes mithilfe der psdImage.layers[0]-Syntax zugreifen. Dies gibt Ihnen eine Referenz auf das Ebenenobjekt, das Sie manipulieren können.

```python 
layer = psdImage.layers[0]
```
Um die Ebene zu bearbeiten, müssen Sie ein Graphics-Objekt erstellen, indem Sie die Ebene als Parameter übergeben. Dieses Objekt bietet verschiedene Methoden zum Zeichnen von Formen und zum Auftragen von Pinseln.

```python 
graphics = Graphics(layer)
```
Im Codebeispiel wird ein Pen-Objekt erstellt, um die Farbe und Dicke der Umrisse der Ellipsenform zu definieren. Die Konstante Color.alice_blue repräsentiert die Farbe, und Sie können die Dicke nach Bedarf anpassen.

```python 
pen = Pen(Color.alice_blue)
```
Ebenso wird ein LinearGradientBrush-Objekt erstellt, um die Füllfarbe der Ellipsenform zu definieren. Das Rectangle(250, 250, 150, 100) repräsentiert die Position und Größe der Ellipsenform, und Color.red und Color.aquamarine repräsentieren die Start- und Endfarben des Verlaufs.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Um die Ellipsenform auf der Ebene zu zeichnen, können Sie die graphics.draw_ellipse()-Methode verwenden. Das Rectangle(100, 100, 200, 200) repräsentiert die Position und Größe der Ellipsenform.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Um die Ellipsenform mit dem Farbverlaufspinsel zu füllen, können Sie die graphics.fill_ellipse()-Methode verwenden. Das Rectangle(250, 250, 150, 100) repräsentiert die Position und Größe der Ellipsenform.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Nachdem Sie die gewünschten Änderungen an der Ebene vorgenommen haben, können Sie das modifizierte PSD-Bild mithilfe der psdImage.save()-Methode speichern. Im Beispiel stellt die Variable psdName den Pfad zur Speicherung der modifizierten PSD-Datei dar.

```python 
psdImage.save(psdName)
```
Zusätzlich können Sie das modifizierte Bild auch in anderen Formaten speichern, wie z.B. PNG, indem Sie die Klasse PngOptions verwenden. Die Variable pngName stellt den Pfad zur Speicherung der PNG-Datei dar.

```python 
psdImage.save(pngName, PngOptions())
```
Das war's! Sie haben erfolgreich die Graphics-API von Aspose.PSD für Python verwendet, um Ebenen in einer PSD-Datei zu bearbeiten. Erkunden Sie weitere Funktionen und Möglichkeiten der Aspose.PSD-Bibliothek, um Ihre Bildbearbeitungsfähigkeiten zu verbessern.

Bitte überprüfen Sie das vollständige Beispiel.

## **Beispiel**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py" >}}

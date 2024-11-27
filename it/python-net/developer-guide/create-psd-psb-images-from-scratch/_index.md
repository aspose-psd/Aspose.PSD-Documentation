---
title: Crea un'immagine PSD o PSB da zero usando Python
weight: 100
type: docs
description: Esempio di come Aspose.PSD per Python può creare un'immagine Psd da zero
keywords: [creare psd, creare psb, creare nuovo, creare layer, creare testo layer, api psd, python, esempio di codice]
url: it/python-net/crea-immagini-psd-psb-da-zero/
---

## **Panoramica**
Per creare un file PSD o PSB da zero utilizzando Aspose.PSD per Python, è possibile seguire i passaggi seguenti:

Importa i moduli e le classi necessari dalla libreria Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Specifica il nome del file di output e il percorso:

```python 
outputFile = "EsempioCreazioneFileDaZero.psd"
```
Crea un'immagine PSD con le dimensioni desiderate:

```python 
with PsdImage(500, 500) as img:
```
Aggiungi un layer PSD regolare e aggiornalo usando l'API grafica:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Crea un layer di testo:
```python 
textLayer = img.add_text_layer("Testo di Esempio", Rectangle(200, 200, 100, 100))
```

Aggiungi un effetto di ombreggiatura al layer di testo:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Salva il file PSD:
```python 
img.save(outputFile)
```

Questo codice crea un'immagine PSD con dimensioni di 500x500 pixel. Aggiunge un layer regolare e disegna un'ellisse su di esso utilizzando una penna e un pennello. Aggiunge quindi un layer di testo con il testo "Testo di Esempio" e applica un effetto di ombreggiatura. Infine, salva il file PSD con il nome del file di output specificato.

Si prega di notare che sarà necessario avere la libreria Aspose.PSD installata e correttamente configurata nel proprio ambiente Python affinché questo codice funzioni. È possibile fare riferimento alla documentazione ufficiale di Aspose.PSD per ulteriori informazioni su come installare e utilizzare la libreria.

Si prega di controllare l'esempio completo.

## **Esempio**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentazione-Python-Aspose-Psd-crea-immagini-psd-psb-da-zero.py" >}}

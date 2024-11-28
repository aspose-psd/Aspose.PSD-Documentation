---
title: Créer une image PSD ou PSB à partir de zéro en utilisant Python
weight: 100
type: docs
description: Exemple de comment Aspose.PSD pour Python peut créer une image Psd à partir de zéro
keywords: [créer psd, créer psb, créer nouveau, créer calque, créer calque de texte, api psd, python, exemple de code]
url: fr/python-net/creer-des-images-psd-psb-a-partir-de-zero/
---

## **Aperçu**
Pour créer un fichier PSD ou PSB à partir de zéro en utilisant Aspose.PSD pour Python, vous pouvez suivre les étapes ci-dessous:

Importer les modules et classes nécessaires de la bibliothèque Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Spécifier le nom et le chemin du fichier de sortie:

```python 
outputFile = "ExempleCreationFichierPSD.psd"
```
Créer une image PSD avec les dimensions désirées:

```python 
with PsdImage(500, 500) as img:
```
Ajouter un calque PSD régulier et le mettre à jour en utilisant l'API graphique:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Créer un calque de texte:
```python 
textLayer = img.add_text_layer("Texte Exemple", Rectangle(200, 200, 100, 100))
```

Ajouter un effet d'ombre portée au calque de texte:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Enregistrer le fichier PSD:
```python 
img.save(outputFile)
```

Ce code crée une image PSD avec des dimensions de 500x500 pixels. Il ajoute un calque régulier et dessine une ellipse dessus en utilisant un stylo et une brosse. Ensuite, il ajoute un calque de texte avec le texte "Texte Exemple" et applique un effet d'ombre portée. Enfin, il enregistre le fichier PSD avec le nom de fichier de sortie spécifié.

Veuillez noter que vous devrez avoir la bibliothèque Aspose.PSD installée et correctement configurée dans votre environnement Python pour que ce code fonctionne. Vous pouvez vous référer à la documentation officielle d'Aspose.PSD pour plus d'informations sur comment installer et utiliser la bibliothèque.

Veuillez consulter l'exemple complet.

## **Exemple**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}

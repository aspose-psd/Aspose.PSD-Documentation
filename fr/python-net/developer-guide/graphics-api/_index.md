---
title: Utiliser l'API graphique pour éditer les calques dans les fichiers PSD
weight: 100
type: docs
description: Exemple d'utilisation de l'API graphique dans Aspose.PSD pour Python
keywords: [mettre à jour le calque, dessiner un cercle, dessiner une ellipse, dessiner un cercle rempli, graphiques, api psd, python, exemple de code]
url: fr/python-net/graphics-api/
---

## **Aperçu**
Tout d'abord, vous devez charger le fichier PSD en utilisant la méthode Image.load() ou créer une image Psd à partir de zéro. Dans l'exemple, la variable inputFile représente le chemin de votre fichier PSD et loadOpt représente les options de chargement (si nécessaire).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Ensuite, vous pouvez accéder au premier calque de l'image PSD en utilisant la syntaxe psdImage.layers[0]. Cela vous donne une référence à l'objet de calque que vous pouvez manipuler.

```python 
layer = psdImage.layers[0]
```
Pour éditer le calque, vous devez créer un objet Graphics en passant le calque en tant que paramètre. Cet objet fournit diverses méthodes pour dessiner des formes et appliquer des pinceaux.

```python 
graphics = Graphics(layer)
```
Dans l'exemple de code, un objet Pen est créé pour définir la couleur et l'épaisseur du contour de la forme ellipse. La constante Color.alice_blue représente la couleur et vous pouvez ajuster l'épaisseur selon vos besoins.

```python 
pen = Pen(Color.alice_blue)
```
De même, un objet LinearGradientBrush est créé pour définir la couleur de remplissage de la forme ellipse. Le Rectangle(250, 250, 150, 100) représente la position et la taille de la forme ellipse, et Color.red et Color.aquamarine représentent les couleurs de départ et de fin du dégradé.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Pour dessiner la forme ellipse sur le calque, vous pouvez utiliser la méthode graphics.draw_ellipse(). Le Rectangle(100, 100, 200, 200) représente la position et la taille de la forme ellipse.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Pour remplir la forme ellipse avec le pinceau dégradé, vous pouvez utiliser la méthode graphics.fill_ellipse(). Le Rectangle(250, 250, 150, 100) représente la position et la taille de la forme ellipse.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Après avoir apporté les modifications souhaitées au calque, vous pouvez enregistrer l'image PSD modifiée en utilisant la méthode psdImage.save(). Dans l'exemple, la variable psdName représente le chemin pour enregistrer le fichier PSD modifié.

```python 
psdImage.save(psdName)
```
De plus, vous pouvez également enregistrer l'image modifiée dans d'autres formats, tels que le PNG, en utilisant la classe PngOptions. La variable pngName représente le chemin pour enregistrer le fichier PNG.

```python 
psdImage.save(pngName, PngOptions())
```
C'est tout ! Vous avez utilisé avec succès l'API graphique d'Aspose.PSD pour Python pour éditer les calques dans un fichier PSD. N'hésitez pas à explorer davantage les fonctionnalités de la bibliothèque Aspose.PSD pour améliorer vos capacités d'édition d'images.

Veuillez consulter l'exemple complet.

## **Exemple**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}

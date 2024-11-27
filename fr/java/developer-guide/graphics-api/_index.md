---
title: Utilisation de l'API graphique pour éditer les calques dans les fichiers PSD
weight: 100
type: docs
description: Exemple d'utilisation de l'API graphique dans Aspose.PSD pour Java
keywords: [mettre à jour le calque, dessiner un cercle, dessiner une ellipse, dessiner un cercle plein, graphiques, api psd, java, exemple de code]
url: fr/java/graphics-api/
---

## **Aperçu**
Pour commencer, chargez le fichier PSD en utilisant la méthode Image.load() ou créez une image Psd à partir de zéro. Utilisez la variable inputFile pour représenter le chemin de votre fichier PSD et spécifiez toutes les options de chargement avec loadOpt, si nécessaire.

Ensuite, accédez au premier calque de l'image PSD en utilisant la syntaxe psdImage.getLayers()[0] pour obtenir une référence à l'objet de calque à manipuler.

Pour éditer le calque, créez un objet Graphics en passant le calque en tant que paramètre. Cet objet propose différentes méthodes pour dessiner des formes et appliquer des pinceaux.

Un objet Pen est utilisé pour définir la couleur et l'épaisseur du contour des formes. De même, des pinceaux tels que LinearGradientBrush sont utilisés pour définir les couleurs de remplissage.

Dessinez les formes sur le calque en utilisant des méthodes comme graphics.drawEllipse() pour contourner les formes et graphics.fillEllipse() pour les remplir.

Après avoir apporté les modifications souhaitées au calque, enregistrez l'image PSD modifiée en utilisant psdImage.save().

De plus, vous pouvez enregistrer l'image modifiée dans d'autres formats comme PNG en utilisant les options appropriées.

Et voilà ! Vous avez utilisé avec succès l'API graphique d'Aspose.PSD pour Java pour éditer les calques dans un fichier PSD. Explorez davantage les fonctionnalités de la bibliothèque Aspose.PSD pour améliorer vos capacités d'édition d'image.

Veuillez consulter l'exemple complet.

## **Exemple**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}

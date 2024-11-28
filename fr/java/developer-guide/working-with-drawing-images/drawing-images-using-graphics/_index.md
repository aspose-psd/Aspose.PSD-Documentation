---
title: Dessiner des images en utilisant Graphics
type: docs
weight: 20
url: /fr/java/drawing-images-using-graphics/
---

## **Dessiner des images en utilisant Graphics**


Avec la bibliothèque Aspose.PSD, vous pouvez dessiner des formes simples comme des lignes, des rectangles et des cercles, ainsi que des formes complexes comme des polygones, des courbes, des arcs et des formes de Bézier. La bibliothèque Aspose.PSD crée de telles formes en utilisant la classe Graphics qui réside dans l'espace de noms Aspose.PSD. Les objets Graphics sont responsables d'effectuer différentes opérations de dessin sur une image, modifiant ainsi la surface de l'image. La classe Graphics utilise une variété d'objets d'aide pour améliorer les formes :

- Stylos, pour dessiner des lignes, des contours de formes ou rendre d'autres représentations géométriques.
- Pinceaux, pour définir comment les zones sont remplies.
- Polices, pour définir la forme des caractères de texte.
### **Dessin avec la classe Graphics**
Voici un exemple de code démontrant l'utilisation de la classe Graphics. Le code source de l'exemple a été divisé en plusieurs parties pour le rendre simple et facile à suivre. Étape par étape, les exemples montrent comment :

1. Créer une image.
1. Créer et initialiser un objet Graphics.
1. Effacer la surface.
1. Dessiner une ellipse.
1. Dessiner un polygone rempli et enregistrer l'image.
### **Exemples de programmation**
#### **Créer une image**
Commencez par créer une image en utilisant l'une des méthodes décrites dans "Créer des fichiers".

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Créer et initialiser un objet Graphics**
Ensuite, créez et initialisez un objet Graphics en passant l'objet Image à son constructeur.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **Effacer la surface**
Effacez la surface Graphics en appelant la méthode Clear de la classe Graphics et en passant une couleur en paramètre. Cette méthode remplit la surface Graphics avec la couleur passée en argument.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **Dessiner une ellipse**
Vous remarquerez que la classe Graphics a exposé de nombreuses méthodes pour dessiner et remplir des formes. Vous trouverez la liste complète des méthodes dans la référence de l'API Aspose.PSD pour Java. La classe Graphics a exposé plusieurs versions surchargées de la méthode DrawEllipse. Toutes ces méthodes acceptent un objet Pen comme premier argument. Les paramètres suivants sont passés pour définir le rectangle de délimitation autour de l'ellipse. Pour cet exemple, utilisez la version acceptant un objet Rectangle comme deuxième paramètre pour dessiner une ellipse en utilisant l'objet Pen dans la couleur de votre choix.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **Dessiner un polygone rempli**
Ensuite, dessinez un polygone en utilisant le LinearGradientBrush et un tableau de points. La classe Graphics a exposé plusieurs versions surchargées de la méthode FillPolygon. Toutes ces méthodes acceptent un objet Brush comme premier argument, définissant les caractéristiques du remplissage. Le deuxième paramètre est un tableau de points. Veuillez noter que chaque deux points consécutifs dans le tableau spécifient un côté du polygone.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **Dessiner des images en utilisant Graphics : Source complet**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}



Toutes les classes qui implémentent IDisposable et accèdent à des ressources non gérées sont instanciées dans une instruction Using pour garantir qu'elles sont correctement libérées.

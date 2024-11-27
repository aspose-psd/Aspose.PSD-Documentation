---
title: Dessiner des images en utilisant GraphicsPath
type: docs
weight: 30
url: /fr/java/dessiner-des-images-en-utilisant-graphicspath/
---

## **Dessiner des images en utilisant GraphicsPath**
La classe GraphicsPath est responsable de la création et de la maintenance d'un chemin graphique. Le GraphicsPath n'a pas de référence à une image et ne modifie pas l'image elle-même, il peut être considéré comme un objet qui contient des métadonnées décrivant les chemins que la classe Graphics peut dessiner. La classe GraphicsPath utilise des figures; chaque figure est composée soit d'une séquence de lignes et de courbes connectées, soit d'une forme géométrique primitive. Chaque forme peut être découpée en segments de forme. Vous pouvez ajouter, supprimer et modifier différentes figures ou formes dans un objet GraphicsPath. Lorsque le GraphicsPath a été entièrement décrit, utilisez les méthodes correspondantes de la classe Graphics (Dessiner le chemin et Remplir les chemins) pour dessiner ou remplir les chemins. La classe Graphics prend chaque segment de forme et le dessine pour produire l'image finale.
### **Dessiner en utilisant la classe GraphicsPath**
Voici un exemple démontrant l'utilisation de la classe GraphicsPath. Le code source de l'exemple a été divisé en plusieurs parties pour le rendre simple et facile à suivre. Étape par étape, les exemples vous montrent comment :

- Créer une image.
- Initialiser un objet Graphics.
- Effacer la surface.
- Créer une instance de GraphicsPath.
- Créer une figure.
- Ajouter des formes à la figure.
- Créer un tableau de figures.
- Dessiner des chemins.
- Remplir des chemins.
### **Dessiner des images en utilisant GraphicsPath: Exemples de programmation**
#### **GraphicsPath : Créer une image**
Commencez par créer une image en utilisant l'une des méthodes décrites dans la création de fichiers.
#### **GraphicsPath : Initialiser un objet Graphics**
Créez et initialisez un objet Graphics en passant l'objet Image à son constructeur.
#### **GraphicsPath : Effacer la surface**
Effacez la surface Graphics en appelant la méthode Clear de la classe Graphics et passez une couleur en paramètre. Cette méthode remplit la surface Graphics avec la couleur passée en argument.
#### **GraphicsPath : Créer une instance de GraphicsPath**
Créez une instance de GraphicsPath avec GraphicsPath défini sur Alternative par défaut. Ce mode détermine comment remplir l'intérieur d'une figure fermée. La autre valeur possible de GraphicsPath est Chevron.
#### **GraphicsPath : Créer une figure**
Créez une instance de la classe Figure. Comme discuté précédemment, Figure peut contenir des Formes et les formes résident dans le namespace Aspose.PSD.Shapes.
#### **GraphicsPath: Ajouter des formes à la figure**
La méthode Add Shapes exposée par la classe Figure vous permet d'ajouter des formes à la figure. Dans les exemples de code ci-dessous, plusieurs formes sont ajoutées à un objet Figure.
#### **GraphicsPath : Ajouter des figures à un tableau**
Plusieurs figures peuvent être ajoutées à un objet GraphicsPath en utilisant la méthode AddFigures exposée par la classe GraphicsPath. Cette méthode accepte un tableau de figures comme paramètre.
#### **GraphicsPath : Dessiner les chemins**
Dessinez le GraphicsPath en utilisant la méthode DrawPath exposée par la classe Graphics. La méthode accepte deux paramètres. Le premier paramètre est un objet de la classe Pen, qui détermine la couleur, la largeur et le style du chemin. Le deuxième paramètre est l'objet de la classe GraphicsPath, représentant le chemin lui-même.
#### **GraphicsPath : Remplir les chemins**
Vous pouvez remplir un chemin en passant un objet GraphicsPath à la méthode Fill Paths exposée par la classe Graphics. La méthode Fill Paths remplit le chemin selon le mode de remplissage (alternative ou entravée) actuellement défini pour le chemin. Si le chemin a des figures ouvertes, le chemin est rempli comme si ces figures étaient fermées.

La méthode Fill Paths accepte deux paramètres. Le premier paramètre est un objet de n'importe quelle classe de pinceau de l'espace de noms Aspose.PSD.Brushes. Le deuxième paramètre est le chemin lui-même. Pour l'exemple, utilisez le HatchBrush qui est un pinceau rectangulaire avec un style de hachure, une couleur avant-plan et une couleur d'arrière-plan. Avant de passer l'objet HatchBrush à la méthode Fill Paths, définissez ses propriétés.
### **GraphicsPath : Source Complet**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}

Toutes les classes qui implémentent IDisposable sont instanciées dans une instruction Using pour garantir qu'elles sont correctement libérées.

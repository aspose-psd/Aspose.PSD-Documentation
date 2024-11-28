---
title: Dessin d'images utilisant GraphicsPath
type: docs
weight: 30
url: /fr/net/drawing-images-using-graphicspath/
---

## **Dessin d'images utilisant GraphicsPath**
La classe [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) est responsable de la création et de la maintenance d'un chemin graphique. Le GraphicsPath n'a pas de référence à une image et ne modifie pas l'image elle-même, à la place, il peut être considéré comme un objet contenant des métadonnées décrivant les chemins que la classe Graphics peut dessiner. La classe GraphicsPath utilise des figures; chaque figure est composée soit d'une séquence de lignes et de courbes connectées, soit d'une forme géométrique primitive. Chaque forme peut être divisée en segments de forme. Vous pouvez ajouter, supprimer et modifier différentes figures ou formes dans un objet GraphicsPath. Lorsque le GraphicsPath a été entièrement décrit, utilisez les méthodes correspondantes de la classe Graphics (DrawPath et Fill Paths) pour dessiner par-dessus ou remplir les chemins. La classe Graphics prend chaque segment de forme et le dessine pour produire l'image finale.
### **Dessin à l'aide de la classe GraphicsPath**
Voici un exemple démontrant l'utilisation de la classe [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath). Le code source de l'exemple a été divisé en plusieurs parties pour le rendre simple et facile à suivre. Étape par étape, les exemples vous montrent comment:

- Créer une image.
- Initialiser un objet Graphics.
- Effacer la surface.
- Créer une instance de [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Créer une figure.
- Ajouter des formes à la figure.
- Créer un tableau de figures.
- Dessiner des chemins.
- Remplir les chemins.


### **Dessin d'images à l'aide de GraphicsPath: Exemples de programmation**
#### **GraphicsPath : Créer une Image**
Commencez par créer une image en utilisant l'une des méthodes décrites dans la création de fichiers.
#### **GraphicsPath : Initialiser un objet Graphics**
Créez et initialisez un objet Graphics en passant l'objet Image à son constructeur.
#### **GraphicsPath : Effacer la Surface**
Effacez la surface Graphics en appelant la méthode Clear de la classe Graphics et passez une couleur en paramètre. Cette méthode remplit la surface Graphics avec la couleur passée en argument.
#### **GraphicsPath : Créer une Instance de GraphicsPath**
Créez une instance de GraphicsPath avec GraphicsPath défini sur Alternate par défaut. Ce mode détermine comment remplir l'intérieur d'une figure fermée. L'autre valeur possible de GraphicsPath est Winding.
#### **GraphicsPath : Créer une Figure**
Créez une instance de la classe Figure. Comme discuté précédemment, une Figure peut contenir des formes et les formes résident dans l'espace de noms Aspose.PSD.Shapes.
#### **GraphicsPath : Ajouter des Formes à la Figure**
La méthode Add Shapes exposée par la classe Figure vous permet d'ajouter des formes à la figure. Dans les exemples de code ci-dessous, plusieurs formes sont ajoutées à un objet Figure.
#### **GraphicsPath : Ajouter des Figures à un Tableau**
Plusieurs figures peuvent être ajoutées à un objet GraphicsPath en utilisant la méthode AddFigures exposée par la classe GraphicsPath. Cette méthode accepte un tableau de figures en paramètre.
#### **GraphicsPath : Dessiner les Chemins**
Dessinez le GraphicsPath en utilisant la méthode DrawPath exposée par la classe Graphics. La méthode accepte deux paramètres. Le premier paramètre est un objet de la classe Pen, qui détermine la couleur, la largeur et le style du chemin. Le deuxième paramètre est l'objet de la classe GraphicsPath, représentant le chemin lui-même.
#### **GraphicsPath : Remplir les Chemins**



Vous pouvez remplir un chemin en passant un objet GraphicsPath à la méthode Fill Paths exposée par la classe Graphics. La méthode Fill Paths remplit le chemin selon le mode de remplissage (alternate ou winding) actuellement défini pour le chemin. Si le chemin contient des figures ouvertes, le chemin est rempli comme si ces figures étaient fermées.

La méthode Fill Paths accepte deux paramètres. Le premier paramètre est un objet de n'importe quelle classe de pinceau de l'espace de noms Aspose.PSD.Brushes. Le deuxième paramètre est le chemin lui-même. Pour l'exemple, utilisez HatchBrush qui est un pinceau rectangulaire avec un style de hachures, une couleur d'avant-plan et une couleur d'arrière-plan. Avant de passer l'objet HatchBrush à la méthode Fill Paths, définissez ses propriétés.
### **GraphicsPath : Source Complète**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinerImages-DessinAvecGraphicsPath-DessinAvecGraphicsPath.cs" >}}



Toutes les classes qui implémentent IDisposable sont instanciées dans une instruction Using pour garantir qu'elles sont correctement disposées.

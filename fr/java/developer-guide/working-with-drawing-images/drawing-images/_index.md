---
title: Dessiner des images
type: docs
weight: 10
url: /fr/java/dessiner-des-images/
---

## **Dessiner des lignes**
Cet exemple utilise la classe Graphics pour dessiner des formes de lignes sur la surface de l'image. Pour illustrer son fonctionnement, l'exemple crée une nouvelle image et dessine des lignes sur la surface de l'image en utilisant la méthode DrawLine exposée par la classe Graphics. Tout d'abord, nous allons créer une PsdImage en spécifiant sa hauteur et sa largeur.

Une fois l'image créée, nous utiliserons la méthode Clear exposée par la classe Graphics pour définir sa couleur de fond. La méthode DrawLine de la classe Graphics est utilisée pour dessiner une ligne sur une image en connectant deux structures de points. Cette méthode a plusieurs surcharges acceptant l'instance de la classe Pen et des paires de coordonnées de points ou des structures Point/PointF en tant qu'arguments. La classe Pen définit un objet utilisé pour dessiner des lignes, des courbes et des formes. La classe Pen a plusieurs constructeurs surchargés pour dessiner des lignes avec une couleur, une épaisseur et un pinceau spécifiés. La classe SolidBrush est utilisée pour dessiner en continu avec une couleur spécifique. Enfin, l'image est exportée au format de fichier BMP. Le code suivant montre comment dessiner des formes de lignes sur la surface de l'image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}
## **Dessiner une ellipse**
L'exemple de dessin d'ellipse est le deuxième article de la série sur le dessin de formes. Nous utiliserons la classe Graphics pour dessiner la forme d'ellipse sur la surface de l'image. Pour illustrer son fonctionnement, l'exemple crée une nouvelle image et dessine la forme d'ellipse sur la surface de l'image en utilisant la méthode DrawEllipse exposée par la classe Graphics. Tout d'abord, nous allons créer une PsdImage en spécifiant sa hauteur et sa largeur.

Après avoir créé l'image, nous créerons et initialiserons un objet de classe Graphics et définirons la couleur de fond de l'image en utilisant la méthode Clear de la classe Graphics. La méthode DrawEllipse de la classe Graphics est utilisée pour dessiner la forme de l'ellipse sur une surface d'image spécifiée par la structure de rectangle englobante. Cette méthode a plusieurs surcharges acceptant les instances des classes Pen et Rectangle/RectangleF ou une paire de coordonnées, une hauteur et une largeur en tant qu'arguments. La classe Pen définit un objet utilisé pour dessiner des lignes, des courbes et des formes. La classe Pen a plusieurs constructeurs surchargés pour dessiner des lignes avec une couleur, une épaisseur et un pinceau spécifiés. La classe Rectangle stocke un ensemble de quatre entiers qui représentent la position et la taille d'un rectangle. La classe Rectangle a plusieurs constructeurs surchargés pour dessiner la structure de rectangle avec une taille et une position spécifiées. La classe SolidBrush est utilisée pour dessiner en continu avec une couleur spécifique. Enfin, l'image est exportée au format de fichier BMP. Le code suivant montre comment dessiner la forme d'une ellipse sur la surface de l'image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
## **Dessiner un rectangle**
Dans cet exemple, nous allons dessiner la forme du rectangle sur la surface de l'image. Pour illustrer son fonctionnement, l'exemple crée une nouvelle image et dessine la forme du rectangle sur la surface de l'image en utilisant la méthode DrawRectangle exposée par la classe Graphics. Tout d'abord, nous allons créer une PsdImage en spécifiant sa hauteur et sa largeur. Ensuite, nous définirons la couleur de fond de l'image en utilisant la méthode Clear de la classe Graphics.

La méthode DrawRectangle de la classe Graphics est utilisée pour dessiner la forme du rectangle sur une surface d'image spécifiée par la structure de rectangle. Cette méthode a plusieurs surcharges acceptant les instances des classes Pen et Rectangle/RectangleF ou une paire de coordonnées, une largeur et une hauteur en tant qu'arguments. La classe Rectangle stocke un ensemble de quatre entiers qui représentent la position et la taille d'un rectangle. La classe Rectangle a plusieurs constructeurs surchargés pour dessiner la structure du rectangle avec une taille et une position spécifiées. Enfin, l'image est exportée au format de fichier BMP. Le code suivant montre comment dessiner la forme d'un rectangle sur la surface de l'image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}
## **Dessiner un arc**
Dans cette session de la série de dessin de formes, nous allons dessiner la forme de l'arc sur la surface de l'image. Nous utiliserons la méthode DrawArc de Graphics pour illustrer l'opération sur une image BMP. Tout d'abord, nous allons créer une PsdImage en spécifiant sa hauteur et sa largeur. Une fois l'image créée, nous utiliserons la méthode Clear exposée par la classe Graphics pour définir sa couleur de fond.

La méthode DrawArc de la classe Graphics est utilisée pour dessiner la forme de l'arc sur une surface d'image. DrawArc représente une partie d'une ellipse spécifiée par la structure de rectangle ou une paire de coordonnées. Cette méthode a plusieurs surcharges acceptant les instances des classes Pen et structure Rectangle/RectangleF ou une paire de coordonnées, une largeur et une hauteur en tant qu'arguments. Enfin, l'image est exportée au format de fichier BMP. Le code suivant montre comment dessiner la forme de l'arc sur la surface de l'image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
## **Dessiner une courbe de Bézier**
Cet exemple utilise la classe Graphics pour dessiner la forme de Bézier sur la surface de l'image. Pour illustrer son fonctionnement, l'exemple crée une nouvelle image et dessine la forme de Bézier sur la surface de l'image en utilisant la méthode DrawBezier exposée par la classe Graphics. Tout d'abord, nous allons créer une PsdImage en spécifiant sa hauteur et sa largeur. Une fois l'image créée, nous utiliserons la méthode Clear exposée par la classe Graphics pour définir sa couleur de fond.

La méthode DrawBezier de la classe Graphics est utilisée pour dessiner la forme de la spline de Bézier sur une surface d'image définie par quatre structures de point. Cette méthode a plusieurs surcharges acceptant les instances de la classe Pen et quatre paires de coordonnées ordonnées, ou quatre structures Point/PointF, ou un tableau de structures Point/PointF. La classe Pen définit un objet utilisé pour dessiner des lignes, des courbes et des formes. La classe Pen a plusieurs constructeurs surchargés pour dessiner des lignes avec une couleur, une épaisseur et un pinceau spécifiés. Enfin, l'image est exportée au format de fichier BMP. Le code suivant montre comment dessiner la forme de Bézier sur la surface de l'image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
## **Dessiner des images en utilisant la fonctionnalité de base**
Aspose.PSD est une bibliothèque qui offre de nombreuses fonctionnalités précieuses, notamment la création d'images à partir de zéro. Dessinez en utilisant la fonctionnalité de base comme la manipulation des informations de bitmap d'une image, ou utilisez les fonctionnalités avancées comme Graphics et GraphicsPath pour dessiner des formes sur la surface de l'image à l'aide de différents pinceaux et stylos. En utilisant la classe RasterImage d'Aspose.PSD, vous pouvez récupérer les informations de pixel d'une zone d'image et les manipuler. La classe RasterImage contient l'ensemble de fonctionnalités de dessin de base, comme obtenir et définir des pixels et d'autres méthodes de manipulation d'images. Créez une nouvelle image en utilisant l'une des méthodes décrites dans la création de fichiers et assignez-la à une instance de la classe RasterImage. Utilisez la méthode LoadPixels de la classe RasterImage pour récupérer les informations de pixel d'une partie d'une image. Une fois que vous disposez d'un tableau de pixels, vous pouvez le manipuler en modifiant par exemple la couleur de chaque pixel. Après avoir manipulé les informations de pixel, réaffectez-les à la zone désirée de l'image en utilisant la méthode SavePixels de la classe RasterImage. Le code suivant montre comment dessiner des images en utilisant la fonctionnalité de base.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}

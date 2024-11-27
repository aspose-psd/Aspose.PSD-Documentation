---
title: Conversion d'images
type: docs
weight: 20
url: /fr/java/conversion-dimages/
---

## **Convertir des images en noir et blanc et en niveaux de gris**
Parfois, vous pourriez avoir besoin de convertir des images en couleur en noir et blanc ou en niveaux de gris pour des besoins d'impression ou d'archivage. Cet article démontre l'utilisation de l'API Aspose.PSD pour Java pour réaliser cela en utilisant deux méthodes comme indiqué ci-dessous.

- Binarisation
- Grisaille
### **Binarisation**
Pour comprendre le concept de binarisation, il est important de définir une image binaire ; il s'agit d'une image numérique qui ne peut avoir que deux valeurs possibles pour chaque pixel. Normalement, les deux couleurs utilisées pour une image binaire sont le noir et le blanc, bien que n'importe quelles deux couleurs puissent être utilisées. La binarisation est le processus de conversion d'une image en bi-niveau, ce qui signifie que chaque pixel est stocké sous forme d'un seul bit (0 ou 1) où 0 indique l'absence de couleur et 1 signifie la présence de couleur. L'API Aspose.PSD pour Java prend en charge actuellement deux méthodes de binarisation.
#### **Binarisation avec seuil fixe**
Le code suivant montre comment utiliser la binarisation avec seuil fixe qui peut être appliquée à une image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Binarisation avec seuil Otsu**
Le code suivant montre comment la binarisation avec seuil Otsu peut être appliquée à une image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Grisaille**
La grisaille est le processus de conversion d'une image en tons continus en une image avec des nuances de gris discontinues. Le code suivant montre comment utiliser la grisaille.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Convertir les couches d'images GIF en image TIFF**
Parfois, il est nécessaire d'extraire et de convertir les couches d'une image PSD en un autre format d'image matricielle pour répondre à un besoin d'application. L'API Aspose.PSD prend en charge la fonction d'extraction et de conversion des couches d'une image PSD en un autre format d'image matricielle. Tout d'abord, nous allons créer une instance d'image et charger l'image PSD à partir du disque local, puis nous itérerons chaque couche dans la propriété Layer. Ensuite, nous convertirons le bloc en image TIFF. Le code suivant montre comment convertir les couches d'une image PSD en images TIFF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **Conversion de PSD CMJN en TIFF CMJN**
Avec Aspose.PSD pour Java, les développeurs peuvent convertir un fichier PSD CMJN en format tiff CMJN. Cet article montre comment exporter / convertir un fichier PSD CMJN en format tiff CMJN avec Aspose.PSD. En utilisant Aspose.PSD pour Java, vous pouvez charger des images PSD, puis vous pouvez définir diverses propriétés à l'aide de la classe TiffOptions et enregistrer ou exporter l'image. Le code suivant montre comment réaliser cette fonctionnalité.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Exportation d'images**
En plus d'un ensemble riche de routines de traitement d'images, Aspose.PSD fournit des classes spécialisées pour convertir les formats de fichiers PSD en d'autres formats. En utilisant cette bibliothèque, la conversion d'images PSD est très simple et intuitive. Voici quelques classes spécialisées à cette fin dans l'espace de noms ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Il est facile d'exporter des images PSD avec l'API Aspose.PSD pour Java. Tout ce dont vous avez besoin est un objet de la classe appropriée de l'espace de noms ImageOptions. En utilisant ces classes, vous pouvez facilement exporter n'importe quelle image créée, éditée ou simplement chargée avec Aspose.PSD pour Java vers n'importe quel format pris en charge.
## **Combinaison d'images**
Cet exemple utilise la classe Graphics et montre comment combiner deux images ou plus en une seule image complète. Pour démontrer l'opération, l'exemple crée une nouvelle PsdImage et dessine des images sur la surface du canevas en utilisant la méthode Draw Image exposée par la classe Graphics. En utilisant la classe Graphics, deux images ou plus peuvent être combinées de telle manière que l'image résultante ressemble à une image complète sans espacement entre les parties de l'image et sans pages. La taille du canevas doit être égale à la taille de l'image résultante. Voici la démonstration du code qui montre comment utiliser la méthode Draw Image de la classe Graphics pour combiner des images en une seule image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Étendre et recadrer les images**
L'API Aspose.PSD vous permet d'étendre ou de recadrer une image pendant le processus de conversion d'image. Le développeur doit créer un rectangle avec des coordonnées X et Y et spécifier la largeur et la hauteur de la boîte du rectangle. Les coordonnées X,Y et la largeur, la hauteur du rectangle vont définir l'extension ou le recadrage de l'image chargée. S'il est nécessaire d'étendre ou de recadrer l'image pendant la conversion d'image, exécutez les étapes suivantes :

1. Créez une instance de la classe RasterImage et chargez l'image existante.
1. Créez une instance de la classe ImageOption.
1. Créez une instance de la classe Rectangle et initialisez les coordonnées X,Y et la largeur, la hauteur du rectangle.
1. Appelez la méthode Save de la classe RasterImage en passant le nom du fichier de sortie, les options d'image et l'objet rectangle en tant que paramètres.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Lire et écrire des données XMP sur des images**
XMP (Extensible Metadata Platform) est une norme ISO. XMP normalise un modèle de données, un format de sérialisation et des propriétés de base pour la définition et le traitement de métadonnées extensibles. Il fournit également des directives pour incorporer des informations XMP dans des images populaires telles que JPEG, sans compromettre leur lisibilité par des applications qui ne prennent pas en charge XMP. En utilisant l'API Aspose.PSD pour Java, les développeurs peuvent lire ou écrire des métadonnées XMP sur des images. Cet article démontre comment les métadonnées XMP peuvent être lues à partir d'une image et comment écrire des métadonnées XMP sur des images.
### **Créer des métadonnées XMP, les écrire et les lire à partir d'un fichier**
À l'aide de l'espace de noms XMP, le développeur peut créer un objet de métadonnées XMP et l'écrire dans une image. Le code suivant montre comment utiliser les packages XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage et DublinCorePackage contenus dans l'espace de noms XMP.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Exporter des images dans un environnement multi-thread**
Aspose.PSD pour Java prend désormais en charge la conversion d'images dans un environnement multi-thread. Aspose.PSD pour Java garantit les performances optimisées des opérations lors de l'exécution du code dans un environnement multi-thread. Toutes les classes d'options d'image (par exemple BmpOptions, TiffOptions, JpegOptions, etc.) dans Aspose.PSD for Java implémentent l'interface IDisposable. Il est donc essentiel que le développeur libère correctement l'objet de la classe d'options d'image dans le cas où la propriété Source est définie. Le code suivant démontre ladite fonctionnalité.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



Aspose.PSD prend désormais en charge la propriété SyncRoot lors du travail dans un environnement multi-thread. Le développeur peut utiliser cette propriété pour synchroniser l'accès au flux source. Le code suivant démontre comment la propriété SyncRoot peut être utilisée.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

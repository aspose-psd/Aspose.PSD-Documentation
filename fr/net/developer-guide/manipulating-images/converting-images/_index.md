---
title: Conversion d'images
type: docs
weight: 20
url: /fr/net/converting-images/
---

## **Conversion d'images en noir et blanc et en niveaux de gris**
Parfois, vous pourriez avoir besoin de convertir des images colorées en noir et blanc ou en niveaux de gris pour l'impression ou l'archivage. Cet article présente l'utilisation de l'API Aspose.PSD pour .NET pour réaliser cela en utilisant deux méthodes comme indiqué ci-dessous.

- Binarisation
- Niveaux de gris
### **Binarisation**
Pour comprendre le concept de binarisation, il est important de définir une image binaire ; une image numérique qui ne peut avoir que deux valeurs possibles pour chaque pixel. Normalement, les deux couleurs utilisées pour une image binaire sont le noir et le blanc bien que n'importe quelle paire de couleurs puisse être utilisée. La binarisation est le processus de conversion d'une image en niveaux de gris, ce qui signifie que chaque pixel est stocké comme un seul bit (0 ou 1) où 0 indique l'absence de couleur et 1 signifie la présence de couleur. L'API Aspose.PSD pour .NET prend actuellement en charge deux méthodes de binarisation.
#### **Binarisation avec un seuil fixe**
Le code suivant vous montre comment appliquer la binarisation avec un seuil fixe à une image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarisation avec un seuil d'Otsu**
Le code suivant vous montre comment appliquer la binarisation avec un seuil d'Otsu à une image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Niveaux de gris**
La mise en niveaux de gris est le processus de conversion d'une image en demi-teinte continue en une image avec des nuances de gris discontinues. Le code suivant vous montre comment utiliser les niveaux de gris.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **Convertir les calques d'images GIF en image TIFF**
Parfois, il est nécessaire d'extraire et de convertir les calques d'une image PSD en un autre format d'image matricielle pour répondre à un besoin d'application. L'API Aspose.PSD prend en charge la fonction d'extraction et de conversion des calques d'une image PSD en un autre format d'image matricielle. Tout d'abord, nous allons créer une instance d'image et charger une image PSD depuis le disque local, puis nous allons itérer sur chaque calque dans la propriété Layer. Ensuite, nous convertirons le bloc en image TIFF. Le code suivant vous montre comment convertir les calques d'une image PSD en images TIFF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **Conversion d'un PSD CMJN en TIFF CMJN**
Avec Aspose.PSD pour .NET, les développeurs peuvent convertir un fichier PSD CMJN en format tiff CMJN. Cet article montre comment exporter/convertir un fichier PSD CMJN en format tiff CMJN avec Aspose.PSD. En utilisant Aspose.PSD pour .NET, vous pouvez charger des images PSD et ensuite vous pouvez définir diverses propriétés à l'aide de la classe [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) et enregistrer ou exporter l'image. Le code suivant montre comment réaliser cette fonctionnalité.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **Exportation d'images**
En plus d'un ensemble complet de routines de traitement d'images, Aspose.PSD fournit des classes spécialisées pour convertir les formats de fichiers PSD en d'autres formats. En utilisant cette bibliothèque, la conversion d'images PSD est très simple et intuitive. Voici quelques classes spécialisées à cet effet dans l'espace de noms [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions).

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Il est facile d'exporter des images PSD avec l'API Aspose.PSD pour .NET. Tout ce dont vous avez besoin est un objet de la classe appropriée provenant de l'espace de noms [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions). En utilisant ces classes, vous pouvez facilement exporter toute image créée, éditée ou simplement chargée avec Aspose.PSD pour .NET vers n'importe quel format pris en charge.
## **Combinaison d'images**
Cet exemple utilise la classe Graphics et montre comment combiner deux ou plusieurs images en une seule image complète. Pour illustrer l'opération, l'exemple crée une nouvelle image PsdImage et dessine des images sur la surface du canevas en utilisant la méthode DrawImage exposée par la classe Graphics. En utilisant la classe Graphics, deux ou plusieurs images peuvent être combinées de telle manière que l'image résultante apparaisse comme une image complète sans espace entre les parties de l'image et sans pages. La taille du canevas doit être égale à la taille de l'image résultante. Voici la démonstration de code montrant comment utiliser la méthode [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) de la classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) pour combiner des images en une seule image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **Agrandir et recadrer des images**
L'API Aspose.PSD vous permet d'agrandir ou de recadrer une image pendant le processus de conversion d'images. Le développeur doit créer un rectangle avec des coordonnées X et Y et spécifier la largeur et la hauteur de la boîte de rectangle. Les coordonnées X, Y et la largeur, la hauteur du rectangle indiqueront l'agrandissement ou le rognage de l'image chargée. S'il est nécessaire d'agrandir ou de recadrer l'image pendant la conversion d'images, effectuez les étapes suivantes :

1. Créez une instance de la classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) et chargez l'image existante.
1. Créez une instance de la classe ImageOption.
1. Créez une instance de la classe [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) et initialisez les coordonnées X, Y et la largeur, la hauteur du rectangle.
1. Appelez la méthode [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) de la classe RasterImage en passant le nom de fichier de sortie, les options d'image et l'objet rectangle en tant que paramètres.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **Lecture et écriture de données XMP sur les images**
XMP (Plateforme de métadonnées extensible) est une norme ISO. XMP normalise un modèle de données, un format de sérialisation et des propriétés de base pour la définition et le traitement des métadonnées extensibles. Il fournit également des directives pour incorporer des informations XMP dans une image populaire telle que JPEG, sans compromettre leur lisibilité par des applications ne prenant pas en charge le XMP. En utilisant l'API Aspose.PSD pour .NET, les développeurs peuvent lire ou écrire des métadonnées XMP sur des images. Cet article montre comment les métadonnées XMP peuvent être lues à partir d'une image et comment les métadonnées XMP peuvent être écrites sur des images.
### **Créer des métadonnées XMP, les écrire et les lire à partir d'un fichier**
Avec l'aide de l'espace de noms Xmp, le développeur peut créer un objet de métadonnées XMP et l'écrire sur une image. Le code suivant vous montre comment utiliser les packages XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage et DublinCorePackage contenus dans l'espace de noms [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **Exporter des images dans un environnement multithread**
Aspose.PSD pour .NET prend désormais en charge la conversion d'images dans un environnement multithread. Aspose.PSD pour .NET garantit des performances optimisées des opérations lors de l'exécution du code dans un environnement multithread. Toutes les classes d'options d'image (par exemple BmpOptions, TiffOptions, JpegOptions, etc.) dans Aspose.PSD pour .NET implémentent l'interface IDisposable. Il est donc impératif que le développeur libère correctement l'objet de la classe d'options d'image si la propriété Source est définie. Le code suivant illustre ladite fonctionnalité.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD prend désormais en charge la propriété SyncRoot lorsqu'il est utilisé dans un environnement multithread. Le développeur peut utiliser cette propriété pour synchroniser l'accès au flux source. Le code suivant montre comment utiliser la propriété SyncRoot.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}

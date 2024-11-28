---
title: Création, ouverture et enregistrement d'images
type: docs
weight: 30
url: /fr/net/creation-ouverture-et-enregistrement-dimages/
---

## **Création de fichiers image**
Aspose.PSD pour .NET permet aux développeurs de créer leurs propres images. Utilisez la méthode statique Create exposée par la classe Image pour créer de nouvelles images. Il vous suffit de fournir l'objet approprié d'une des classes de l'espace de noms ImageOptions pour le format d'image de sortie souhaité. Pour créer un fichier image, commencez par créer une instance d'une des classes de l'espace de noms ImageOptions. Ces classes déterminent le format d'image de sortie. Voici quelques classes de l'espace de noms ImageOptions (notez que seule la famille de formats de fichiers PSD est actuellement prise en charge pour la création) :

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) définit les options pour la création d'un fichier PSD. Les fichiers image peuvent être créés en définissant un chemin de sortie ou en définissant un flux.
### **Création en définissant un chemin**
Créez des PsdOptions à partir de l'espace de noms [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) et définissez les différentes propriétés. La propriété la plus importante à définir est la propriété Source. Cette propriété spécifie où réside les données de l'image (dans un fichier ou un flux). Dans l'exemple ci-dessous, la source est un fichier. Après avoir défini les propriétés, transmettez l'objet à l'une des méthodes statiques [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) en passant les paramètres de largeur et de hauteur. La largeur et la hauteur sont définies en pixels.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Création en utilisant un flux**
Le processus de création d'une image en utilisant un flux est le même que celui utilisant un chemin. La seule différence est que vous devez créer une instance de [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) en passant un objet Stream à son constructeur et en l'assignant à la propriété Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Ouverture de fichiers image**
Les développeurs peuvent utiliser l'API Aspose.PSD pour .NET pour ouvrir des fichiers image PSD existants à des fins différentes, comme ajouter des effets à l'image ou convertir un fichier existant dans un autre format. Quel que soit le but, Aspose.PSD propose deux façons standard d'ouvrir des fichiers existants : à partir d'un fichier ou à partir d'un flux.
### **Ouverture depuis le disque**
Ouvrez un fichier image en passant le chemin et le nom de fichier en tant que paramètre à la méthode statique Load exposée par la classe Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Ouverture en utilisant un flux**
Parfois, l'image que nous devons ouvrir est stockée sous forme de flux. Dans de tels cas, utilisez la version surchargée de la méthode Load. Celle-ci accepte un objet Stream comme argument pour ouvrir l'image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Charger une image comme calque**
Cet article montre comment utiliser Aspose.PSD pour charger une image comme calque. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD a exposé la méthode AddLayer de la classe PsdImage pour ajouter une image dans un fichier PSD en tant que calque.

Les étapes pour charger une image dans un PSD en tant que calque sont aussi simples que ci-dessous :

- Créez une instance d'une image en utilisant la classe PsdImage avec une largeur et une hauteur spécifiées.
- Chargez un fichier PSD en tant qu'image en utilisant la méthode de fabrique Load exposée par la classe Image.
- Créez une instance de la classe Layer et assignez-y le calque d'image PSD.
- Ajoutez le calque créé en utilisant la méthode AddLayer exposée par la classe PsdImage.
- Enregistrez les résultats.
  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Charger une image comme calque à partir d'un flux**
Cet article montre comment utiliser Aspose.PSD pour charger une image comme calque à partir d'un flux. Pour charger une image à partir d'un flux, il suffit de passer un objet flux contenant une image au constructeur de la classe Layer. Ajoutez le calque créé en utilisant la méthode AddLayer exposée par la classe PsdImage et enregistrez les résultats.


Voici un exemple de code.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Enregistrement de fichiers image**
Aspose.PSD vous permet de créer des fichiers image à partir de zéro. Il offre également la possibilité de modifier des fichiers image existants. Une fois l'image créée ou modifiée, le fichier est généralement enregistré sur le disque. Aspose.PSD vous propose des méthodes pour enregistrer des images sur un disque en spécifiant un chemin ou en utilisant un objet Stream.
### **Enregistrement sur disque**
La classe Image représente un objet image, donc cette classe fournit tous les outils nécessaires pour créer, charger et enregistrer un fichier image. Utilisez la méthode Save de la classe Image pour enregistrer les images. Une version surchargée de la méthode Save accepte l'emplacement du fichier sous forme de chaîne.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Enregistrement sur un flux**
Une autre version surchargée de la méthode Save accepte l'objet Stream en tant qu'argument et enregistre le fichier image dans le flux.

Si l'image est créée en spécifiant l'une des CreateOptions dans le constructeur de l'Image, l'image est automatiquement enregistrée dans le chemin ou le flux fourni lors de l'initialisation de la classe Image en appelant la méthode Save qui n'accepte aucun paramètre.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Paramétrage pour remplacer les polices manquantes**
Les développeurs peuvent utiliser l'API Aspose.PSD pour .NET pour charger des fichiers image PSD existants à des fins différentes, par exemple, définir un nom de police par défaut lors de l'enregistrement de documents PSD en tant qu'image raster (dans les formats PNG, JPG et BMP). Cette police par défaut doit être utilisée comme remplacement pour toutes les polices manquantes (polices non trouvées dans le système d'exploitation actuel). Une fois l'image modifiée, le fichier sera enregistré sur le disque.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}


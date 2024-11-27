---
title: Création, ouverture et enregistrement d'images
type: docs
weight: 30
url: /fr/java/creation-ouverture-et-enregistrement-dimages/
---

## **Créer des fichiers image**
Aspose.PSD pour Java permet aux développeurs de créer leurs propres images. Utilisez la méthode statique Create exposée par la classe Image pour créer de nouvelles images. Tout ce que vous avez à faire est de fournir l'objet approprié d'une des classes de l'espace de noms ImageOptions pour le format d'image de sortie souhaité. Pour créer un fichier image, commencez par créer une instance d'une des classes de l'espace de noms ImageOptions. Ces classes déterminent le format de sortie de l'image. Voici quelques classes de l'espace de noms ImageOptions (notez que seuls les formats de fichier PSD sont actuellement pris en charge pour la création) :

PsdOptions configure les options pour créer un fichier PSD. Les fichiers image peuvent être créés en définissant un chemin de sortie ou en définissant un flux.
### **Création en définissant un chemin**
Créez PsdOptions à partir de l'espace de noms ImageOptions et définissez les différentes propriétés. La propriété la plus importante à définir est la propriété Source. Cette propriété spécifie où se trouvent les données de l'image (dans un fichier ou un flux). Dans l'exemple ci-dessous, la source est un fichier. Après avoir défini les propriétés, passez l'objet à l'une des méthodes Create statiques avec les paramètres de largeur et de hauteur. La largeur et la hauteur sont définies en pixels.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Création en utilisant un flux**
Le processus pour créer une image en utilisant un flux est le même que pour utiliser un chemin. La seule différence est que vous devez créer une instance de StreamSource en passant un objet Stream à son constructeur et en l'assignant à la propriété Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Ouverture des fichiers image**
Les développeurs peuvent utiliser l'API Aspose.PSD pour Java pour ouvrir des fichiers image PSD existants à diverses fins, telles que l'ajout d'effets à l'image ou la conversion d'un fichier existant vers un autre format. Quel que soit le but, Aspose.PSD propose deux méthodes standard pour ouvrir des fichiers existants : à partir d'un fichier ou à partir d'un flux.
### **Ouverture depuis le disque**
Ouvrez un fichier image en passant le chemin et le nom du fichier en tant que paramètre à la méthode statique Load exposée par la classe Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Ouverture en utilisant un flux**
Parfois, l'image que nous devons ouvrir est stockée sous forme de flux. Dans de tels cas, utilisez la version surchargée de la méthode Load. Cela accepte un objet Stream comme argument pour ouvrir l'image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Charger une image en tant que calque**
Cet article montre comment utiliser Aspose.PSD pour charger une image en tant que calque. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD a exposé la méthode AddLayer de la classe PsdImage pour ajouter une image dans un fichier PSD en tant que calque.

Les étapes pour charger une image dans un PSD en tant que calque sont aussi simples que ci-dessous :

- Créer une instance d'image en utilisant la classe PsdImage avec une largeur et une hauteur spécifiées.
- Charger un fichier PSD en tant qu'image en utilisant la méthode statique Load exposée par la classe Image.
- Créer une instance de la classe Layer et assigner le calque d'image PSD.
- Ajouter le calque créé en utilisant la méthode AddLayer exposée par la classe PsdImage
- Enregistrer les résultats.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Enregistrer des fichiers image**
Aspose.PSD vous permet de créer des fichiers image à partir de zéro. Il fournit également les moyens de modifier des fichiers image existants. Une fois l'image créée ou modifiée, le fichier est généralement enregistré sur le disque. Aspose.PSD vous fournit des méthodes pour enregistrer des images sur un disque en spécifiant un chemin ou en utilisant un objet Stream.
### **Enregistrement sur le disque**
La classe Image représente un objet image, cette classe fournit tous les outils nécessaires pour créer, charger et enregistrer un fichier image. Utilisez la méthode Save de la classe Image pour enregistrer des images. Une version surchargée de la méthode Save accepte l'emplacement du fichier en tant que chaîne.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Enregistrement sur un flux**
Une autre version surchargée de la méthode Save accepte un objet Stream comme argument et enregistre le fichier image sur le flux.

Si l'image est créée en spécifiant l'une des CreateOptions dans le constructeur de l'Image, l'image est automatiquement enregistrée sur le chemin ou le flux fourni lors de l'initialisation de la classe Image en appelant la méthode Save qui n'accepte aucun paramètre.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Paramètres pour remplacer les polices manquantes**
Les développeurs peuvent utiliser l'API Aspose.PSD pour Java pour charger des fichiers image PSD existants à diverses fins, par exemple pour définir le nom de police par défaut lors de l'enregistrement de documents PSD en tant qu'image matricielle (en PNG, JPG et BMP). Cette police par défaut doit être utilisée comme remplacement pour toutes les polices manquantes (polices non trouvées dans le système d'exploitation actuel). Une fois l'image modifiée, le fichier sera enregistré sur le disque.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}



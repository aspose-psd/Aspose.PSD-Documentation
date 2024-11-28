---
title: Manipulation des images JPEG
type: docs
weight: 30
url: /fr/net/manipulating-jpeg-images/
---

## **Utilisation de la classe ExifData pour lire et modifier les balises EXIF Jpeg**
Pratiquement tous les appareils photo numériques (y compris les smartphones), les scanners et d'autres systèmes de manipulation d'images enregistrent les images avec des informations EXIF (Exchangeable Image File). Les réglages de l'appareil photo et les informations de la scène sont enregistrés par l'appareil photo dans le fichier image. Les données EXIF incluent également la vitesse d'obturation, la date et l'heure à laquelle la photo a été prise, la longueur focale, la compensation d'exposition, le mode de mesure et si un flash a été utilisé. Les API Aspose.Imaging ont rendu possible l'extraction des informations EXIF à partir d'une image donnée de manière très simple et facile. Les développeurs peuvent également écrire des données EXIF sur les images ou modifier les informations existantes selon leurs besoins. Aspose.PSD a fourni la classe [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) pour lire, écrire et modifier les données EXIF, tandis que l'espace de noms [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) contient les énumérations pertinentes utilisées dans le processus.
### **Lecture des données EXIF**
Les API Aspose.PSD fournissent des moyens pour lire les données EXIF à partir d'une image donnée. Les étapes fournies ci-dessous illustrent l'utilisation de la classe ExifData pour lire les informations EXIF à partir d'une image.

- Charger l'image PSD en utilisant la méthode de fabrique Load.
- Rechercher la vignette Jpeg parmi les ressources PSD.
- Extraire une instance de la classe ExifData.

Récupérez les informations nécessaires et écrivez-les dans la console.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Alternativement, les développeurs peuvent également obtenir des informations spécifiques en utilisant le code suivant.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Écriture & modification des données EXIF**
En utilisant les API Aspose.PSD, les développeurs peuvent écrire de nouvelles informations EXIF et modifier les données EXIF existantes d'une image. Les deux processus (écriture & modification) nécessitent le chargement d'une image et l'obtention des données EXIF dans une instance de la classe ExifData. Ensuite, on peut accéder aux propriétés exposées par la classe ExifData pour les définir en conséquence. Veuillez noter que les images destinées à la manipulation doivent être des images Jpeg ou Tiff qui sont généralement des miniatures PSD. Le code d'exemple pour démontrer l'utilisation est le suivant :



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Extraction de miniatures des ressources PSD**
Les miniatures sont des versions réduites des images, utilisées pour afficher une partie significative de l'image au lieu du cadre complet. Certains fichiers image (surtout ceux pris avec un appareil photo numérique) contiennent une image miniature intégrée dans le fichier. L'API Aspose.PSD vous permet d'extraire les miniatures des ressources PSD et de les stocker séparément sur le disque. Les ressources de vignettes contiennent la propriété [Vignette](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) d'ExifData qui peut récupérer les données de la vignette. Le code fourni ci-dessous montre comment l'utiliser.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Utilisez l'approche discutée ci-dessus pour stocker la vignette dans d'autres formats de fichiers pris en charge. Si vous souhaitez exporter les données de la vignette vers d'autres formats d'image tels que BMP & PNG, veuillez utiliser d'autres options d'exportation d'images.


### **Extraction de miniatures des segments JFIF**
Il est également possible d'extraire des miniatures des segments ExifData ou JFIF des ressources de miniatures PSD. Le code suivant montre comment effectuer l'extraction des données de la vignette à partir du segment JFIF ou ExifData :


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Utilisez l'approche discutée ci-dessus pour stocker la vignette dans d'autres formats de fichiers pris en charge. Si vous souhaitez exporter les données de la vignette vers d'autres formats d'image tels que BMP & PNG, veuillez utiliser d'autres options d'exportation d'images.
### **Ajout d'une vignette au segment JFIF**
Le code ci-dessous montre comment utiliser la propriété JFIF. Vignette pour ajouter une image miniature au segment JFIF d'une image PSD chargée.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Les images miniatures avec d'autres données de segment ne peuvent pas occuper plus de 65 545 octets en raison des spécifications du format JPEG. Dans les cas où de grandes images doivent être définies comme vignette, une exception peut survenir.


### **Ajout d'une vignette au segment EXIF**
Le code ci-dessous montre comment utiliser la propriété ExifData.Vignette pour ajouter une image miniature au segment EXIF d'une image PSD chargée.


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


Dans ce cas, l'API Aspose.PSD ne peut pas estimer la taille de l'image miniature, mais elle peut vérifier la taille de l'ensemble du segment de données EXIF. Cela ne peut pas dépasser 65 535 octets.
## **Utilisation de la classe JpegExifData pour lire et modifier les balises EXIF Jpeg**
Les API Aspose.PSD fournissent la classe [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) qui est exclusive aux formats d'image Jpeg pour récupérer et mettre à jour les informations EXIF. Cet article démontre comment utiliser la classe JpegExifData pour obtenir le même résultat. La classe Aspose.PSD.Exif.JpegExifData sert de conteneur de données EXIF pour les images Jpeg, et permet de récupérer les balises EXIF standard des images Jpeg comme démontré ci-dessous :



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Liste complète des balises EXIF**
Le snippet de code ci-dessus lit quelques balises EXIF en utilisant les propriétés offertes par la classe Aspose.PSD.Exif.JpegExifData. La liste complète de ces propriétés est disponible ici. Le code suivant lira toutes les balises EXIF en utilisant la [Propriété PropertyInfo de System.Reflection](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0).


{{< gist "ascompose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Correction automatique de l'orientation des images JPEG**


Les photos peuvent être prises avec un appareil photo tourné à 90°, 180°, 270° ou pas (orientation normale). La plupart des appareils photo numériques stockent les informations d'orientation avec les données d'image sous forme de tags EXIF des images JPEG. Ces informations peuvent être utilisées pour effectuer la rotation automatique sur les images afin de corriger l'orientation. Les API Aspose.PSD fournissent la méthode AutoRotate pour la classe JpegImage afin de corriger automatiquement l'orientation des images JPEG. Voici comment vous pouvez utiliser la méthode AutoRotate avec l'API Aspose.PSD pour .NET.


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Prise en charge de JPEG-LS avec CMJN et YCCK**


L'API Aspose.PSD pour .NET prend en charge les modèles de couleurs CMJN et YCCK avec JPEG-LS. Le fragment de code ci-dessous montre comment utiliser cette prise en charge pour JPEG-LS.



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Prise en charge de 2-7 bits par échantillon dans les images JPEG-LS**


L'API Aspose.PSD pour .NET prend en charge les images JPEG-LS avec 2-7 bits par échantillon. Le code ci-dessous montre comment utiliser cette prise en charge pour JPEG-LS.



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Définition du type de couleur et du type de compression pour les images JPEG**




L'API Aspose.PSD pour .NET prend en charge le type de couleur et le type de compression et les définit en niveaux de gris et progressif pour les images JPEG. Le code ci-dessous montre comment utiliser cette prise en charge.



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}





Le code ci-dessous montre comment utiliser la propriété ExifData.Vignette pour ajouter une image miniature au segment EXIF d'une image PSD chargée.



{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

Dans ce cas, l'API Aspose.PSD ne peut pas estimer la taille de l'image miniature, mais elle peut vérifier la taille de l'ensemble du segment de données EXIF. Cela ne peut pas dépasser 65 535 octets.


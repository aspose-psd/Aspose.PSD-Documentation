---
title: Manipulation des images JPEG
type: docs
weight: 20
url: /fr/java/manipulation-dimages-jpeg/
---

## **Utilisation de la classe ExifData pour lire et modifier les balises EXIF JPEG**


Presque tous les appareils photo numériques (y compris les smartphones), les scanners et autres systèmes manipulant des images enregistrent les informations EXIF (Exchangeable Image File) des images. Les réglages de l'appareil photo et les informations de la scène sont enregistrés par l'appareil photo dans le fichier image. Les données EXIF incluent également la vitesse d'obturation, la date et l'heure de la prise de vue d'une photo, la longueur focale, la compensation d'exposition, le motif de mesure et si un flash a été utilisé. Les API Aspose.Imaging ont rendu possible l'extraction des informations EXIF à partir d'une image donnée de manière très facile et simple. Les développeurs peuvent également écrire des données EXIF sur les images ou modifier les informations existantes selon leurs besoins. Aspose.Imaging a fourni la classe ExifData pour lire, écrire et modifier les données EXIF, tandis que l'espace de noms Aspose.PSD.Exif.Enums contient les énumérations pertinentes utilisées dans le processus.
### **Lecture des données EXIF**
Les APIs Aspose.PSD permettent de lire les données EXIF à partir d'une image donnée. Les étapes fournies ci-dessous illustrent l'utilisation de la classe ExifData pour lire les informations EXIF à partir d'une image.

- Charger une image PSD à l'aide de la méthode de fabrication Load.
- Trouver la vignette JPEG parmi les ressources PSD.
- Extraire une instance de la classe ExifData.

Récupérez les informations requises et écrivez-les sur la console.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-LireToutesLesBalisesEXIF-LireToutesLesBalisesEXIF.java" >}}



Alternativement, les développeurs peuvent également obtenir des informations spécifiques en utilisant le code suivant.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-LireInformationsBalisesEXIFSpecifiques-LireInformationsBalisesEXIFSpecifiques.java" >}}
### **Écriture et modification des données EXIF**
En utilisant les APIs Aspose.PSD, les développeurs peuvent écrire de nouvelles informations EXIF et modifier les données EXIF existantes d'une image. Les deux processus (Écriture et Modification) nécessitent le chargement d'une image et l'obtention des données EXIF dans une instance de la classe ExifData. Ensuite, il est possible d'accéder aux propriétés exposées par la classe ExifData pour les configurer en conséquence. Veuillez noter que les images à manipuler doivent être des images JPEG ou TIFF qui sont habituellement des vignettes PSD. Le code d'exemple ci-dessous démontre l'utilisation :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-EcritureEtModificationDonneesEXIF-EcritureEtModificationDonneesEXIF.java" >}}
## **Extraction des vignettes des ressources PSD**
Les vignettes sont des versions réduites d'images, utilisées pour afficher une partie significative de l'image au lieu du cadre complet. Certains fichiers d'image (en particulier ceux pris avec un appareil photo numérique) ont une image miniature intégrée dans le fichier. L'API Aspose.PSD vous permet d'extraire les vignettes des ressources PSD et de les stocker séparément sur le disque. Les ressources de vignettes contiennent la propriété ExifData.Thumbnail qui peut récupérer les données de la vignette. Le code d'exemple fourni ci-dessous montre comment l'utiliser.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-ExtraireVignetteDuPSD-ExtraireVignetteDuPSD.java" >}}



Utilisez l'approche discutée ci-dessus pour stocker la vignette dans d'autres formats de fichier pris en charge. Si vous souhaitez exporter les données de la vignette vers d'autres formats d'image tels que BMP et PNG, veuillez utiliser d'autres options d'exportation d'image.


### **Extraction des vignettes des segments JFIF**
Il est également possible d'extraire des vignettes du segment ExifData ou JFIF des ressources de vignettes PSD. Le code suivant montre comment effectuer l'extraction des données de la vignette à partir du segment JFIF ou ExifData :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-ExtraireVignetteDuPSD-ExtraireVignetteDuPSD.java" >}}



Utilisez l'approche discutée ci-dessus pour stocker la vignette dans d'autres formats de fichier pris en charge. Si vous souhaitez exporter les données de la vignette vers d'autres formats d'image tels que BMP et PNG, veuillez utiliser d'autres options d'exportation d'image.
### **Ajout d'une vignette au segment JFIF**
Le code d'exemple ci-dessous montre comment utiliser la propriété JFIF.Thumbnail pour ajouter une image miniature au segment JFIF d'une image PSD chargée.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-AjouterVignetteSegmentJFIF-AjouterVignetteSegmentJFIF.java" >}}

Les images miniatures avec d'autres données de segment ne peuvent pas occuper plus de 65 545 octets en raison des spécifications du format JPEG. Dans les cas où des images de grande taille doivent être définies comme vignette, une exception peut survenir.


### **Ajout d'une vignette au segment EXIF**
Le code d'exemple ci-dessous montre comment utiliser la propriété ExifData.Thumbnail pour ajouter une image miniature au segment EXIF d'une image PSD chargée.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-AjouterVignetteSegmentEXIF-AjouterVignetteSegmentEXIF.java" >}}

Dans ce cas, l'API Aspose.PSD ne peut pas estimer la taille de l'image miniature, mais elle peut vérifier la taille de l'ensemble du segment de données EXIF. Celle-ci ne doit pas dépasser 65 535 octets.
## **Utilisation de la classe JpegExifData pour lire et modifier les balises EXIF JPEG**
Les APIs Aspose.PSD fournissent la classe JpegExifData exclusive aux formats d'image JPEG pour récupérer et mettre à jour les informations EXIF. Cet article démontre l'utilisation de la classe JpegExifData pour atteindre le même objectif. La classe Aspose.PSD.Exif.JpegExifData sert de conteneur de données EXIF pour les images JPEG et permet de récupérer les balises JPEG EXIF standard comme démontré ci-dessous :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-AjouterVignetteSegmentEXIF-AjouterVignetteSegmentEXIF.java" >}}
### **Liste complète des balises EXIF**
Le code ci-dessus lit quelques balises EXIF en utilisant les propriétés offertes par la classe Aspose.PSD.Exif.JpegExifData. La liste complète de ces propriétés est disponible ici. Le code suivant lira toutes les balises EXIF en utilisant la classe System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-LireToutesLesListesBalisesEXIF-LireToutesLesListesBalisesEXIF.java" >}}
## **Correction automatique de l'orientation des images JPEG**
Les photos peuvent être prises avec un appareil photo tourné à 90°, 180°, 270° ou aucun (orientation normale). La plupart des appareils photo numériques stockent les informations d'orientation ainsi que les données d'image sous forme de balises EXIF des images JPEG. Ces informations peuvent être utilisées pour effectuer la rotation automatique sur les images afin de corriger l'orientation. Les APIs Aspose.PSD proposent la méthode AutoRotate pour la classe JpegImage afin de corriger automatiquement l'orientation des images JPEG. Voici comment utiliser la méthode AutoRotate avec l'API Aspose.PSD pour Java :



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-CorrectionAutoOrientationDesImagesJPEG-CorrectionAutoOrientationDesImagesJPEG.java" >}}
## **Prise en charge de JPEG-LS avec CMJN et YCCK**


L'API Aspose.PSD pour Java prend en charge les modèles de couleur CMJN et YCCK avec JPEG-LS. Le code d'exemple ci-dessous montre comment utiliser cette prise en charge pour JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-PriseEnChargePourJPEGLSAvecCMJN-PriseEnChargePourJPEGLSAvecCMJN.java" >}}
## **Prise en charge de 2 à 7 bits par échantillon dans les images JPEG-LS**


L'API Aspose.PSD pour Java prend en charge les images JPEG-LS avec 2 à 7 bits par échantillon. Le code d'exemple ci-dessous montre comment utiliser cette prise en charge pour JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-PriseEnChargePour2Et7BitsJPEG-PriseEnChargePour2Et7BitsJPEG.java" >}}
## **Définition du type de couleur et du type de compression pour les images JPEG**




Aspose.PSD pour Java API prend en charge le type de couleur et le type de compression et les définir en niveaux de gris et en progression pour les images JPEG. Le code d'exemple ci-dessous montre comment utiliser cette prise en charge.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Exemples-src-main-java-com-aspose-psd-exemples-ModificationEtConversionImages-JPEG-TypeCouleurEtTypeCompression-TypeCouleurEtTypeCompression.java" >}}






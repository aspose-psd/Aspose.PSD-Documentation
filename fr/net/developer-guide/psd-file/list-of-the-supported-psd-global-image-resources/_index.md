---
title: Liste des ressources d'images globales PSD prises en charge
type: docs
weight: 30
url: /fr/net/list-of-the-supported-psd-global-image-resources/
---

## **Aspose.PSD prend en charge l'édition de bas niveau des ressources d'images.**
La liste des ressources d'images entièrement prises en charge se trouve dans le [Référence de l'API Aspose.PSD .Net](https://reference.aspose.com/psd/net).

Selon les spécifications du format Adobe® Photoshop® : Les ressources d'images utilisent plusieurs numéros d'identification standard, comme indiqué dans les ID des ressources d'images. Tous les formats de fichier n'utilisent pas tous les ID. Certaines informations peuvent être stockées dans d'autres sections du fichier.

Pour les ID de ressources qui ont été ajoutés depuis Photoshop 3.0, l'entrée indique la version dans laquelle ils ont été introduits, par exemple (*Photoshop 6.0).*

ID des ressources d'images.

|**ID**|**Description**|
| :- | :- |
|**Décimal**||
|1000|*(Obsolète - Photoshop 2.0 uniquement)* Nombre de canaux, lignes, colonnes, profondeur et mode|
|1001|Enregistrement d'informations d'impression du gestionnaire d'impression Macintosh|
|1002|Informations sur le format de page Macintosh. Non lu par Photoshop. *(Obsolète)*|
|1003|*(Obsolète - Photoshop 2.0 uniquement)* Table des couleurs indexées|
|1005|[Structure ResolutionInfo](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource)|
|1006|Noms des canaux alpha sous forme de séries de chaînes Pascal.|
|1007|*(Obsolète) Voir la structure ID 1077 DisplayInfo.*|
|1008|La légende sous forme de chaîne Pascal.|
|1009|[Informations de la bordure.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource) Contient un nombre fixe (2 octets réels, 2 octets fractionnels) pour la largeur de la bordure et 2 octets pour les unités de bordure (1 = pouces, 2 = cm, 3 = points, 4 = pica, 5 = colonnes).|
|1010|[Couleur d'arrière-plan.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|Drapeaux d'impression. Une série de valeurs booléennes sur un octet : étiquettes, marques de recadrage, barres de couleur, marques d'imposition, négatif, retournement, interpoler, légende, drapeaux d'impression.|
|1012|Informations de demi-teinte niveaux de gris et multicanal|
|1013|[Informations de demi-teinte couleur](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|Informations de demi-teinte duotone|
|1015|Fonction de transfert niveaux de gris et multicanal|
|1016|[Fonctions de transfert de couleur](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188)|
|1017|Fonctions de transfert duotone|
|1018|Informations d'image duotone|
|1019|Deux octets pour les valeurs noire et blanche effectives pour la plage de points|
|1020|*(Obsolète)*|
|1021|Options EPS|
|1022|[Informations du masque rapide](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource). ID du canal du masque rapide; 1 octet booléen indiquant si le masque était initialement vide.|
|1023|*(Obsolète)*|
|1024|[Informations d'état de calque](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource).|
|1025|Chemin de travail (non enregistré). Format de ressource de chemin.|
|1026|[Informations sur les groupes de calques](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource). 2 octets par calque contenant un ID de groupe pour les groupes de déplacement. Les calques d'un groupe ont le même ID de groupe.|
|1027|*(Obsolète)*|
|1028|Enregistrement IPTC-NAA. Contient les informations *File Info...*.|
|1029|Mode d'image pour les fichiers au format brut|
|1030|Qualité JPEG. Privé.|
|1032|*(Photoshop 4.0) [Informations sur la grille et les guides.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)*|
|1033|*(Photoshop 4.0) [](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[Ressource miniature](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[pour Photoshop 4.0](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* uniquement|
|1034|*(Photoshop 4.0)* Drapeau de copyright. Booléen indiquant si l'image est protégée par des droits d'auteur.|
|1035|*(Photoshop 4.0)* URL. Poignée d'une chaîne de texte avec localisateur de ressource uniforme.|
|1036|*(Photoshop 5.0)[Ressource miniature](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)* (remplace la ressource 1033).|
|1037|*(Photoshop 5.0) [Angle global](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*. 4 octets contenant un entier entre 0 et 359, qui est l'angle global d'éclairage pour le calque d'effets. S'il n'est pas présent, on suppose qu'il est de 30.|
|1038|*(Obsolète) Voir ID 1073 ci-dessous. (Photoshop 5.0)* Ressource des échantillons de couleur.|
|1039|*(Photoshop 5.0) [Profil ICC](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*. Les octets bruts d'un profil au format ICC (International Color Consortium).*  |
|1040|*(Photoshop 5.0) [Filigrane](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*.|
|1041|*(Photoshop 5.0) [Profil non étiqueté ICC](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*. 1 octet qui désactive toute manipulation de profil supposée lors de l'ouverture du fichier. 1 = intentionnellement non étiqueté.|
|1042|*(Photoshop 5.0)* Effets visibles. Drapeau global d'1 octet pour afficher/masquer tous les calques d'effets. Présent uniquement lorsqu'ils sont masqués.|
|1043|*(Photoshop 5.0)* Demi-teinte spot. 4 octets pour la version, 4 octets pour la longueur et les données de longueur variable.|
|1044|*(Photoshop 5.0)[ID spécifiques au document](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)* nombre de départ. 4 octets : Valeur de base, à partir de laquelle les ID de calques seront générés (ou une valeur supérieure si les ID existants dépassent déjà cette valeur). Son but est d'éviter le cas où nous ajoutons des calques, les aplatissons, enregistrons, ouvrons, et ajoutons ensuite plus de calques qui se retrouvent avec les mêmes ID que le premier groupe.|
|1045|*(Photoshop 5.0) [Noms alpha Unicode](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*.|
|1046|*(Photoshop 6.0)* Nombre de couleurs définies dans la table de couleurs indexées. 2 octets pour le nombre de couleurs dans la table qui sont réellement définies|
|1047|*(Photoshop 6.0)* [Indice de transparence](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource).|
|1049|*(Photoshop 6.0)* [Altitude globale.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* Tranches.|
|1051|*(Photoshop 6.0)* URL du flux de travail.|
|1052|*(Photoshop 6.0)* Accéder à XPEP. 2 octets de version majeure, 2 octets de version mineure, 4 octets de compte. Suivant est répété pour le décompte : 4 octets de taille de bloc, 4 octets de clé, si la clé = *'jtDd'* , alors suivante est un booléen pour le drapeau sale ; sinon c'est une entrée de 4 octets pour la date de modification.|
|1053|*(Photoshop 6.0)* Identificateurs alpha.|
|1054|*(Photoshop 6.0)[Liste d'URL](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*.|
|1057|*(Photoshop 6.0)* [Informations de version](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource).|
|1058|*(Photoshop 7.0)* Données EXIF 1.|
|1059|*(Photoshop 7.0)* Données EXIF 3*.*|
|1060|*(Photoshop 7.0)* [Métadonnées XMP](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource). Informations sur le fichier sous forme de description XML.|
|1061|*(Photoshop 7.0)[Digeste de la légende](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)*. 16 octets : RSA Data Security, algorithme de condensation de message MD5|
|1062|*(Photoshop 7.0)[Échelle d'impression](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)*. (0 = centré, 1 = ajuster à la taille, 2 = défini par l'utilisateur). 4 octets position x (flottant). 4 octets position y (flottant). 4 octets échelle (flottant)|
|1064|*(Photoshop CS)* [Rapport d'aspect des pixels](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource).|
|1065|*(Photoshop CS)* Compositions de calques.|
|1066|*(Photoshop CS)* Couleurs duotones alternatives. Cette ressource n'est pas lue ou utilisée par Photoshop.|
|1067|*(Photoshop CS)* Couleurs spot alternatives. Cette ressource n'est pas lue ou utilisée par Photoshop.|
|1069|*(Photoshop CS2)* ID(s) de sélection de calque(s). 2 octets de compte, suivis de la répétition pour chaque compte : 4 octets ID de calque|
|1070|*(Photoshop CS2)* Informations de tonalité HDR|
|1071|*(Photoshop CS2)* Informations d'impression|
|1072|*(Photoshop CS2)* [ID activés des groupes de calques](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource). 1 octet pour chaque calque dans le document, répété par la longueur de la ressource. REMARQUE : Les groupes de calques ont des marqueurs de début et de fin|
|1073|*(Photoshop CS3)* Ressource des échantillons de couleur. Voir également l'ID 1038 pour l'ancien format.|
|1074|*(Photoshop CS3)* Échelle de mesure.|
|1075|*(Photoshop CS3)* Informations de la chronologie.|
|1076|*(Photoshop CS3)* Divulgation de la feuille.|
|1077|*(Photoshop CS3) Structure DisplayInfo* pour prendre en charge les couleurs flottantes en virgule. Voir également l'ID 1007.|
|1078|*(Photoshop CS3)* Onions Skins.|
|1080|*(Photoshop CS4)* Informations de comptage.|
|1082|*(Photoshop CS5)* Informations d'impression.|
|1083|*(Photoshop CS5)* Style d'impression. Les marques d'impression, étiquettes, ornements, etc.|
|1084|*(Photoshop CS5)* Macintosh NSPrintInfo. Informations spécifiques à l'OS variables pour Macintosh.|
|1085|*(Photoshop CS5)* Windows DEVMODE. Informations spécifiques à l'OS variables pour Windows.|
|1086|*(Photoshop CS6)* Chemin d'enregistrement automatique du fichier.|
|1087|*(Photoshop CS6)* Format d'enregistrement automatique. |
|1088|*(Photoshop CC)* État de sélection du chemin.|
|2000-2997|Informations sur le chemin (chemins enregistrés).|
|2999|Nom du chemin d'écrêtage.|
|3000|*(Photoshop CC)* Informations sur le chemin d'origine|
|4000-4999|Ressource(s) du plug-in. Ressources ajoutées par un plug-in.|
|7000|Variables Image Ready. Représentation XML des définitions de variables|
|7001|Ensembles de données Image Ready|
|7002|État sélectionné par défaut Image Ready|
|7003|État étendu des rollovers Image Ready 7|
|7004|État étendu des rollovers Image Ready|
|7005|Paramètres de calques enregistrés Image Ready|
|7006|Version Image Ready|
|8000|*(Photoshop CS3)* Flux de travail Lightroom, si présent le document est en milieu de flux de travail Lightroom.|
|10000|[Informations des drapeaux d'impression](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printflagsresource).|

Aspose.PSD prend en charge certaines de ces ressources. Si une ressource n'a pas sa propre classe, vous pouvez utiliser [UnknownResource ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unknownresource)de la Référence de l'API Aspose.PSD.

Les ressources d'images globales PSD peuvent être utilisées pour un grand nombre de cas. Vous pouvez obtenir des données de bas niveau spécifiques que vous ne pouvez pas obtenir dans Adobe Photoshop.

N'hésitez pas à signaler les ressources d'images dont vous avez besoin. Le [Forum Aspose pour PSD](https://forum.aspose.com/c/psd) peut aider.
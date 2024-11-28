---
title: Conversion d'espace de couleur pour JPEG via profils ICC
type: docs
weight: 60
url: /fr/net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **Gestion des couleurs pour le format JPEG**


Cet article aborde l'utilisation des profils ICC pour effectuer la gestion de l'espace de couleur lors de la manipulation du format JPEG avec les API Aspose.PSD. L'espace de couleur interne du JPEG est YCbCr cependant, ce [format](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) peut également accueillir des espaces de couleur en niveaux de gris, RGB, CMJN et YCCK pour stocker les métadonnées de l'image. Les API Aspose.PSD fonctionnent principalement dans l'espace RGB donc l'API doit effectuer des conversions d'espace de couleur de et vers pour gérer correctement les fichiers JPEG. Les conversions de niveaux de gris en RGB et de YCbCr en RGB peuvent être effectuées avec des transformations mathématiques mais les espaces CMJN et YCCK ne peuvent pas être facilement convertis en espace RGB.

Les API Aspose.PSD doivent effectuer une transformation directe de la couleur RGB en CMJN pour les images JPEG ayant un espace de couleur CMJN. D'autre part, les images ayant un espace de couleur YCCK nécessitent une transformation de la couleur RGB en CMJN en YCCK, où la transformation de CMJN en YCCK utilise la conversion [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) appliquée pour les trois premiers canaux, laissant le canal k inchangé. En bref, les API Aspose.PSD doivent effectuer l'interconversion des espaces de couleur RGB et CMJN pour les images CMJN et YCCK, et de telles transformations sont effectuées à l'aide de profils ICC qui sont essentiellement des tables de consultation décrivant les propriétés d'une couleur et aidant dans les transformations de couleur.


## **Profils ICC**
Le mécanisme de conversion ICC utilise des "Profils" qui mappent l'espace de couleur source vers les espaces de couleur CIELAB ou CIEXYZ indépendants du périphérique. Aspose.PSD peut convertir les données en espace couleur tel que requis en utilisant ces deux espaces de couleur avec des profils supplémentaires. Par conséquent, pour la conversion ICC, l'utilisateur doit fournir deux profils - un profil RGB pour accéder à l'espace couleur CIE interne et un profil CMJN pour obtenir les caractéristiques de couleur CMJN. Pour réaliser la conversion CMJN en RGB, il est nécessaire d'échanger les profils, c'est-à-dire; utiliser le profil CMJN comme profil source et le profil RGB comme profil de destination.
## **Conversion de couleur pour JPEG via profils ICC**
Les API Aspose.PSD cachent les détails, fournissant un mécanisme simple à utiliser pour spécifier des profils ICC via la classe [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). De plus, Aspose.PSD utilise les profils d'échantillonnage de SWOP, CMJN et sRGB intégrés dans son cœur, donc dans la plupart des cas d'utilisation courante, l'utilisateur n'a pas besoin de rechercher des profils spécifiques. Il y a un inconvénient à de telles corrections, c'est-à-dire que de telles conversions d'espace couleur sont irréversibles car nous ne pouvons pas nous attendre à obtenir la même couleur après une conversion de RGB en CMJN en RGB en raison d'espaces couleur incompatibles et de profils de couleur différents. L'extrait de code suivant illustre l'utilisation d'Aspose.PSD pour l'API .NET pour spécifier des profils de couleur RGB et CMJN pour une image JPEG en YCCK. Dans l'exemple ci-dessous, les profils de couleur RGB et CMJN sont modifiés et l'image est enregistrée dans l'espace de couleur YCCK. Veuillez noter que ces propriétés [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) et [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) fonctionneront pour modifier les données de pixels pour l'espace couleur YCCK. Tous les autres espaces couleur ne récupèrent pas les profils de couleur pour mettre à jour les données de couleur.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


Si aucun profil n'est défini, alors l'API Aspose.PSD pour .NET utilisera les profils par défaut à la place. L'exemple ci-dessous utilise les propriétés de profils de destination qui changent l'espace couleur de destination pour la plupart des images JPEG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}

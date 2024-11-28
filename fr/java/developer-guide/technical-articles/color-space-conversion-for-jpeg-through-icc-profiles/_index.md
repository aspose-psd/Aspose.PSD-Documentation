---
title: Conversion de l'espace colorimétrique pour JPEG via profils ICC
type: docs
weight: 50
url: /fr/java/conversion-de-lespace-colorimetrique-pour-jpeg-via-profils-icc/
---

## **Gestion des couleurs pour le format JPEG**

Cet article aborde l'utilisation des profils ICC pour effectuer la gestion de l'espace colorimétrique lors du traitement du format JPEG avec les API Aspose.PSD. L'espace colorimétrique interne du JPEG est YCbCr, cependant ce format peut également accueillir les espaces colorimétriques en niveaux de gris, RVB, CMJN et YCCK pour stocker les métadonnées de l'image. Les API Aspose.PSD fonctionnent principalement dans l'espace RVB, donc l'API doit effectuer des conversions d'espace colorimétrique de et vers cet espace pour gérer correctement les fichiers JPEG. Les conversions de niveaux de gris en RVB et de YCbCr en RVB peuvent être effectuées avec des transformations mathématiques, mais les espaces CMJN et YCCK ne peuvent pas être facilement convertis en espace RVB.

Les API Aspose.PSD doivent effectuer une transformation de couleurs directe de RVB en CMJN pour les images JPEG ayant un espace colorimétrique CMJN. D'autre part, les images ayant un espace colorimétrique YCCK nécessitent une transformation de couleurs de RVB en CMJN en YCCK, où la transformation de CMJN en YCCK utilise la conversion ITU-R BT.601 appliquée pour les trois premiers canaux, en laissant le canal k inchangé. En résumé, les API Aspose.PSD doivent effectuer l'interconversion des espaces colorimétriques RVB et CMJN pour les images CMJN et YCCK, et de telles transformations sont effectuées avec l'aide de profils ICC qui sont essentiellement des tables de recherche décrivant les propriétés d'une couleur et aidant dans les transformations de couleur.

## **Profils ICC**
Le mécanisme de conversion ICC utilise des "Profils" qui cartographient l'espace colorimétrique source vers les espaces colorimétriques CIELAB ou CIEXYZ indépendants de l'appareil. Aspose.PSD peut convertir les données en espace colorimétrique tel que requis en utilisant ces deux espaces colorimétriques avec des profils supplémentaires. Par conséquent, pour la conversion ICC, l'utilisateur doit fournir deux profils - un profil RVB pour atteindre l'espace colorimétrique interne CIE et un profil CMJN pour obtenir les caractéristiques de couleur CMJN. Afin d'effectuer la conversion de CMJN en RVB, il est nécessaire d'échanger les profils ; c'est-à-dire, utiliser le profil CMJN comme profil source et le profil RVB comme profil de destination.

## **Conversion de la couleur pour JPEG via profils ICC**
Les API Aspose.PSD masquent les détails, fournissant un mécanisme facile à utiliser pour spécifier les profils ICC via la classe JpegOptions. De plus, Aspose.PSD utilise les profils d'échantillonnage SWOP CMJN et sRGB intégrés dans son cœur, donc dans la plupart des cas d'utilisation courante, l'utilisateur n'a pas besoin de rechercher des profils spécifiques. Il y a un inconvénient à de telles corrections, c'est-à-dire que de telles conversions d'espace colorimétrique sont irréversibles car nous ne pouvons pas nous attendre à obtenir la même couleur après une conversion de RVB en CMJN en RVB en raison d'espaces colorimétriques incompatibles et de profils de couleur différents. L'extrait de code suivant démontre l'utilisation d'Aspose.PSD pour l'API Java pour spécifier des profils de couleur RVB et CMJN pour une image JPEG YCCK. Dans l'exemple ci-dessous, les profils de couleur RVB et CMJN sont modifiés et l'image est enregistrée dans l'espace colorimétrique YCCK. Veuillez noter que ces propriétés de profil de couleur RgbColorProfile et CmykColorProfile fonctionneront pour modifier les données de pixels pour l'espace colorimétrique YCCK. Tous les autres espaces colorimétriques ne récupèrent pas les profils de couleur pour mettre à jour les données de couleur.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}

Si aucun profil n'est défini, alors Aspose.PSD pour l'API Java utilisera les profils par défaut à la place. L'exemple ci-dessous utilise les propriétés de profils de destination qui modifient l'espace colorimétrique de destination pour la plupart des images Jpeg.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}

---
title: Calque d'ajustement noir et blanc
type: docs
weight: 30
url: /fr/java/layer-types/adjustment-layer/levels/
---

## Travailler avec la calque d'ajustement de niveaux dans Photoshop en Java

Dans cet article, nous apprendrons comment ajuster la gamme tonale et l'équilibre des couleurs d'une photo au format de fichier PSD de manière programmable en Java. Nous n'utilisons pas l'éditeur de photos Adobe® Photoshop® lui-même. Au lieu de cela, nous utilisons la bibliothèque Aspose.PSD for Java qui fonctionne de manière autonome pour manipuler le document Photoshop.

Bien qu'Aspose.PSD for Java supporte plus qu'assez d'outils pour éditer la photo tels que nous le souhaitons, **nous allons utiliser l'API du calque d'ajustement de niveaux** qui est l'une des façons les plus simples et rapides de réaliser le travail.

## Aperçu de l'API

L'implémentation actuelle (20.6 au moment de l'écriture) de l'API du calque d'ajustement de niveaux **prend en charge toutes les fonctionnalités de base des niveaux de Photoshop**, à savoir, ajuster les niveaux d'entrée et de sortie pour le canal composite (RGB) ainsi que pour chaque canal de couleur primaire (rouge, vert et bleu).

L'API du calque d'ajustement de niveaux est simple. La classe [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) est un point d'entrée pour l'ajustement de niveaux. Elle contient quelques méthodes pour accéder aux canaux de couleur : getMasterChannel et getChannel(int). Les deux méthodes renvoient [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) qui possède des propriétés correspondantes pour la manipulation des niveaux d'entrée et de sortie. La différence est que getMasterChannel sert à ajuster le canal de couleur composite (RGB) tandis que getChannel accède à un canal de couleur particulier (rouge, vert ou bleu) par son indice.

## Compatibilité avec les modes de couleur

Il convient d'ajouter que **le calque d'ajustement de niveaux est compatible avec la grande majorité des modes de couleur** selon les niveaux de Photoshop. Par conséquent, il est possible d'ajuster les niveaux pour les images en niveaux de gris (canal gris), RVB (RVB, canaux rouge, vert et bleu), CMJN (CMJN, canaux cyan, magenta, jaune et noir), Duotone (canal monochrome) et LAB (luminosité, a et b canaux).

## Ajuster la gamme tonale

En termes simples, la correction tonale s'applique à une image pour remapper les ombres et les reflets afin de mieux distribuer les mi-tons. En général, **cela rend l'image plus contrastée**si cela est fait correctement. Par exemple, prenons une photo d'un chien (b) et ajustons sa gamme tonale (a - la capture d'écran est prise à partir de la fenêtre des niveaux de Photoshop pour plus de clarté) pour rendre la photo plus contrastée (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Figure 1 du calque de niveaux](levels-adjustment-figure-1.png)|

Pour **ajuster la gamme tonale globale** d'une image, les niveaux d'entrée du canal principal doivent être définis :

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

Il est nécessaire de garder à l'esprit que les niveaux d'entrée doivent être compris entre 0 et 253 pour les ombres, de 9,99 à 0,01 pour les mi-tons et de 2 à 255 pour les reflets. La plage des niveaux de sortie doit être comprise entre 0 et 255.

Besoin de plus d'exemples ? Vous pouvez les trouver sur [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) et dans la [base de connaissances] (https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Conclusion

En conclusion, Aspose.PSD for Java dispose d'une API pratique et simple pour modifier la gamme tonale et l'équilibre des couleurs d'une image compatible avec presque tous les modes de couleur. L'API du calque d'ajustement de niveaux de la bibliothèque ressemble à celle des niveaux de Photoshop, il est donc facile de commencer même si vous n'avez jamais travaillé avec la bibliothèque auparavant.

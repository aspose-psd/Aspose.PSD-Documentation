---
title: Couche d'ajustement de l'équilibre des couleurs
type: docs
weight: 30
url: /fr/java/layer-types/adjustment-layer/color-balance/
---

# Travailler avec la couche d'ajustement de l'équilibre des couleurs de Photoshop en Java

Dans cet article, nous allons **ajuster l'équilibre des couleurs de l'image** au format de fichier PSD en Java. Nous utiliserons une bibliothèque spéciale appelée Aspose.PSD pour Java qui est une boîte à outils pour la manipulation de documents Photoshop.

Étant donné que la bibliothèque fonctionne avec le format de fichier PSD, elle contient presque [toutes les fonctionnalités](https://docs.aspose.com/psd/java/features/) disponibles dans l'éditeur Photoshop et la couche d'ajustement de l'équilibre des couleurs, qui est tout à fait adaptée à cette tâche, ne fait pas exception.

La couche d'ajustement de l'équilibre des couleurs permet de modifier l'équilibre entre les couleurs primaires (RVB) et soustractives (CMJ) pour les ombres, les tons moyens et les hautes lumières de manière simple et rapide.

## Ajuster l'équilibre des couleurs

Comme mentionné plus tôt, la couche d'ajustement de l'équilibre des couleurs dans Aspose.PSD pour Java est exactement ce qu'elle est, **un équilibreur entre les couleurs primaires et soustractives**. Cela signifie qu'il y a trois échelles pour chaque paire de couleurs (cyan/rouge, magenta/vert, jaune/bleu). L'intensité d'une couleur particulière dans la paire augmentera si la valeur se déplace vers elle et vice versa. De plus, ces trois paires sont inhérentes à chaque zone de la gamme de tons (ombres, tons moyens et hautes lumières) ce qui augmente la flexibilité de ce type d'ajustement.

Donc, appliquons cette connaissance en pratique. Par exemple, nous choisissons une photo rougeâtre du visage d'une femme (b). Le visage est tellement rougeâtre et nous allons corriger cela en **ajoutant une couche d'ajustement de l'équilibre des couleurs** pour diminuer le rouge et augmenter le cyan essentiellement (a) afin d'obtenir un visage qui paraît plus naturel (c). Encore une fois, il y a beaucoup de travail à faire avec cette image mais dans cet article c'est tout ce que nous allons faire.

![Exemple de couche d'ajustement de l'équilibre des couleurs](color-balance-adjustment-layer-example-figure-1.png) L'API de la couche d'ajustement de l'équilibre des couleurs a un design plat. Par conséquent, la [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), c'est tout ce dont vous avez besoin. Tout d'abord, préservez la luminosité car elle est désactivée par défaut. Ensuite, ajoutez un peu de vert et un peu plus de jaune pour les ombres en utilisant les méthodes correspondantes (dont les noms se composent du nom de la zone de la gamme de tons particulière et des noms des couleurs de la paire de couleurs), puis ajoutez plus de cyan et un peu de bleu pour les tons moyens, et enfin ajoutez plus de cyan en plus de peu de magenta et de bleu :

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Maintenant, nous avons obtenu l'image que nous voulions! C'est si simple, n'est-ce pas?

Notez que _la valeur de chaque paire de couleurs doit être comprise entre -100 et 100_ : des valeurs négatives pour les couleurs soustractives et positives pour les couleurs primaires respectivement, tout comme dans l'éditeur Photoshop.

Consultez notre référence API pour en savoir plus sur les détails techniques de la [couche d'ajustement de l'équilibre des couleurs](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Conclusion

Dans cet article, nous avons examiné comment ajuster l'équilibre des couleurs de l'image de manière programmative en Java en utilisant la bibliothèque Aspose.PSD pour Java. La bibliothèque contient une API entièrement fonctionnelle pour travailler avec les couches d'ajustement de l'équilibre des couleurs dans les documents Photoshop.

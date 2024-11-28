---
title: Calque d'ajustement du mélangeur de canaux
type: docs
weight: 30
url: /fr/java/layer-types/adjustment-layer/channel-mixer/
---

# Travailler avec le calque d'ajustement du mélangeur de canaux de Photoshop en Java

Aujourd'hui, nous allons voir comment mélanger les couleurs des canaux dans les documents Photoshop de manière programmatique en Java. Étant donné que l'éditeur Photoshop ne prend pas en charge le scripting Java, nous utiliserons une bibliothèque de manipulation de format de fichier PSD spéciale appelée Aspose.PSD pour Java.

La bibliothèque contient une **API pour travailler avec les canaux de couleur**. Il existe plusieurs façons de mélanger les couleurs, mais dans cet article, nous nous concentrerons sur le calque d'ajustement du mélangeur de canaux.

L'API du calque d'ajustement du mélangeur de canaux **permet de jouer avec les canaux de couleur** pour créer des images colorées ou des effets de couleur créatifs différents, voire même convertir l'image en noir et blanc. Ensuite, nous verrons comment appliquer un calque d'ajustement du mélangeur de canaux à un document Photoshop existant en utilisant Aspose.PSD pour Java, mais d'abord, nous devons parler des fonctionnalités générales de l'API.

## Aperçu de l'API

Il n'y a rien de spécial dans la création d'un calque d'ajustement du mélangeur de canaux. Il peut être ajouté via [la méthode d'usine par défaut](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) qui renvoie une instance de la classe ChannelMixerLayer. Cette classe contient des fonctionnalités générales comme l'option Monochrome et une méthode pour obtenir un canal de sortie. Un canal de sortie particulier peut être de l'un des deux types : [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) ou [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Le type de [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) dépend du [mode de couleur](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) de l'image.

## Rendre l'image monochrome

Maintenant, examinons un exemple d'application du calque d'ajustement du mélangeur de canaux à un document Photoshop existant. Comme ce type de calque d'ajustement ne prend pas encore en charge les préréglages, nous allons **recréer le préréglage (a) Noir & Blanc Infrarouge (RGB) de Photoshop**. Le préréglage sera appliqué à l'image d'un arbre en fleurs (b). En résultat, nous souhaitons obtenir l'effet de la photographie infrarouge (c).

![Example du calque d'ajustement du mélangeur de canaux](channel-mixer-adjustment-psd-layer-figure-1.png) Pour recréer le préréglage (a) Noir & Blanc Infrarouge (RGB) de Photoshop, il est nécessaire d'activer le drapeau monochrome et de définir des valeurs brutes appropriées pour chaque couleur (rouge, vert et bleu) du canal de sortie Gris :

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

L'image doit être en mode couleur RVB pour que le code fonctionne (en raison de la conversion en la classe RgbMixerChannel). Le mode couleur CMJN est également pris en charge, mais uniquement pour les images avec le mode couleur correspondant.

N'oubliez pas que la valeur de chaque couleur ainsi que la propriété Constant doit être comprise entre -200 et 200.

## Conclusion

Dans cet article, nous avons examiné comment travailler avec l'API du mélangeur de canaux d'Aspose.PSD pour Java pour ajuster les couleurs dans les canaux de couleur ainsi que convertir l'image en noir et blanc.

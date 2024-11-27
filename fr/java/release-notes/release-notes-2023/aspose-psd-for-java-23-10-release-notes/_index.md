---
title: Aspose.PSD pour Java 23.10 - Notes de version
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-23-10-notes-de-version/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.10/) {{% /alert %}}

| **Clé**        | **Résumé**                                                                             | **Catégorie** |
|:---------------|:---------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-538    | Prise en charge de la direction du texte vertical                                       |   Fonctionnalité|
| PSDJAVA-542    | Utiliser les paramètres de contour à partir de la ressource vstk dans le rendu du contour de forme| Fonctionnalité|
| PSDJAVA-540    | Implémenter le rendu de la zone interne des formes de contour                             | Fonctionnalité|
| PSDJAVA-541    | Ne pas redessiner le calque de forme s'il n'a pas été modifié                           | Fonctionnalité|
| PSDJAVA-545    | [Format AI] Ajouter la prise en charge de la lecture de l'en-tête des fichiers AI basés sur PDF| Fonctionnalité|
| PSDJAVA-546    | Différentes façons de définir la résolution du fichier Psd ne fonctionnent pas          |      Problème    |
| PSDJAVA-547    | FontSettings.SetFontsFolders ne fonctionne pas ou Aspose.PSD utilise une police incorrecte |      Problème     |
| PSDJAVA-548    | Régression. Correction de l'exception de référence nulle déclenchée sur PsdImage.Save lors de la présence d'un calque de forme |      Problème     |

## **Changements d'API publics**
# **APIs ajoutées :**

- M:com.aspose.psd.FontSettings.getGetSystemAlternativeFont
- M:com.aspose.psd.FontSettings.setGetSystemAlternativeFont(boolean)
- M:com.aspose.psd.Graphics.getPaintableImageOptions
- M:com.aspose.psd.Graphics.setPaintableImageOptions(com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.getAutoAdjustPalette
- M:com.aspose.psd.Image.getFileFormat(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.extensions.RegionExtensions.#ctor
- M:com.aspose.psd.fileformats.psd.PsdImage.setResolution(double,double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.getStroke
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.setStroke(com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings
...

---
title: Notes de publication d'Aspose.PSD pour Java 20.2
type: docs
weight: 20
url: /fr/java/notes-de-version-daspose-psd-pour-java-20-2/
---

{{% alert color="primary" %}} Cette page contient les notes de publication pour [Aspose.PSD for Java 20.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDJAVA-96|Amélioration de la capacité de rendre du texte de différentes couleurs dans la couche de texte|Fonctionnalité|
|PSDJAVA-97|Prise en charge de la ressource clbl (La ressource de couche contient des informations sur les éléments de découpe Blend)|Fonctionnalité|
|PSDJAVA-100|Prise en charge de la ressource blwh (La ressource contient les données de la couche d'ajustement Noir et Blanc)|Fonctionnalité|
|PSDJAVA-101|Capacité d'exporter un groupe de calques en Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Fonctionnalité|
|PSDJAVA-105|Prise en charge de la ressource lspf (Contient des paramètres sur le paramétrage des calques protégés)|Fonctionnalité|
|PSDJAVA-106|Prise en charge de la ressource infx (Contient des données sur le mélange des éléments intérieurs)|Fonctionnalité|
|PSDJAVA-99|Refonte de PsdImage et Layer pour changer le comportement de transformation (Redimensionnement/rotation/recadrage corrects pour les masques de calque si on transforme un calque séparément)|Amélioration|
|PSDJAVA-98|Dans certains paramètres de globalisation, une image raster AI ne peut pas être ouverte|Correctif|
|PSDJAVA-102|Après avoir effectué l'opération FlipRotate sur un calque, l'image PSD devient illisible|Correctif|
|PSDJAVA-103|System.ArgumentException lors du chargement du fichier PSD|Correctif|
|PSDJAVA-104|Après avoir utilisé une méthode de transformation pour un calque uniquement, le calque enregistré a des limites incorrectes ou un masque|Correctif|

# **Modifications de l'API publique**
# **Cette API est temporairement désactivée et sera activée dans la prochaine version:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.saveData(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)

` `**Veuillez utiliser la version 19.4 en attendant si vous avez une dépendance appropriée.**
# **APIs ajoutées:**
- M:com.aspose.psd.Color.op_Equality(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.Color.op_Inequality(com.aspose.psd.Color,com.aspose.psd.Color)
- ...

**Exemples d'utilisation:**
**PSDJAVA-96. Amélioration de la capacité de rendre du texte de différentes couleurs dans la couche de texte**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-97. Prise en charge de la ressource clbl (La ressource de calque contient des informations sur les éléments de découpe Blend)**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-100. Prise en charge de la ressource blwh (La ressource contient les données de la couche d'ajustement Noir et Blanc)**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-101. Capacité d'exporter un groupe de calques en Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-105. Prise en charge de la ressource lspf (Contient des paramètres sur le paramétrage des calques protégés)**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-106. Prise en charge de la ressource infx (Contient des données sur le mélange des éléments intérieurs)**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-99. Refonte de PsdImage et Layer pour changer le comportement de transformation (Redimensionnement/rotation/recadrage corrects pour les masques de calque si on transforme un calque séparément)**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-98. Dans certains paramètres de globalisation, une image raster AI ne peut pas être ouverte**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-102. Après avoir effectué l'opération FlipRotate sur un calque, l'image PSD devient illisible**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-103. System.ArgumentException lors du chargement du fichier PSD**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-104. Après avoir utilisé une méthode de transformation pour un calque uniquement, le calque enregistré a des limites incorrectes ou un masque**

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}# **Modifications de l'API publique (suite)**
# **Cette API est temporairement désactivée et sera activée dans la prochaine version:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.saveData(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)

` `**Veuillez utiliser la version 19.4 en attendant si vous avez une dépendance appropriée.**
# **APIs ajoutées (suite):**
- M:com.aspose.psd.Color.op_Equality(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.Color.op_Inequality(com.aspose.psd.Color,com.aspose.psd.Color)
- ...

**Exemples d'utilisation (suite):**
**PSDJAVA-96. Amélioration de la capacité de rendre du texte de différentes couleurs dans la couche de texte** (suite)

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-97. Prise en charge de la ressource clbl (La ressource de calque contient des informations sur les éléments de découpe Blend)** (suite)

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-100. Prise en charge de la ressource blwh (La ressource contient les données de la couche d'ajustement Noir et Blanc)** (suite)

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-101. Capacité d'exporter un groupe de calques en Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf** (suite)

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-105. Prise en charge de la ressource lspf (Contient des paramètres sur le paramétrage des calques protégés)** (suite)

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}

**PSDJAVA-106. Prise en charge de la ressource infx (Contient des données sur le mélange des éléments intérieurs)** (suite)

{{< highlight java >}}

// Code de l'exemple...

{{< /highlight >}}
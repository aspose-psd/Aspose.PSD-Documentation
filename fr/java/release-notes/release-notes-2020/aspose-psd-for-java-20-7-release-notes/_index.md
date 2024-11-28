---
title: Notes de version Aspose.PSD pour Java 20.7
type: docs
weight: 50
url: /fr/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDJAVA-231|Prise en charge de l'ajout de l'effet de contour en cours d'exécution|Fonctionnalité|
|PSDJAVA-249|Prise en charge des ressources lnk2 / lnk3 (Ressources de la couche d'objet intelligent)|Fonctionnalité|
|PSDJAVA-247|Modification du message d'exception lors de la tentative d'ouverture de formats non pris en charge en tant qu'image|Amélioration|
|PSDJAVA-235|Si nous enregistrons un fichier PSD après la création d'un nouveau groupe de calques, nous obtenons un avertissement de Photoshop lors de l'ouverture du fichier.|Bogue|
|PSDJAVA-236|Échec de l'enregistrement de LayerMask|Bogue|
|PSDJAVA-237|Le masque d'écrêtage ne s'applique pas au dossier|Bogue|
|PSDJAVA-238|Impossible d'ouvrir le fichier avec Aspose.PSD pour Java|Bogue|
|PSDJAVA-239|Exception d'échec de l'enregistrement de l'image lors de la conversion PSD en PDF|Bogue|
|PSDJAVA-240|L'opération de rognage rend le chemin de détourage invalide dans l'image PSD|Bogue|
|PSDJAVA-241|Exception NullReference lors de l'essai d'enregistrement d'un fichier PSD spécifique avec l'effet d'ombre|Bogue|
|PSDJAVA-243|Aspose.PSD renvoie true sur Image.CanLoad(pdfStream)|Bogue|
|PSDJAVA-244|Échec du rendu des calques dans le PNG généré|Bogue|
|PSDJAVA-245|Exception lors de l'accès aux TextData|Bogue|
|PSDJAVA-246|ImageSaveException lors de l'enregistrement du PSD|Bogue|
# **Changements d'API publics**
# **APIs ajoutées :**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData
- T:com.aspose.psd.fileformats.psd.resources.WorkingPathResource
## **APIs supprimées :**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
# **Exemples d'utilisation:**

**PSDJAVA-231. Prise en charge de l'ajout de l'effet de contour en cours d'exécution**
{{< highlight java >}}
// Cet exemple montre comment ajouter un effet de contour (bordure) à des calques existants d'un fichier PSD en Java.
// Il existe trois types de contour : couleur, dégradé et motif. Chacun des types a
// trois façons (positions) d'afficher la bordure : intérieur, au centre et à l'extérieur.
// Cet exemple illustre l'utilisation de tous ces cas.
 
String srcPsdPath = "StrokeEffectsSource.psd";
String dstPngPath = "output.png";
 
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath, psdLoadOptions);
try
{
    StrokeEffect strokeEffect;
    IColorFillSettings colorFillSettings;
    IGradientFillSettings gradientFillSettings;
    IPatternFillSettings patternFillSettings;
 
    // 1. Ajoute un remplissage de couleur, en position Intérieure
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 2. Ajoute un remplissage de couleur, en position Extérieure
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 3. Ajoute un remplissage de couleur, en position Centrale
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // ... (Le reste de l'exemple a été tronqué)
 
    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-249. Prise en charge des ressources lnk2 / lnk3 (Ressources de la couche d'objet intelligent)**
{{< highlight java >}}
// Cet exemple montre comment travailler avec les ressources d'objet intelligent (principalement Lnk2Resource).
// Le programme charge plusieurs documents Photoshop et exporte leurs objets intelligents vers
// des formats de fichiers raster. De plus, le code démontre l'utilisation des méthodes publiques de Lnk2Resource.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-247. Modification du message d'exception lors de la tentative d'ouverture de formats non pris en charge en tant qu'image**
{{< highlight java >}}
// Cet exemple montre qu'une exception avec un nouveau message plus descriptif est levée lors du chargement
// d'images raster de la manière qui n'est pas prise en charge (les images raster ne peuvent être chargées que comme calques).
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-235. Si nous enregistrons un fichier PSD après la création d'un nouveau groupe de calques, nous obtenons un avertissement de Photoshop lors de l'ouverture du fichier.**
{{< highlight java >}}
// Cet exemple montre qu'il n'y a pas d'exception lors de l'enregistrement d'un fichier PSD généré
// contenant des groupes de calques internes.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-236. Échec de l'enregistrement de LayerMask**
{{< highlight java >}}
// Cet exemple démontre la possibilité de sauvegarder et de rendre des masques de calque pour
// des groupes de calques lorsque des calques sont ajoutés à partir d'une autre image PSD.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-237. Le masque d'écrêtage ne s'applique pas au dossier**
{{< highlight java >}}
// Cet exemple vérifie que les masques d'écrêtage liés aux groupes de calques sont exportés
// correctement pour un fichier PSD prédéfini.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-238. Impossible d'ouvrir le fichier avec Aspose.PSD pour Java**
{{< highlight java >}}
// Cet exemple charge et enregistre un fichier PSD particulier sans générer d'exception.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-239. Exception d'échec de l'enregistrement de l'image lors de la conversion PSD en PDF**
{{< highlight java >}}
// Cet exemple exporte un fichier PSD particulier au format de fichier PDF avec le mode lecture seule activé
// ou non pour s'assurer qu'aucune erreur n'est lancée et que le fichier de sortie est correct.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-240. L'opération de rognage rend le chemin de détourage invalide dans l'image PSD**
{{< highlight java >}}
// Cet exemple démontre que l'opération de rognage ne rend pas un chemin de détourage invalide.
// Le programme charge un fichier PSD particulier puis le rogne et l'enregistre. Ensuite, le programme
// ouvre le fichier enregistré et vérifie que l'opération de rognage s'est déroulée comme prévu.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-241. Exception NullReference lors de l'essai d'enregistrement d'un fichier PSD spécifique avec l'effet d'ombre**
{{< highlight java >}}
// Cet exemple démontre qu'il n'y a pas d'exception lors de l'enregistrement d'un fichier PSD spécifique.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-243. Aspose.PSD renvoie true sur Image.CanLoad(pdfStream)**
{{< highlight java >}}
// Cet exemple vérifie que la propriété Image.canLoad a été corrigée et renvoie "false" pour
// les fichiers non pris en charge. Le programme parcourt simplement une liste de fichiers prédéfinis pris en charge et non pris en charge.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-244. Échec du rendu des calques dans le PNG généré**
{{< highlight java >}}
// Cet exemple vérifie qu'un fichier PSD particulier est exporté correctement après aplatissement.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-245. Exception lors de l'accès aux TextData**
{{< highlight java >}}
// Cet exemple vérifie qu'il n'y a pas d'exception lors de l'accès à des données textuelles particulières.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}

**PSDJAVA-246. ImageSaveException lors de l'enregistrement du PSD**
{{< highlight java >}}
// Cet exemple vérifie qu'il n'y a pas d'exception lors de l'enregistrement d'un fichier PSD particulier.
 
// ... (L'exemple entier a été tronqué)

{{< /highlight >}}**PSDJAVA-244. Échec du rendu des calques dans le PNG généré**
{{< highlight java >}}
// Cet exemple vérifie qu'un fichier PSD particulier est exporté correctement après aplatissement.
 
String srcPsdPath = "sccnn_2020053000075715XUHD.psd";
String dstPngPath = "sccnn_2020053000075715XUHD_output.png";
 
PngOptions pngOptions = new PngOptions();
pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath);
try
{
    // Fusionner tous les calques et exporter le calque résultant en tant qu'image
    psdImage.flattenImage();
    psdImage.save(dstPngPath, pngOptions);
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-245. Exception lors de l'accès aux TextData**
{{< highlight java >}}
// Cet exemple vérifie qu'il n'y a pas d'exception lors de l'accès à des données textuelles particulières.
 
String srcPsdPath = "A.psd";
 
PsdImage image = (PsdImage)Image.load(srcPsdPath);
try
{
    // Accéder et modifier les données textuelles sans exception
    TextLayer textLayer = (TextLayer)image.getLayers()[1];
    String text = textLayer.getText(); // pas d'exception ici...
    IText textData = textLayer.getTextData(); // pas d'exception ici...
    textLayer.updateText("abc");  // pas d'exception ici...
}
finally
{
    image.dispose();
}
{{< /highlight >}}

**PSDJAVA-246. ImageSaveException lors de l'enregistrement du PSD**
{{< highlight java >}}
// Cet exemple vérifie qu'il n'y a pas d'exception lors de l'enregistrement d'un fichier PSD particulier.
 
String srcPsdPath = "snowflake-ui-kit.psd";
String dstPsdPath = "snowflake-ui-kit-output.psd";
 
PsdImage image = (PsdImage)Image.load(srcPsdPath);
try
{
    image.save(dstPsdPath, new PsdOptions(image));
}
finally
{
    image.dispose();
}
{{< /highlight >}}
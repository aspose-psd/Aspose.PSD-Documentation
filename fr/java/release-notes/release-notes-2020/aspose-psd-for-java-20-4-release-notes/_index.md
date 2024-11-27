---
title: Aspose.PSD pour Java 20.4 - Notes de version
type: docs
weight: 30
url: /fr/java/aspose-psd-pour-java-20-4-notes-de-version/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDJAVA-156|Prise en charge de la ressource 'Données d'origine vectorielle'|Fonctionnalité|
|PSDJAVA-171|Prise en charge de lclrResource (Paramètres de couleur de la feuille)|Fonctionnalité|
|PSDJAVA-157|Prise en charge des propriétés des données LengthRecord. (Opérations de chemin (opérations booléennes), index de la forme dans la couche, nombre d'enregistrements de nœuds de bézier)|Fonctionnalité|
|PSDJAVA-158|Support de la ressource 'Couleur de fond' de la section d'image n°1010 |Fonctionnalité|
|PSDJAVA-161|Ajout de couches de remplissage à l'exécution|Fonctionnalité|
|PSDJAVA-168|Prise en charge de la ressource 'Information de bordure' de la section d'image n°1009|Fonctionnalité|
|PSDJAVA-169|Prise en charge des couches dans les fichiers au format AI|Fonctionnalité|
|PSDJAVA-163|Prise en charge de la lecture et de la modification de l'effet de calque de superposition de dégradé|Fonctionnalité|
|PSDJAVA-164|Rendu de l'effet de calque de superposition de dégradé|Fonctionnalité|
|PSDJAVA-149|Erreur Aspose.PSD pour Java lors de l'obtention de la propriété textData.items de la couche de texte|Erreur|
|PSDJAVA-166|Correction de l'enregistrement de l'image PSD avec le mode de couleur en niveaux de gris et 16 bits par canal vers le format PSD en niveaux de gris|Erreur|
|PSDJAVA-167|Correction de l'enregistrement de l'image PSD avec le mode de couleur en niveaux de gris et 16 bits par canal vers le format PNG|Erreur|
|PSDJAVA-159|Les modifications de la propriété GradientOverlayEffect.BlendMode ne sont pas affichées dans Photoshop|Erreur|
# **Modifications de l'API Publique**
# **APIs ajoutées:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(flottant)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(flottant,flottant)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **APIs Supprimées:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **Exemples d'utilisation:**

**PSDJAVA-156. Prise en charge de la ressource "Données d'origine vectorielle"**

{{< highlight java >}}

 /*

Un exemple de lecture et de modification d'une ressource de données d'origine vectorielle.

*/

// Conservez les méthodes dans la portée locale pour plus de simplicité

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("Ressource Vogk non trouvée.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Chargez un fichier PSD contenant une ressource VOGK prédéfinie

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Trouvez d'abord VogkResource dans les ressources de la couche prédéfinie

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Vérifiez les propriétés des ressources prédéfinies

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("Ressource Vogk mal lue.");

    }

    // Modifiez certaines propriétés de la ressource Vogk

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Enregistrez une copie modifiée du fichier PSD chargé sur le chemin

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Prise en charge de lclrResource (Paramètres de couleur de la feuille)**

{{< highlight java >}}

 /*

Un exemple d'utilisation de la couleur de la feuille de calque pour mettre en évidence visuellement les calques. Par exemple, vous pouvez

mettre à jour certains calques dans PSD, puis mettre en surbrillance par couleur le calque que vous souhaitez attirer

attention.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // La ressource lcrl est toujours présente dans la liste des ressources du fichier psd.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("La couleur de la feuille a été mal lue");

                }

                // Inversion des couleurs de la feuille de style. Configuration de la mise en surbrillance de la couleur de calque.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// Dans le fichier, les couleurs de la mise en surbrillance des calques sont dans cet ordre

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Rouge,

        SheetColorHighlightEnum.Orange,

        SheetColorHighlightEnum.Jaune,

        SheetColorHighlightEnum.Vert,

        SheetColorHighlightEnum.Bleu,

        SheetColorHighlightEnum.Violet,

        SheetColorHighlightEnum.Gris,

        SheetColorHighlightEnum.SansCouleur

};

// Chargez un fichier PSD contenant une ressource LclrResource prédéfinie

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Chargez un fichier PSD nouvellement enregistré

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Inversion des couleurs

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Prise en charge des propriétés des données LengthRecord. (Opérations de chemin (opérations booléennes), index de la forme dans la couche, nombre d'enregistrements de nœuds de bézier)**

{{< highlight java >}}

 /*

Un exemple de modification des opérations de chemin lors du travail avec des formes. Le programme lit

des enregistrements de tracé vectoriel prédéfinis (LengthRecord) et modifie leurs opérations de chemin, puis enregistre

une copie modifiée du document sous forme de nouveau fichier PSD.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Chargez un fichier PSD contenant une ressource vsms prédéfinie

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Trouvez d'abord VsmsResource dans les ressources de la couche prédéfinie

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // Changez la manière dont les formes sont combinées

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Enregistrez une copie modifiée du fichier PSD chargé sur le chemin

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();
    
}

{{< /highlight >}}

**PSDJAVA-158. Support de la ressource 'Couleur de fond' de la section d'image n°1010**

{{< highlight java >}}

 /*

Un exemple de lecture et de modification d'une ressource de couleur de fond.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Chargez un fichier PSD contenant une ressource de couleur de fond prédéfinie

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("Ressource de couleur de fond non trouvée");

    }

    // Mettez à jour la couleur de la ressource de couleur de fond

    backgroundColorResource.setColor(Color.getDarkRed());

    // Enregistrez une copie modifiée du fichier PSD chargé sur le chemin

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Ajout de couches de remplissage à l'exécution**

{{< highlight java >}}

 /*

Un exemple d'ajout de couches de remplissage de différents types à un document Photoshop.

*/

String outPsdFilePath = "output.psd";

// Créez un document Photoshop avec un canevas vide

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // Ajoutez des couches de remplissage de différents types à PSD

    FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);

    colorFillLayer.setDisplayName("Couche de remplissage de couleur");

    psdImage.addLayer(colorFillLayer);

    FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);

    gradientFillLayer.setDisplayName("Couche de remplissage de dégradé");

    psdImage.addLayer(gradientFillLayer);

    FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);

    patternFillLayer.setDisplayName("Couche de remplissage de motif");

    patternFillLayer.setOpacity((byte)50);

    psdImage.addLayer(patternFillLayer);

    // Enregistrez une copie modifiée du fichier PSD chargé sur le chemin

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-168. Support de la ressource 'Information de bordure' de la section d'image n°1009**

{{< highlight java >}}

 /*

Un exemple de lecture, de modification et d'enregistrement d'un fichier PSD contenant une information de bordure

ressource.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Chargez un
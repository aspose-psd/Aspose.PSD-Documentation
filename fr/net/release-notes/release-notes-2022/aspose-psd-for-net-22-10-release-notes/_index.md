---
title: Notes de publication d'Aspose.PSD for .NET 22.10
type: docs
weight: 30
url: /fr/net/aspose-psd-for-net-22-10-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD for .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Cette version présente une régression dans le cas des exportations sur 16 bits, nous vous recommandons donc de faire preuve de prudence lors de l'utilisation de cette fonctionnalité dans cette version.
Merci de ne pas mettre à jour Aspose.PSD vers la version 22.9-22.10 si le traitement d'images sur 16 bits est votre fonctionnalité principale.

Nous travaillons sur des solutions à ces problèmes.

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-1287|Supprimer les propriétés obsolètes dans Lfx2Resource|Amélioration|
|PSDNET-1071|Aspose.PSD ne peut pas ouvrir les fichiers PSD (RGB/16 bits) avec la compression ZipWithoutPrediction|Bogue|
|PSDNET-1257|Les effets de la chronologie disparaissent et s'affichent de manière étrange (dans Photoshop)|Bogue|
|PSDNET-1278|La transparence ne fonctionne pas pour l'effet de contour avec une position intérieure|Bogue|
|PSDNET-1279|Régression : Erreur à l'ouverture du fichier PSD|Bogue|
|PSDNET-1284|La mise à jour du texte échoue avec certains symboles asiatiques. Erreur d'analyse du symbole spécifique|Bogue|
|PSDNET-1291|La mise à jour du texte échoue avec certains symboles asiatiques. Erreur lors du rendu du symbole spécifique|Bogue|
|PSDNET-1292|Erreur à l'ouverture du fichier exporté par Photoshop après avoir enregistré des symboles asiatiques spécifiques|Bogue|


## **Changements de l'API publique**
# **APIs ajoutées:**
- Aucune


# **APIs supprimées:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Exemples d'utilisation:**

**PSDNET-1071. Aspose.PSD ne peut pas ouvrir les fichiers PSD (RGB/16 bits) avec la compression ZipWithoutPrediction**

{{< highlight csharp >}}
chaîne src = "237708.psd";
chaîne sortie = "out_237708.psd";

utilisation(var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Les effets de la chronologie disparaissent et s'affichent de manière étrange (dans Photoshop)**

{{< highlight csharp >}}
chaîne fichierSource = "clearFile.psd";
chaîne fichierSortie = "sortie_pas_clair.psd";

utilisation(var psdImage = (PsdImage)Image.Load(fichierSource))
{
    // Créer une chronologie avec quelques images clés.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    Liste<Frame> frames = nouvelle Liste<Frame>(timeLine.Frames);
    pour(int i = 0; i < 3; i++)
    {
        frames.Ajouter(nouveau Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. La transparence ne fonctionne pas pour l'effet de contour avec une position intérieure**

{{< highlight csharp >}}
chaîne fichierSource = "psdnet1278.psd";
chaîne sortie = "out_1278.png";

utilisation(var image = (PsdImage)Image.Load(fichierSource, nouvelle PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(sortie, nouvelle PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Régression : Erreur à l'ouverture du fichier PSD**

{{< highlight csharp >}}
chaîne fichierSource = "AllTypesLayerPsd.psd";
chaîne sortiePsd = "out_1279.psd";

utilisation(var image = (PsdImage) Image.Load(fichierSource))
{
    image.Save(sortiePsd);
}
{{< /highlight >}}

**PSDNET-1284. La mise à jour du texte échoue avec certains symboles asiatiques. Erreur d'analyse du symbole spécifique**

{{< highlight csharp >}}
chaîne testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // Sélectionnez le symbole problématique

chaîne fichierSrc = "TestFileForAsianCharsBig.psd";
chaîne sortie = "output.psd";

utilisation(var image = (PsdImage)Image.Load(fichierSrc))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(sortie);
}
{{< /highlight >}}

**PSDNET-1287. Supprimer les propriétés obsolètes dans Lfx2Resource**

{{< highlight csharp >}}
chaîne src = "fichierAvecEffets.psd";
chaîne sortie = "sortie.psd";

utilisation(var psdImage = (PsdImage)Image.Load(src, nouvelle PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Mettre à jour l'option BlendMode de l'effet
    effect.BlendMode = BlendMode.Darken;

    // Mettre à jour l'option Opacité de l'effet
    effect.Opacity = 128; // 50%

    // Mettre à jour la couleur de remplissage de l'effet de contour
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(sortie);
}
{{< /highlight >}}

**PSDNET-1291. La mise à jour du texte échoue avec certains symboles asiatiques. Erreur lors du rendu du symbole spécifique**

{{< highlight csharp >}}
chaîne testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // Sélectionnez les symboles problématiques

chaîne fichierSrc = "TestFileForAsianCharsBig 2.psd";
chaîne sortie = "output.psd";

utilisation(var image = (PsdImage)Image.Load(fichierSrc))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(sortie);
}
{{< /highlight >}}

**PSDNET-1292. Erreur à l'ouverture du fichier exporté par Photoshop après l'enregistrement de symboles asiatiques spécifiques**

{{< highlight csharp >}}
chaîne testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

chaîne fichierSrc = "TestFileForAsianCharsBig 2.psd";
chaîne fichierSortie = "output.psd";

utilisation(var image = (PsdImage)Image.Load(fichierSrc))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(fichierSortie);
}
{{< /highlight >}}

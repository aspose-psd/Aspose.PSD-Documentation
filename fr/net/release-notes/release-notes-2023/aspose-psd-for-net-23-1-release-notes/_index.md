---
title: Notes de version Aspose.PSD pour .NET 23.1
type: docs
weight: 120
url: /fr/net/aspose-psd-pour-net-23-1-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-401|Support de vstkResource|Fonctionnalité|
|PSDNET-1346|Ajout de la propriété BaselineDirection/IsStandardVerticalRomanAlignmentEnabled modifiable à l'interface IText|Fonctionnalité|
|PSDNET-181|Conversion incorrecte d'un PSD en JPEG|Bogue|
|PSDNET-958|Échec de la conversion PSB en PDF pour les fichiers volumineux|Bogue|
|PSDNET-1171|Ajout du traitement du masque de découpe à la couche d'ajustement|Bogue|
|PSDNET-1252|Après le redimensionnement de l'image entière puis après le redimensionnement de la couche spécifique Aspose.PSD lance une exception lors de la sauvegarde de la couche|Bogue|

## **Modifications de l'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleMiterLimit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineJoinType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleScaleLock
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleStrokeAdjust
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleBlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleOpacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleResolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleContent
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Levels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.TypeToolKey

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**

**PSDNET-181. Conversion incorrecte d'un PSD en JPEG**

{{< highlight csharp >}}
string fileSrc = "helicopter.psd";
string imageSortieJpg = "sortie.jpg";

using (var imagePsd = (PsdImage)Image.Load(fileSrc))
{
    imagePsd.Save(imageSortieJpg, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. Support de vstkResource**

{{< highlight csharp >}}
string fichierSrc = "StrokeShapeTest1.psd";
string fichierDst = "StrokeShapeTest2.psd";

using (PsdImage image = (PsdImage)Image.Load(fichierSrc))
{
    Layer calque = image.Layers[1];
    foreach (LayerResource ressource in calque.Resources)
    {
        if (ressource is VstkResource)
        {
            VstkResource ressourceVstk = (VstkResource)ressource;
            ressourceVstk.StrokeStyleLineAlignment = StrokePosition.Outside;
            ressourceVstk.StrokeStyleLineWidth = 20;
        }
    }

    image.Save(fichierDst);
}
{{< /highlight >}}

**PSDNET-958. Échec de la conversion PSB en PDF pour les fichiers volumineux**

{{< highlight csharp >}}
string cheminEntree = "SteveKohli-CarTOP.psb";
string cheminSortie ="sortie.pdf";

using (var image = Image.Load(cheminEntree))
{
    image.Save(cheminSortie, new PdfOptions());
}
{{< /highlight >}}

**PSDNET-1171. Ajout du traitement du masque de découpe à la couche d'ajustement**

{{< highlight csharp >}}
string fichierSrc = "helicopter_part.psd";
string imageSortieJpg = "sortie.jpg";

using (var imagePsd = (PsdImage)Image.Load(fichierSrc))
{
    imagePsd.Save(imageSortieJpg, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1252. Après le redimensionnement de l'image entière puis après le redimensionnement de la couche spécifique Aspose.PSD lance une exception lors de la sauvegarde de la couche**

{{< highlight csharp >}}
string fichierSource = "source.psd";
string imgFichier1 = "img1.png";
string imgFichier2 = "img2.png";

var optionsChargement = new PsdLoadOptions()
{
    ReadOnlyMode = false,
    LoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(fichierSource, optionsChargement))
{
    // Tout d'abord, nous redimensionnons l'image entière
    image.Resize(110, 90);
    var calques = image.Layers;

    var calqueOk = calques[0];
    calqueOk.Resize(100, 80);

    var calqueException = calques[1];
    calqueException.Resize(100, 80);

    // Ici tout ira bien
    calqueOk.Save(imgFichier1, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    // Maintenant tout ira bien ici
    calqueException.Save(imgFichier2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });                
}
{{< /highlight >}}

**PSDNET-1346. Ajout de la propriété BaselineDirection/IsStandardVerticalRomanAlignmentEnabled modifiable à l'interface IText**

{{< highlight csharp >}}
// Le code suivant démontre la possibilité de modifier la nouvelle propriété IsStandardVerticalRomanAlignmentEnabled.
// Cela n'affecte pas le rendu pour l'instant, mais vous permet uniquement de modifier la valeur de la propriété.

string fichierSrc = "1346test.psd";
string fichierSortie = "sortie_1346test.psd";

using (var image = (PsdImage)Image.Load(fichierSrc))
{
    var calqueTexte = image.Layers[1] as TextLayer;
    var textePortion = calqueTexte.TextData.Items[0];
    if (textePortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Lecture correcte
    }
    else
    {
        throw new Exception("Lecture incorrecte de la valeur de la propriété IsStandardVerticalRomanAlignmentEnabled");
    }

    textePortion.Style.IsStandardVerticalRomanAlignmentEnabled = false;
    calqueTexte.TextData.UpdateLayerData();

    image.Save(fichierSortie);
}

using (var image = (PsdImage)Image.Load(fichierSortie))
{
    var calqueTexte = image.Layers[1] as TextLayer;
    var textePortion = calqueTexte.TextData.Items[0];
    if (!textePortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Lecture correcte
    }
    else
    {
        throw new Exception("Lecture incorrecte de la valeur de la propriété IsStandardVerticalRomanAlignmentEnabled");
    }
}
{{< /highlight >}}

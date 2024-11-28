---
title: Aspose.PSD pour .NET 22.11 - Notes de version
type: docs
weight: 20
url: /fr/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Cette version a une régression dans le cas des exports sur 16 bits, nous recommandons donc de faire preuve de prudence lors de l'utilisation de cette fonctionnalité dans cette version. 
Veuillez ne pas mettre à jour Aspose.PSD vers 22.9-22.11 si le traitement d'images sur 16 bits est votre fonctionnalité principale.

Nous travaillons sur des solutions à ces problèmes.

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-1320|Impossible d'exporter des fichiers PSB extrêmement grands|Amélioration|
|PSDNET-659|Rendre le centre du dégradé radial mobile|Fonctionnalité|
|PSDNET-1330|Méthode de compression ZipWithoutPrediction non prise en charge pour les fichiers spécifiques|Fonctionnalité|
|PSDNET-735|Après l'utilisation d'une méthode de transformation pour un calque uniquement, le calque enregistré a une boîte englobante incorrecte|Bogue|
|PSDNET-1234|Exception lors du chargement d'une image PSD avec motif|Bogue|
|PSDNET-1244|Échec de l'exportation d'image (IndexOutOfRangeException) lors de l'enregistrement d'un fichier PSD avec des symboles chinois|Bogue|
|PSDNET-1303|TimeLine ActiveFrame applique incorrectement|Bogue|
|PSDNET-1307|Régression 22.7 : le rendu incorrect du texte avec des caractères arabes|Bogue|
|PSDNET-1321|Masque vectoriel sur le calque de groupe ne fonctionne pas correctement. L'image finale a un trou noir mais ne devrait pas|Bogue|


## **Changements de l'API publique**
# **APIs ajoutées :**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation:**

**PSDNET-659. Rendre le centre du dégradé radial mobile**

{{< highlight csharp >}}
string fichierSource = "psdnet659.psd";
string fichierSortie = "sortie.png";

using (var imagePsd = (PsdImage)Image.Load(fichierSource))
{
    FillLayer calqueRadial = (FillLayer)imagePsd.Layers[5];
    GradientFillSettings parametres = (GradientFillSettings)calqueRadial.FillSettings;

    // Mettre à jour le point de décalage
    parametres.HorizontalOffset = 10;
    parametres.VerticalOffset = -25;

    imagePsd.Save(fichierSortie, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Après utilisation d'une méthode de transformation pour un calque uniquement, le calque enregistré a une boîte englobante incorrecte**

{{< highlight csharp >}}
string nomFichierSource = @"TextLayer.psd";
string fichierSortie = "TextLayerRedimensionne_sortie.psd";

using (PsdImage image = (PsdImage)Image.Load(nomFichierSource, new PsdLoadOptions()))
{
    TextLayer calqueTexte = (TextLayer)image.Layers[1];

    // Définir la nouvelle taille du calque de texte
    const int NouvelleLargeur = 250;
    const int NouvelleHauteur = 250;

    // Définir le mécanisme selon lequel la fonction de redimensionnement redimensionnera le calque (valeur par défaut)
    ResizeType typeRedimensionnement = ResizeType.NearestNeighbourResample;

    // Nouveau mécanisme de redimensionnement pour le calque de texte
    // Non seulement le calque mais aussi la matrice de transformation du calque de texte seront modifiées
    calqueTexte.Resize(NouvelleLargeur, NouvelleHauteur, typeRedimensionnement);

    image.Save(fichierSortie, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(fichierSortie, new PsdLoadOptions()))
{
    TextLayer calqueTxt = (TextLayer)image.Layers[1];

    // La raison de la différence est la police par défaut différente
    if (calqueTxt.TransformMatrix[4] >= 65 
        && calqueTxt.TransformMatrix[4] <= 67
        && calqueTxt.TransformMatrix[5] >= 234
        && calqueTxt.TransformMatrix[5] <= 237)
    {
        // Tout va bien
    }
    else
    {
        throw new Exception("Le point de localisation est incorrect");
    }
}
{{< /highlight >}}

**PSDNET-1234. Exception lors du chargement d'une image PSD avec motif**

{{< highlight csharp >}}
string fichierSrc = "test.psd";
string sortie = "sortie1234.png";

using (PsdImage imagePsd = (PsdImage)PsdImage.Load(fichierSrc,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions optionsPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    imagePsd.Save(sortie, optionsPng);
}
{{< /highlight >}}

**PSDNET-1244. Échec de l'exportation d'image (IndexOutOfRangeException) lors de l'enregistrement d'un fichier PSD avec des symboles chinois**

{{< highlight csharp >}}
string fichierSource = "input.psd";
string cheminSortie = "output.psd";

var optionsChargement = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(fichierSource, optionsChargement))
{
    foreach (var calque in image.Layers)
    {
        if (calque.Name == "1")
        {
            var calqueTxt = (TextLayer)calque;

            calqueTxt.UpdateText("测试测试");
        }
    }

    // Il ne devrait pas y avoir d'exception ici.
    image.Save(cheminSortie, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame applique incorrectement**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string sortie = "out_timeline.psd";

using (var imagePsd = (PsdImage)Image.Load(src))
{
    TimeLine ligneTemps = TimeLine.InitializeFrom(imagePsd);

    ligneTemps.ActiveFrame = 2;
    ligneTemps.ApplyTo(imagePsd);

    imagePsd.Save(sortie);
}
{{< /highlight >}}

**PSDNET-1307. Régression 22.7 : le rendu incorrect du texte avec des caractères arabes**

{{< highlight csharp >}}
string dossierPolicesTest = "Fonts";
FontSettings.SetFontsFolder(dossierPolicesTest);
FontSettings.UpdateFonts();

string cheminFichierSource = "sarbarg.fin12.psd";
string cheminFichierSortie = "result.tiff";

using (var imagePsd = (PsdImage)Image.Load(cheminFichierSource))
{
    imagePsd.Save(cheminFichierSortie, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Impossible d'exporter des fichiers PSB extrêmement grands**

{{< highlight csharp >}}
string fichierSource = "hf-mim-liman-han-guc-art-kuvvet.psb";
string cheminExportPsd = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(cheminExportPsd, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Masque vectoriel sur le calque de groupe ne fonctionne pas correctement. L'image finale a un trou noir mais ne devrait pas**

{{< highlight csharp >}}
string fichierSrc = "demo.psd";
string sortie = "demo_net.png";

using (PsdImage imagePsd = (PsdImage)PsdImage.Load(fichierSrc))
{
    PngOptions optionsPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    imagePsd.Save(sortie, optionsPng);
}
{{< /highlight >}}

**PSDNET-1330. Méthode de compression ZipWithoutPrediction non prise en charge pour les fichiers spécifiques**

{{< highlight csharp >}}
string fichierSource = "20221017_220706_0000.psd";
string fichierSortie = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(fichierSortie, optionsBase);
}
{{< /highlight >}}

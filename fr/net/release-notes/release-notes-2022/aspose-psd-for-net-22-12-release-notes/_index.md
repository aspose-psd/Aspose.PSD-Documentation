---
title: Notes de version d'Aspose.PSD pour .NET 22.12
type: docs
weight: 10
url: /fr/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- Cette version a corrigé une régression liée à l'exportation en 16 bits.

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-1336|Ajouter la propriété TextOrientation éditable à l'interface IText|Fonctionnalité|
|PSDNET-725|Le redimensionnement du fichier PSD spécifié avec un masque de calque produit un masque incorrect|Bogue|
|PSDNET-1277|Ajouter la capacité de sauvegarder et charger un masque pour 16 images|Bogue|
|PSDNET-1281|Transparence incorrecte lors de la sauvegarde de l'image en 16 bits en image 16 ou 8 bits|Bogue|
|PSDNET-1375|Corriger CMJN en couleur 16 bits|Bogue|


## **Changements d'API publique**
# **APIs ajoutées :**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation:**

**PSDNET-725. Le redimensionnement du fichier PSD spécifié avec un masque de calque produit un masque incorrect**

{{< highlight csharp >}}
string fichierSource = "source.psd";
string cheminExportPsd = "output.psd";
string cheminExportPng = "output.png";

// Il ouvre le fichier PSD source
using (PsdImage image = (PsdImage)Image.Load(fichierSource))
{
    const int Échelle = 4;

    int nouvelleLargeur = image.Width * Échelle;
    int nouvelleHauteur = image.Height * Échelle;

    // Il redimensionne 
    image.Resize(nouvelleLargeur, nouvelleHauteur);
    image.Save(cheminExportPsd, new PsdOptions(image));
}

// Il ouvre un fichier PSD redimensionné
using (PsdImage image = (PsdImage)Image.Load(cheminExportPsd))
{
    // Il rend en PNG
    image.Save(cheminExportPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Ajouter la capacité de sauvegarder et charger un masque pour 16 images**

{{< highlight csharp >}}
string fichier8bitPsdSource = @"input_8bitColor.psd";
string fichier16bitPsdExport = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(fichier8bitPsdSource))
{
    // Les options permettent de sauvegarder en couleur 16 bits
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Le fichier PSD sera sauvegardé avec transparence
    image.Save(fichier16bitPsdExport, options16);
}
{{< /highlight >}}

**PSDNET-1281. Transparence incorrecte lors de la sauvegarde de l'image en 16 bits en image 16 ou 8 bits**

{{< highlight csharp >}}
string fichierSource = @"Exemple_16bit.psd";
string fichierSauvegarde = @"Resave_16bit.psd";
string fichierImage = @"TotalImage_16bit.png";

// Le fichier PSD couleur 16 bits (avec transparence) sera ouvert et sauvegardé en couleur 16 bits
using (var image = (PsdImage)Image.Load(fichierSource))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(fichierSauvegarde, options16);
}

// Le fichier PSD couleur 16 bits sauvegardé sera rendu au format PNG avec transparence
using (var image = (PsdImage)Image.Load(fichierSauvegarde))
{
    image.Save(fichierImage, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Ajouter la propriété TextOrientation éditable à l'interface IText**

{{< highlight csharp >}}
// Le code suivant démontre la possibilité de modifier la nouvelle propriété TextOrientation.
// Cela n'affecte pas le rendu pour le moment, mais vous permet seulement de modifier la valeur de la propriété.

string src = "1336test.psd";
string sortie = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var calqueTexte = image.Layers[1] as TextLayer;
    if (calqueTexte.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Lecture correcte
    }
    else
    {
        throw new Exception("Lecture incorrecte de la valeur de la propriété TextOrientation");
    }

    calqueTexte.TextData.TextOrientation = TextOrientation.Horizontal;
    calqueTexte.TextData.UpdateLayerData();

    image.Save(sortie);
}

using (var image = (PsdImage)Image.Load(sortie))
{
    var calqueTexte = image.Layers[1] as TextLayer;
    if (calqueTexte.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Lecture correcte
    }
    else
    {
        throw new Exception("Lecture incorrecte de la valeur de la propriété TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Corriger CMJN en couleur 16 bits**

{{< highlight csharp >}}
string fichierSrc = @"ClippingMaskRegular.psd";
string cheminExport = @"export.psd";
string cheminExportPng = @"export.png";

// Il définit les options de conversion
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Il convertit et sauvegarde
using (var image = (PsdImage)Image.Load(fichierSrc))
{
    image.Convert(psdOptions);
    image.Save(cheminExport);
}

// Il ouvre le fichier converti et le rend en PNG
using (PsdImage image = (PsdImage)Image.Load(cheminExport))
{
    image.Save(cheminExportPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

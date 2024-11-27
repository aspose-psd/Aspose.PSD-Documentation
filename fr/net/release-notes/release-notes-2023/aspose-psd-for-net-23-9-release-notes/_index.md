---
title: Aspose.PSD pour .NET 23.9 - Notes de version
type: docs
weight: 40
url: /fr/net/aspose-psd-pour-net-23-9-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                                                | **Catégorie** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | Mettre en œuvre la création de masque pour les nouvelles couches d'ajustement                                    | Fonctionnalité |
| PSDNET-1654 | Ajouter le support des couches superposées mélangées en tant qu'option de mélange de groupe                          | Fonctionnalité |
| PSDNET-1194 | Le fichier PSD en mode couleur 16 bits n'applique pas le masque pour les couches d'ajustement                  | Problème |
| PSDNET-1235 | Rendu incorrect des crochets dans la couche de texte                                                                      | Problème |
| PSDNET-1559 | Ne peut pas mettre à jour les styles dans les couches de texte                                                           | Problème |
| PSDNET-1583 | Après l'exportation d'un fichier PSD avec CMJN, les couleurs dans le PSD exporté sont altérées                      | Problème |
| PSDNET-1619 | Un fichier PSB spécifique lance l'exception "Le rectangle n'a pas de zone de traitement commune"                      | Problème |
| PSDNET-1648 | L'échec du chargement de l'image. OverflowException: L'opération arithmétique a entraîné un dépassement                                  | Problème |


## **Changements de l'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation:**

**PSDNET-1638. Mettre en œuvre la création de masque pour les nouvelles couches d'ajustement**

{{< highlight csharp >}}
string srcFile = "zendeya_BW.psd";
string dstFile = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(dstFile);
}

using (var im = (PsdImage)Image.Load(dstFile))
{
    Layer layer = im.Layers[1];

    AssertAreEqual((ushort)5, layer.ChannelsCount);
    AssertAreEqual((short)-2, layer.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Ajouter le support des couches superposées mélangées en tant qu'option de mélange de groupe**

{{< highlight csharp >}}
string sourceFile = "exemple_source.psd";
string outputPsd = "exemple_sortie.psd";
string outputPng = "exemple_sortie.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. Le fichier PSD en mode couleur 16 bits n'applique pas le masque pour les couches d'ajustement**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string outputPng = "courant.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Rendu incorrect des crochets dans la couche de texte**

{{< highlight csharp >}}
string fichier = "fichier1.psd";
string sortie = "sortie_1235.png";

using (var psdImage = (PsdImage)Image.Load(file))
{
    foreach (var layer in psdImage.Layers)
    if (layer is TextLayer textLayer)
    textLayer.TextData.UpdateLayerData();

    var imageOptions = new PsdOptions(psdImage);
    psdImage.Save(output, imageOptions);
}
{{< /highlight >}}

**PSDNET-1559. Ne peut pas mettre à jour les styles dans les couches de texte**

{{< highlight csharp >}}
string sourceFile = "Exemple_TaillePolice.psd";
string outputFile = "sortie_Exemple_TaillePolice.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdImage.Layers[4];
    var l2 = (TextLayer)psdImage.Layers[5];

    var textItems1 = l1.TextData.ProducePortions(new string[] { "texte1", "texte2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var item in textItems1)
    {
        l1.TextData.AddPortion(item);
    }

    var textItems2 = l2.TextData.ProducePortions(new string[] { "couche de texte 1", "couche de texte 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var item in textItems2)
    {
        l2.TextData.AddPortion(item);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1583. Après l'exportation d'un fichier PSD avec CMJN, les couleurs dans le PSD exporté sont altérées**

{{< highlight csharp >}}
string sourceFile = "canyon.psd";
string outputFilePng = "sortie_canyon.png";

using (var outputStream = new MemoryStream())
{
    using (var psdImage = (PsdImage)Image.Load(sourceFile))
    {
        psdImage.Save(outputStream);
    }

    outputStream.Position = 0;
    using (var psdImage = (PsdImage)Image.Load(outputStream))
    {
        psdImage.Save(outputFilePng, new PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. Un fichier PSB spécifique lance l'exception "Le rectangle n'a pas de zone de traitement commune"**

{{< highlight csharp >}}
var input = "1619_src.psb";
var output = "1619_sortie.png";
using (PsdImage img = (PsdImage)Image.Load(input, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(output,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. L'échec du chargement de l'image. OverflowException: L'opération arithmétique a entraîné un dépassement**

{{< highlight csharp >}}
string sourceFile = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    Layer layer = im.Layers[28];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}
{{< /highlight >}}

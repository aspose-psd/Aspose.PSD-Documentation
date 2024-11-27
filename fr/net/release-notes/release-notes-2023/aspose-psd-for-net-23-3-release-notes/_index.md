---
title: Aspose.PSD pour .NET 23.3 - Notes de publication
type: docs
weight: 100
url: /fr/net/aspose-psd-pour-net-23-3-notes-de-publication/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-146|Support de la couche d'ajustement Posterize|Fonctionnalité|
|PSDNET-1366|Mise en œuvre du support VscgResource|Fonctionnalité|
|PSDNET-1437|Ajout du support de la ressource PostResource pour les données de la couche d'ajustement Posterize|Fonctionnalité|
|PSDNET-931|Exportation incorrecte vers la couche PNG avec un ajustement de courbes et un mode couleur CMJN|Bogue|
|PSDNET-1403|Le style du paragraphe est manquant après la sauvegarde et la mise à jour du fichier par PS|Bogue|
|PSDNET-1453|Rendu cassé des effets de lueur et d'ombre sur le texte|Bogue|


## **Changements de l'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation:**

**PSDNET-146. Support de la couche d'ajustement Posterize**

{{< highlight csharp >}}
string fichierSource = "zendeya_posterize.psd";
string fichierSortie = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions()))
{
    foreach (Layer couche in image.Layers)
    {
        if (couche is PosterizeLayer)
        {
            ((PosterizeLayer)couche).Levels = 10;
            image.Save(fichierSortie);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Exportation incorrecte vers la couche PNG avec un ajustement de courbes et un mode couleur CMJN**

{{< highlight csharp >}}
string fichierSrc = "input_LevelsLayerWithLayerMaskCmyk.psd";
string fichierSortie = "output_LevelsLayerWithLayerMaskCmykTest.png";
string fichierOutputPsd = "output.psd";

var optionsChargementPsd = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(fichierSrc, optionsChargementPsd))
{
    image.Save(fichierOutputPsd, new PsdOptions()); // la ', new PsdOptions()' provoque un bogue.
    image.Save(fichierSortie, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Implémenter le support de VscgResource**

{{< highlight csharp >}}
string fichierSource = "StrokeInternalFill_src.psd";
string fichierSortie = "StrokeInternalFill_res.psd";

void AreEqual(double attendu, double actuel, double tolérance = 0.1)
{
    if (Math.Abs(attendu - actuel) > tolérance)
    {
        throw new Exception(
        $"Les valeurs ne sont pas égales.\nAttendu:{attendu}\nRésultat:{actuel}\nDifférence:{attendu - actuel}");
    }
}

using (PsdImage image = (PsdImage)Image.Load(fichierSource))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure structureCouleurRGB = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)structureCouleurRGB.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)structureCouleurRGB.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)structureCouleurRGB.Structures[2]).Value);

    ((DoubleStructure)structureCouleurRGB.Structures[0]).Value = 255d; // Rouge
    ((DoubleStructure)structureCouleurRGB.Structures[1]).Value = 0d; // Vert
    ((DoubleStructure)structureCouleurRGB.Structures[2]).Value = 0d; // Bleu

    image.Save(fichierSortie);
}

// vérification des changements
using (PsdImage image = (PsdImage)Image.Load(fichierSortie))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure structureCouleurRGB = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)structureCouleurRGB.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)structureCouleurRGB.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)structureCouleurRGB.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Le style du paragraphe est manquant après la sauvegarde et la mise à jour du fichier par PS**

{{< highlight csharp >}}
string fichierSource = "PSDTest3.psd";
string fichierSortie = "output.psd";

string[] nouvelTexte = new string[]
{
    "Titre \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(fichierSource))
{
    TextLayer couche2 = image.AddTextLayer("Nouvelle couche", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var donnéesTexte = couche2.TextData;

    ITextStyle styleParagrapheParDéfaut = donnéesTexte.ProducePortion().Style;

    ITextParagraph paragrapheParDéfaut = donnéesTexte.ProducePortion().Paragraph;
    ITextPortion[] nouvellesPortions = donnéesTexte.ProducePortions(nouvelTexte, styleParagrapheParDéfaut, paragrapheParDéfaut);

    nouvellesPortions[0].Style.FontSize = 14;
    nouvellesPortions[0].Style.FontName = "TwCenMT-Bold";

    nouvellesPortions[1].Style.Leading = 20;
    nouvellesPortions[1].Style.FontSize = 10;
    nouvellesPortions[1].Style.FontName = "TwCenMT-Bold";

    // Suppression de l'ancien texte
    donnéesTexte.RemovePortion(0);

    // Ajout des nouvelles portions de texte
    foreach (var nouvellePortion in nouvellesPortions)
    {
        donnéesTexte.AddPortion(nouvellePortion);
    }

    donnéesTexte.UpdateLayerData();

    image.Save(fichierSortie);
}

using (PsdImage imagePSD = (PsdImage)Aspose.PSD.Image.Load(fichierSortie))
{
    Txt2Resource ressourceTxt2 = (Txt2Resource)imagePSD.GlobalLayerResources[1];
    byte[] octets = ressourceTxt2.Data;
    string donnéesTxt2 = "";
    for (int i = 18900; i < octets.Length; i++)
    {
        donnéesTxt2 += (char)octets[i];
    }

    string clé0 = @" >> /6 0 >> >> /1 "; // préfixe à la longueur du paragraphe 0
    string clé1 = @" >> /6 1 >> >> /1 "; // préfixe à la longueur du paragraphe 1
    int index0 = donnéesTxt2.IndexOf(clé0);
    int index1 = donnéesTxt2.IndexOf(clé1);

    string longPar0 = donnéesTxt2.Substring(index0 + clé0.Length, 1);
    string longPar1 = donnéesTxt2.Substring(index1 + clé1.Length, 3);

    string attendu0 = nouvelTexte[0].Length.ToString();
    string attendu1 = (nouvelTexte[1].Length + 1).ToString();

    if (longPar0 != attendu0 || longPar1 != attendu1)
    {
        throw new Exception(
            $"La longueur des paragraphes est incorrecte.\nAttendu : {attendu0} et {attendu1}\nRésultat : {longPar0} et {longPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Ajouter le support de la ressource PostResource pour les données de la couche d'ajustement Posterize**

{{< highlight csharp >}}
string fichierSource = "zendeya_posterize.psd";
string fichierSortie = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions()))
{
    Layer couche = image.Layers[1];

    foreach (LayerResource ressource in couche.Resources)
    {
        if (ressource is PostResource)
        {
            ((PostResource)ressource).Levels = 10;
            image.Save(fichierSortie);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Rendu cassé des effets de lueur et d'ombre sur le texte**

{{< highlight csharp >}}
string fichierPsdSortie = "effect_bug.psd";
string fichierPngSortie = "effect_bug.png";

using (var psdImage = new PsdImage(500, 500))
{
    // Ajouter des calques texte
    Aspose.PSD.Rectangle zoneDeTexte1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle zoneDeTexte2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle zoneDeTexte3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer coucheTexte1 = psdImage.AddTextLayer("Texte avec effets", zoneDeTexte1);
    TextLayer coucheTexte2 = psdImage.AddTextLayer("Texte avec effets", zoneDeTexte2);
    TextLayer coucheTexte3 = psdImage.AddTextLayer("Texte avec effets", zoneDeTexte3);

    // Modifier les calques texte
    coucheTexte1.TextData.Items[0].Style.FontSize = 150;
    coucheTexte1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    coucheTexte1.TextData.UpdateLayerData();

    coucheTexte2.TextData.Items[0].Style.FontSize = 150;
    coucheTexte2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    coucheTexte2.TextData.UpdateLayerData();

    coucheTexte3.TextData.Items[0].Style.FontSize = 150;
    coucheTexte3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    coucheTexte3.TextData.UpdateLayerData();

    // Ajouter des effets
    OuterGlowEffect lueur = coucheTexte1.BlendingOptions.AddOuterGlow(); // casser
    lueur.Spread = 15;
    ((ColorFillSettings)lueur.FillColor).Color = Color.Red;

    var ombrePortée = coucheTexte2.BlendingOptions.AddDropShadow(); // casser avec un texte long
    ombrePortée.Distance = 25;
    ombrePortée.Color = Color.DarkBlue;

    var ombreInterne = coucheTexte3.BlendingOptions.AddInnerShadow(); // casser avec un texte long
    ombreInterne.UseGlobalLight = false;
    ombreInterne.Angle = -179;
    ombreInterne.Distance = 10;
    ombreInterne.Size = 8;
    ombreInterne.Color = Color.HotPink;

    // export
    psdImage.Save(fichierPsdSortie);
    psdImage.Save(fichierPngSortie, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
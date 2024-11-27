---
title: Aspose.PSD pour .NET 20.3 - Notes de version
type: docs
weight: 100
url: /fr/net/aspose-psd-pour-net-20-3-notes-de-version/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD pour .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

| **Clé** | **Résumé** | **Catégorie** |
| :- | :- | :- |
|PSDNET-188|Support de .Net Core|Fonctionnalité|
|PSDNET-523|Convertir des fichiers Adobe Illustrator en PDF|Fonctionnalité|
|PSDNET-212|Ajouter la capacité de rendre différents styles dans une couche de texte|Fonctionnalité|
|PSDNET-144|Support de la couche d'ajustement noir et blanc|Fonctionnalité|
|PSDNET-233|Ajouter le support de l'exportation du format AI (Version 8) vers d'autres formats|Fonctionnalité|
|PSDNET-540|Support du mode de fusion PassThrough (Utilisé uniquement pour les groupes de calques).|Fonctionnalité|
|PSDNET-539|Exception: Échec du chargement de l'image lors du chargement de l'image avec une ressource de noms Alpha Unicode vide|Bogue|
|PSDNET-541|Sortie incorrecte après avoir modifié la visibilité d'un groupe de calques|Bogue|
|PSDNET-516|Exception lors du chargement de l'image PSD : La section de couleur (Ressource d'ombre portée) doit contenir 3 composants de couleur pour RVB ou 4 composants de couleur pour CMJN|Bogue|
|PSDNET-536|Exception si essayez de dessiner sur une couche nouvellement créée si la version simple du constructeur est utilisée|Bogue|

## **Changements d'API publique**
# **APIs ajoutées :**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**
**PSDNET-523. Convertir des fichiers Adobe Illustrator en PDF**

{{< highlight java >}}

 string fichierSource = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(fichierSource))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Ajouter la capacité de rendre différents styles dans une couche de texte**

{{< highlight java >}}

 string fichierSource = "text212.psd";

string fichierEthalon = "Ethalon_text212.psd";

string fichierSortie = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(fichierSource))

{

    TextLayer coucheTexte = (TextLayer)img.Layers[1];

    IText donnéesTexte = coucheTexte.TextData;

    ITextStyle styleParDéfaut = donnéesTexte.ProducePortion().Style;

    ITextParagraph paragrapheParDéfaut = donnéesTexte.ProducePortion().Paragraph;

    styleParDéfaut.FillColor = Color.DimGray;

    styleParDéfaut.FontSize = 51;

    donnéesTexte.Items[1].Style.Strikethrough = true;

    ITextPortion[] nouvellesPortions = donnéesTexte.ProducePortions(new string[] { "E=mc",  "2\r",  "Gras",  "Italique\r",  "Texte en minuscules" }, styleParDéfaut, paragrapheParDéfaut);

    nouvellesPortions[0].Style.Underline = true; // modifier le style du texte "E=mc"

    nouvellesPortions[1].Style.FontBaseline = FontBaseline.Superscript; // modifier le style du texte "2\r"

    nouvellesPortions[2].Style.FauxBold = true; // modifier le style du texte "Gras"

    nouvellesPortions[3].Style.FauxItalic = true; // modifier le style du texte "Italique\r"

    nouvellesPortions[3].Style.BaselineShift = -25; // modifier le style du texte "Italique\r"

    nouvellesPortions[4].Style.FontCaps = FontCaps.SmallCaps; // modifier le style du texte "Texte en minuscules"

    foreach (var nouvellePortion in nouvellesPortions)

    {

        donnéesTexte.AddPortion(nouvellePortion);

    }

    donnéesTexte.UpdateLayerData();

    img.Save(fichierSortie);

}

{{< /highlight >}}

**PSDNET-233. Ajouter le support de l'exportation du format AI (Version 8) vers d'autres formats**

{{< highlight java >}}

 // Exemple d'exportation d'un fichier AI en format PSD et PNG

string nomFichierSource = "form_8.ai";

string nomFichierSortie = "form_8_export";

using (AiImage image = (AiImage)Image.Load(nomFichierSource))

{

    image.Save(nomFichierSortie + ".psd", new PsdOptions());

    image.Save(nomFichierSortie + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Support du mode de fusion PassThrough (Utilisé uniquement pour les groupes de calques).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string nomFichierSource = "Pomme.psd";

string nomFichierSortie = "Sortie" + nomFichierSource;

using (PsdImage image = (PsdImage)Image.Load(nomFichierSource))

{

    AssertIsTrue(image.Layers.Length >= 23, "Il n'y a pas de 23e couche.");

    var couche = image.Layers[23] as LayerGroup;

    AssertIsTrue(couche != null, "La 23e couche n'est pas un groupe de calques.");

    AssertIsTrue(couche.Name == "GroupeAjustement", "Le nom de la 23e couche n'est pas 'GroupeAjustement'.");

    AssertIsTrue(couche.BlendModeKey == BlendMode.PassThrough, "La couche de GroupeAjustement devrait avoir le mode de fusion 'pass through'.");

    image.Save(nomFichierSortie, new PsdOptions());

    image.Save("SortiePomme.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    couche.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + nomFichierSortie, new PsdOptions());

    image.Save("NormalSortiePomme.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. La mise à jour du texte dans une couche de texte lance une exception**

{{< highlight java >}}

 // La mise à jour du texte dans une couche de texte lance une exception

string cheminFichier = "FlipVertical.psd";

string cheminSortie = "FlipVertical_modifie.psd";

var nouveauTexte = "Test";

using (var image = Image.Load(cheminFichier))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var couches = psdImage.Layers;

    for (var index = couches.Length - 1; index >= 0; index--)

    {

        var couche = couches[index] as TextLayer;

        if (couche == null)

        {

            continue;

        }

        couche.UpdateText(nouveauTexte);

    }

    var optionsImage = new PsdOptions(psdImage);

    psdImage.Save(cheminSortie, optionsImage);

}

{{< /highlight >}}

**PSDNET-182. Enregistrer l'image PSD après une opération RotateFlip produit un fichier corrompu qui ne peut pas être ouvert.**

{{< highlight java >}}

 string nomFichierSource = "1.psd";

RotateFlipType typeRetournement = RotateFlipType.Rotate270FlipXY;

string nomFichierSortiePsd = "TestRotateFlip2617.psd";

using (PsdImage image = (PsdImage)Image.Load(nomFichierSource))

{

    image.RotateFlip(typeRetournement);

    image.Save(nomFichierSortiePsd);

}

// Devrait être exécuté sans exceptions

using (PsdImage image = (PsdImage)Image.Load(nomFichierSortiePsd)) 

{

    // Ne rien faire

}

{{< /highlight >}}

**PSDNET-539. Exception: Échec du chargement de l'image lors du chargement de l'image avec une ressource de noms Alpha Unicode vide**

{{< highlight java >}}

 string cheminSource = "pomme.psd";

using (var psdImage = (PsdImage)Image.Load(cheminSource)) // Ici, nous ne devrions pas obtenir d'exceptions

{

    // ne rien faire

}

{{< /highlight >}}

**PSDNET-541. Sortie incorrecte après avoir modifié la visibilité d'un groupe de calques**

{{< highlight java >}}

 string fichierSource = "entrée.psd";

string fichierSortie = "sortie.psd";

// effectuer des changements dans les noms des calques et enregistrer

using (var image = (PsdImage)Image.Load(fichierSource))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var calque = image.Layers[i];

        // Désactiver tout à l'intérieur d'un groupe

        if (calque is LayerGroup)

        {

            calque.IsVisible = false;

        }

    }

    image.Save(fichierSortie);

}

{{< /highlight >}}

**PSDNET-516. Exception lors du chargement de l'image PSD : La section de couleur (Ressource ombre portée) doit contenir 3 composants de couleur pour RVB ou 4 composants de couleur pour CMJN**

{{< highlight java >}}

 string fichierSource = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(fichierSource)) // Ici, nous ne devrions pas obtenir d'exceptions

{

    // ne rien faire

}

{{< /highlight >}}

**PSDNET-536. Exception si vous essayez de dessiner sur une couche nouvellement créée si la version simple du constructeur est utilisée**

{{< highlight java >}}

 string fichierSortie = "sortie.psd";

int largeur = 100;

int hauteur = 100;

using (var image = new PsdImage(largeur, hauteur))

{

    var calque = new Calque();

    calque.Bottom = hauteur;

    calque.Right = largeur;

    image.AddLayer(calque);

    Graphics graphique = new Graphics(calque);

    graphique.Clear(Color.Yellow);

    // dessiner un rectangle avec l'outil Crayon

    graphique.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // dessiner un autre rectangle avec une brosse unie en couleur bleue

    graphique.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(fichierSortie);

}

{{< /highlight >}}

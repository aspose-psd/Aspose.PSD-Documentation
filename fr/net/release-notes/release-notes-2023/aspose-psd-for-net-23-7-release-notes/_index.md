---
title: Notes de version Aspose.PSD pour .NET 23.7
type: docs
weight: 60
url: /fr/net/aspose-psd-pour-net-23-7-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                                    | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | Ajouter la capacité d'exporter chaque calque d'un fichier PSD vers un fichier GIF animé                       | Fonctionnalité |
| PSDNET-1441 | Assigner la propriété Remplissage du calque de forme à partir de la ressource VSCG                            | Fonctionnalité |
| PSDNET-1534 | Ajouter de nouveaux types de déformation (arc et arche)                                                        | Fonctionnalité |
| PSDNET-1543 | Changer l'application qui enregistre le fichier PSD en Aspose.PSD si la propriété UpdateMetadata est définie à true | Fonctionnalité |
| PSDNET-1567 | Augmenter la zone de calcul de l'image déformée                                                               | Fonctionnalité |
| PSDNET-1471 | Le calque d'ajustement noir et blanc traite mal la semi-transparence                                          | Problème |
| PSDNET-1505 | Le remplacement du contenu de l'objet intelligent (lorsque l'option AllowWarpRepaint est active) échoue après 2 minutes de calcul | Problème |
| PSDNET-1585 | Ajouter la capacité d'obtenir la véritable position de gauche et de haut du groupe de calques                | Problème |
| PSDNET-1589 | Le redimensionnement du calque ne fonctionne pas correctement lorsque le fichier PSD a une ressource Vogk avec des structures en points | Problème |
| PSDNET-1608 | TextBound ne fonctionne pas comme prévu                                                                       | Problème |
| PSDNET-1612 | Ajout d'un calque créé avec le constructeur par défaut à une image PSD ne lui ajoute pas de ressources par défaut | Problème |
| PSDNET-1623 | La propriété LoopesCount de Timeline est ignorée lors de l'exportation vers un GIF animé                     | Problème |


## **Changements d'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **APIs supprimées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Exemples d'utilisation:**

**PSDNET-802. Ajouter la capacité d'exporter chaque calque d'un fichier PSD vers un fichier GIF animé**

{{< highlight csharp >}}
string src = "ChaqueCalqueEstFrame.psd";
string outputGif = "out_ChaqueCalqueEstFrame.gif";
string outputPsd = "out_ChaqueCalqueEstFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Créer des images pour chaque calque.
    int nombreCalques = psdImage.Layers.Length;
    var chronologie = psdImage.Timeline;

    Frame[] frames = new Frame[nombreCalques];
    for (int i = 0; i < nombreCalques; i++)
    {
        frames[i] = new Frame();
        LayerState[] étatsCalque = new LayerState[nombreCalques];

        for (int j = 0; j < nombreCalques; j++)
        {
            étatsCalque[j] = new LayerState();
            étatsCalque[j].Enabled = i == j;
        }

        frames[i].LayerStates = étatsCalque;
    }

    chronologie.Frames = frames;

    // Mettre à jour les états actuels
    Layer[] calques = psdImage.Layers;
    LayerState[] états = chronologie.Frames[chronologie.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < nombreCalques; i++)
    {
        calques[i].IsVisible = états[i].Enabled;
    }

    chronologie.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Assigner la propriété Remplissage du calque de forme à partir de la ressource VSCG**

{{< highlight csharp >}}
string fichierSrc = "FormeInterneSolide.psd";
string fichierSortie = "FormeInterneSolide.psd.sortie.psd";

using (PsdImage image = (PsdImage)Image.Load(
    fichierSrc,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer calqueForme = (ShapeLayer)image.Layers[1];
    ColorFillSettings paramètresRemplissage = (ColorFillSettings)calqueForme.Fill;
    paramètresRemplissage.Color = Color.Red;

    calqueForme.Update();

    image.Save(fichierSortie);
}

// Vérifier les modifications enregistrées
using (PsdImage image = (PsdImage)Image.Load(
    fichierSortie,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer calqueForme = (ShapeLayer)image.Layers[1];
    ColorFillSettings paramètresRemplissage = (ColorFillSettings)calqueForme.Fill;

    AssertAreEqual(Color.Red, paramètresRemplissage.Color);

    image.Save(fichierSortie);
}

void AssertAreEqual(object attendu, object réel, string message = null)
{
    if (!object.Equals(attendu, réel))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Le calque d'ajustement noir et blanc traite mal la semi-transparence**

{{< highlight csharp >}}
string fichierSrc = "grenouille_nosymb.psd";
string fichierSortie = "grenouille_nosymb.psd.sortie.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(fichierSrc))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(fichierSortie);
}

// Vérifier les modifications enregistrées
using (PsdImage image = (PsdImage)Image.Load(
    fichierSortie,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer calqueAjustementNoirBlanc = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (calqueAjustementNoirBlanc == null)
    {
        throw new Exception("Le calque 2 devrait être BlackWhiteAdjustmentLayer");
    }

    image.Save(fichierSortie);
}

void AssertAreEqual(object attendu, object réel, string message = null)
{
    if (!object.Equals(attendu, réel))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}
{{< /highlight >}}

**PSDNET-1505. Le remplacement du contenu de l'objet intelligent (lorsque l'option AllowWarpRepaint est active) échoue après 2 minutes de calcul**

{{< highlight csharp >}}
string fichierSource = "mug 4.psd";
string fichierChange = "illustration_remplacer.png";
string fichierSortie = "export.png";

int nouvelleHauteur = 300;

using (var psdImage = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer calqueObjetIntelligent = (SmartObjectLayer)psdImage.Layers[3];

    var échelle = (double)nouvelleHauteur / calqueObjetIntelligent.Height;
    var nouvelleLargeur = (int)Math.Round(calqueObjetIntelligent.Width * échelle);

    PsdImage imageInterne = new PsdImage(nouvelleLargeur, nouvelleHauteur);
    innerImage.SetResolution(72, 72);

    Stream fluxInterne = new FileStream(fichierChange, FileMode.Open);
    Layer calque = new Layer(fluxInterne) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        innerImage.AddLayer(calque);

        calqueObjetIntelligent.ReplaceContents(imageInterne);
        calqueObjetIntelligent.UpdateModifiedContent();

        psdImage.Save(fichierSortie, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        imageInterne.Dispose();
        fluxInterne.Dispose();
        calque.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. Ajouter de nouveaux types de déformation (arc et arche)**

{{< highlight csharp >}}
string fichierArcSource = "arc_deformation.psd";
string fichierArcSortie = "arc_export.png";

string fichierArcheSource = "arch_deformation.psd";
string fichierArcheSortie = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(fichierArcSource, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(fichierArcSortie, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(fichierArcheSource, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(fichierArcheSortie, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. Changer l'application qui enregistre le fichier PSD en Aspose.PSD si la propriété UpdateMetadata est définie à true**

{{< highlight csharp >}}
string chemin = "sortie.psd";
using (var image = new PsdImage(100, 100))
{
    // Si vous voulez changer l'outil créateur, assurez-vous que la propriété "UpdateMetadata" est définie à true. Elle est définie à true par défaut.
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // Enregistrer l'image.
    image.Save(chemin, psdOptions);

    // Vérifier l'outil créateur dans le code.
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // Ici, les informations sur l'outil créateur seront mises à jour.
    var outilCréateurActuel = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. Augmenter la zone de calcul de l'image déformée**

{{< highlight csharp >}}
string fichierSource = "mug4_deformation.psd";
string fichierSortie = "mug4_export.png";

using (var psdImage = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(fichierSortie, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. Ajouter la capacité d'obtenir la véritable position de gauche et de haut du groupe de calques**

{{< highlight csharp >}}
string fichierSource = "CalquesFigures.psd";

void AssertAreEqual(object attendu, object réel)
{
    if (!object.Equals(attendu, réel))
    {
        throw new Exception("Les objets ne sont pas égaux.");
    }
}

using (var image = (PsdImage)Image.Load(fichierSource))
{
    var calques = image.Layers;

    for (int i = 0; i < calques.Length; i++)
    {
        var calque = calques[i];

        if (calque is LayerGroup)
        {
            // Obtenir LayerGroup.
            var groupe = (LayerGroup)calque;

            var gaucheAttendue = int.MaxValue;
            var hautAttendu = int.MaxValue;
            var droiteAttendue = 0;
            var basAttendu = 0;

            // Calculer les vraies positions de gauche, de haut, de droite et de bas.
            foreach (var calqueInterne in groupe.Layers)
            {
                if (calqueInterne is AdjustmentLayer || calqueInterne.Bounds.IsEmpty)
                {
                    continue;
                }

                gaucheAttendue = Math.Min(gaucheAttendue, calqueInterne.Left);
                hautAttendu = Math.Min(hautAttendu, calqueInterne.Top);
                droiteAttendue = Math.Max((gaucheAttendue + groupe.Width), (calqueInterne.Left + calqueInterne.Width));
                basAttendu = Math.Max((hautAttendu + groupe.Height), (calqueInterne.Top + calqueInterne.Height));
            }

            // Les positions de gauche, de haut, de droite et de bas du groupe de calques sont maintenant calculées correctement.
            AssertAreEqual(groupe.Left, gaucheAttendue);
            AssertAreEqual(groupe.Top, hautAttendu);
            AssertAreEqual(groupe.Right, droiteAttendue);
            AssertAreEqual(groupe.Bottom, basAttendu);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. Le redimensionnement du calque ne fonctionne pas correctement lorsque le fichier PSD a une ressource Vogk avec des structures en points**

{{< highlight csharp >}}
string[] fichiersSources = new string[]
{
    "PointsVecteursOrigine.psd",
    "TopVogkResStruct.psd"
};

foreach (string fichierSource in fichiersSources)
{
    using (PsdImage image = (PsdImage)Image.Load(fichierSource))
    {
        Layer calque = image.Layers[0];

        calque.Resize(50, 50);

        AssertAreEqual(calque.Height, 50);
        AssertAreEqual(calque.Width, 50);
    }
}

void AssertAreEqual(object attendu, object réel, string message = null)
{
    if (!object.Equals(attendu, réel))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound ne fonctionne pas comme prévu**

{{< highlight csharp >}}
string fichierSource = "entrée_Test_forTicket.psd";
string fichierSortie = "sortie_1608.psd";

Size nouveauTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(fichierSource))
{
    //Étape: Remplacer le texte
    TextLayer calqueTexte = (TextLayer)psdImage.Layers[3];
    calqueTexte.TextData.Items[0].Text = "Texte test remplacé";

    //Étape: Mettre à jour TextBoundBox
    calqueTexte.TextData.UpdateLayerData();
    nouveauTextBox = new Size((int)Math.Ceiling(calqueTexte.TextBoundBox.Width), calqueTexte.Height);

    calqueTexte.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, nouveauTextBox);
    calqueTexte.TextData.UpdateLayerData();

    psdImage.Save(fichierSortie);
}

// Vérifier les changements
using (var psdImage = (PsdImage)Image.Load(fichierSortie))
{
    Txt2Resource ressourceTxt2 = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string donnéesTexte = Encoding.GetEncoding("Windows-1251").GetString(ressourceTxt2.Data);

    string recherche = "<< /0 << /1 << /0 ["; // ensemble de caractères spécifique pour trouver la valeur de la zone de texte dans ce fichier.

    int débutIndex = donnéesTexte.IndexOf(recherche) + recherche.Length;
    int finIndex = donnéesTexte.IndexOf("]", débutIndex);
    string élémentsBoîte = donnéesTexte.Substring(débutIndex, finIndex - débutIndex);

    string hauteur = nouveauTextBox.Height.ToString("0.0####").Replace(",", ".");
    string largeur = nouveauTextBox.Width.ToString("0.0####").Replace(",", ".");

    if (!élémentsBoîte.Contains(hauteur) || !élémentsBoîte.Contains(largeur))
    {
        throw new Exception("La zone de texte n'est pas mise à jour.");
    }
}
{{< /highlight >}}

**PSDNET-1612. Ajout d'un calque créé avec le constructeur par défaut à une image PSD ne lui ajoute pas de ressources par défaut**

{{< highlight csharp >}}
string sortie = "nouveauCalque.psd";

using (var psdImage = new PsdImage(500, 500))
{
    var calque = new Layer();
    psdImage.AddLayer(calque);

    LyidResource ressourceLyid = (LyidResource)FindResource(LyidResource.TypeToolKey, calque.Resources);

    int idCalque = ressourceLyid.Value; // N'
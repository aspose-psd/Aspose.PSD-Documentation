---
title: Aspose.PSD pour .NET 18.12 - Notes de publication
type: docs
weight: 10
url: /fr/net/aspose-psd-pour-net-18-12-notes-de-sortie/
---

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-76|Support de la couche de contour|Fonctionnalité|
|PSDNET-83|Support de l'effet de dégradé|Fonctionnalité|
|PSDNET-84|Support de l'effet de motif|Fonctionnalité|
|PSDNET-89|Permettre l'ajout d'une nouvelle couche régulière générée à PsdImage|Fonctionnalité|
|PSDNET-93|Après la mise à jour du contenu de la couche de texte avec le caractère \ (barre oblique inversée), le fichier résultant ne peut pas être ouvert dans Photoshop|Bogue|
|PSDNET-39|Images corrompues après l'exportation avec des données d'image surdimensionnées en mode couleur CMJN|Bogue|
|PSDNET-52|Possible : La rotation dans PSD ne fonctionne pas|Bogue|
|PSDNET-88|Possible : Les méthodes de recadrage dans Aspose.Psd ne fonctionnent pas|Bogue|
|PSDNET-91|Appliquer les modifications d'Aspose.Imaging à Aspose.PSD|Amélioration|

## **Changements de l'API publique**
Méthode Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Classe Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Méthode Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Méthode Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Champ/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Méthode Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Propriété Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **Exemples d'utilisation:**
**PSDNET-76. Support de la couche de contour**

**1) Type de remplissage - Motif**

{{< highlight fr >}}

     // Effet de contour. Type de remplissage - Motif. Exemple

    string nomFichierSource = "Contour.psd";

    string cheminExportation = "ContourMotifModifié.psd";

    var optionsChargement = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // Préparation de nouvelles données

    var nouveauMotif = new int[]

    {

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

    };

   var nouvellesBornesMotif = new Rectangle(0, 0, 4, 4);

   var identifiant = Guid.NewGuid();

    using (var im = (PsdImage)Image.Load(nomFichierSource, optionsChargement))

    {

         var contourMotif = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

         Assert.AreEqual(BlendMode.Normal, contourMotif.BlendMode);

         Assert.AreEqual(255, contourMotif.Opacity);

         Assert.AreEqual(true, contourMotif.IsVisible);

         var paramRemplissage = (PatternFillSettings)contourMotif.FillSettings;

         Assert.AreEqual(FillType.Pattern, paramRemplissage.FillType);

         contourMotif.Opacity = 127;

         contourMotif.BlendMode = BlendMode.Color;

         PattResource ressource;

         foreach (var ressourceCalqueGlobal in im.GlobalLayerResources)

         {

             if (ressourceCalqueGlobal is PatternResource)

             {

                  ressource = (PatternResource)ressourceCalqueGlobal;

                  ressource.PatternId = identifiant.ToString();

                  ressource.Name = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";        

                  ressource.SetPattern(nouveauMotif, nouvellesBornesMotif);               

             }

         }

         ((PatternFillSettings)contourMotif.FillSettings).PatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";

         ((PatternFillSettings)contourMotif.FillSettings).PatternId = identifiant.ToString() + "\0";

        im.Save(cheminExportation);

    }

    // Fichier test après modification

    using (var im = (PsdImage)Image.Load(nomFichierSource, optionsChargement))

    {

        var contourMotif = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

        PattResource ressource = null;

        foreach (var ressourceCalqueGlobal in im.GlobalLayerResources)

        {

            if (ressourceCalqueGlobal is PatternResource)

            {

                ressource = (PatternResource)ressourceCalqueGlobal;

            }

        }

        if (ressource == null)

        {

            throw new Exception("Ressource motif non trouvée");

        }

        // Vérifier les données du motif

        Assert.AreEqual(nouveauMotif, ressource.PatternData);

        Assert.AreEqual(nouvellesBornesMotif, new Rectangle(0, 0, ressource.Width, ressource.Height));

        Assert.AreEqual(identifiant.ToString(), ressource.PatternId);

        Assert.AreEqual(BlendMode.Color, contourMotif.BlendMode);

        Assert.AreEqual(127, contourMotif.Opacity);

        Assert.AreEqual(true, contourMotif.IsVisible);

        var paramRemplissage = (PatternFillSettings)contourMotif.FillSettings;

        Assert.AreEqual(FillType.Pattern, paramRemplissage.FillType);

    }

{{< /highlight >}}

**Type de remplissage - Dégradé**

{{< highlight fr >}}

     // Effet de contour. Type de remplissage - Dégradé. Exemple

    string nomFichierSource = "Contour.psd";

    string cheminExportation = "ContourDégradéModifié.psd";

    var optionsChargement = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(nomFichierSource, optionsChargement))

    {

        var contourDégradé = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, contourDégradé.BlendMode);

        Assert.AreEqual(255, contourDégradé.Opacity);

        Assert.AreEqual(true, contourDégradé.IsVisible);

        var paramRemplissage = (GradientFillSettings)contourDégradé.FillSettings;

        Assert.AreEqual(Color.Black, paramRemplissage.Color);

        Assert.AreEqual(FillType.Gradient, paramRemplissage.FillType);

        Assert.AreEqual(true, paramRemplissage.AlignWithLayer);

        Assert.AreEqual(GradientType.Linear, paramRemplissage.GradientType);

        Assert.IsTrue(Math.Abs(90 - paramRemplissage.Angle) < 0.001, "L'angle est incorrect");

        Assert.AreEqual(false, paramRemplissage.Dither);

        Assert.IsTrue(Math.Abs(0 - paramRemplissage.HorizontalOffset) < 0.001, "Le décalage horizontal est incorrect");

        Assert.IsTrue(Math.Abs(0 - paramRemplissage.VerticalOffset) < 0.001, "Le décalage vertical est incorrect");

        Assert.AreEqual(false, paramRemplissage.Reverse);

        // Points de couleur

        var pointsCouleur = paramRemplissage.ColorPoints;

        Assert.AreEqual(2, pointsCouleur.Length);

        Assert.AreEqual(Color.Black, pointsCouleur[0].Color);

        Assert.AreEqual(0, pointsCouleur[0].Location);

        Assert.AreEqual(50, pointsCouleur[0].MedianPointLocation);

        Assert.AreEqual(Color.White, pointsCouleur[1].Color);

        Assert.AreEqual(4096, pointsCouleur[1].Location);

        Assert.AreEqual(50, pointsCouleur[1].MedianPointLocation);

        // Points de transparence

        var pointsTransparence = paramRemplissage.TransparencyPoints;

        Assert.AreEqual(2, pointsTransparence.Length);

        Assert.AreEqual(0, pointsTransparence[0].Location);

        Assert.AreEqual(50, pointsTransparence[0].MedianPointLocation);

        Assert.AreEqual(100, pointsTransparence[0].Opacity);

        Assert.AreEqual(4096, pointsTransparence[1].Location);

        Assert.AreEqual(50, pointsTransparence[1].MedianPointLocation);

        Assert.AreEqual(100, pointsTransparence[1].Opacity);

        // Test d'édition

        paramRemplissage.Color = Color.Green;

        contourDégradé.Opacity = 127;

        contourDégradé.BlendMode = BlendMode.Color;

        paramRemplissage.AlignWithLayer = false;

        paramRemplissage.GradientType = GradientType.Radial;

        paramRemplissage.Angle = 45;

        paramRemplissage.Dither = true;

        paramRemplissage.HorizontalOffset = 15;

        paramRemplissage.VerticalOffset = 11;

        paramRemplissage.Reverse = true;

        // Ajouter un nouveau point de couleur

        var pointCouleur = paramRemplissage.AddColorPoint();

        pointCouleur.Color = Color.Green;        

        pointCouleur.Location = 4096;

        pointCouleur.MedianPointLocation = 75;

        // Modifier l'emplacement du point précédent

        paramRemplissage.ColorPoints[1].Location = 1899;

        // Ajouter un nouveau point de transparence

        var pointTransparence = paramRemplissage.AddTransparencyPoint();

        pointTransparence.Opacity = 25;

        pointTransparence.MedianPointLocation = 25;

        pointTransparence.Location = 4096;

        // Modifier l'emplacement du point de transparence précédent

        paramRemplissage.TransparencyPoints[1].Location = 2411;

        im.Save(cheminExportation);

    }

    // Fichier test après modification

    using (var im = (PsdImage)Image.Load(cheminExportation, optionsChargement))

    {

        var contourDégradé = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, contourDégradé.BlendMode);

        Assert.AreEqual(127, contourDégradé.Opacity);

        Assert.AreEqual(true, contourDégradé.IsVisible);

        var paramRemplissage = (GradientFillSettings)contourDégradé.FillSettings;

        Assert.AreEqual(Color.Green, paramRemplissage.Color);

        Assert.AreEqual(FillType.Gradient, paramRemplissage.FillType);

        // Vérifier les points de couleur

        Assert.AreEqual(3, paramRemplissage.ColorPoints.Length);

        var point = paramRemplissage.ColorPoints[0];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.Black, point.Color);

        Assert.AreEqual(0, point.Location);

        point = paramRemplissage.ColorPoints[1];

        Assert.AreEqual(50, point.MedianPointLocation);

        Assert.AreEqual(Color.White, point.Color);

        Assert.AreEqual(1899, point.Location);

        point = paramRemplissage.ColorPoints[2];

        Assert.AreEqual(75, point.MedianPointLocation);

        Assert.AreEqual(Color.Green, point.Color);

        Assert.AreEqual(4096, point.Location);

        // Vérifier les points de transparence

        Assert.AreEqual(3, paramRemplissage.TransparencyPoints.Length);

        var pointTransparence = paramRemplissage.TransparencyPoints[0];

        Assert.AreEqual(50, pointTransparence.MedianPointLocation);

        Assert.AreEqual(100, pointTransparence.Opacity);

        Assert.AreEqual(0, pointTransparence.Location);

        pointTransparence = paramRemplissage.TransparencyPoints[1];

        Assert.AreEqual(50, pointTransparence.MedianPointLocation);

        Assert.AreEqual(100, pointTransparence.Opacity);

        Assert.AreEqual(2411, pointTransparence.Location);

        pointTransparence = paramRemplissage.TransparencyPoints[2];

        Assert.AreEqual(25, pointTransparence.MedianPointLocation);

        Assert.AreEqual(25, pointTransparence.Opacity);

        Assert.AreEqual(4096, pointTransparence.Location);

    }

{{< /highlight >}}

**PSDNET-84. Support de l'effet de motif.**

{{< highlight fr >}}

    // Exemple d'effet de superposition de motif

    string nomFichierSource = "SuperpositionMotif.psd";

    string cheminExportation = "SuperpositionMotifModifié.psd";

    var nouveauMotif = new int[]

    {

        Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

        Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

    };

    var nouvellesBornesMotif = new Rectangle(0, 0, 4, 2);

    var identifiant = Guid.NewGuid();

    var nouveauNomMotif = "$$$/Presets/Patterns/Motif=Nouveau nom de motif\0";

    var optionsChargement = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(nomFichierSource, optionsChargement))

    {

        var motifSuperposition = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, motifSuperposition.BlendMode);

        Assert.AreEqual(127, motifSuperposition.Opacity);

        Assert.AreEqual(true, motifSuperposition.IsVisible);

        var parametres = motifSuperposition.Settings;

        Assert.AreEqual(Color.Empty, parametres.Color);

        Assert.AreEqual(FillType.Pattern, parametres.FillType);

        Assert.AreEqual("85163837-eb9e-5b43-86fb-e6d5963ea29a\0", parametres.PatternId);

        Assert.AreEqual("$$$/Presets/Patterns/OpticalSquares=Optical Squares\0", parametres.PatternName);

        Assert.AreEqual(null, parametres.PointType);

        Assert.AreEqual(100, parametres.Scale);

        Assert.AreEqual(false, parametres.Linked);

        Assert.IsTrue(Math.Abs(0 - parametres.HorizontalOffset) < 0.001, "Le décalage horizontal est incorrect");

        Assert.IsTrue(Math.Abs(0 - parametres.VerticalOffset) < 0.001, "Le décalage vertical est incorrect");

        // Test d'édition

        parametres.Color = Color.Green;

        motifSuperposition.Opacity = 193;

        motifSuperposition.BlendMode = BlendMode.Difference;        

        parametres.HorizontalOffset = 15;

        parametres.VerticalOffset = 11;

        PattResource ressource;

        foreach (var ressourceCalqueGlobal in im.GlobalLayerResources)

        {

            if (ressourceCalqueGlobal is PatternResource)

            {

                ressource = (PatternResource)ressourceCalqueGlobal;

                ressource.PatternId = identifiant.ToString();

                ressource.Name = nouveauNomMotif;

                ressource.SetPattern(nouveauMotif, nouvellesBornesMotif);

            }

        }

        parametres.PatternName = nouveauNomMotif;

        parametres.PatternId = identifiant.ToString() + "\0";

        im.Save(cheminExportation);

    }

    // Fichier test après modification

    using (var im = (PsdImage)Image.Load(nomFichierSource, optionsChargement))

    {

        var motifSuperposition = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Difference, motifSuperposition.BlendMode);

        Assert.AreEqual(193, motifSuperposition.Opacity);

        Assert.AreEqual(true, motifSuperposition.IsVisible);

        var parametres = motifSuperposition.Settings;


        Assert.AreEqual(Color.Empty, parametres.Color);       

        Assert.AreEqual(FillType.Pattern, parametres.FillType);

        PattResource ressource = null;

        foreach (var ressourceCalqueGlobal in im.GlobalLayerResources)

        {

             if (ressourceCalqueGlobal is PatternResource)

             {

                 ressource = (PatternResource)ressourceCalqueGlobal;

             }

        }

        if (ressource == null)

        {

             throw new Exception("Ressource motif non trouvée");

        }

        // Vérifier les données du motif

        Assert.AreEqual(nouveauMotif, ressource.PatternData);

        Assert.AreEqual(nouvellesBornesMotif, new Rectangle(0, 0, ressource.Width, ressource.Height));

        Assert.AreEqual(identifiant.ToString(), ressource.PatternId);

    }

{{< /highlight >}}
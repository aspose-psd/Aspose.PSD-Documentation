---
title: Aspose.PSD pour .NET 19.10 - Notes de publication
type: docs
weight: 30
url: /fr/net/aspose-psd-for-net-19-10-release-notes/
---

{{% alert color="primary" %}} 

Cette page contient les notes de publication pour Aspose.PSD pour .NET 19.10

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-207|[Support de la couche d'ajustement d'équilibre des couleurs](/psd/fr/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|Fonctionnalité|
|PSDNET-145|[Support de la couche d'ajustement d'inversion](/psd/fr/net/modifying-images/#modifyingimages-invertadjustmentlayer)|Fonctionnalité|
|PSDNET-139|[Implémenter le rééchantillonneur bicubique](/psd/fr/net/modifying-images/#modifyingimages-implementbicubicresampling)|Fonctionnalité|
|PSDNET-169|[Ajouter le support de l'exportation PSD en PDF avec masque de découpe](/psd/fr/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|Fonctionnalité|
|PSDNET-168|[Ajouter le support de l'exportation PSD en PDF avec des couches d'ajustement](/psd/fr/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|Fonctionnalité|
|PSDNET-179|Problème Obtenir Effet d'Ombre Portée de la Couche|Amélioration|
|PSDNET-203|Lors de la mise à jour du texte avec des caractères / (barre oblique), le fichier ne peut pas être ouvert dans Photoshop|Bogue|
|PSDNET-199|Le fichier PSD ne peut pas être enregistré lorsque la couche de texte contient uniquement un saut de ligne|Bogue|
|PSDNET-185|Taille de police extraite incorrecte|Bogue|

## **Changements de l'API publique**
# **APIs ajoutées :**
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F:Aspose.PSD.ResizeType.CatmullRom
- F:Aspose.PSD.ResizeType.CubicConvolution
- F:Aspose.PSD.ResizeType.CubicBSpline
- F:Aspose.PSD.ResizeType.Mitchell
- F:Aspose.PSD.ResizeType.SinC
- F:Aspose.PSD.ResizeType.Bell
# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**
**PSDNET-207. Support de la couche d'ajustement d'équilibre des couleurs**

{{< highlight java >}}

            var cheminFichier = "ColorBalance.psd";

            var cheminSortie = "ColorBalance_sortie.psd";

            using (var im = (PsdImage)Image.Load(cheminFichier))

            {

                foreach (var couche in im.Layers)

                {

                    var coucheEqCou = couche as ColorBalanceAdjustmentLayer;

                    if (coucheEqCou != null)

                    {

                        coucheEqCou.ShadowsCyanRedBalance = 30;

                        coucheEqCou.ShadowsMagentaGreenBalance = -15;

                        coucheEqCou.ShadowsYellowBlueBalance = 40;

                        coucheEqCou.MidtonesCyanRedBalance = -90;

                        coucheEqCou.MidtonesMagentaGreenBalance = -25;

                        coucheEqCou.MidtonesYellowBlueBalance = 20;

                        coucheEqCou.HighlightsCyanRedBalance = -30;

                        coucheEqCou.HighlightsMagentaGreenBalance = 67;

                        coucheEqCou.HighlightsYellowBlueBalance = -95;

                        coucheEqCou.PreserveLuminosity = true;

                    }

                }

                im.Save(cheminSortie);

            }

{{< /highlight >}}

**PSDNET-145. Support de la couche d'ajustement d'inversion**

{{< highlight java >}}

            var cheminFichier = "InvertStripes_avant.psd";

            var cheminSortie = "InvertStripes_apres.psd";

            using (var im = (PsdImage)Image.Load(cheminFichier))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(cheminSortie);

            }

{{< /highlight >}}

**PSDNET-139. Implémenter le rééchantillonneur bicubique**

{{< highlight java >}}

             string fichierSource = "sample.psd";

            string nomDest = "ResamplerCubicConvolutionStripes_apres.psd";

            // Charger une image existante dans une instance de la classe PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fichierSource))

            {

                image.Resize(300, 300, ResizeType.CubicConvolution);

                image.Save(nomDest, new PsdOptions(image));

            }

            string fichierSource = "sample.psd";

            string nomDest = "ResamplerCatmullRomStripes_apres.psd";

            // Charger une image existante dans une instance de la classe PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fichierSource))

            {

                image.Resize(300, 300, ResizeType.CatmullRom);

                image.Save(nomDest, new PsdOptions(image));

            }

            string fichierSource = "sample.psd";

            string nomDest = "ResamplerMitchellStripes_apres.psd";

            // Charger une image existante dans une instance de la classe PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fichierSource))

            {

                image.Resize(300, 300, ResizeType.Mitchell);

                image.Save(nomDest, new PsdOptions(image));

            }

            string fichierSource = "sample.psd";

            string nomDest = "ResamplerCubicBSplineStripes_apres.psd";

            // Charger une image existante dans une instance de la classe PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fichierSource))

            {

                image.Resize(300, 300, ResizeType.CubicBSpline);

                image.Save(nomDest, new PsdOptions(image));

            }

            string fichierSource = "sample.psd";

            string nomDest = "ResamplerSinCStripes_apres.psd";

            // Charger une image existante dans une instance de la classe PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fichierSource))

            {

                image.Resize(300, 300, ResizeType.SinC);

                image.Save(nomDest, new PsdOptions(image));

            }

            string fichierSource = "sample.psd";

            string nomDest = "ResamplerBellStripes_apres.psd";

            // Charger une image existante dans une instance de la classe PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fichierSource))

            {

                image.Resize(300, 300, ResizeType.Bell);

                image.Save(nomDest, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-169. Ajouter le support de l'exportation PSD en PDF avec masque de découpe**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-168. Ajouter le support de l'exportation PSD en PDF avec des couches d'ajustement**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("exemple.psd"))

    {

      image.Save("document.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. Lors de la mise à jour du texte avec / (barre oblique), le fichier ne peut pas être ouvert dans Photoshop**

{{< highlight java >}}

         var psdImage = (PsdImage)image;

        var layers = psdImage.Layers;

        for (var index = layers.Length - 1; index >= 0; index--)

        {

            var layer = layers[index];

            if (!(layer is TextLayer)) continue;

            var textLayer = (TextLayer)layer;

            textLayer.UpdateText("/");

        }

        var imageOptions = new PsdOptions(psdImage);

        var nomFichier = Path.GetFileName(cheminFichier);

        var cheminSortieFichier = Path.GetDirectoryName(cheminFichier) + "\\cible_" + nomFichier;

        psdImage.Save(cheminSortieFichier, imageOptions);



{{< /highlight >}}

**PSDNET-199. Le fichier PSD ne peut pas être enregistré lorsque la couche de texte contient uniquement un saut de ligne**

{{< highlight java >}}

 string cheminFichier = "testLineBreaks2.psd";

string cheminSortie = "testLineBreaks2_modifie.psd";

var nouveauTexte = "\r";

        using (var image = Image.Load(cheminFichier))

        {

            var psdImage = image as PsdImage;

            if (image == null)

            {

                return;

            }

            var layers = psdImage.Layers;

            for (var index = layers.Length - 1; index >= 0; index--)

            {

                var layer = layers[index] as TextLayer;

                if (layer == null)

                {

                    continue;

                }

                layer.UpdateText(nouveauTexte);

            }

            var imageOptions = new PsdOptions(psdImage);

            psdImage.Save(cheminSortie, imageOptions);

        }

{{< /highlight >}}

**PSDNET-185. Taille de police extraite incorrecte**

{{< highlight java >}}

             // Taille de police extraite incorrecte

            string cheminFichier = "直播+电商.psd";

            var tolérance = 0,001;

            using (var image = Image.Load(cheminFichier))

            {

                int indexCouche = 22;

                // Ancienne API (Utilisation de la première taille de police du paragraphe)

                PsdImage psdImage = image as PsdImage;

                double[] matrice = ((TextLayer)psdImage.Layers[indexCouche]).TransformMatrix;

                double taillePoliceBase = ((TextLayer)psdImage.Layers[indexCouche]).Font.Size;

                double taillePolice = matrice[0] * taillePoliceBase;

                // Vérification de la taille de police de base

                if (Math.Abs(100,0 - taillePoliceBase) > tolérance)

                {

                    throw new Exception("La taille de police a été lue incorrectement");

                }

                // Vérification de la taille de police réelle

                if (Math.Abs(88,425 - taillePolice) > tolérance)

                {

                    throw new Exception("La matrice de transformation a été lue incorrectement");

                }

                // Nouvelle API (Une seule couche de texte peut contenir une quantité quelconque de tailles de police)

                ITextPortion[] portions = ((TextLayer)psdImage.Layers[indexCouche]).TextData.Items;

                ITextStyle style = portions[0].Style;

                double taillePolicePortion = matrice[0] * style.FontSize;

                // Vérification de la taille de police de la portion de base

                if (Math.Abs(100,0 - style.FontSize) > tolérance)

                {

                    throw new Exception("La taille de police a été lue incorrectement");

                }

                // Vérification de la taille de police réelle de la portion

                if (Math.Abs(88,425 - taillePolicePortion) > tolérance)

                {

                    throw new Exception("La matrice de transformation a été lue incorrectement");

                }

            }

{{< /highlight >}}

**PSDNET-179. Problème Obtenir Effet d'Ombre Portée de la Couche**

{{< highlight java >}}

       // Lorsque la propriété DropShadowEffect.UseGlobalLight est 'true', alors l'objet DropShadowEffect utilise la valeur d'angle de la propriété PsdImage.GlobalAngle.

		using (PsdImage image = (PsdImage)Image.Load("4.psd"))

		{

    		image.GlobalAngle = 30;

    		image.Save("output.psd");

		}

{{< /highlight >}}
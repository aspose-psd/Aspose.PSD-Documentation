---
title: Notes de version d'Aspose.PSD pour .NET 22.9
type: docs
weight: 40
url: /fr/net/aspose-psd-pour-net-22-9-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Cette version présente une régression dans le cas des exports 16 bits, nous vous recommandons donc d'être prudents lors de l'utilisation de cette fonctionnalité dans cette version.
Veuillez ne pas mettre à jour Aspose.PSD vers 22.9 si le traitement d'image 16 bits est votre fonctionnalité principale.
- Pour plusieurs versions de Photoshop, les utilisateurs peuvent rencontrer une fenêtre avec une erreur de lecture de calque, cela n'affectera pas le travail avec le fichier PSD.

Nous travaillons sur des solutions à ces problèmes.

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-1237|Créer le modèle interne LayerStyleFX qui contiendra des effets et des données connexes pour utiliser le modèle unique dans les ressources d'effets Lfx2, lmfx, et mlst|Amélioration|
|PSDNET-1227|Ajouter la lecture et l'écriture des structures 'Lefx' avec les informations d'effets pour les états de calque dans les modèles de ligne de temps|Fonction|
|PSDNET-1230|Application de l'état de calque de la ligne de temps au calque dans PsdImage|Fonction|
|PSDNET-1072|Transparence incorrecte lors de la sauvegarde du fichier PSD (RGB/16 bits) lors de l'exportation en 8 bits|Bogue|
|PSDNET-1140|Exception lors du chargement de l'étape de ressources de calque globales lors de l'ouverture d'un document PSB|Bogue|
|PSDNET-1266|Fuite de mémoire lors du traitement de fichiers spécifiques|Bogue|


## **Changements d'API publics**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **APIs retirées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Exemples d'utilisation :**
 
**PSDNET-1072. Transparence incorrecte lors de la sauvegarde du fichier PSD (RGB/16 bits) lors de l'exportation en 8 bits**

{{< highlight csharp >}}
string fichierPsdEntree    = "8bitAvecTransparence.psd";
string fichierPsdSortie    = "16bitAvecTransparence.psd";
string fichierImageSortie  = "SortieAvecTransparence.png";

using (var img = Image.Load(fichierPsdEntree))
{
    // Options de sauvegarde 16 bits
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(fichierPsdSortie, p16);
}
using (var img = Image.Load(fichierPsdSortie))
{
    // Enregistrer l'image avec des couleurs 16 bits
    img.Save(fichierImageSortie, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Exception lors du chargement de l'étape de ressources de calque globales lors de l'ouverture d'un document PSB**

{{< highlight csharp >}}
string fichierPsbSource = "entrée.psb";
string fichierImageSortie = "sortie.png";

using (var image = (PsdImage)Image.Load(fichierPsbSource))
{
    // Il ne devrait y avoir aucune exception ici.
    image.Save(fichierImageSortie, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Ajouter la lecture et l'écriture des structures 'Lefx' avec les informations d'effets pour les états de calque dans les modèles de ligne de temps**

{{< highlight csharp >}}
string fichierSource = "4_animé.psd";
string fichierSortie = "sortie.psd";

using (var psdImage = (PsdImage)Image.Load(fichierSource))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] idsCalque = timeLine.LayerIds;

    var effetsEtatCalque11 = timeLine.Frames[1].LayerStates[idsCalque[1]].StateEffects;

    effetsEtatCalque11.AddDropShadow();
    effetsEtatCalque11.AddGradientOverlay();

    var effetsEtatCalque21 = timeLine.Frames[2].LayerStates[idsCalque[1]].StateEffects;
    effetsEtatCalque21.AddStroke(FillType.Color);
    effetsEtatCalque21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(fichierSortie);
}
{{< /highlight >}}

**PSDNET-1230. Application de l'état de calque de la ligne de temps au calque dans PsdImage**

{{< highlight csharp >}}
string fichierSource = "3_animé.psd";
string fichierPsdSortie = "sortie.psd";
string fichierPngSortie = "sortie.png";

using (var psdImage = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var idsCalque = timeLine.LayerIds;

    var etatCalque11 = timeLine.Frames[1].LayerStates[idsCalque[1]];

    timeLine.Frames[1].LayerStates[idsCalque[1]].StateEffects.AddPatternOverlay();
    etatCalque11.BlendMode = BlendMode.Multiply;

    // Changer le cadre actif de 0 à 1 pour activer l'application de LayerState au calque
    timeLine.ActiveFrame = 1;

    // Appliquer les changements à PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(fichierPsdSortie);
    psdImage.Save(fichierPngSortie, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Fuite de mémoire lors du traitement de fichiers spécifiques**

{{< highlight csharp >}}
string[] fichiersACharger = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int numeroEntree = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(numeroEntree, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double compteurMémoire = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total des octets utilisés avant le test : {0:N2} Mio", compteurMémoire);

double max = compteurMémoire;

for (int i = 0; i < 50; i++)
{
    int indiceFichier = i % numeroEntree;
    string fichierSource = Path.Combine(dossierBase, fichiersACharger[indiceFichier]);

    // VérificationOuvertureSauvegarde
    using (MemoryStream fluxSortie = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(fluxSortie, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(numeroEntree, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    compteurMémoire = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, compteurMémoire);
}

compteurMémoire = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total des octets utilisés après le test : {0:N2} Mio", compteurMémoire);
Assert.IsTrue(Math.Abs(compteurMémoire - max) < 20, "Fuite de mémoire trouvée dans la fonctionnalité de base !");
{{< /highlight >}}

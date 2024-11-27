---
title: Aspose.PSD pour .NET 22.8 - Notes de version
type: docs
weight: 50
url: /fr/net/aspose-psd-pour-net-22-8-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-1225|Investigation et correction des problèmes dans l'installateur|Amélioration|
|PSDNET-800|Support de la chronologie des trames à partir du fichier PSD|Fonctionnalité|
|PSDNET-1219|Support de la ressource 'mlst' contenue dans ShmdResource en tant que sous-ressource|Fonctionnalité|
|PSDNET-814|Le hachage de la couche change si nous appelons layer.BlendingOptions.Effects|Bogue|


## **Changements de l'API publique**
# **APIs ajoutées :**
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Delay
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.LayerStates
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.DisposalMethod
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Automatic
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.DoNotDispose
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Dispose
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.HorizontalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.VerticalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.FillOpacity
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.DescriptorVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.SubResourcesx


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation :**

**PSDNET-800. Support de la chronologie des trames à partir du fichier PSD**

{{< highlight csharp >}}
string fichierSource = "image1219.psd";
string psdSortie = "output_image800.psd";

using (PsdImage imagePsd = (PsdImage)Image.Load(fichierSource))
{
    TimeLine timeLine = TimeLine.InitializeFrom(imagePsd);

    // Changer la méthode de disposition de la trame 1
    timeLine.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;

    // Changer le délai de la trame 2
    timeLine.Frames[1].Delay = 15;

    // Changer l'opacité de la 'Couche 1' sur la trame 2
    LayerState etatCouche11 = timeLine.Frames[1].LayerStates[timeLine.LayerIds[1]];
    etatCouche11.Opacity = 50;

    // Déplacer la 'Couche 1' en bas à gauche sur la trame 3
    LayerState etatCouche21 = timeLine.Frames[2].LayerStates[timeLine.LayerIds[1]];
    etatCouche21.Offset = new Point(-50, 230);

    // Ajouter une nouvelle trame
    List<Frame> trames = new List<Frame>(timeLine.Frames);
    trames.Add(new Frame(timeLine));
    timeLine.Frames = trames.ToArray();

    // Changer le mode de fusion de 'Couche 1' sur la trame 4
    LayerState etatCouche31 = timeLine.Frames[3].LayerStates[timeLine.LayerIds[1]];
    etatCouche31.BlendMode = BlendMode.Dissolve;

    // Appliquer les changements à l'instance PsdImage
    timeLine.ApplyTo(imagePsd);
    imagePsd.Save(psdSortie);
}
{{< /highlight >}}

**PSDNET-814. Le hachage de la couche change si nous appelons layer.BlendingOptions.Effects**

{{< highlight csharp >}}
string fichierSource = "AllTypesLayerPsd.psd";

using (var image = (PsdImage)Image.Load(fichierSource))
{
    var couche = image.Layers[0];
    var hachageDebut = couche.GetHashCode();
    var effets = couche.BlendingOptions.Effects;
    var hachageFin = couche.GetHashCode();

    if (hachageDebut != hachageFin)
    {
        throw new Exception("Le hachage ne doit pas changer");
    }
}
{{< /highlight >}}

**PSDNET-1219. Support de la ressource 'mlst' contenue dans ShmdResource en tant que sous-ressource**

{{< highlight csharp >}}
string fichierSource = "image1219.psd";
string psdSortie = "output_image1219.psd";

using (PsdImage image = (PsdImage)Image.Load(fichierSource))
{
    Layer couche1 = image.Layers[1];
    ShmdResource shmdResource = (ShmdResource)couche1.Resources[8];
    MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];

    ListStructure listeStatesCouche = (ListStructure)mlstResource.Items[1];
    DescriptorStructure layersStateSurTrame1 = (DescriptorStructure)listeStatesCouche.Types[1];
    BooleanStructure coucheActivee = (BooleanStructure)layersStateSurTrame1.Structures[0];

    // Désactiver la couche 1 sur la trame 1
    coucheActivee.Value = false;

    image.Save(psdSortie);
}
{{< /highlight >}}

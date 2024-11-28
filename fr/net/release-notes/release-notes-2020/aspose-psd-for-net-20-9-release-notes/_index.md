---
title: Aspose.PSD pour .NET 20.9 - Notes de version
type: docs
weight: 40
url: /fr/net/aspose-psd-for-net-20-9-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version de [Aspose.PSD pour .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-408|Support de SoLEResource (Ressource externe de calque d'objet intelligent)|Fonctionnalité|
|PSDNET-614|Support des objets intelligents liés|Fonctionnalité|
|PSDNET-615|Support des objets intelligents incorporés|Fonctionnalité|
|PSDNET-690|Mise à jour du texte dans un fichier PSD donné et enregistrement qui modifie certains calques et de nombreux paramètres de texte|Bogue|
|PSDNET-696|Les calques de remplissage ne sont pas mis à jour après la création et ne peuvent pas être rendus correctement|Bogue|
|PSDNET-712|Régression : Aspose.PSD 20.8.0 ne peut pas ouvrir le fichier|Bogue|
|PSDNET-714|Dans un fichier PSD spécifique, le redimensionnement de TextLayer casse la valeur d'emplacement|Bogue|

## **Changements d'API publique**
# **API ajoutées :**

- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- ...
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.EmbedAllLinked
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.UpdateAllModifiedContent
- ...

# **APIs supprimées :**

- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- ...
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Exemples d'utilisation :**

**PSDNET-408. Prise en charge de SoLEResource (Ressource externe de calque d'objet intelligent)**
{{< highlight csharp >}}
// Code d'exemple ici...
{{< /highlight >}}

**PSDNET-614. Support des objets intelligents liés**
{{< highlight csharp >}}
// Code d'exemple ici...
{{< /highlight >}}

**PSDNET-615. Support des objets intelligents incorporés**
{{< highlight csharp >}}
// Code d'exemple ici...
{{< /highlight >}}

**PSDNET-690. Mise à jour du texte dans un fichier PSD donné et enregistrement qui modifie certains calques et de nombreux paramètres de texte**
{{< highlight csharp >}}
// Code d'exemple ici...
{{< /highlight >}}

**PSDNET-696. Les calques de remplissage ne sont pas mis à jour après la création et ne peuvent pas être rendus correctement**
{{< highlight csharp >}}
// Code d'exemple ici...
{{< /highlight >}}

**PSDNET-712. Régression : Aspose.PSD 20.8.0 ne peut pas ouvrir le fichier**
{{< highlight csharp >}}
// Code d'exemple ici...
{{< /highlight >}}

**PSDNET-714. Dans un fichier PSD spécifique, le redimensionnement de TextLayer casse la valeur d'emplacement**
{{< highlight csharp >}}
// Code d'exemple ici...
{{< /highlight >}}```csharp
conversion.EmbedAllLinked();
foreach (Layer layer in image.Layers)
{
    var smartLayer = layer as SmartObjectLayer;
    if (smartLayer != null)
    {
        AssertAreEqual(SmartObjectType.Embedded, smartLayer.ContentType);
    }
}

}

// Vérifions si l'image convertie est enregistrée correctement
image.Save(psdOutputPath, new PsdOptions(image));
image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}

using (PsdImage image = (PsdImage)Image.Load(psdOutputPath))
{
    var smartObjectLayer = (SmartObjectLayer)image.Layers[0];
    AssertAreEqual(contentsLength, smartObjectLayer.Contents.Length);
    AssertAreEqual(left, smartObjectLayer.ContentsBounds.Left);
    AssertAreEqual(top, smartObjectLayer.ContentsBounds.Top);
    AssertAreEqual(right, smartObjectLayer.ContentsBounds.Right);
    AssertAreEqual(bottom, smartObjectLayer.ContentsBounds.Bottom);
    AssertAreEqual(SmartObjectType.Embedded, smartObjectLayer.ContentType);
}
}

// Cet exemple montre comment changer le calque d'objet intelligent externe Adobe® Photoshop® et exporter / mettre
```
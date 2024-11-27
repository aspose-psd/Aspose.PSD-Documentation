---
title: Notes de version Aspose.PSD Adapters pour .NET 24.4
type: docs
weight: 100
url: /fr/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD Adapters pour .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                          | **Catégorie** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Publication initiale de Aspose.PSD.Adapters.Imaging sur Nuget      | Amélioration |


## **Changements dans l'API publique**
# **APIs ajoutées :**
- Aucune

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**

Veuillez consulter la [page de documentation Aspose.PSD.Adapters](/psd/fr/net/adapters)

**PSDNET-1985. Exemple le plus complet de l'utilisation d'Aspose.PSD Adapters**

{{< highlight csharp >}}
// Ajoutez l'activation des adaptateurs dans votre configuration initiale
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// Activez également les exportateurs
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Pour travailler avec les adaptateurs, vous avez besoin des licences Aspose.PSD et adaptee
// Voici comment appliquer la licence Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Voici un exemple de comment appliquer la licence Adaptee pour Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Ensuite, vous pouvez exécuter n'importe quel code des adaptateurs ou de la bibliothèque PSD ou Imaging

// Après cela, tous ces fichiers peuvent être ouverts par Aspose.PSD sans aucun code supplémentaire, il suffit d'utiliser
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Après l'exécution de ce code, vous obtiendrez le fichier PSD créé à partir de WEBP et pourrez appliquer tous les filtres, calques et ajustements Aspose.PSD, y compris la transformation Warp
}

// Vous pouvez également créer des adaptateurs Export des images vers le format PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Utilisez l'API Aspose.Imaging pour modifier le fichier WEBP avec des fonctionnalités spécifiques à Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Ensuite, utilisez simplement la méthode ToPsdImage() et modifiez le fichier comme un PSD avec des fonctionnalités semblables à Photoshop, y compris les calques, les filtres intelligents et les objets intelligents.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Enregistrez le fichier PSD final en utilisant Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Si vous n'avez pas besoin d'utiliser les Chargeurs ou Exportateurs fournis par les Adaptateurs, il suffit de les désactiver
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}

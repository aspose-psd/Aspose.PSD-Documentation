---
title: Aspose.PSD pour .NET 20.12 - Notes de version
type: docs
weight: 10
url: /fr/net/aspose-psd-for-net-20-12-release-notes/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD pour .NET 20.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-757|Prise en charge de la conversion des calques en calque d'objet intelligent|Fonctionnalité|
|PSDNET-764|La méthode SmartObjectLayer.ReplaceContents lance une NullReferenceException si nous essayons d'ajouter un fichier PSB|Bogue|
|PSDNET-773|Rendu incorrect des images CMJN 8 bits et CMJN 16 bits, si le calque est plus grand que le canevas|Bogue|
|PSDNET-782|Le fichier PSB enregistré peut être ouvert avec notre API, mais pas avec Photoshop|Bogue|
|PSDNET-783|Si nous essayons de modifier un calque intelligent dans un PSD spécifique avec une source de données partagée, nous obtenons une exception|Bogue|
|PSDNET-172|Renommer FileFormatVersion en PsdVersion pour éviter les confusions|Amélioration|
|PSDNET-620|Supprimer la configuration du framework Compact de Aspose.PSD .NET|Amélioration|
|PSDNET-765|PsdImageException: En-tête de ressource inconnu en essayant d'ouvrir un fichier PSB avec des calques SmartObject|Amélioration|
|PSDNET-798|Déplacer la hiérarchie des classes de masque vectoriel vers l'espace de noms Core pour assurer l'uniformité des produits Aspose.PSD et Aspose.Imaging|Amélioration|

## **Modifications de l'API publique**
# **APIs ajoutées:**
- T:Aspose.PSD.FileFormats.Psd.PsdVersion
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.PsdVersion
- T:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord
- M:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord.#ctor(System.Byte[])
-...

# **APIs supprimées:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- T:Aspose.PSD.FileFormats.Psd.Layers.BlendMode
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Color
-...

## **Exemples d'utilisation:**
**PSDNET-757. Prise en charge de la conversion des calques en calque d'objet intelligent**
{{< highlight csharp >}}
            string dataDir = "PSDNET757_1\\";
            string outputDir = dataDir + "output\\";

            // Ces exemples montrent comment convertir des calques en un calque d'objet intelligent dans le fichier PSD
            ExampleOfConvertingToSmartObjectLayer("TroisCalquesReguliers", 0, 1);
            ExampleOfConvertingToSmartObjectLayer("QuatreAvecMasques", 0, 2);
            ExampleOfConvertingToSmartObjectLayer("factice", 2, 3, 1);
            ExampleOfConvertingToSmartObjectLayer("groupeFactice", 6, 2);
            ExampleOfConvertingToSmartObjectLayer("argb16bits_5x5", 0);
            ExampleOfConvertingToSmartObjectLayer("cmyk16bits_5x5", 0);
            ExampleOfConvertingToSmartObjectLayer("niveauxDeGris5x5", 0);

            void ExampleOfConvertingToSmartObjectLayer(string filePath, params int[] layerNumbers)
            {
                string outputFilePath = outputDir + "Converti_" + filePath + ".psd";
                string pngOutputPath = Path.ChangeExtension(outputFilePath, ".png");
                using (PsdImage image = (PsdImage)Image.Load(dataDir + filePath + ".psd"))
                {
                    var layerCount = image.Layers.Length;
                    var smartObjectLayer = image.SmartObjectProvider.ConvertToSmartObject(layerNumbers);
                    var newLayerCount = image.Layers.Length;

                    image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                    image.Save(outputFilePath, new PsdOptions(image));
                }
            }
{{< /highlight >}}
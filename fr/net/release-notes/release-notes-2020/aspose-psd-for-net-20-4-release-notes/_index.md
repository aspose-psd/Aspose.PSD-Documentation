---
title: Notes de version Aspose.PSD pour .NET 20.4
type: docs
weight: 90
url: /fr/net/aspose-psd-pour-net-20-4-notes-de-version/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD pour .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-567|Prise en charge de la ressource 'Données d'origine vectorielle'|Fonctionnalité|
|PSDNET-373|Prise en charge de lclrResource (Paramètres de couleur de la feuille)|Fonctionnalité|
|PSDNET-563|Prise en charge des propriétés des données LengthRecord. (Opérations de tracé (opérations booléennes), index de la forme dans le calque, nombre d’enregistrements de nœuds Bezier)|Fonctionnalité|
|PSDNET-425|Prise en charge de la couleur d'arrière-plan de la ressource Image Section #1010|Fonctionnalité|
|PSDNET-530|Ajout de calques de remplissage à l'exécution|Fonctionnalité|
|PSDNET-424|Prise en charge des informations de bordure de la ressource Image Section #1009|Fonctionnalité|
|PSDNET-592|Prise en charge des calques dans les fichiers de format AI|Fonctionnalité|
|PSDNET-256|Prise en charge de la lecture et de la modification de l'effet de superposition de dégradé|Fonctionnalité|
|PSDNET-257|Rendu de l'effet de superposition de dégradé|Fonctionnalité|
|PSDNET-585|Le changement de la propriété BlendMode de GradientOverlayEffect n'est pas affiché dans Photoshop|Bogue|
|PSDNET-561|Correction de l'enregistrement d'une image PSD en mode couleur en niveaux de gris avec 16 bits par canal au format PSD en niveaux de gris|Bogue|
|PSDNET-560|Correction de l'enregistrement d'une image PSD en mode couleur en niveaux de gris avec 16 bits par canal au format PNG|Bogue|

## **Changements d'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**
**PSDNET-567. Prise en charge de la ressource 'Données d'origine vectorielle'**

{{< highlight java >}}

         // Prise en charge de VogkResource

        static void ExempleDePriseEnChargeVogkResource()

        {

            string nomFichier = "RessourceDonneesOrigineVectorielle.psd";

            string nomFichierSortie = "sortie_RessourceDonneesOrigineVectorielle_.psd";

            using (var imagePsd = (PsdImage)Image.Load(nomFichier))

            {

                var ressource = GetVogkResource(imagePsd);

                // Lecture

                if (ressource.ShapeOriginSettings.Length != 1 ||

                    !ressource.ShapeOriginSettings[0].IsShapeInvalidated ||

                    ressource.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource a été lu à tort.");

                }

                // Édition

                ressource.ShapeOriginSettings = new[]

                {

                    ressource.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                imagePsd.Save(nomFichierSortie);

            }

        }

        static VogkResource GetVogkResource(PsdImage image)

        {

            var calque = image.Layers[1];

            VogkResource ressource = null;

            var ressources = calque.Resources;

            for (int i = 0; i < ressources.Length; i++)

            {

                if (ressources[i] is VogkResource)

                {

                    ressource = (VogkResource)ressources[i];

                    break;

                }

            }

            if (ressource == null)

            {

                throw new Exception("La ressource VogkResource n'a pas été trouvée.");

            }

            return ressource;

        }   

{{< /highlight >}}
...

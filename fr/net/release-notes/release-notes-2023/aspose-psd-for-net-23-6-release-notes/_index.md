---
title: Notes de version Aspose.PSD pour .NET 23.6
type: docs
weight: 70
url: /fr/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}
Cette page contient les notes de version pour [Aspose.PSD pour .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)
{{% /alert %}}

| **Clé**     | **Résumé**                                                                                                                                      | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Refactoriser l'API TimeLine                                                                                                                      | Amélioration  |
| PSDNET-1517 | Supprimer les artefacts lors du rendu de la déformation                                                                                           | Amélioration  |
| PSDNET-1528 | Optimisation du rendu de déformation                                                                                                             | Amélioration  |
| PSDNET-147  | Support de la couche d'ajustement seuil                                                                                                           | Fonctionnalité |
| PSDNET-149  | Support de la couche d'ajustement de la couleur sélective                                                                                         | Fonctionnalité |
| PSDNET-801  | Possibilité d'exporter la timeline PSD vers le fichier GIF animé                                                                                 | Fonctionnalité |
| PSDNET-1555 | Ajouter le support des calques de texte sans bordures rectangulaires                                                                              | Fonctionnalité |
| PSDNET-1582 | Support de la couche de forme                                                                                                                    | Fonctionnalité |
| PSDNET-864  | Le remplacement de l'image dans un objet intelligent ne se met pas à jour                                                                        | Bug          |
| PSDNET-1404 | Impossible de sauvegarder le fichier PSD en tant que PSD avec l'exception suivante : Les modes Rgb et Lab ne peuvent pas contenir moins de 3 canaux et plus de 4 canaux | Bug          |
| PSDNET-1546 | La justification du texte est perdue si l'on ouvre le calque de texte en mode édition de Photoshop                                               | Bug          |
| PSDNET-1548 | Exception de référence nulle lors de la sauvegarde du fichier PSD                                                                                | Bug          |
| PSDNET-1578 | Exception lors du chargement du calque de forme : Les points pour les limites vectorielles d'origine ne sont pas encore pris en charge          | Bug          |
| PSDNET-1579 | Exception lors du chargement de VogkResource : Les points sont enregistrés en tant que DoubleStructures, nous les lisons comme UnitStructures   | Bug          |
| PSDNET-1581 | LayerType de ShapeLayer est vide                                                                                                                 | Bug          |


## **Modifications de l'API publique**
# **APIs ajoutées :**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(Système.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(Système.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(Système.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers. 
...
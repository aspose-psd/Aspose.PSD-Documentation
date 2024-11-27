---
title: Notes de version Aspose.PSD pour Python via .NET 24.8
type: docs
weight: 10
url: /fr/python-net/aspose-psd-for-python-via-net-24-8-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour Python via .NET 24.8](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                                                                       | **Catégorie** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-81 | [AI Format] Ajout de la gestion des groupes XObject                                                             | Amélioration  |
| PSDPYTHON-82 | Améliorer les capacités de transformation de déformation en ajoutant WarpSettings pour TextLayer et SmartObjectLayer | Fonctionnalité      |
| PSDPYTHON-83 | [Format AI] Gérer les calques dans les opérateurs de flux de contenu                                             | Fonctionnalité      |
| PSDPYTHON-84 | Le résultat de rendu du fichier AI est très différent de celui des résultats Illustrator                        | Problème         |
| PSDPYTHON-85 | Le remplacement de l'objet intelligent ne s'applique pas à tous les objets intelligents dans le fichier PSD     | Problème         |

## **Changements de l'API publique**
# **APIs ajoutées:**

- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.WarpSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.WarpSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[],Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Rotate
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.MeshPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Horizontal
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Vertical
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.None
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Custom
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arc
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcUpper
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcLower
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arch
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Bulge
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Flag
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Fish
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Rise
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Wave
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Twist
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Squeeze
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Inflate

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDPYTHON-81. [Format AI] Ajouter la gestion des groupes XObject**
{{< highlight python >}}
# Aucun exemple. Il s'agit d'une amélioration interne
{{< /highlight >}}

**PSDPYTHON-82. Améliorer les capacités de transformation de déformation en ajoutant WarpSettings pour TextLayer et SmartObjectLayer**
{{< highlight python >}}
        fichierSource = "smart_without_warp.psd"

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True
        fichierImageSortie = [None] * 4
        fichierPsdSortie = [None] * 4
        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        for indiceCase in range(len(fichierImageSortie)):
            fichierImageSortie[indiceCase] = "export_" + str(indiceCase) + ".png"
            fichierPsdSortie[indiceCase] = "export_" + str(indiceCase) + ".psd"

            with PsdImage.load(fichierSource, opt) as image:
                img = cast(PsdImage, image)
                for calque in img.layers:
                    if is_assignable(calque, SmartObjectLayer):
                        calqueIntelligent = cast(SmartObjectLayer, calque)
                        calqueIntelligent.warp_settings = GetWarpSettingsByIndex(calqueIntelligent.warp_settings, indiceCase)

                    if is_assignable(calque, TextLayer):
                        calqueTexte = cast(TextLayer, calque)
                        if indiceCase != 3:
                            calqueTexte.warp_settings = GetWarpSettingsByIndex(calqueTexte.warp_settings, indiceCase)

                img.save(fichierPsdSortie[indiceCase], PsdOptions())
                img.save(fichierImageSortie[indiceCase], PsdOptions())

            with PsdImage.load(fichierPsdSortie[indiceCase], opt) as img:
                img.save(fichierImageSortie[indiceCase], pngOpt)

        def GetWarpSettingsByIndex(parametresDeDeformation, indiceCase):
            switcher = {
                0: {"Style": WarpStyles.RISE, "Rotate": WarpRotates.HORIZONTAL, "Value": 20},
                1: {"Style": WarpStyles.RISE, "Rotate": WarpRotates.VERTICAL, "Value": 10},
                2: {"Style": WarpStyles.FLAG, "Rotate": WarpRotates.HORIZONTAL, "Value": 30},
                3: {"Style": WarpStyles.CUSTOM}
            }
            params = switcher.get(indiceCase)
            if params:
                parametresDeDeformation.style = params.get("Style")
                if params.get("Rotate") is not None:
                    parametresDeDeformation.rotate = params.get("Rotate")
                if params.get("Value") is not None:
                    parametresDeDeformation.value = params.get("Value")
                if indiceCase == 3:
                    parametresDeDeformation.mesh_points[2].y += 70

            return parametresDeDeformation
{{< /highlight >}}

**PSDPYTHON-83. [Format AI] Gérer les calques dans les opérateurs de flux de contenu**
{{< highlight python >}}
        fichierSource = "Layers-NoPen.ai"
        fichierSortie = "Layers-NoPen.output.png"

        with AiImage.load(fichierSource) as image:
            image.save(fichierSortie, PngOptions())    
{{< /highlight >}}

**PSDPYTHON-84. Le résultat de rendu du fichier AI est très différent de celui des résultats Illustrator**
{{< highlight python >}}
        fichierSource = "4.ai"
        fichierSortie = "4_output.png"
        fichierReference = "4_ethalon.png"

        with AiImage.load(fichierSource) as image:
            image.save(fichierSortie, PngOptions())
{{< /highlight >}}

**PSDPYTHON-85. Le remplacement de l'objet intelligent ne s'applique pas à tous les objets intelligents dans le fichier PSD**
{{< highlight python >}}
        fichiers = ["simple_test", "w22"]
        fichierDeChangement = "image(19).png"

        for fichier in fichiers:
            fichierSource = fichier + ".psd"
            fichierSortie = fichier + "_output.psd"
            with Image.load(fichierSource) as img:
                image = cast(PsdImage, img)
                for calque in image.layers:
                    if is_assignable(calque, SmartObjectLayer):
                        calqueIntelligent = cast(SmartObjectLayer, calque)
                        calqueIntelligent.replace_contents(fichierDeChangement)
                image.save(fichierSortie)           
{{< /highlight >}}

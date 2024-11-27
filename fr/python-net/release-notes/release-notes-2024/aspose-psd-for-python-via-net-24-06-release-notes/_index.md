---
title: Aspose.PSD pour Python via .NET 24.6 - Notes de version
type: docs
weight: 10
url: /fr/python-net/aspose-psd-for-python-via-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version de [Aspose.PSD pour Python via .NET 24.6](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                                                                       | **Catégorie** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-69 | Implémenter la prise en charge de la couche de carte de dégradé                                                   | Fonctionnalité      |
| PSDPYTHON-70 | [Format AI] Ajouter la prise en charge de Métadonnées XPacket au Format AI (Pour le moment non disponible pour la version Python)        | Fonctionnalité      |
| PSDPYTHON-71 | Implémenter les types de distorsion Décompression, Compression et Torsion                                                                        | Fonctionnalité      |
| PSDPYTHON-72 | Les modes Rgb et Lab ne peuvent pas contenir moins de 3 canaux et plus de 4 canaux dans le fichier avec des calques de planche artistique | Erreur          |
| PSDPYTHON-79 | La zone de traitement supérieure doit être positive. (Paramètre 'areaToProcess') lors du traitement d'un fichier spécifique          | Erreur          |
| PSDPYTHON-74 | L'image étendue sur la toile est rognée après la sauvegarde. Les données sont perdues mais l'aperçu est correct                                   | Erreur          |

## **Changements dans l'API publique**
# **APIs ajoutées:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDPYTHON-69. Implémenter la prise en charge de la couche de carte de dégradé**

{{< highlight python >}}
        sourceFile = "gradient_map_src.psd"
        outputFile = "gradient_map_src_output.psd"
      
        def AssertAreEqual(expected, actual, message=None):
            if expected != actual:
                raise Exception(message or "Les objets ne sont pas égaux.")

        with PsdImage.load(sourceFile) as image:
            im = cast(PsdImage, image)
            layer = im.add_gradient_map_adjustment_layer()
            layer.gradient_settings.reverse = True

            im.save(outputFile)

        with PsdImage.load(outputFile) as image:
            im = cast(PsdImage, image)
            gradient_map_layer = cast(GradientMapLayer, im.layers[1])
            gradient_settings = cast(GradientFillSettings, gradient_map_layer.gradient_settings)

            AssertAreEqual(0.0, gradient_settings.angle)
            AssertAreEqual(4096, gradient_settings.interpolation)
            AssertAreEqual(True, gradient_settings.reverse)
            AssertAreEqual(False, gradient_settings.align_with_layer)
            AssertAreEqual(False, gradient_settings.dither)
            AssertAreEqual(GradientType.LINEAR, gradient_settings.gradient_type)
            AssertAreEqual(100, gradient_settings.scale)
            AssertAreEqual(0.0, gradient_settings.horizontal_offset)
            AssertAreEqual(0.0, gradient_settings.vertical_offset)
            AssertAreEqual("Personnalisé", gradient_settings.gradient_name)
{{< /highlight >}}

**PSDPYTHON-70. [Format AI] Ajouter la prise en charge de Métadonnées XPacket au Format AI (Pour le moment non disponible pour la version Python)**

{{< highlight python >}}
    #     En ce moment, cette API n'est pas disponible pour Aspose.PSD pour Python
    #     sourceFile = "ai_one.ai"
    #
    #     def AssertAreEqual(expected, actual):
    #         if expected != actual:
    #             raise Exception("Les objets ne sont pas égaux.")
    #
    #     def AssertIsNotNull(test_object):
    #         if test_object is None:
    #             raise Exception("L'objet de test est nul.")
    #
    #     creator_tool_key = ":CreatorTool"
    #     n_pages_key = "xmpTPg:NPages"
    #     unit_key = "stDim:unit"
    #     height_key = "stDim:h"
    #     width_key = "stDim:w"
    #
    #     expected_creator_tool = "Adobe Illustrator CC 22.1 (Windows)"
    #     expected_n_pages = "1"
    #     expected_unit = "Pixels"
    #     expected_height = 768
    #     expected_width = 1366
    #
    #     with AiImage.load(sourceFile) as img:
    #         image = cast(AiImage, img)
    #
    #         xmp_metadata = image.xmp_data
    #         # XmpPacketWrapper a
    #         AssertIsNotNull(xmp_metadata)
    #
    #         basic_package = cast(XmpBasicPackage, xmp_metadata.get_package(Namespaces.XMP_BASIC))
    #         package = xmp_metadata.packages[4]
    #
    #         creator_tool = basic_package.g[creator_tool_key].to_string()
    #         n_pages = package[n_pages_key]
    #         unit = package[unit_key]
    #         height = np.double.parse(package[height_key].to_string())
    #         width = np.double.parse(package[width_key].to_string())
    #
    #         AssertAreEqual(creator_tool, expected_creator_tool)
    #         AssertAreEqual(n_pages, expected_n_pages)
    #         AssertAreEqual(unit, expected_unit)
    #         AssertAreEqual(height, expected_height)
    #         AssertAreEqual(width, expected_width)

{{< /highlight >}}

**PSDPYTHON-71. Implémenter les types de distorsion Décompression, Compression et Torsion**

{{< highlight python >}}
        files = ["Torsion", "Compression", "Compression_verticale", "Décompression"]

        for prefix in files:
            sourceFile = prefix + ".psd"
            outputFile = prefix + "_export.png"

            loadOpt = PsdLoadOptions()
            loadOpt.allow_warp_repaint = True
            loadOpt.load_effects_resource = True

            pngOpt = PngOptions()
            pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            with PsdImage.load(sourceFile, loadOpt) as psdImage:
                psdImage.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-72.  Les modes Rgb et Lab ne peuvent pas contenir moins de 3 canaux et plus de 4 canaux dans le fichier avec des calques de planche artistique**

{{< highlight python >}}
        sourceFile = "Rgb5Canaux.psb"
        outputFile = "Sortie_Rgb5Canaux.psd"

        with PsdImage.load(sourceFile) as image:
            image.save(outputFile)

{{< /highlight >}}

**PSDPYTHON-79. La zone de traitement supérieure doit être positive. (Paramètre 'areaToProcess') lors du traitement d'un fichier spécifique**

{{< highlight python >}}
        sourceFile = "BANNERS_2_Intel-Gamer_psak.psd")
        outputFile = "BANNERS_2_Intel-Gamer_psak_out.psd"
        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True
        psdLoadOptions.allow_warp_repaint = True

        with PsdImage.load(sourceFile, psdLoadOptions) as image:
            image.save(outputFile)
{{< /highlight >}}

**PSDPYTHON-74. L'image étendue sur la toile est rognée après la sauvegarde. Les données sont perdues mais l'aperçu est correct**

{{< highlight python >}}
        sourceFile = "fichier_volumineux.psd"
        outputFile = "Sortie_fichier_volumineux.psd"
        outputPicture = "fichier_volumineux.png"

        loadOptions = PsdLoadOptions()
        loadOptions.load_effects_resource = True
        loadOptions.use_disk_for_load_effects_resource = True

        with PsdImage.load(sourceFile, loadOptions) as image:
            psdImage = cast(PsdImage, image)
            psdOpt = PsdOptions()
            psdOpt.compression_method = CompressionMethod.RLE
            psdImage.save(outputFile, psdOpt)


{{< /highlight >}}

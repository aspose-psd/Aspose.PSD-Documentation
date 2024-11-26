---
title: Aspose.PSD voor Python via .NET 24.6 - Release-opmerkingen
type: docs
weight: 10
url: /nl/python-net/aspose-psd-voor-python-via-net-24-6-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Python via .NET 24.6](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Sleutel**   | **Samenvatting**                                                                                                    | **Categorie** |
|:--------------|:--------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDPYTHON-69  | Implementeer ondersteuning voor het Verloopkaart-laag                                                                 | Functie       |
| PSDPYTHON-70  | [AI-indeling] Voeg ondersteuning toe voor XPacket Metadata aan AI-indeling (Op dit moment niet beschikbaar voor Python-versie) | Functie       |
| PSDPYTHON-71  | Implementeer Inflateren, Knijpen en Draaien types van vervorming                                                     | Functie       |
| PSDPYTHON-72  |  Rgb- en Lab-modi kunnen niet minder dan 3 kanalen en meer dan 4 kanalen bevatten in het bestand met ArtBoard-lagen | Fout         |
| PSDPYTHON-79  | Het verwerkingsgebied top moet positief zijn. (Parameter 'areaToProcess') bij de verwerking van een specifiek bestand | Fout         |
| PSDPYTHON-74  | Uitgebreid over het canvasbeeld is bijgesneden na het opslaan. Gegevens gaan verloren, maar de voorvertoning ziet er correct uit | Fout         |

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDPYTHON-69. Implementeer ondersteuning voor het Verloopkaart-laag**

{{<highlight python>}}
        sourceFile = "gradient_map_src.psd"
        outputFile = "gradient_map_src_output.psd"
      
        def AssertAreEqual(expected, actual, message=None):
            if expected != actual:
                raise Exception(message or "Objecten zijn niet gelijk.")

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
            AssertAreEqual("Aangepast", gradient_settings.gradient_name)
{{< /highlight >}}

**PSDPYTHON-70. [AI-indeling] Voeg ondersteuning toe voor XPacket Metadata aan AI-indeling (Op dit moment niet beschikbaar voor Python-versie)**

{{<highlight python>}}
    #     Op dit moment is deze API niet beschikbaar voor Aspose.PSD voor Python
    #     sourceFile = "ai_one.ai"
    #
    #     def AssertAreEqual(expected, actual):
    #         if expected != actual:
    #             raise Exception("Objecten zijn niet gelijk.")
    #
    #     def AssertIsNotNull(test_object):
    #         if test_object is None:
    #             raise Exception("Testobject is nul.")
    #
    #     creator_tool_key = ":CreatorTool"
    #     n_pages_key = "xmpTPg:NPages"
    #     unit_key = "stDim:e-enheid"
    #     height_key = "stDim:h"
    #     width_key = "stDim:b"
    #
    #     verwachte_creator_tool = "Adobe Illustrator CC 22.1 (Windows)"
    #     verwachte_n_pages = "1"
    #     verwachte_eenheid = "Pixels"
    #     verwachte_hoogte = 768
    #     verwachte_breedte = 1366
    #
    #     with AiImage.load(sourceFile) as img:
    #         image = cast(AiImage, img)
    #
    #         xmp_metadata = image.xmp_data
    #         # XmpPacketWrapper
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
    #         AssertAreEqual(creator_tool, verwachte_creator_tool)
    #         AssertAreEqual(n_pages, verwachte_n_pages)
    #         AssertAreEqual(unit, verwachte_eenheid)
    #         AssertAreEqual(height, verwachte_hoogte)
    #         AssertAreEqual(width, verwachte_breedte)
{{< /highlight >}}

**PSDPYTHON-71. Implementeer Inflate, Squeeze en Draai typen van vervorming**

{{<highlight python>}}
        bestanden = ["Twist", "Squeeze", "Squeeze_vert", "Inflate"]

        for voorvoegsel in bestanden:
            sourceFile = voorvoegsel + ".psd"
            outputFile = voorvoegsel + "_export.png"

            loadOpties = PsdLoadOptions()
            loadOpties.allow_warp_repaint = True
            loadOpties.load_effects_resource = True

            pngOpties = PngOptions()
            pngOpties.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            with PsdImage.load(sourceFile, loadOpties) as psdAfbeelding:
                psdAfbeelding.save(outputFile, pngOpties)
{{< /highlight >}}

**PSDPYTHON-72.  Rgb- en Lab-modi kunnen niet minder dan 3 kanalen en meer dan 4 kanalen bevatten in het bestand met ArtBoard-lagen**

{{<highlight python>}}
        sourceFile = "Rgb5Channels.psb"
        outputFile = "Rgb5Channels_output.psd"

        with PsdImage.load(sourceFile) as afbeelding:
            afbeelding.save(outputFile)

{{< /highlight >}}

**PSDPYTHON-79. Het verwerkingsgebied top moet positief zijn. (Parameter 'areaToProcess') tijdens de verwerking van een specifiek bestand**

{{<highlight python>}}
        sourceFile = "BANNERS_2_Intel-Gamer_psak.psd")
        outputFile = "BANNERS_2_Intel-Gamer_psak_out.psd"
        psdLaadopties = PsdLoadOptions()
        psdLaadopties.load_effects_resource = True
        psdLaadopties.allow_warp_repaint = True

        with PsdImage.load(sourceFile, psdLaadopties) as afbeelding:
            afbeelding.save(outputFile)
{{< /highlight >}}

**PSDPYTHON-74. Uitgebreid over het canvasbeeld is bijgesneden na het opslaan. Gegevens gaan verloren, maar de voorvertoning ziet er correct uit**

{{<highlight python>}}
        sourceFile = "bigfile.psd"
        outputFile = "bigfile_output.psd"
        outputAfbeelding = "bigfile.png"

        laadOpties = PsdLoadOptions()
        laadOpties.load_effects_resource = True
        laadOpties.use_disk_for_load_effects_resource = True

        with PsdImage.load(sourceFile, laadOpties) as afbeelding:
            psdAfbeelding = cast(PsdImage, afbeelding)
            psdOpt = PsdOptions()
            psdOpt.compression_method = CompressionMethod.RLE
            psdAfbeelding.save(outputFile, psdOpt)


{{< /highlight >}}

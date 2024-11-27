---
title: Aspose.PSD pro Python pomocí .NET 24.6 - Poznámky k vydání
type: docs
weight: 10
url: /cs/python-net/aspose-psd-pro-python-pomoci-net-24-6-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Python pomocí .NET 24.6](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klíč**      | **Souhrn**                                                                                                       | **Kategorie** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-69 | Implementovat podporu vrstvy mapy přechodů                                                                           | Funkce      |
| PSDPYTHON-70 | [Formát AI] Přidat podporu metadat XPacket do Formátu AI (V tuto chvíli není dostupné pro verzi Python)        | Funkce      |
| PSDPYTHON-71 | Implementovat typy zkroubání Inflate, Squeeze a Twist                                                               | Funkce      |
| PSDPYTHON-72 |  Rgb a Lab režimy nemohou obsahovat méně než 3 kanály a více než 4 kanály v souboru s vrstvami ArtBoard Layers | Chyba          |
| PSDPYTHON-79 | Horní hranice zpracovávané oblasti musí být kladná. (Parametr 'areaToProcess') při zpracování konkrétního souboru          | Chyba          |
| PSDPYTHON-74 | Rozšířený obraz mimo plátno je po uložení oříznut. Data jsou ztracena, ale náhled vypadá správně               | Chyba          |

## **Změny ve veřejném rozhraní API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Odebraná API:**
- Žádné

## **Příklady použití:**

**PSDPYTHON-69. Implementovat podporu vrstvy mapy přechodů**

{{< highlight python >}}
        sourceFile = "gradient_map_src.psd"
        outputFile = "gradient_map_src_output.psd"
      
        def AssertAreEqual(expected, actual, message=None):
            if expected != actual:
                raise Exception(message or "Objekty nejsou stejné.")

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
            AssertAreEqual("Vlastní", gradient_settings.gradient_name)
{{< /highlight >}}

**PSDPYTHON-70. [Formát AI] Přidat podporu metadat XPacket do Formátu AI (V tuto chvíli není dostupné pro verzi Python)**

{{< highlight python >}}
    #     V tuto chvíli tato API není dostupná pro Aspose.PSD pro Python
    #     sourceFile = "ai_one.ai"
    #
    #     def AssertAreEqual(expected, actual):
    #         if expected != actual:
    #             raise Exception("Objekty nejsou stejné.")
    #
    #     def AssertIsNotNull(test_object):
    #         if test_object is None:
    #             raise Exception("Testovací objekt je null.")
    #
    #     creator_tool_key = ":CreatorTool"
    #     n_pages_key = "xmpTPg:NPages"
    #     unit_key = "stDim:unit"
    #     height_key = "stDim:h"
    #     width_key = "stDim:w"
    #
    #     expected_creator_tool = "Adobe Illustrator CC 22.1 (Windows)"
    #     expected_n_pages = "1"
    #     expected_unit = "Pixely"
    #     expected_height = 768
    #     expected_width = 1366
    #
    #     with AiImage.load(sourceFile) as img:
    #         image = cast(AiImage, img)
    #
    #         xmp_metadata = image.xmp_data
    #        # XmpPacketWrapper a
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

**PSDPYTHON-71. Implementovat typy zkroubání Inflate, Squeeze a Twist**

{{< highlight python >}}
        soubory = ["Twist", "Squeeze", "Squeeze_vert", "Inflate"]

        for prefix in soubory:
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

**PSDPYTHON-72. Rgb a Lab režimy nemohou obsahovat méně než 3 kanály a více než 4 kanály v souboru s vrstvami ArtBoard Layers**

{{< highlight python >}}
        sourceFile = "Rgb5Channels.psb"
        outputFile = "Rgb5Channels_output.psd"

        with PsdImage.load(sourceFile) as image:
            image.save(outputFile)

{{< /highlight >}}

**PSDPYTHON-79. Horní hranice zpracovávané oblasti musí být kladná. (Parametr 'areaToProcess') při zpracování konkrétního souboru**

{{< highlight python >}}
        sourceFile = "BANNERS_2_Intel-Gamer_psak.psd"
        outputFile = "BANNERS_2_Intel-Gamer_psak_out.psd"
        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True
        psdLoadOptions.allow_warp_repaint = True

        with PsdImage.load(sourceFile, psdLoadOptions) as image:
            image.save(outputFile)
{{< /highlight >}}

**PSDPYTHON-74. Rozšířený obraz mimo plátno je po uložení oříznut. Data jsou ztracena, ale náhled vypadá správně**

{{< highlight python >}}
        sourceFile = "bigfile.psd"
        outputFile = "bigfile_output.psd"
        outputPicture = "bigfile.png"

        loadOptions = PsdLoadOptions()
        loadOptions.load_effects_resource = True
        loadOptions.use_disk_for_load_effects_resource = True

        with PsdImage.load(sourceFile, loadOptions) as image:
            psdImage = cast(PsdImage, image)
            psdOpt = PsdOptions()
            psdOpt.compression_method = CompressionMethod.RLE
            psdImage.save(outputFile, psdOpt)


{{< /highlight >}}

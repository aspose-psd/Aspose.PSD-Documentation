---
title: Aspose.PSD für Python via .NET 24.6 - Versionshinweise
type: docs
weight: 10
url: /de/python-net/aspose-psd-fur-python-via-net-24-6-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält die Versionshinweise für [Aspose.PSD für Python via .NET 24.6](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                               | **Kategorie** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-69 | Unterstützung der Gradientenkarten-Ebene implementieren                                                              | Feature      |
| PSDPYTHON-70 | [AI-Format] Hinzufügen der Unterstützung für XPacket-Metadaten zum AI-Format (Derzeit nicht verfügbar für Python-Version) | Feature      |
| PSDPYTHON-71 | Implementieren von Aufblähen, Zusammenziehen und Verdrehen von Verkrümmungstypen                                 | Feature      |
| PSDPYTHON-72 | RGB- und Lab-Modi können in der Datei mit Artboard-Ebenen nicht weniger als 3 Kanäle und nicht mehr als 4 Kanäle enthalten | Bug          |
| PSDPYTHON-79 | Der obere Verarbeitungsbereich muss positiv sein. (Parameter 'areaToProcess') bei der Verarbeitung einer bestimmten Datei | Bug          |
| PSDPYTHON-74 | Die über die Leinwand erweiterte Bild wird nach dem Speichern beschnitten. Daten gehen verloren, aber die Vorschau sieht korrekt aus | Bug          |

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M: Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P: Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P: Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Entfernte APIs:**
- Keine

## **Beispielanwendungen:**

**PSDPYTHON-69. Implementierung der Unterstützung für die Gradientenkarten-Ebene**

{{< highlight python >}}
        sourceFile = "gradient_map_src.psd"
        outputFile = "gradient_map_src_output.psd"
      
        def AssertAreEqual(expected, actual, message=None):
            if expected != actual:
                raise Exception(message or "Objekte sind nicht gleich.")

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
            AssertAreEqual("Benutzerdefiniert", gradient_settings.gradient_name)
{{< /highlight >}}

**PSDPYTHON-70. [AI-Format] Hinzufügen der Unterstützung für XPacket-Metadaten zum AI-Format (Derzeit nicht verfügbar für Python-Version)**

{{< highlight python >}}
#     Aktuell ist diese API nicht für Aspose.PSD für Python verfügbar
#     sourceFile = "ai_one.ai"
#
#     def AssertAreEqual(expected, actual):
#         if expected != actual:
#             raise Exception("Objekte sind nicht gleich.")
#
#     def AssertIsNotNull(test_object):
#         if test_object is None:
#             raise Exception("Testobjekt ist null.")
#
#     creator_tool_key = ":CreatorTool"
#     n_pages_key = "xmpTPg:NPages"
#     unit_key = "stDim:unit"
#     height_key = "stDim:h"
#     width_key = "stDim:w"
#
#     expected_creator_tool = "Adobe Illustrator CC 22.1 (Windows)"
#     expected_n_pages = "1"
#     expected_unit = "Pixel"
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

**PSDPYTHON-71. Implementierung von Aufblähen, Zusammenziehen und Verdrehen von Verkrümmungstypen**

{{< highlight python >}}
        files = ["Twist", "Squeeze", "Squeeze_vert", "Inflate"]

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

**PSDPYTHON-72.  RGB- und Lab-Modi können in der Datei mit Artboard-Ebenen nicht weniger als 3 Kanäle und nicht mehr als 4 Kanäle enthalten**

{{< highlight python >}}
        sourceFile = "Rgb5Channels.psb"
        outputFile = "Rgb5Channels_output.psd"

        with PsdImage.load(sourceFile) as image:
            image.save(outputFile)

{{< /highlight >}}

**PSDPYTHON-79. Der obere Verarbeitungsbereich muss positiv sein. (Parameter 'areaToProcess') bei der Verarbeitung einer bestimmten Datei**

{{< highlight python >}}
        sourceFile = "BANNERS_2_Intel-Gamer_psak.psd")
        outputFile = "BANNERS_2_Intel-Gamer_psak_out.psd"
        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True
        psdLoadOptions.allow_warp_repaint = True

        with PsdImage.load(sourceFile, psdLoadOptions) as image:
            image.save(outputFile)
{{< /highlight >}}

**PSDPYTHON-74. Das über das Leinwandbild erweiterte Bild wird nach dem Speichern beschnitten. Daten gehen verloren, aber die Vorschau sieht korrekt aus**

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

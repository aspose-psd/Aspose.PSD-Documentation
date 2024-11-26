---
title: Notas da Versão Aspose.PSD para Python via .NET 24.6
type: docs
weight: 10
url: /pt/python-net/aspose-psd-for-python-via-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de versão para [Aspose.PSD for Python via .NET 24.6](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chave**    | **Resumo**                                                                                                       | **Categoria** |
|:------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-69 | Implementar suporte de camada de mapa de gradiente                                                                | Recurso      |
| PSDPYTHON-70 | [Formato AI] Adicionar suporte de Metadados de XPacket ao Formato AI (Neste momento não disponível para a versão Python) | Recurso      |
| PSDPYTHON-71 | Implementar tipos de transformação Inflate, Squeeze e Twist                                                       | Recurso      |
| PSDPYTHON-72 |  Modos Rgb e Lab não podem conter menos de 3 canais e mais de 4 canais no arquivo com Camadas de ArtBoard        | Bug          |
| PSDPYTHON-79 | A área de processamento superior deve ser positiva. (Parâmetro 'areaToProcess') no processamento de arquivo específico | Bug          |
| PSDPYTHON-74 | A imagem expandida sobre o canvas é cortada após a salvamento. Os dados são perdidos, mas a visualização parece correta | Bug          |

## **Alterações na API Pública**
# **APIs Adicionadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs Removidas:**
- Nenhuma

## **Exemplos de Uso:**

**PSDPYTHON-69. Implementar suporte de camada de mapa de gradiente**

{{< highlight python >}}
        sourceFile = "gradient_map_src.psd"
        outputFile = "gradient_map_src_output.psd"
      
        def AssertAreEqual(expected, actual, message=None):
            if expected != actual:
                raise Exception(message or "Os objetos não são iguais.")

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
            AssertAreEqual("Custom", gradient_settings.gradient_name)
{{< /highlight >}}

**PSDPYTHON-70. [Formato AI] Adicionar suporte de Metadados de XPacket ao Formato AI (Neste momento não disponível para a versão Python)**

{{< highlight python >}}
    #     Neste momento esta API não está disponível para o Aspose.PSD para Python
    #     sourceFile = "ai_one.ai"
    #
    #     def AssertAreEqual(expected, actual):
    #         if expected != actual:
    #             raise Exception("Os objetos não são iguais.")
    #
    #     def AssertIsNotNull(test_object):
    #         if test_object is None:
    #             raise Exception("O objeto de teste é nulo.")
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

**PSDPYTHON-71. Implementar tipos de transformação Inflate, Squeeze e Twist**

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

**PSDPYTHON-72.  Modos Rgb e Lab não podem conter menos de 3 canais e mais de 4 canais no arquivo com Camadas de ArtBoard**

{{< highlight python >}}
        sourceFile = "Rgb5Channels.psb"
        outputFile = "Rgb5Channels_output.psd"

        with PsdImage.load(sourceFile) as image:
            image.save(outputFile)

{{< /highlight >}}

**PSDPYTHON-79. A área de processamento superior deve ser positiva. (Parâmetro 'areaToProcess') no processamento de arquivo específico**

{{< highlight python >}}
        sourceFile = "BANNERS_2_Intel-Gamer_psak.psd")
        outputFile = "BANNERS_2_Intel-Gamer_psak_out.psd"
        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True
        psdLoadOptions.allow_warp_repaint = True

        with PsdImage.load(sourceFile, psdLoadOptions) as image:
            image.save(outputFile)
{{< /highlight >}}

**PSDPYTHON-74. A imagem expandida sobre o canvas é recortada após a salvamento. Os dados são perdidos, mas a visualização parece correta**

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

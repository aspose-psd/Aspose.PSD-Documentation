---
title: Notas de la versión de Aspose.PSD para Python via .NET 24.6
type: docs
weight: 10
url: /es/python-net/aspose-psd-for-python-via-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para Python via .NET 24.6](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clave**    | **Resumen**                                                                                                       | **Categoría** |
|:------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-69 | Implementar soporte de capa de mapa de degradado                                                                       | Característica |
| PSDPYTHON-70 | [Formato AI] Agregar soporte de metadatos de XPacket al formato AI (En este momento no disponible para la versión de Python)        | Característica |
| PSDPYTHON-71 | Implementar tipos de deformación de Inflar, Comprimir y Girar                                                          | Característica |
| PSDPYTHON-72 |  Los modos Rgb y Lab no pueden contener menos de 3 canales y más de 4 canales en el archivo con capas de ArtBoard          | Error         |
| PSDPYTHON-79 | El área de procesamiento superior debe ser positiva. (Parámetro 'areaToProcess') en el procesamiento de un archivo específico     | Error         |
| PSDPYTHON-74 | La imagen ampliada sobre el lienzo se recorta después de guardarla. Los datos se pierden pero la vista previa se ve correcta       | Error         |

## **Cambios en la API pública**
# **APIs agregadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDPYTHON-69. Implementar soporte de capa de mapa de degradado**

{{< highlight python >}}
        archivoFuente = "gradient_map_src.psd"
        archivoSalida = "gradient_map_src_output.psd"
      
        def AssertAreEqual(esperado, actual, mensaje=None):
            if esperado != actual:
                raise Exception(mensaje or "Los objetos no son iguales.")

        with PsdImage.load(archivoFuente) as imagen:
            im = cast(PsdImage, imagen)
            capa = im.add_gradient_map_adjustment_layer()
            capa.gradient_settings.reverse = True

            im.save(archivoSalida)

        with PsdImage.load(archivoSalida) as imagen:
            im = cast(PsdImage, imagen)
            capa_mapa_degradado = cast(GradientMapLayer, im.layers[1])
            ajustes_degradado = cast(GradientFillSettings, capa_mapa_degradado.gradient_settings)

            AssertAreEqual(0.0, ajustes_degradado.angle)
            AssertAreEqual(4096, ajustes_degradado.interpolation)
            AssertAreEqual(True, ajustes_degradado.reverse)
            AssertAreEqual(False, ajustes_degradado.align_with_layer)
            AssertAreEqual(False, ajustes_degradado.dither)
            AssertAreEqual(GradientType.LINEAR, ajustes_degradado.gradient_type)
            AssertAreEqual(100, ajustes_degradado.scale)
            AssertAreEqual(0.0, ajustes_degradado.horizontal_offset)
            AssertAreEqual(0.0, ajustes_degradado.vertical_offset)
            AssertAreEqual("Personalizado", ajustes_degradado.gradient_name)
{{< /highlight >}}

**PSDPYTHON-70. [Formato AI] Agregar soporte de metadatos de XPacket al formato AI (En este momento no disponible para la versión de Python)**

{{< highlight python >}}
    #     En este momento, esta API no está disponible para Aspose.PSD para Python
    #     archivoFuente = "ai_one.ai"
    #
    #     def AssertAreEqual(esperado, actual):
    #         if esperado != actual:
    #             raise Exception("Los objetos no son iguales.")
    #
    #     def AssertIsNotNull(objeto_prueba):
    #         if objeto_prueba is None:
    #             raise Exception("El objeto de prueba es nulo.")
    #
    #     clave_creador_herramienta = ":CreatorTool"
    #     clave_n_paginas = "xmpTPg:NPages"
    #     clave_unidad = "stDim:unit"
    #     clave_altura = "stDim:h"
    #     clave_ancho = "stDim:w"
    #
    #     creador_esperado_herramienta = "Adobe Illustrator CC 22.1 (Windows)"
    #     n_paginas_esperado = "1"
    #     unidad_esperada = "Píxeles"
    #     altura_esperada = 768
    #     ancho_esperado = 1366
    #
    #     with AiImage.load(archivoFuente) as img:
    #         imagen = cast(AiImage, img)
    #
    #         metadatos_xmp = imagen.xmp_data
    #         # XmpPacketWrapper a
    #         AssertIsNotNull(metadatos_xmp)
    #
    #         paquete_basico = cast(XmpBasicPackage, metadatos_xmp.get_package(Namespaces.XMP_BASIC))
    #         paquete = metadatos_xmp.packages[4]
    #
    #         creador_herramienta = paquete_basico.g[clave_creador_herramienta].to_string()
    #         n_paginas = paquete[clave_n_paginas]
    #         unidad = paquete[clave_unidad]
    #         altura = np.double.parse(paquete[clave_altura].to_string())
    #         ancho = np.double.parse(paquete[clave_ancho].to_string())
    #
    #         AssertAreEqual(creador_herramienta, creador_esperado_herramienta)
    #         AssertAreEqual(n_paginas, n_paginas_esperado)
    #         AssertAreEqual(unidad, unidad_esperada)
    #         AssertAreEqual(altura, altura_esperada)
    #         AssertAreEqual(ancho, ancho_esperado)

{{< /highlight >}}

**PSDPYTHON-71. Implementar tipos de deformación de Inflar, Comprimir y Girar**

{{< highlight python >}}
        archivos = ["Twist", "Squeeze", "Squeeze_vert", "Inflate"]

        for prefijo in archivos:
            archivoFuente = prefijo + ".psd"
            archivoSalida = prefijo + "_export.png"

            loadOpt = PsdLoadOptions()
            loadOpt.allow_warp_repaint = True
            loadOpt.load_effects_resource = True

            pngOpt = PngOptions()
            pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            with PsdImage.load(archivoFuente, loadOpt) as psdImage:
                psdImage.save(archivoSalida, pngOpt)
{{< /highlight >}}

**PSDPYTHON-72.  Los modos Rgb y Lab no pueden contener menos de 3 canales y más de 4 canales en el archivo con capas de ArtBoard**

{{< highlight python >}}
        archivoFuente = "Rgb5Canales.psb"
        archivoSalida = "Rgb5Canales_output.psd"

        with PsdImage.load(archivoFuente) as imagen:
            imagen.save(archivoSalida)

{{< /highlight >}}

**PSDPYTHON-79. El área de procesamiento superior debe ser positiva. (Parámetro 'areaToProcess') en el procesamiento de un archivo específico**

{{< highlight python >}}
        archivoFuente = "BANNERS_2_Intel-Gamer_psak.psd"
        archivoSalida = "BANNERS_2_Intel-Gamer_psak_out.psd"
        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True
        psdLoadOptions.allow_warp_repaint = True

        with PsdImage.load(archivoFuente, psdLoadOptions) as imagen:
            imagen.save(archivoSalida)
{{< /highlight >}}

**PSDPYTHON-74. La imagen ampliada sobre el lienzo se recorta después de guardarla. Los datos se pierden pero la vista previa se ve correcta**

{{< highlight python >}}
        archivoFuente = "bigfile.psd"
        archivoSalida = "bigfile_output.psd"
        imagenSalida = "bigfile.png"

        loadOptions = PsdLoadOptions()
        loadOptions.load_effects_resource = True
        loadOptions.use_disk_for_load_effects_resource = True

        with PsdImage.load(archivoFuente, loadOptions) as imagen:
            psdImagen = cast(PsdImage, imagen)
            psdOpt = PsdOptions()
            psdOpt.compression_method = CompressionMethod.RLE
            psdImagen.save(archivoSalida, psdOpt)


{{< /highlight >}}

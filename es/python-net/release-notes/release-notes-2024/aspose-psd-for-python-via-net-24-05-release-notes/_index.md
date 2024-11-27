---
title: Notas de Lanzamiento de Aspose.PSD for Python via .NET 24.5
type: docs
weight: 10
url: /es/python-net/aspose-psd-for-python-via-net-24-5-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de lanzamiento de [Aspose.PSD para Python via .NET 24.5](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clave**    | **Resumen**                                                                         | **Categoría** |
|:-------------|:------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-60 | [Formato AI] Agregar soporte para manejar archivos AI con encabezado EPSF           | Característica |
| PSDPYTHON-59 | La semi transparencia se procesa incorrectamente en la vista previa del archivo psd | Error         |
| PSDPYTHON-61 | La representación de la capa de forma es parcialmente incorrecta                    | Error         |
| PSDPYTHON-62 | Excepción al guardar archivos PSD con tamaño superior a 200 MB y grandes dimensiones| Error         |
| PSDPYTHON-63 | Fallo al guardar la imagen como excepción al guardar como PDF después de actualizar de la versión 23.7 a la 24.3 | Error |
| PSDPYTHON-64 | Solucionar el problema en el método GetFontInfoRecords para las fuentes chinas      | Error         |

## **Cambios en la API Pública**
# **APIs Agregadas:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de Uso:**

**PSDPYTHON-59. La semi transparencia se procesa incorrectamente en la vista previa del archivo psd**

{{< highlight python >}}
// La semi transparencia se procesa incorrectamente en la vista previa del archivo psd.
// BackgroundContents asignado a blanco. Las áreas transparentes deberían tener color blanco.

        archivoFuente = "rana_nosimbolo.psd"
        archivoSalida = "rana_nosimbolo_salida_backgroundcontents.psd"

        with PsdImage.load(archivoFuente) as imagenPsd:

            colorDeFondo = RawColor(PixelDataFormat.rgb_32_bpp, 0)

            valorArgb = ctypes.c_int32(255 << 24 | 255 << 16 | 255 << 8 | 255).value

            colorDeFondo.set_as_int(valorArgb)  # Blanco

            opcionesPsd = PsdOptions(imagenPsd)
            opcionesPsd.color_mode = ColorModes.RGB
            opcionesPsd.compression_method = CompressionMethod.RLE
            opcionesPsd.channels_count = 4
            opcionesPsd.background_contents = colorDeFondo

            imagenPsd.save(archivoSalida, opcionesPsd)
{{< /highlight >}}

**PSDPYTHON-60. [Formato AI] Agregar soporte para manejar archivos AI con encabezado EPSF**

{{< highlight python >}}
        archivoFuente = "ejemplo.ai"
        rutaDeSalida = "ejemplo.png"
       
        def assert_are_equal(expected, actual):
            if expected != actual:
                raise Exception("Los objetos no son iguales.")

        with AiImage.load(archivoFuente) as img:
            imagen = cast(AiImage, img)
            assert_are_equal(len(imagen.layers), 2)
            assert_are_equal(imagen.layers[0].has_multi_layer_masks, False)
            assert_are_equal(imagen.layers[0].color_index, -1)
            assert_are_equal(imagen.layers[1].has_multi_layer_masks, False)
            assert_are_equal(imagen.layers[1].color_index, -1)

            imagen.save(rutaDeSalida, PngOptions())

{{< /highlight >}}

**PSDPYTHON-61. La representación de la capa de forma es parcialmente incorrecta**

{{< highlight python >}}
        archivoFuente = "PruebaCapaDeForma.psd"
        archivoSalida = "PruebaCapaDeForma_salida.psd"

        with PsdImage.load(archivoFuente) as imagen:
            img = cast(PsdImage, imagen)
            capaDeForma = cast(ShapeLayer, img.layers[2])
            ruta = capaDeForma.path
            formasDeRuta = ruta.get_items()
            listaDeNudos = []
            for formaDeRuta in formasDeRuta:
                nudos = formaDeRuta.get_items()
                listaDeNudos.extend(nudos)

            nuevaForma = PathShape()

            nudoBezier1 = BezierKnotRecord()
            nudoBezier1.is_linked=True
            nudoBezier1.points=[
                    PointFToResourcePoint(PointF(100, 100), capaDeForma.container.size),
                    PointFToResourcePoint(PointF(100, 100), capaDeForma.container.size),
                    PointFToResourcePoint(PointF(100, 100), capaDeForma.container.size)
                ]

            nudoBezier2 = BezierKnotRecord()
            nudoBezier2.is_linked=True
            nudoBezier2.points=[
                    PointFToResourcePoint(PointF(50, 490), capaDeForma.container.size),
                    PointFToResourcePoint(PointF(100, 490), capaDeForma.container.size),
                    PointFToResourcePoint(PointF(150, 490), capaDeForma.container.size)
                ]

            nudoBezier3 = BezierKnotRecord()
            nudoBezier3.is_linked=True
            nudoBezier3.points=[
                    PointFToResourcePoint(PointF(490, 150), capaDeForma.container.size),
                    PointFToResourcePoint(PointF(490, 50), capaDeForma.container.size),
                    PointFToResourcePoint(PointF(490, 20), capaDeForma.container.size)
                ]

            nudosBezier = [
                nudoBezier1,
                nudoBezier2,
                nudoBezier3
            ]

            nuevaForma.set_items(nudosBezier)

            nuevasFormas = list(formasDeRuta)
            nuevasFormas.append(nuevaForma)

            formaDeRutaNueva = nuevasFormas
            ruta.set_items(formaDeRutaNueva)

            capaDeForma.update()

            img.save(archivoSalida, PsdOptions())

        with PsdImage.load(archivoSalida) as imagen:
            img = cast(PsdImage, imagen)
            capaDeForma = cast(ShapeLayer, img.layers[2])
            ruta = capaDeForma.path
            formasDeRuta = ruta.get_items()
            listaDeNudos = []
            for formaDeRuta in formasDeRuta:
                nudos = formaDeRuta.get_items()
                listaDeNudos.extend(nudos)

            assert len(formasDeRuta) == 3
            assert capaDeForma.left == 42
            assert capaDeForma.top == 14
            assert capaDeForma.bounds.width == 1600
            assert capaDeForma.bounds.height == 1086
{{< /highlight >}}

**PSDPYTHON-62. Excepción al guardar archivos PSD con tamaño superior a 200 MB y grandes dimensiones**

{{< highlight python >}}
        archivoFuente = "archivo_grande.psd"
        archivoSalida = "salida_bruta.psd"
        archivoDeReferencia = "salida_bruta.psd"

        opcionesDeCarga = PsdLoadOptions()
        opcionesDeCarga.load_effects_resource = True
        opcionesDeCarga.use_disk_for_load_effects_resource = True

        with PsdImage.load(archivoFuente, opcionesDeCarga) as imagenPsd:
            opt = PsdOptions()
            opt.compression_method = CompressionMethod.RLE
            imagenPsd.save(archivoSalida, opt)
{{< /highlight >}}

**PSDPYTHON-63. Error de excepción al guardar la imagen como PDF después de actualizar de la versión 23.7 a la 24.3**

{{< highlight python >}}
        archivoFuente = "CVFlor.psd"
        archivoSalida = "_exportar.pdf"

        with PsdImage.load(archivoFuente) as imagenPsd:
            opcionesDeGuardado = PdfOptions()
            opcionesDeGuardado.pdf_core_options = PdfCoreOptions()

            imagenPsd.save(archivoSalida, opcionesDeGuardado)
{{< /highlight >}}

**PSDPYTHON-64. Solucionar el problema en el método GetFontInfoRecords para las fuentes chinas**

{{< highlight python >}}
        carpetaFuente = "Fuente"
        archivoFuente = "bd-mejor-rosa.psd"

        opcionesDeCargaPsd = PsdLoadOptions()
        opcionesDeCargaPsd.load_effects_resource = True
        opcionesDeCargaPsd.allow_warp_repaint = True

        try:
            FontSettings.set_fonts_folders([carpetaFuente], True)
            FontSettings.update_fonts()

            with PsdImage.load(archivoFuente, opcionesDeCargaPsd) as img:
                imagen = cast(PsdImage, img)
                for capa in imagen.layers:
                    if is_assignable(capa, TextLayer):
                        capaTexto = cast(TextLayer, capa)
                        if capaTexto.text == "mejor":
                            # Sin esta corrección habrá una excepción debido a la fuente china.
                            capaTexto.update_text("ÉXITO")
        finally:
            FontSettings.reset()
            FontSettings.update_fonts()
{{< /highlight >}}

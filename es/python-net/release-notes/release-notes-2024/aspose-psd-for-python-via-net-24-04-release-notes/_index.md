---
title: Notas de la versión de Aspose.PSD para Python via .NET 24.4
type: docs
weight: 10
url: /es/python-net/aspose-psd-for-python-via-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clave**    | **Resumen**                                                        | **Categoría**|
|:------------ |:-------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | Agregar manejo de recursos XObjectForm para formato AI              | Función     |
| PSDPYTHON-51 | Agregar constructor para el ShapeLayer                              | Función     |
| PSDPYTHON-52 | Corregir conversión de archivo Psd de RGB a CMYK                    | Error       |
| PSDPYTHON-53 | No se puede exportar un archivo PSD específico utilizando Aspose.PSD| Error       |



## **Cambios en la API pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDPYTHON-50. [AI Format] Agregar manejo de recursos XObjectForm**

{{< highlight python >}}
        nombreArchivoFuente = "ejemplo.ai"
        rutaArchivoSalida = "salida_ejemplo.png"

        with AiImage.load(nombreArchivoFuente) as imagen:
            imagen.save(rutaArchivoSalida, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. Agregar constructor para el ShapeLayer**

{{< highlight python >}}
     def verificar ShapeLayerConstructor():
        archivoSalida = "salida_AgregarShapeLayer.psd"

        with PsdImage(600, 400) as nuevaPsd:
            shapeLayer = nuevaPsd.add_shape_layer()

            nuevaForma = generar_nueva_forma(nuevaPsd.size)
            nuevasFormas = [nuevaForma]
            shapeLayer.path.set_items(nuevasFormas)

            shapeLayer.update()

            nuevaPsd.save(archivoSalida)

        with PsdImage.load(archivoSalida) as img:
            imagen = cast(PsdImage, img)
            assert len(imagen.layers) == 2

            shapeLayer = cast(ShapeLayer, imagen.layers[1])
            rellenoInterno = shapeLayer.fill
            configuracionesTrazo = shapeLayer.stroke
            rellenoTrazo = shapeLayer.stroke.fill

            assert len(shapeLayer.path.get_items()) == 1
            assert len(shapeLayer.path.get_items()[0].get_items()) == 3

            assert rellenoInterno.color.to_argb() == -16127182

            assert configuracionesTrazo.size == 7.41
            assert not configuracionesTrazo.enabled
            assert configuracionesTrazo.line_alignment == StrokePosition.CENTER
            assert configuracionesTrazo.line_cap == LineCapType.BUTT_CAP
            assert configuracionesTrazo.line_join == LineJoinType.MITER_JOIN
            assert rellenoTrazo.color.to_argb() == -16777216
			
    def generar_nueva_forma(tamañoImagen):
        nuevaForma = PathShape()

        punto1 = PointF(20, 100)
        punto2 = PointF(200, 100)
        punto3 = PointF(300, 10)

        nudo1 = BezierKnotRecord()
        nudo1.is_linked = True
        nudo1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punto1, tamañoImagen),
                    Release_24_04_Tests.PointFToResourcePoint(punto1, tamañoImagen),
                    Release_24_04_Tests.PointFToResourcePoint(punto1, tamañoImagen)
                ]

        nudo2 = BezierKnotRecord()
        nudo2.is_linked = True
        nudo2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punto2, tamañoImagen),
                    Release_24_04_Tests.PointFToResourcePoint(punto2, tamañoImagen),
                    Release_24_04_Tests.PointFToResourcePoint(punto2, tamañoImagen)
                ]

        nudo3 = BezierKnotRecord()
        nudo3.is_linked = True
        nudo3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punto3, tamañoImagen),
                    Release_24_04_Tests.PointFToResourcePoint(punto3, tamañoImagen),
                    Release_24_04_Tests.PointFToResourcePoint(punto3, tamañoImagen)
                ]

        nudosBezier = [
            nudo1,
            nudo2,
            nudo3
        ]

        nuevaForma.set_items(nudosBezier)

        return nuevaForma
		
    def PointFToResourcePoint(punto, tamañoImagen):
        RelacionImgAPsd = 256 * 65535
        return Point(
            int(round(punto.y * (RelacionImgAPsd / tamañoImagen.height))),
            int(round(punto.x * (RelacionImgAPsd / tamañoImagen.width)))
        )

    def assert_are_equal(esperado, actual, mensaje=None):
        if esperado != actual:
            raise Exception(mensaje or "Los objetos no son iguales.")
			
{{< /highlight >}}

**PSDPYTHON-52. Corregir conversión de archivo Psd de RGB a CMYK**

{{< highlight python >}}
     def verificarConversionDeRgbACmyk():
        archivoFuente = "rananoseguro.psd"
        archivoSalida = "rananoseguro_salida.psd"

        with PsdImage.load(archivoFuente) as imagen:
            imagenPsd = cast(PsdImage, imagen)
            imagenPsd.has_transparency_data = False

            opcionesPsd = PsdOptions(imagenPsd)
            opcionesPsd.color_mode = ColorModes.CMYK
            opcionesPsd.compression_method = CompressionMethod.RLE
            opcionesPsd.channels_count = 4

            imagenPsd.save(archivoSalida, opcionesPsd)

        with PsdImage.load(archivoSalida) as imagen:
            imagenPsd = cast(PsdImage, imagen)
            assert not imagenPsd.has_transparency_data
            assert imagenPsd.layers[0].channels_count == 4

        def assert_are_equal(esperado, actual, mensaje=None):
            if esperado != actual:
                raise Exception(mensaje or "Los objetos no son iguales.")			

    def assert_are_equal(esperado, actual, mensaje=None):
        if esperado != actual:
            raise Exception(mensaje or "Los objetos no son iguales.")
				
{{< /highlight >}}

**PSDPYTHON-53. No se puede exportar un archivo PSD específico utilizando Aspose.PSD**

{{< highlight python >}}
        archivoFuente = "1966fuente.psd"
        pngSalida = "salida.png"

        opcionesCargaPsd = PsdLoadOptions()
        opcionesCargaPsd.load_effects_resource = True

        with PsdImage.load(archivoFuente, opcionesCargaPsd) as imagenPsd:
            imagenPsd.save(pngSalida, PngOptions())
			
{{< /highlight >}}

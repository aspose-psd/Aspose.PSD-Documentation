---
title: Notas de lanzamiento de Aspose.PSD para Python via .NET 23.12
type: docs
weight: 10
url: /es/net/aspose-psd-for-python-via-net-23-12-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de lanzamiento para [Aspose.PSD para Python via .NET 23.12](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clave**    | **Resumen**                                                                                               | **Categoría** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-7  | [Formato AI] Agregar soporte para el renderizado de imágenes ráster en la nueva versión de AI                   |   Funcionalidad  |
|  PSDPYTHON-8  | Manejar el tipo de ruido de gradiente en GdflResrource                                                               |   Funcionalidad  |
|  PSDPYTHON-9  | Error "Referencia de objeto no establecida como instancia de un objeto." al guardar la capa de texto después de la actualización        |     Error     |
|  PSDPYTHON-10 | Corregir la carga manual de fuentes en MacOS utilizando System.Drawing.Common y Aspose.Drawing.                  |     Error     |
|  PSDPYTHON-11 | AllowWarpRepaint en las PsdLoadOptions conduce a la excepción                                             |     Error     |
|  PSDPYTHON-12 | [Formato AI] Implementar el proceso de corrientes de referencia cruzada                              | Mejora |
|  PSDPYTHON-13 | El control de licencia para VectorPathDataResource funciona incorrectamente                                | Mejora |


## **Cambios en la API pública**
# **APIs agregadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.#ctor(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.RGB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.HSB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.LAB
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientMode
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.#ctor
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.Metered.GetProductName
- M:Aspose.PSD.Metered.IsMeteredLicensed
- T:Aspose.PSD.PluginLicenseException
- M:Aspose.PSD.PluginLicenseException.#ctor
- M:Aspose.PSD.Metered.Equals(System.Object)

# **APIs eliminadas:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **Ejemplos de uso:**

**PSDPYTHON-7. [Formato AI] Agregar soporte para el renderizado de imágenes ráster en la nueva versión de AI**

{{< highlight python >}}
        archivoFuente = "raster.ai"
        archivoSalida = "raster_output.png"

        with Image.load(archivoFuente) as imagen:
            imagen.save(archivoSalida, OpcionesPng())mage.Save(archivoSalida, NuevasOpcionesPng());

{{< /highlight >}}

**PSDPYTHON-8. Manejar el tipo de ruido de gradiente en GdflResrource**

{{< highlight python >}}
        # Ejemplo para trabajar con este GdFlResource utilizando la API base   
        archivoFuente = "Relleno-Degradado.psd"
        archivoDestino = "Relleno-Degradado-out.psd"

        with Image.load(archivoFuente, OpcionesCargaPsd()) as imagen:
            imagenPsd = cast(PsdImage, imagen)
            capa = imagenPsd.capas[1]

            for res in capa.recursos:
                recurso = a_partir_de(res, GdFlResource)
                if (recurso != None):
                    recurso.escala = 90
                    recurso.ángulo = 30
                    recurso.difuminar = False
                    recurso.alinear_con_capa = True
                    recurso.invertir = False

                    break

            imagenPsd.save(archivoDestino, OpcionesPsd())
		
		# Ejemplo para manejar un Degradado sólido
		archivoFuente = "Relleno-con-Degradado-Complejo.psd"
        archivoSalida =  "Relleno-con-Degradado-Complejo_output.psd"

        with Image.load(archivoFuente) as imagen:
            im = cast(PsdImage, imagen)
            for capa in im.capas:
                if is_assignable(capa, CapaDeRelleno):
                    capaRelleno = a_partir_de(capa, CapaDeRelleno)
                    ajustesRellenoDegradado = capaRelleno.ajustes_de_relleno

                    # Lectura
                    assert ajustesRellenoDegradado.alinear_con_capa == False
                    assert abs(ajustesRellenoDegradado.ángulo - 45.0) < 0.001

                    assert ajustesRellenoDegradado.difuminar == True
                    assert ajustesRellenoDegradado.invertir == False
                    assert ajustesRellenoDegradado.color == Color.vacío
                    assert ajustesRellenoDegradado.desplazamiento_horizontal == -39
                    assert ajustesRellenoDegradado.desplazamiento_vertical == -5

                    assert len(ajustesRellenoDegradado.puntos_de_transparencia) == 3
                    assert len(ajustesRellenoDegradado.puntos_de_color) == 2

                    punto = ajustesRellenoDegradado.puntos_de_transparencia[0]
                    assert abs(100.0 - punto.opacidad) < 0.25
                    assert punto.ubicación == 0
                    assert punto.ubicación_punto_medio == 50

                    punto = ajustesRellenoDegradado.puntos_de_transparencia[1]
                    assert abs(50.0 - punto.opacidad) < 0.25
                    assert punto.ubicación == 2048
                    assert punto.ubicación_punto_medio == 50

                    punto = ajustesRellenoDegradado.puntos_de_transparencia[2]
                    assert abs(100.0 - punto.opacidad) < 0.25
                    assert punto.ubicación == 4096
                    assert punto.ubicación_punto_medio == 50

                    punto_color = ajustesRellenoDegradado.puntos_de_color[0]
                    assert punto_color.color == Color.desde_argb(203, 64, 140)
                    assert punto_color.ubicación == 0
                    assert punto_color.ubicación_punto_medio == 50

                    punto_color = ajustesRellenoDegradado.puntos_de_color[1]
                    assert punto_color.color == Color.desde_argb(203, 0, 0)
                    assert punto_color.ubicación == 4096
                    assert punto_color.ubicación_punto_medio == 50

                    # Edición
                    ajustesRellenoDegradado.ángulo = 30.0
                    ajustesRellenoDegradado.difuminar = False
                    ajustesRellenoDegradado.alinear_con_capa = True
                    ajustesRellenoDegradado.invertir = True
                    ajustesRellenoDegradado.desplazamiento_horizontal = 25
                    ajustesRellenoDegradado.desplazamiento_vertical = -15

                    puntos_de_color = lista(ajustesRellenoDegradado.puntos_de_color)
                    puntos_de_transparencia = lista(ajustesRellenoDegradado.puntos_de_transparencia)

                    puntoGrad = PuntoDeColorDeDegradado()
                    puntoGrad.color = Color.violeta
                    puntoGrad.ubicación = 4096
                    puntoGrad.ubicación_punto_medio = 75
                    puntos_de_color.append(puntoGrad)

                    puntos_de_color[1].ubicación = 3000

                    puntoTransp = PuntoDeTransparenciaDeDegradado()
                    puntoTransp.opacidad = 80.0
                    puntoTransp.ubicación = 4096
                    puntoTransp.ubicación_punto_medio = 25
                    puntos_de_transparencia.append(puntoTransp)


{{< /highlight >}}
---
title: Aspose.PSD para .NET 23.12 - Notas de Lanzamiento
type: docs
weight: 10
url: /es/net/aspose-psd-para-net-23-12-notas-de-lanzamiento/
---

{{% alert color="primary" %}}

Esta página contiene las notas de lanzamiento de [Aspose.PSD para .NET 23.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                               | **Categoría** |
|:------------|:----------------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1679 | [Formato AI] Agregar soporte de renderización de imagen Raster en nueva versión de AI                    |   Funcionalidad   |
| PSDNET-1454 | Manejar tipo de ruido Gradient en GdflResrource                                                           |   Funcionalidad   |
| PSDNET-1827 | Error "Referencia de objeto no establecida como instancia de un objeto." al guardar Capa de Texto después de Actualizar        |     Error     |
| PSDNET-1776 | Corregir la carga manual de fuentes en MacOS usando System.Drawing.Common y Aspose.Drawing.                  |     Error     |
| PSDNET-1536 | AllowWarpRepaint en las PsdLoadOptions lleva a la excepción                                             |     Error     |
| PSDNET-1714 | [Formato AI] Implementar procesamiento de transmisiones de referencia cruzada                      | Mejora |
| PSDNET-1834 | El Control de Licencia para VectorPathDataResource funciona incorrectamente                       | Mejora |
| PSDNET-770  | Abrir cualquier archivo de imagen como un objeto inteligente incrustado en la imagen de PSD      | Mejora |
| PSDNET-1864 | Sistema de Licencia del Complemento Aspose.PSD                                                                             | Mejora |



## **Cambios en la API Pública**
# **APIs Agregadas:**
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

# **APIs Eliminadas:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **Ejemplos de Uso:**

**PSDNET-1679. [Formato AI] Agregar soporte de renderización de imagen Raster en nueva versión de AI**

{{< highlight csharp >}}
            string archivoFuente = Path.Combine(carpetaBase, "raster.ai");
            string archivoSalida = Path.Combine(carpetaSalida, "raster_output.png");

            using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
            {
                imagen.Save(archivoSalida, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1454. Manejar tipo de ruido Gradient en GdflResrource**

{{< highlight csharp >}}
            string archivoFuente = "Gradient-Fill.psd";
            string archivoDestino = "Gradient-Fill-out.psd";

            using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions()))
            {
                Capa capa = imagen.Layers[1];

                foreach (LayerResource recurso in capa.Resources)
                {
                    GdFlResource gdFlRecurso = recurso as GdFlResource;

                    if (gdFlRecurso != null)
                    {
                        gdFlRecurso.Scale = 90;
                        gdFlRecurso.Angle = 30;
                        gdFlRecurso.Dither = false;
                        gdFlRecurso.AlignWithLayer = true;
                        gdFlRecurso.Reverse = false;

                        break;
                    }
                }

                imagen.Save(archivoDestino, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-1827. Error "Referencia de objeto no establecida como instancia de un objeto." al guardar Capa de Texto después de Actualizar**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(carpetaBase, "input_1827.psd");
string archivoSalida = Path.Combine(carpetaSalida, "out_1827.psd");

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    foreach (var capa in imagenPsd.Layers)
    {
        if (capa is TextLayer capaTexto)
        {
            capaTexto.TextData.UpdateLayerData();
        }
    }

    // No debería haber errores aquí
    imagenPsd.Save(archivoSalida);
}
{{< /highlight >}}

**PSDNET-1536. AllowWarpRepaint en las PsdLoadOptions lleva a la excepción**

{{< highlight csharp >}}
            string archivoFuente = @"SizeChart-4 Colors.psd";
            string archivoSalida = @"SizeChart-4 Colors.png";

            using (var imagenPsd = (PsdImage)Aspose.PSD.Image.Load(archivoFuente, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true })) 
			{ 
				imagenPsd.Save(archivoSalida + "_original.png", new PngOptions()
				{
					ColorType = PngColorType.TruecolorWithAlpha,
					Progressive = true,
					CompressionLevel = 9
				});
			}
{{< /highlight >}}

**PSDNET-1834. El Control de Licencia para VectorPathDataResource funciona incorrectamente**

{{< highlight csharp >}}
 using (PsdImage im = (PsdImage)Image.Load(DifferentLayerMasks.psd))
 {
     im.Save(complexFiles[i] + "out" + "output.psd");
     im.Save(complexFiles[i] + "out" + "output.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
 }
{{< /highlight >}}

**PSDNET-770. Abrir cualquier archivo de imagen como un objeto inteligente incrustado en la imagen de PSD**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(carpetaBase, "empty.psd");

string agregarArchivoArbol = Path.Combine(carpetaBase, "tree.psd");
string agregarArchivoEscarcha = Path.Combine(carpetaBase, "frost.png");

string archivoSalidaArbol = Path.Combine(carpetaSalida, "tree_export.psd");
string archivoSalidaEscarcha = Path.Combine(carpetaSalida, "frost_export.psd");

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream flujo = new FileStream(agregarArchivoArbol, FileMode.Open))
    {
        using (SmartObjectLayer capaInteligente = new SmartObjectLayer(flujo))
        {
            imagenPsd.AddLayer(capaInteligente);

            imagenPsd.Save(archivoSalidaArbol, new PsdOptions());                        
        }
    }
}

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream flujo = new FileStream(agregarArchivoEscarcha, FileMode.Open))
    {
        using (SmartObjectLayer capaInteligente = new SmartObjectLayer(flujo))
        {
            imagenPsd.AddLayer(capaInteligente);

            imagenPsd.Save(archivoSalidaEscarcha, new PsdOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1864. Sistema de Licencia del Complemento Aspose.PSD**

{{< highlight csharp >}}            
    var medido = new Medido();
    medido.SetLlaveMedida(pluginPublic, pluginPrivate);
			
	// Manipulación específica del complemento
{{< /highlight >}}
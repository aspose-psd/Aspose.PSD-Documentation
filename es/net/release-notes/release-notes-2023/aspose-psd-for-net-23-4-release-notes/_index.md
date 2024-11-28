---
title: Notas de lanzamiento de Aspose.PSD para .NET 23.4
type: docs
weight: 90
url: /es/net/aspose-psd-for-net-23-4-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de lanzamiento para [Aspose.PSD para .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-1409|Diseñar la clase RawColor para la API pública y utilizarla en la API de PSD en lugar de la estructura Color obsoleta|Mejora|
|PSDNET-1332|Integrar la Capa de Ajuste de Mapa de Degradado desde Probation al código principal de Aspose.PSD|Funcionalidad|
|PSDNET-1448|La edición de texto utilizando porciones de texto no guarda el resultado correcto|Error|
|PSDNET-1449|El inicio y el final de los estilos o párrafos aparecen en el lugar incorrecto al editar la Capa de Texto por ITextPortion|Error|
|PSDNET-1509|El formato cambia al editar en Photoshop|Error|


## **Cambios en la API pública**
# **APIs Añadidas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode 
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints 
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints 
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor  


# **APIs Eliminadas:**
- Nada


## **Ejemplos de uso:**

**PSDNET-1332. Integrar la Capa de Ajuste de Mapa de Degradado desde Probation al código principal de Aspose.PSD**

{{< highlight csharp >}}
string archivoFuente = "gradient_map_default.psd";
string archivoSalida = "gradient_map_res.psd";

using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions()))
{
    Capa capa = imagen.Layers[1];
    GrdmResource recursoGrdm = (GrdmResource)capa.Resources[0];

    // verificar valores actuales
    AssertAreEqual(false, recursoGrdm.Reverse);
    AssertAreEqual((ulong)65535, recursoGrdm.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, recursoGrdm.ColorPoints[1].RawColor.Components[3].Value);

    recursoGrdm.Reverse = true;
    // Color rojo para el segundo punto de color del degradado
    recursoGrdm.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    recursoGrdm.ColorPoints[1].RawColor.Components[2].Value = 0;
    recursoGrdm.ColorPoints[1].RawColor.Components[3].Value = 0;

    imagen.Save(archivoSalida, new PsdOptions());
}

using (var imagen = (PsdImage)Image.Load(archivoSalida))
{
    Capa capa = imagen.Layers[1];
    GrdmResource recursoGrdm = (GrdmResource)capa.Resources[0];

    // verificar valores cambiados
    AssertAreEqual(true, recursoGrdm.Reverse);
    AssertAreEqual((ulong)0, recursoGrdm.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)0, recursoGrdm.ColorPoints[1].RawColor.Components[3].Value);
}

void AssertAreEqual(object esperado, object real, string mensaje = null)
{
    if (!object.Equals(esperado, real))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1409. Diseñar la clase RawColor para la API pública y utilizarla en la API de PSD en lugar de la estructura Color obsoleta**

{{< highlight csharp >}}
// métodos adicionales
void AssertAreEqual(object esperado, object real, string mensaje = null)
{
    if (!object.Equals(esperado, real))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}

var color = new RawColor(PixelDataFormat.Rgba32Bpp);
var colorAntiguo = Color.FromArgb(5, 1, 2, 3);

var valorArgb = colorAntiguo.ToArgb();
color.SetAsInt(valorArgb);

AssertAreEqual("ARGB", color.GetColorModeName());
AssertAreEqual(32, color.GetBitDepth());
AssertAreEqual("A Alpha", color.Components[0].FullName);
AssertAreEqual(5, (int)color.Components[0].Value);
AssertAreEqual("R Red", color.Components[1].FullName);
AssertAreEqual(1, (int)color.Components[1].Value);
AssertAreEqual("G Green", color.Components[2].FullName);
AssertAreEqual(2, (int)color.Components[2].Value);
AssertAreEqual("B Blue", color.Components[3].FullName);
AssertAreEqual(3, (int)color.Components[3].Value);

AssertAreEqual(valorArgb, color.GetAsInt());
{{< /highlight >}}

**PSDNET-1448. La edición de texto utilizando porciones de texto no guarda el resultado correcto**

{{< highlight csharp >}}
string archivoFuente =  "originalv5.psd";
string rutaExportacionPsd =  "export.psd";

using (var imagenCorreoPrueba = (PsdImage)Image.Load(archivoFuente))
{
    var capas = imagenCorreoPrueba.Layers;
    foreach (var itemCapa in capas)
    {
        var esCapaTexto = itemCapa.GetType() == typeof(TextLayer) ? true : false;
        if (esCapaTexto)
        {
            var capaTextoActualizar = (TextLayer)itemCapa;

            //Buscar lsak texto
            if (capaTextoActualizar.Text.Contains("lsak"))
            {
                var datosTextoCapa = capaTextoActualizar.TextData;
                if (datosTextoCapa.Text.Contains("lsak") && datosTextoCapa.Text.Contains("\r"))
                {
                    //Reemplazar texto
                    reemplazarTextoLsak(datosTextoCapa);
                    //Formatear texto
                    formatearEstiloTexto(datosTextoCapa);
                }
            }
        }
    }

    imagenCorreoPrueba.Save(rutaExportacionPsd, new PsdOptions());
}
...
{{< /highlight >}}
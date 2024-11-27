---
title: Notas de versión de Aspose.PSD for .NET 23.1
type: docs
weight: 120
url: /es/net/aspose-psd-para-net-23-1-notas-de-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de lanzamiento para [Aspose.PSD for .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-401|Soporte de vstkResource|Característica|
|PSDNET-1346|Agregar la propiedad editable BaselineDirection/IsStandardVerticalRomanAlignmentEnabled a la interfaz IText|Característica|
|PSDNET-181|PSD no se convierte correctamente a JPEG|Error|
|PSDNET-958|PSB a PDF falla para archivos grandes|Error|
|PSDNET-1171|Agregar procesamiento de máscara de recorte a la capa de ajuste|Error|
|PSDNET-1252|Después de cambiar el tamaño de toda la imagen y luego cambiar el tamaño de la capa específica, Aspose.PSD lanza una excepción al guardar la capa|Error|


## **Cambios en la API pública**
# **APIs agregadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleMiterLimit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineJoinType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleScaleLock
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleStrokeAdjust
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleBlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleOpacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleResolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleContent
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashSet
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Levels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.TypeToolKey


# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDNET-181. PSD no se convierte correctamente a JPEG**

{{< highlight csharp >}}
string archivoFuente = "helicopter.psd";
string jpgResultado = "resultado.jpg";

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    imagenPsd.Save(jpgResultado, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. Soporte de vstkResource**

{{< highlight csharp >}}
string archivoFuente = "StrokeShapeTest1.psd";
string archivoDestino = "StrokeShapeTest2.psd";

using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    Layer capa = imagen.Layers[1];
    foreach (LayerResource recurso in capa.Resources)
    {
        if (recurso is VstkResource)
        {
            VstkResource vstkRecurso = (VstkResource)recurso;
            vstkRecurso.StrokeStyleLineAlignment = StrokePosition.Outside;
            vstkRecurso.StrokeStyleLineWidth = 20;
        }
    }

    imagen.Save(archivoDestino);
}
{{< /highlight >}}

**PSDNET-958. PSB a PDF falla para archivos grandes**

{{< highlight csharp >}}
string rutaEntrada = "SteveKohli-CarTOP.psb";
string rutaSalida = "resultado.pdf";

using (var imagen = Image.Load(rutaEntrada))
{
    imagen.Save(rutaSalida, new PdfOptions());
}
{{< /highlight >}}

**PSDNET-1171. Agregar procesamiento de máscara de recorte a la capa de ajuste**

{{< highlight csharp >}}
string archivoFuente = "helicopter_part.psd";
string jpgResultado = "resultado.jpg";

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    imagenPsd.Save(jpgResultado, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1252. Después de cambiar el tamaño de toda la imagen y luego cambiar el tamaño de la capa específica, Aspose.PSD lanza una excepción al guardar la capa**

{{< highlight csharp >}}
string archivoFuente = "source.psd";
string imgFile1 = "img1.png";
string imgFile2 = "img2.png";

var opcionesCarga = new PsdLoadOptions()
{
    ReadOnlyMode = false,
    LoadEffectsResource = true
};

using (var imagen = (PsdImage)Image.Load(archivoFuente, opcionesCarga))
{
    // Primero cambiamos el tamaño de toda la imagen
    imagen.Resize(110, 90);
    var capas = imagen.Layers;

    var capaOk = capas[0];
    capaOk.Resize(100, 80);

    var capaExcepcion = capas[1];
    capaExcepcion.Resize(100, 80);

    // Aquí todo funcionará bien
    capaOk.Save(imgFile1, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    // Ahora aquí todo funcionará bien
    capaExcepcion.Save(imgFile2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });    
}
{{< /highlight >}}

**PSDNET-1346. Agregar la propiedad editable BaselineDirection/IsStandardVerticalRomanAlignmentEnabled a la interfaz ITexto**

{{< highlight csharp >}}
// El siguiente código demuestra la capacidad de editar la nueva propiedad IsStandardVerticalRomanAlignmentEnabled.
// Esto no afecta la renderización en este momento, solo te permite editar el valor de la propiedad.

string archivoFuente = "1346test.psd";
string salida = "out_1346test.psd";

using (var imagen = (PsdImage)Image.Load(archivoFuente))
{
    var capaTexto = imagen.Layers[1] as TextLayer;
    var porcionTexto = capaTexto.TextData.Items[0];
    if (porcionTexto.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Lectura correcta
    }
    else
    {
        throw new Exception("Incorrect reading of IsStandardVerticalRomanAlignmentEnabled property value");
    }

    porcionTexto.Style.IsStandardVerticalRomanAlignmentEnabled = false;
    capaTexto.TextData.UpdateLayerData();

    imagen.Save(salida);
}

using (var imagen = (PsdImage)Image.Load(salida))
{
    var capaTexto = imagen.Layers[1] as TextLayer;
    var porcionTexto = capaTexto.TextData.Items[0];
    if (!porcionTexto.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Lectura correcta
    }
    else
    {
        throw new Exception("Incorrect reading of IsStandardVerticalRomanAlignmentEnabled property value");
    }
}
{{< /highlight >}}

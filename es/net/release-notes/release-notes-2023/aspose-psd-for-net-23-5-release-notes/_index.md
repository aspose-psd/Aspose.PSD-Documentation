---
title: Aspose.PSD para .NET 23.5 - Notas de la versión
type: docs
weight: 80
url: /es/net/aspose-psd-para-net-23-5-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 23.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**    | **Resumen**                                                                 | **Categoría** |
|:------------ |:--------------------------------------------------------------------------- |:------------- |
| PSDNET-343   | Soporte del filtro: Afilado -> Afilado                                      | Característica |
| PSDNET-1179  | Guardar archivo PSD (RGB/8 bits o RGB/16 bits) sin capas a 32 bits           | Característica |
| PSDNET-1408  | Implementar manejo de objetos de ruta de recursos vsms o vmsk para ShapeLayer | Característica |
| PSDNET-1508  | Agregar la influencia de puntos de malla entre sí                             | Característica |


## **Cambios en la API pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsDisabled
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.PathOperations
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor(Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord,Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ShapeIndex
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ToVectorPathRecords
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsInverted
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.DescriptorStructure)
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterId
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterType


# **APIs eliminadas:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Save(Aspose.PSD.StreamContainer,System.Int32)


## **Ejemplos de uso:**

**PSDNET-343. Soporte del filtro: Afilado -> Afilado**

{{< highlight csharp >}}
string archivoFuente = "sharpen_source.psd";
string archivoSalidaPsd = "sharpen_output.psd";
string archivoSalidaPng = "sharpen_output.png";

void AssertAreEqual(object esperado, object actual)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception("Los objetos no son iguales.");
    }
}

using (var imagen = (PsdImage)Image.Load(archivoFuente))
{
    SmartObjectLayer smartObj = (SmartObjectLayer)imagen.Layers[1];

    // editar filtros inteligentes
    SharpenSmartFilter sharpen = (SharpenSmartFilter)smartObj.SmartFilters.Filters[0];

    // verificar los valores de los filtros
    AssertAreEqual(BlendMode.Normal, sharpen.BlendMode);
    AssertAreEqual(100d, sharpen.Opacity);
    AssertAreEqual(true, sharpen.IsEnabled);

    // actualizar los valores de los filtros
    sharpen.BlendMode = BlendMode.Divide;
    sharpen.Opacity = 75;
    sharpen.IsEnabled = false;

    // añadir nuevos elementos de filtro
    var filtros = new List<SmartFilter>(smartObj.SmartFilters.Filters);
    filtros.Add(new SharpenSmartFilter());
    smartObj.SmartFilters.Filters = filtros.ToArray();

    // aplicar cambios
    smartObj.SmartFilters.UpdateResourceValues();
    smartObj.UpdateModifiedContent();

    imagen.Save(archivoSalidaPsd);
    imagen.Save(archivoSalidaPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1179. Guardar archivo PSD (RGB/8 bits o RGB/16 bits) sin capas a 32 bits**

{{< highlight csharp >}}
string archivoEntrada =  "input_8bit_rle.psd";
string archivoSalidaPsd = "output_32bit.psd";
string archivoSalidaImagen32 = "output_from_32bit.png";

using (PsdImage imgSrc = (PsdImage)Image.Load(archivoEntrada))
{
    PsdOptions opcionesTotales = new PsdOptions() { ChannelBitsCount = 32, ColorMode = ColorModes.Rgb };
    imgSrc.Save(archivoSalidaPsd, opcionesTotales);

    using (var img32 = Image.Load(archivoSalidaPsd))
    {
        img32.Save(archivoSalidaImagen32, new PngOptions() { ColorType = PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}

**PSDNET-1408. Implementar el manejo de objetos de ruta de recursos vsms o vmsk para ShapeLayer**

{{< highlight csharp >}}
string archivoFuente = "ShapeLayerTest.psd";
string archivoSalida = "ShapeLayerTest-out.psd";

using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer shapeLayer = imagen.Layers[1];
    VectorPathDataResource vectorPathDataResource = (VectorPathDataResource)shapeLayer.Resources[1];

    bool isFillStartsWithAllPixels;
    List<IPathShape> shapes = GetShapesFromResource(vectorPathDataResource, out isFillStartsWithAllPixels);

    // Remover una forma
    shapes.RemoveAt(1);

    // Guardar los datos cambiados en el recurso
    List<VectorPathRecord> path = new List<VectorPathRecord>();
    path.Add(new PathFillRuleRecord(null));
    path.Add(new InitialFillRuleRecord(isFillStartsWithAllPixels));

    for (ushort i = 0; i < shapes.Count; i++)
    {
        PathShape shape = (PathShape)shapes[i];
        shape.ShapeIndex = i;
        path.AddRange(shape.ToVectorPathRecords());
    }

    vectorPathDataResource.Paths = path.ToArray();

    imagen.Save(archivoSalida);
}

// Verificar los valores cambiados en el archivo guardado
using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer shapeLayer = imagen.Layers[1];
    VectorPathDataResource vectorPathDataResource = (VectorPathDataResource)shapeLayer.Resources[1];

    bool isFillStartsWithAllPixels;
    List<IPathShape> shapes = GetShapesFromResource(vectorPathDataResource, out isFillStartsWithAllPixels);

    // El archivo guardado debería tener 1 forma
    AssertAreEqual(1, shapes.Count);
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}

List<IPathShape> GetShapesFromResource(VectorPathDataResource vectorPathDataResource, out bool isFillStartsWithAllPixels)
{
    List<IPathShape> shapes = new List<IPathShape>();
    LengthRecord lengthRecord = null;
    isFillStartsWithAllPixels = false;
    List<BezierKnotRecord> bezierKnotRecords = new List<BezierKnotRecord>();

    foreach (var pathRecord in vectorPathDataResource.Paths)
    {
        if (pathRecord is LengthRecord)
        {
            if (bezierKnotRecords.Count > 0)
            {
                shapes.Add(new PathShape(lengthRecord, bezierKnotRecords.ToArray()));
                lengthRecord = null;
                bezierKnotRecords.Clear();
            }

            lengthRecord = (LengthRecord)pathRecord;
        }
        else if (pathRecord is BezierKnotRecord)
        {
            bezierKnotRecords.Add((BezierKnotRecord)pathRecord);
        }
        else if (pathRecord is InitialFillRuleRecord)
        {
            InitialFillRuleRecord initialFillRuleRecord = (InitialFillRuleRecord)pathRecord;
            isFillStartsWithAllPixels = initialFillRuleRecord.IsFillStartsWithAllPixels;
        }
    }

    if (bezierKnotRecords.Count > 0)
    {
        shapes.Add(new PathShape(lengthRecord, bezierKnotRecords.ToArray()));
        lengthRecord = null;
        bezierKnotRecords.Clear();
    }

    return shapes;
}
{{< /highlight >}}

**PSDNET-1508. Agregar la influencia de puntos de malla entre sí**

{{< highlight csharp >}}
string archivoFuente = "Bottom_Right.psd";
string archivoSalida = "output.png";

using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    imagen.Save(archivoSalida, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha});
}
{{< /highlight >}}
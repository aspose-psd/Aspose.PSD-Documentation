---
title: Notas de la versión Aspose.PSD para .NET 20.7
type: docs
weight: 60
url: /es/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

Esta página contiene notas de lanzamiento para [Aspose.PSD para .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-673|Soporte de recurso LnkE|Característica|
|PSDNET-392|Soporte de britResource (Recurso de Capa de Ajuste de Brillo/Contraste)|Característica|
|PSDNET-629|Cambiar mensaje de excepción al intentar abrir formatos no compatibles como imagen|Mejora|
|PSDNET-594|Error al guardar máscara de capa|Error|
|PSDNET-597|Si guardamos archivo PSD después de la creación de nuevo Grupo de Capa, se muestra advertencia de Photoshop al abrir el archivo|Error|
|PSDNET-618|Máscara de recorte no se aplica a la carpeta|Error|
|PSDNET-625|No se puede abrir archivo con Aspose.PSD para .NET|Error|
|PSDNET-650|Excepción al guardar imágen al convertir PSD a PDF|Error|
|PSDNET-655|La operación rop invalida la ruta de recorte en la imagen PSD|Error|
|PSDNET-662|Excepción de NullReference al intentar guardar archivo PSD específico con Efecto de Sombra|Error|
|PSDNET-666|Aspose.PSD devuelve true en Image.CanLoad(pdfStream)|Error|
|PSDNET-676|Capas no se renderizan correctamente en PNG generado|Error|
|PSDNET-677|Excepción al acceder a TextData|Error|
|PSDNET-679|Excepción al guardar el PSD|Error|

## **Cambios en la API Pública**
# **APIs Agregadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **APIs Eliminadas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Ejemplos de Uso:**
**PSDNET-606. Soporte de recurso LnkE**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(actual, expected))
    {
        throw new FormatException(string.Format("El valor actual {0} no es igual al esperado {1}.", actual, expected));
    }
}

object[] CasosDeSoporteLnk2Resource = new object[]
{
    new object[]
    {
        "00af34a0-a90b-674d-a821-73ee508c5479",
        "rgb8_2x2.png",
        "png",
        string.Empty,
        0x53,
        0d,
        string.Empty,
        7,
        true,
        0x124L,
        0x74cL
    }
};
//Más código...
{{< /highlight >}}
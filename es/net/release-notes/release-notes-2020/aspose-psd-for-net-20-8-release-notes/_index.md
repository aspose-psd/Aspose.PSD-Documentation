---
title: Notas de la versión de Aspose.PSD para .NET 20.8
type: docs
weight: 50
url: /es/net/aspose-psd-for-net-20-8-release-notes/
---

{{% alert color="primary" %}} 

Esta página contiene notas de la versión para [Aspose.PSD para .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-390|Soporte de PlLdResource (recurso de capa colocada para Capa de Objeto Inteligente)|Característica|
|PSDNET-400|Soporte de SoLdResource (recurso de datos de Capa de Objeto Inteligente)|Característica|
|PSDNET-693|Agregar soporte para estructuras de Array de Objetos y Array de Unidades: firmas ObAr / UnFl|Característica|
|PSDNET-600|Corregir guardar imagen PSD modificada con Modo de Color CMYK de 16 bits por canal|Error|
|PSDNET-664|Subrayado y tachado perdidos después de enfocarse en el texto en un archivo guardado con Aspose.PSD|Error|
|PSDNET-710|Regresión: Aspose.PSD 20.7.0 rompe tamaños de fuente para archivos antiguos|Error|

## Cambios en la API pública
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.Byte[],System.Boolean)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.String,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Structures
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitTypes,System.Double[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.UnitType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Values
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.ValueCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UOrder
- P:```
Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VOrder
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Items
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TypeToolKey

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**
**PSDNET-390. Soporte de PlLdResource (recurso de capa colocada para Capa de Objeto Inteligente)**
{{< highlight csharp >}}
        void AssertAreEqual(object actual, object expected)
        {
            var areEqual = object.Equals(actual, expected);
            if (!areEqual && actual is Array && expected is Array)
            {
                var actualArray = (Array)actual;
                var expectedArray = (Array)actual;
                if (actualArray.Length == expectedArray.Length)
                {
                    for (int i = 0; i < actualArray.Length; i++)
                    {
                        if (!object.Equals(actualArray.GetValue(i), expectedArray.GetValue(i)))
                        {
                            break;
                        }
                    }

                    areEqual = true;
                }
            }

            if (!areEqual)
            {
                throw new FormatException(
                    string.Format("El valor actual {0} no es igual al esperado {1}.", actual, expected));
            }
        }


        string dataDir = "PSDNET390_1\\";
        var sourceFilePath = dataDir + "LayeredSmartObjects8bit2.psd";
        var outputFilePath = dataDir + "LayeredSmartObjects8bit2_output.psd";
        var expectedValues = new object[]
        {
            new object[]
            {
                true,
                "76f05a3b-7523-5e42-a1bb-27f4735bffa0",
                1,
                1,
                0x10,
                PlacedLayerType.Raster,
                new double[8]
                {
                    29.937922786050663,
                    95.419959734187131,
                    126.85445817782261,
                    1.0540625423957124,
                    172.20861031651307,
                    47.634102808208553,
                    75.292074924741144,
                    142
                },
                0d,
                0d,
                0d,
                0d,
                0d,
                149d,
                310d,
                4,
                4,
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d,
                    0.0d, 103.33333333333333d, 206.66666666666666d, 310.0d
                },
                UnitTypes.Pixels,
                new double[16]
                {
                    0.0d, 0.0d, 0.0d, 0.0d,
                    49.666666666666664d, 49.666666666666664d, 49.666666666666664d, 49.666666666666664d,
                    99.333333333333329d, 99.333333333333329d, 99.333333333333329d, 99.333333333333329d,
                    149, 149, 149, 149,
                },
            },
            new object[]
            {
                true,
                "cf0477a8-8f92-ac4f-9462-f78e26234851",
                1,
                1,
                0x10,
                PlacedLayerType.Raster,
                new doubl
```
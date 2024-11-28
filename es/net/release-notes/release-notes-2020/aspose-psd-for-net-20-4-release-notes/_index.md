---
title: Notas de la versión de Aspose.PSD para .NET 20.4
type: docs
weight: 90
url: /es/net/aspose-psd-for-net-20-4-release-notes/
---

{{% alert color="primary" %}} 

Esta página contiene notas de la versión de [Aspose.PSD para .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-567|Soporte del recurso 'Datos de origen vectorial'|Característica|
|PSDNET-373|Soporte de lclrResource (Ajuste de color de hoja)|Característica|
|PSDNET-563|Soporte de propiedades de datos de LengthRecord. (Operaciones de trazado (operaciones booleanas), índice de la forma en la capa, recuento de los registros de anclaje de beziers)|Característica|
|PSDNET-425|Soporte del color de fondo del Recurso de la Sección de Imagen #1010|Característica|
|PSDNET-530|Añadiendo capas de relleno en tiempo de ejecución|Característica|
|PSDNET-424|Soporte de la información de borde del Recurso de la Sección de Imagen #1009|Característica|
|PSDNET-592|Soporte de capas en archivos de formato AI|Característica|
|PSDNET-256|Soporte de lectura y edición del efecto de capa de sobreimpresión de degradado|Característica|
|PSDNET-257|Renderizado del efecto de capa de sobreimpresión de degradado|Característica|
|PSDNET-585|Los cambios en la propiedad GradientOverlayEffect.BlendMode no se muestran en Photoshop|Error|
|PSDNET-561|Corregir guardar imagen PSD con modo de color en escala de grises y 16 bits por canal a formato PSD en escala de grises|Error|
|PSDNET-560|Corregir guardar imagen PSD con modo de color en escala de grises y 16 bits por canal a formato PNG|Error|

## **Cambios en la API Pública**
# **APIs añadidas:**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**
**PSDNET-567. Soporte del recurso 'Datos de origen vectorial'**

{{< highlight java >}}

         // Soporte de VogkResource

        static void EjemploDeSoporteDeVogkResource()

        {

            string nombreArchivo = "VectorOriginationDataResource.psd";

            string nombreArchivoSalida = "salida_VectorOriginationDataResource_.psd";

            using (var imagenPsd = (PsdImage)Image.Load(nombreArchivo))

            {

                var recurso = ObtenerVogkResource(imagenPsd);

                // Lectura

                if (recurso.ShapeOriginSettings.Length != 1 ||

                    !recurso.ShapeOriginSettings[0].IsShapeInvalidated ||

                    recurso.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("Se leyeron incorrectamente los datos de VogkResource.");

                }

                // Edición

                recurso.ShapeOriginSettings = new[]

                {

                    recurso.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                imagenPsd.Save(nombreArchivoSalida);

            }

        }

        static VogkResource ObtenerVogkResource(PsdImage imagen)

        {

            var capa = imagen.Layers[1];

            VogkResource recurso = null;

            var recursos = capa.Resources;

            for (int i = 0; i < recursos.Length; i++)

            {

                if (recursos[i] is VogkResource)

                {

                    recurso = (VogkResource)recursos[i];

                    break;

                }

            }

            if (recurso == null)

            {

                throw new Exception("Recurso VogkResource no encontrado.");

            }

            return recurso;

        }   

{{< /highlight >}}

**PSDNET-373. Soporte de lclrResource (Ajuste de color de hoja)**
...

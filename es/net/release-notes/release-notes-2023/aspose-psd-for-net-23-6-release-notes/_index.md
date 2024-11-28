---
title: Aspose.PSD para .NET 23.6 - Notas de la versión
type: docs
weight: 70
url: /es/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**     | **Resumen**                                                                                                                                      | **Categoría** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Refactorizar API de Línea de Tiempo                                                                                                              | Mejora       |
| PSDNET-1517 | Eliminar artefactos al renderizar deformación                                                                                                    | Mejora       |
| PSDNET-1528 | Optimización de renderizado de deformación                                                                                                       | Mejora       |
| PSDNET-147  | Soporte de Capa de Ajuste de Umbral                                                                                                              | Funcionalidad|
| PSDNET-149  | Soporte de Capa de Ajuste de Color Selectivo                                                                                                     | Funcionalidad|
| PSDNET-801  | Capacidad para exportar Línea de Tiempo PSD al archivo Animated Gif                                                                               | Funcionalidad|
| PSDNET-1555 | Agregar soporte para Capa de Texto sin bordes rectangulares                                                                                       | Funcionalidad|
| PSDNET-1582 | Soporte de Capa de Forma                                                                                                                        | Funcionalidad|
| PSDNET-864  | Reemplazar imagen en Objeto Inteligente no se actualiza                                                                                          | Error        |
| PSDNET-1404 | No se puede guardar archivo PSD como PSD con la siguiente excepción: los modos Rgb y Lab no pueden contener menos de 3 canales y más de 4 canales| Error        |
| PSDNET-1546 | La Justificación de Texto se pierde si se abre la Capa de Texto en el modo de edición de Photoshop                                                | Error        |
| PSDNET-1548 | Excepción de referencia nula al guardar archivo PSD                                                                                              | Error        |
| PSDNET-1578 | Excepción en la carga de la Capa de Forma: los puntos para límites de origen vectorial aún no son compatibles                                      | Error        |
| PSDNET-1579 | Excepción en la carga de VogkResource: los puntos se guardan como DoubleStructures, los leemos como UnitStructures                               | Error        |
| PSDNET-1581 | LayerType de ShapeLayer está vacío                                                                                                              | Error        |


## **Cambios en la API pública**
# **APIs Agregadas:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ÍndiceMarcoActivo
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Marcos
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ConteoLazos
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Guardar(Sistema.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Guardar(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Línea de tiempo
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PuntosTipoUnidad
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cián
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Amarillo
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Negro
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relativo
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absoluto
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Rojos
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Amarillos
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Verdes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyan
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Azules
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blancos
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutros
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Negros
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Versión
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.MétodoCorrección
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.ObtenerCorrecciónCmyk(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.AjustarCorrecciónCmyk(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AñadirCapaAjusteColorSelectivo
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Nivel
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AñadirCapaAjusteUmbral
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CrearInstancia
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Actualizar
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Ruta


# **APIs Eliminadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(Sistema.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.MarcoActivo
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ConteoLazos
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Marcos
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.IdCapa


## **Ejemplos de uso:**

**PSDNET-147. Soporte de Capa de Ajuste de Umbral**

{{< highlight csharp >}}
string archivoFuenteConCapaDeUmbral = "flores_umbral_fuente.psd";
string archivoPsdConCapaDeUmbral = "flores_umbral_output.psd";
string archivoPngConCapaDeUmbral = "flores_umbral_output.png";

string archivoFuenteSinCapaDeUmbral = "flores_fuente.psd";
string archivoPsdSinCapaDeUmbral = "flores_output.psd";
string archivoPngSinCapaDeUmbral = "flores_output.png";

void AfirmarIguales(objeto esperado, objeto real)
{
    si (!Object.Equals(esperado, real))
    {
        lanzar nueva Excepción("Los objetos no son iguales.");
    }
}

// Obtener, verificar y cambiar la Capa de ajuste de umbral de la imagen.
usando (var imagen = (PsdImage)Image.Load(archivoFuenteConCapaDeUmbral))
{
    foreach (var capa en imagen.Layers)
    {
        if (capa es ThresholdLayer)
        {
            // Obtener Capa de ajuste de umbral.
            ThresholdLayer capaUmbral = (ThresholdLayer)capa;
            var nivel = capaUmbral.Nivel;

            // Verificar parámetros de las capas.
            AfirmarIguales(nivel, (corto)115);

            // Establecer parámetros de las capas.
            capaUmbral.Nivel = 50;

            imagen.Save(archivoPsdConCapaDeUmbral);
            imagen.Save(archivoPngConCapaDeUmbral, new PngOptions());
        }
    }
}

// Agregar y establecer la Capa de ajuste de umbral a la imagen.
usando (var imagen = (PsdImage)Image.Load(archivoFuenteSinCapaDeUmbral))
{
    // Agregar Capa de Ajuste de Umbral.
    ThresholdLayer capaUmbral = imagen.AddThresholdAdjustmentLayer();

    // Establecer parámetros de las capas.
    capaUmbral.Nivel = 115;

    imagen.Save(archivoPsdSinCapaDeUmbral);
    imagen.Save(archivoPngSinCapaDeUmbral, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149. Soporte de Capa de Ajuste de Color Selectivo**

...Continúa con la misma estructura para los demás ejemplos.
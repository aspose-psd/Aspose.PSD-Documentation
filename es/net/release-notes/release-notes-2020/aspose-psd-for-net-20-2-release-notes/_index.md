---
title: Notas de lanzamiento de Aspose.PSD para .NET 20.2
type: docs
weight: 110
url: /es/net/aspose-psd-for-net-20-2-release-notes/
---

{{% alert color="primary" %}} 

Esta página contiene las notas de lanzamiento de [Aspose.PSD para .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-206|Mejora de la capacidad de representar texto de diferentes colores en la capa de texto|Característica|
|PSDNET-369|Soporte de recurso clbl (El recurso de capa contiene información sobre elementos de recorte de mezcla)|Característica|
|PSDNET-274 |Soporte de recurso blwh (El recurso contiene Datos de capa de Ajuste de Blanco y Negro)|Característica|
|PSDNET-230|Capacidad para exportar Grupo de capas a Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Característica|
|PSDNET-372|Soporte de recurso lspf (Contiene configuraciones sobre la configuración de capa protegida)|Característica|
|PSDNET-370|Soporte de recurso infx (Contiene datos sobre la Mezcla de elementos interiores)|Característica|
|PSDNET-251|Refactorización de PsdImage y Layer para cambiar el comportamiento de la Transformación (Tamaño correcto/rotación/recorte para máscaras de capa si transformamos una capa por separado)|Mejora|
|PSDNET-276 |En algunas configuraciones de globalización, la imagen raster de AI no se puede abrir|Error|
|PSDNET-194|Después de realizar la operación FlipRotate en la capa, la imagen PSD se vuelve ilegible|Error|
|PSDNET-177. |System.ArgumentException durante la carga del archivo PSD|Error|
|PSDNET-249|Después de usar un método de transformación solo para una capa, la capa guardada tiene límites incorrectos o una máscara|Error|

## **Cambios en la API pública**
# **APIs agregadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.Height
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorRed
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorGreen
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.BlackWhiteAdjustmentLayer.TintColorBlue
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Reds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Yellows
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Greens
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Cyans
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Blues
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Magentas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.UseTint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BwPresetKind
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.BlackAndWhitePresetFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.TintColor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor
- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues
- T:Aspose.PSD.AggregateException
- M:Aspose.PSD.CmykColor.Equals(System.Object)
- T:Aspose.PSD.CompositeException
- T:Aspose.PSD.CoreExceptions.IndexOutOFRangeException
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String)
- M:Aspose.PSD.CoreExceptions.IndexOutOFRangeException.#ctor(System.String,System.Exception)
- F:Aspose.PSD.FileFormat.Otg
- T:Aspose.PSD.FileFormats.Jpeg2000.Jpeg2000CustomException
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.IsDataStoredDiscretely
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetChannelData(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetActiveManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.GetCurveManager
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.TypeToolKey
- T:Aspose.PSD.ImageOptions.TiffOptionsUtils
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.#ctor
- M:Aspose.PSD.ImageOptions.TiffOptionsUtils.GetValidTagsCount(Aspose.PSD.FileFormats.Tiff.TiffDataType[])
- P:Aspose.PSD.ImageOptionsBase.ProgressEventHandler
- P:Aspose.PSD.LoadOptions.ProgressEventHandler
- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)
- M:Aspose.PSD.Metered.Equals(System.Object)
- T:Aspose.PSD.ProgressEventHandler
- T:Aspose.PSD.ProgressManagement.EventType
- F:Aspose.PSD.ProgressManagement.EventType.RelativeProgress
- F:Aspose.PSD.ProgressManagement.EventType.StageChange
- F:Aspose.PSD.ProgressManagement.EventType.Initialization
- F:Aspose.PSD.ProgressManagement.EventType.PreProcessing
- F:Aspose.PSD.ProgressManagement.EventType.Processing
- F:Aspose.PSD.ProgressManagement.EventType.Finalization
- T:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Description
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.EventType
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.MaxValue
- P:Aspose.PSD.ProgressManagement.ProgressEventHandlerInfo.Value
- M:Aspose.PSD.RasterImage.GetSkewAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle
- M:Aspose.PSD.RasterImage.NormalizeAngle(System.Boolean,Aspose.PSD.Color)
# **APIs removidas:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Types.Derived.RenditionClass.DefinedValues

## **Ejemplos de uso:**
**PSDNET-206. Mejora de la capacidad de representar texto de diferentes colores en la capa de texto**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("texto_ethalon_diferentes_colores.psd"))

{

    var capaTexto = (TextLayer)psdImage.Layers[1];

    capaTexto.TextData.UpdateLayerData();

    psdImage.Save("salida.png", new PngOptions());

}

{{< /highlight >}}

**PSDNET-369. Soporte de recurso clbl (El recurso de capa contiene información sobre elementos de recorte de mezcla)**

{{< highlight java >}}

        void AssertIsTrue(bool condición, string mensaje)

        {

            if (!condición)

            {

                throw new FormatException(mensaje);

            }

        }

        string nombreArchivoFuente = "MuestraParaRecurso.psd";

        string nombreArchivoDestino = "Salida" + nombreArchivoFuente;

        ClblResource ObtenerRecursoClbl(PsdImage im)

        {

            foreach (var capa in im.Layers)

            {

                foreach (var recursoCapa in capa.Resources)

                {

                    if (recursoCapa is ClblResource)

                    {

                        return (ClblResource)recursoCapa;

                    }

                }

            }

            throw new Exception("No se encontró el recurso Clbl especificado");

        }

        using (PsdImage im = (PsdImage)Image.Load(nombreArchivoFuente))

        {

            var recurso = ObtenerRecursoClbl(im);

            AssertIsTrue(recurso.BlendClippedElements, "El ClblResource.BlendClippedElements debería ser verdadero");

            // Prueba de edición y guardado

            recurso.BlendClippedElements = false;

            im.Save(nombreArchivoDestino);

        }

        using (PsdImage im = (PsdImage)Image.Load(nombreArchivoDestino))

        {

            var recurso = ObtenerRecursoClbl(im);

            AssertIsTrue(!recurso.BlendClippedElements, "El ClblResource.BlendClippedElements debería cambiar a falso");

        }

{{< /highlight >}}

**PSDNET-274. Soporte de recurso blwh (El recurso contiene Datos de capa de Ajuste de Blanco y Negro)**

{{< highlight java >}}

         const string MensajeValorEsperadoErroneo = "El valor de propiedad esperado no es igual al valor actual";

        void AssertIsTrue(bool condición, string mensaje)

        {

            if (!condición)

            {

                throw new FormatException(mensaje);

            }

        }

        void EjemploSoporteDeRecursoBlwh(

            string nombreArchivoFuente,

            int rojos,

            int amarillos,

            int verdes,

            int cianos,

            int azules,

            int magentas,

            bool usarTinte,

            int tipoBwPreset,

            string nombreArchivoPresetBw,

            double tinteRojo,

            double tinteVerde,

            double tinteAzul,

            int tinte,

            int nuevoTinte)

        {

            string nombreArchivoDestino = "Salida" + nombreArchivoFuente;

            bool seEncontróRecursoRequerido = false;

            using (PsdImage im = (PsdImage)Image.Load(nombreArchivoFuente))

            {

                foreach (var capa in im.Layers)

                {

                    foreach (var recursoCapa in capa.Resources)

                    {

                        if (recursoCapa is BlwhResource)

                        {

                            var recursoBlwh = (BlwhResource)recursoCapa;

                            var capaBlwh = (BlackWhiteAdjustmentLayer)capa;

                            seEncontróRecursoRequerido = true;

                            AssertIsTrue(recursoBlwh.Reds == rojos, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Yellows == amarillos, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Greens == verdes, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Cyans == cianos, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Blues == azules, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Magentas == magentas, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.UseTint == usarTinte, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.TintColor == tinte, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.BwPresetKind == tipoBwPreset, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.BlackAndWhitePresetFileName == nombreArchivoPresetBw, MensajeValorEsperadoErroneo);

                            AssertIsTrue(Math.Abs(capaBlwh.TintColorRed - tinteRojo) < 1e-6, MensajeValorEsperadoErroneo);

                            AssertIsTrue(Math.Abs(capaBlwh.TintColorGreen - tinteVerde) < 1e-6, MensajeValorEsperadoErroneo);

                            AssertIsTrue(Math.Abs(capaBlwh.TintColorBlue - tinteAzul) < 1e-6, MensajeValorEsperadoErroneo);

                            // Prueba de edición y guardado

                            recursoBlwh.Reds = rojos - 15;

                            recursoBlwh.Yellows = amarillos - 15;

                            recursoBlwh.Greens = verdes + 15;

                            recursoBlwh.Cyans = cianos + 15;

                            recursoBlwh.Blues = azules - 15;

                            recursoBlwh.Magentas = magentas - 15;

                            recursoBlwh.UseTint = !usarTinte;

                            recursoBlwh.BwPresetKind = 4;

                            recursoBlwh.BlackAndWhitePresetFileName = "nombrePresetBw";

                            capaBlwh.TintColorRed = tinteRojo - 60;

                            capaBlwh.TintColorGreen = tinteVerde - 60;

                            capaBlwh.TintColorBlue = tinteAzul - 60;

                            im.Save(nombreArchivoDestino);

                            break;

                        }

                    }

                }

            }

            AssertIsTrue(seEncontróRecursoRequerido, "No se encontró el recurso Blwh especificado");

            seEncontróRecursoRequerido = false;

            using (PsdImage im = (PsdImage)Image.Load(nombreArchivoDestino))

            {

                foreach (var capa in im.Layers)

                {

                    foreach (var recursoCapa in capa.Resources)

                    {

                        if (recursoCapa is BlwhResource)

                        {

                            var recursoBlwh = (BlwhResource)recursoCapa;

                            var capaBlwh = (BlackWhiteAdjustmentLayer)capa;

                            seEncontróRecursoRequerido = true;

                            AssertIsTrue(recursoBlwh.Reds == rojos - 15, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Yellows == amarillos - 15, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Greens == verdes + 15, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Cyans == cianos + 15, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Blues == azules - 15, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.Magentas == magentas - 15, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.UseTint == !usarTinte, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.TintColor == nuevoTinte, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.BwPresetKind == 4, MensajeValorEsperadoErroneo);

                            AssertIsTrue(recursoBlwh.BlackAndWhitePresetFileName == "nombrePresetBw", MensajeValorEsperadoErroneo);

                            AssertIsTrue(Math.Abs(capaBlaBlwh.TintColorRed - tinteRojo + 60) < 1e-6, MensajeValorEsperadoErroneo);

                            AssertIsTrue(Math.Abs(capaBlwh.TintColorGreen - tinteVerde + 60) < 1e-6, MensajeValorEsperadoErroneo);

                            AssertIsTrue(Math.Abs(capaBlwh.TintColorBlue - tinteAzul + 60) < 1e-6, MensajeValorEsperadoErroneo);

                            break;

                        }

                    }

                }

            }

            AssertIsTrue(seEncontróRecursoRequerido, "No se encontró el recurso Blwh especificado");

        }

        EjemploSoporteDeRecursoBlwh(

            "CapaAjusteBlancoNegroRayasMáscara.psd",

            0x28,

            0x3c,

            0x28,

            0x3c,

            0x14,

            0x50,

            false,

            1,

            "\0",

            225.00045776367188,

            211.00067138671875,

            179.00115966796875,

            -1977421,

            -5925001);

        EjemploSoporteDeRecursoBlwh(

            "CapaAjusteBlancoNegroRayasMáscara2.psd",

            0x80,

            0x40,

            0x20,

            0x10,

            0x08,

            0x04,

            true,

            4,

            "\0",

            239.996337890625,

            127.998046875,

            63.9990234375,

            -1015744,

            -4963324);

        Console.WriteLine("La actualización de BlwhResource funciona como se espera. Presione cualquier tecla.");

{{< /highlight >}}

**PSDNET-230. Capacidad para exportar Grupo de capas a Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}

  using (var psdImage = (PsdImage)Image.Load("1.psd"))

            {

                // carpeta con fondo

                LayerGroup carpetaFondo = (LayerGroup)psdImage.Layers[0];

                // carpeta con contenido

                LayerGroup carpetaContenido = (LayerGroup)psdImage.Layers[4];

                carpetaFondo.Save("fondo.png", new PngOptions());

                carpetaContenido.Save("contenido.png", new PngOptions());

            }

{{< /highlight >}}

` `**PSDNET-372. Soporte de recurso lspf (Contiene configuraciones sobre la configuración de capa protegida)**

{{< highlight java >}}

         const string MensajeValorEsperadoErroneo = "El valor de propiedad esperado no es igual al valor actual";

        void AssertIsTrue(bool condición, string mensaje)

        {

            if (!condición)

            {

                throw new FormatException(mensaje);

            }

        }

        string nombreArchivoFuente = "MuestraParaRecurso.psd";

        string nombreArchivoDestino = "Salida" + nombreArchivoFuente;

        bool seEncontróRecursoRequerido = false;

        using (PsdImage im = (PsdImage)Image.Load(nombreArchivoFuente))

        {

            foreach (var capa in im.Layers)

            {

                foreach (var recursoCapa in capa.Resources)

                {

                    if (recursoCapa is LspfResource)

                    {

                        var recurso = (LspfResource)recursoCapa;

                        seEncontróRecursoRequerido = true;

                        AssertIsTrue(false == recurso.IsCompositeProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(false == recurso.IsPositionProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(false == recurso.IsTransparencyProtected, MensajeValorEsperadoErroneo);

                        // Prueba de edición y guardado

                        recurso.IsCompositeProtected = true;

                        AssertIsTrue(true == recurso.IsCompositeProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(false == recurso.IsPositionProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(false == recurso.IsTransparencyProtected, MensajeValorEsperadoErroneo);

                        recurso.IsCompositeProtected = false;

                        recurso.IsPositionProtected = true;

                        AssertIsTrue(false == recurso.IsCompositeProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(true == recurso.IsPositionProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(false == recurso.IsTransparencyProtected, MensajeValorEsperadoErroneo);

                        recurso.IsPositionProtected = false;

                        recurso.IsTransparencyProtected = true;

                        AssertIsTrue(false == recurso.IsCompositeProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(false == recurso.IsPositionProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(true == recurso.IsTransparencyProtected, MensajeValorEsperadoErroneo);

                        recurso.IsCompositeProtected = true;

                        recurso.IsPositionProtected = true;

                        recurso.IsTransparencyProtected = true;

                        im.Save(nombreArchivoDestino);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(seEncontróRecursoRequerido, "No se encontró el recurso Lspf especificado");

        seEncontróRecursoRequerido = false;

        using (PsdImage im = (PsdImage)Image.Load(nombreArchivoDestino))

        {

            foreach (var capa in im.Layers)

            {

                foreach (var recursoCapa in capa.Resources)

                {

                    if (recursoCapa is LspfResource)

                    {

                        var recurso = (LspfResource)recursoCapa;

                        seEncontróRecursoRequerido = true;

                        AssertIsTrue(recurso.IsCompositeProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(recurso.IsPositionProtected, MensajeValorEsperadoErroneo);

                        AssertIsTrue(recurso.IsTransparencyProtected, MensajeValorEsperadoErroneo);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(seEncontróRecursoRequerido, "No se encontró el recurso Lspf especificado");

        Console.WriteLine("La actualización de LspfResource funciona como se espera. Presione cualquier tecla.");

{{< /highlight >}}

` `**PSDNET-370. Soporte de recurso infx (Contiene datos sobre la Mezcla de elementos interiores)**

{{< highlight java >}}

         void AssertIsTrue(bool condición, string mensaje)

        {

            if (!condición)

            {

                throw new FormatException(mensaje);

            }

        }

        string nombreArchivoFuente = "MuestraParaRecurso.psd";

        string nombreArchivoDestino = "Salida" + nombreArchivoFuente;

        bool seEncontróRecursoRequerido = false;

        using (PsdImage im = (PsdImage)Image.Load(nombreArchivoFuente))

        {

            foreach (var capa in im.Layers)

            {

                foreach (var recursoCapa in capa.Resources)

                {

                    if (recursoCapa is InfxResource)

                    {

                        var recurso = (InfxResource)recursoCapa;

                        seEncontróRecursoRequerido = true;

                        AssertIsTrue(!recurso.BlendInteriorElements, "El InfxResource.BlendInteriorElements debería ser falso");

                        // Prueba de edición y guardado

                        recurso.BlendInteriorElements = true;

                        im.Save(nombreArchivoDestino);

                        break;

                    }

                }

            }

        }

        AssertIsTrue(seEncontróRecursoRequerido, "No se encontró el recurso Infx especificado");

        seEncontróRecursoRequerido = false;

        using (PsdImage im = (PsdImage)Image.Load(nombreArchivoDestino))

        {

            foreach (var capa in im.Layers)

            {

                foreach (var recursoCapa in capa.Resources)

                {

                    if (recursoCapa is InfxResource)

                    {

                        var recurso = (InfxResource)recursoCapa;

                        seEncontróRecursoRequerido = true;

                        AssertIsTrue(recurso.BlendInteriorElements, "El InfxResource.BlendInteriorElements debería cambiar a verdadero");

                        break;

                    }

                }

            }

        }

        AssertIsTrue(seEncontróRecursoRequerido, "No se encontró el recurso Infx especificado");

{{< /highlight >}}

**PSDNET-251. Refactorización de PsdImage y Layer para cambiar el comportamiento de la Transformación (Tamaño correcto/rotación/recorte para máscaras de capa si transformamos una capa por separado)**

{{< highlight java >}}

             var enums = (RotateFlipType[])Enum.GetValues(typeof(RotateFlipType));

            var fileNames = new string[]

            {

                "UnaRegularYUnaAjusteConVectorYMáscaraDeCapa",

                "UnaRegularYUnaAjusteConMáscaraDeCapa", 

                "CapaTexto",

                "FormasVinculadasConTexto"

            };

            foreach (string nombreArchivo in fileNames)

            {

                foreach (RotateFlipType rotateFlipType in enums)

                {

                    string nombreArchivoFuente = nombreArchivo + ".psd";

                    string nombreArchivoDestino = nombreArchivo + "_" + rotateFlipType;

                    var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

                    using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente, psdLoadOptions))

                    {

                        imagen.RotateFlip(rotateFlipType);

                        imagen.Save(nombreArchivoDestino);

                    }

                }

            }

{{< /highlight >}}

**PSDNET-276. En algunas configuraciones de globalización, la imagen raster de AI no se puede abrir**

{{< highlight java >}}

        string nombreArchivoFuente = "formulario_raster_8.ai";

        System.Threading.Thread.CurrentThread.CurrentCulture = new System.Globalization.CultureInfo("ru_RU");

        System.Threading.Thread.CurrentThread.CurrentUICulture = System.Threading.Thread.CurrentThread.CurrentCulture;

        using (AiImage imagen = (AiImage)Image.Load(nombreArchivoFuente))

        {

            // no debería lanzarse ninguna excepción

        }

{{< /highlight >}}

**PSDNET-194. Después de realizar la operación FlipRotate en la capa, la imagen PSD se vuelve ilegible**

{{< highlight java >}}

             string nombreArchivoFuente = GetFileInCustomFolderRelativeToBase(@"testdata\Issues\IMAGINGNET-2617\1.psd");

            var tipoFlip = RotateFlipType.Rotate90FlipNone;

            var nombreArchivoSalidaPsd = this.GetFileInOutputFolder("PruebaRotarVoltear2617.psd");

            try

            {

                using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))

                {

                    for (int i = 0; i < imagen.Layers.Length; i++)

                    {

                        var capa = imagen.Layers[i];

                        if (!capa.Bounds.IsEmpty)

                        {

                            capa.RotateFlip(tipoFlip);

                        }

                    }

                    string nombreArchivoSalidaPng = this.GetFileInOutputFolder("PruebaRotarVoltear2617.png");

                    imagen.Save(nombreArchivoSalidaPsd);

                }

            // Aquí obtenemos una excepción. Para Photoshop este archivo también es ilegible,

            using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoSalidaPsd)) // Lanza una excepción

            {

                // No hacer nada

            }

{{< /highlight >}}

**PSDNET-177. System.ArgumentException durante la carga del archivo PSD**

{{< highlight java >}}

         string rutaFuente = "1.psd";

        string rutaPsd = "PruebaRotarVoltear2617.psd";

        RotateFlipType tipoVolteo = RotateFlipType.Rotate270FlipXY;

        using (var im = (PsdImage)(Image.Load(rutaFuente)))

        {

            im.RotateFlip(tipoVolteo);

            im.Save(rutaPsd);

        }

        using (var im = (PsdImage)(Image.Load(rutaPsd))) // Aquí no deberíamos obtener excepciones

        {

            // no hacer nada

        }

{{< /highlight >}}

**PSDNET-249. Después de usar un método de transformación solo para una capa, la capa guardada tiene límites incorrectos o una máscara**

{{< highlight java >}}

         void AssertIsTrue(bool condición, string mensaje)

        {

            if (!condición)

            {

                throw new FormatException(mensaje);

            }

        }

        const double Tolerancia = 1e-6;

        int nuevoAncho = 132;

        int nuevaAltura = 247;

        double xEscala = nuevoAncho / 48.0;

        double yEscala = nuevaAltura / 19.0;

        string nombreArchivoFuente = "CapaTexto.psd";

        string nombreArchivoSalida = "CapaTextoRedimensionar" + nuevoAncho + "_" + nuevaAltura;

        var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

        using (PsdImage imagen = (PsdImage) Image.Load(nombreArchivoFuente, psdLoadOptions))

        {

            var capa = imagen.Layers[1] as TextLayer;

            var nuevoIzquierda = capa.Izquierda - (nuevoAncho - capa.Ancho) / 2;

            var nuevoArriba = capa.Arriba - (nuevaAltura - capa.Altura) / 2;

            capa.Redimensionar(nuevoAncho, nuevaAltura);

            AssertIsTrue(capa.Izquierda == nuevoIzquierda, "La propiedad Izquierda de la capa debería ser " + nuevoIzquierda);

            AssertIsTrue(capa.Arriba == nuevoArriba, "La propiedad Arriba de la capa debería ser " + nuevoArriba);

            AssertIsTrue(capa.Ancho == nuevoAncho, "La propiedad Ancho de la capa debería ser " + nuevoAncho);

            AssertIsTrue(capa.Altura == nuevaAltura, "La propiedad Altura de la capa debería ser " + nuevaAltura);

            AssertIsTrue(Math.Abs(capa.MatrizTransformación[0] - xEscala) <= Tolerancia, "La propiedad MatrizTransformación[0] de la capa debería ser " + xEscala);

            AssertIsTrue(Math.Abs(capa.MatrizTransformación[3] - yEscala) <= Tolerancia, "La propiedad MatrizTransformación[3] de la capa debería ser " + yEscala);

            AssertIsTrue(Math.Abs(capa.MatrizTransformación[4] - nuevoIzquierda) <= Tolerancia, "La propiedad MatrizTransformación[4] de la capa debería ser " + nuevoIzquierda);

            AssertIsTrue(Math.Abs(capa.MatrizTransformación[5] - nuevoArriba) <= Tolerancia, "La propiedad MatrizTransformación[5] de la capa debería ser " + nuevoArriba);

            imagen.Save(nombreArchivoSalida + ".psd", new PsdOptions());

            imagen.Save(nombreArchivoSalida + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

        }

{{< /highlight >}}
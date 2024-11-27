---
title: Notas de la versión de Aspose.PSD for .NET 19.12
type: docs
weight: 10
url: /es/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}} 

Esta página contiene notas de la versión de [Aspose.PSD for .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-11|[Soporte de Capa Enlazada](/psd/es/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|Característica|
|PSDNET-131|[Soporte de SoCoResource](/psd/es/net/support-of-socoresource/)|Característica|
|PSDNET-115|Se agregan saltos de línea a los saltos de línea existentes si la capa de texto se actualiza con una cadena|Error|
|PSDNET-157|Congelación al guardar PSB como PNG|Error|
|PSDNET-250|Excepción al cargar archivo PSD CMYK sin capas con compresión RLE|Error|
|PSDNET-161|Excepción al actualizar capas de texto|Error|
|PSDNET-222|Redimensionar algunos archivos PSD con máscaras de capa funciona incorrectamente|Error|
|PSDNET-244|Guardar PSD con CurrentCulture de Globalization.CultureInfo conduce a excepciones al cargar|Error|

## **Cambios en la API pública**
# **APIs Añadidas:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **APIs Eliminadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Ejemplos de Uso:**
**PSDNET-11. Soporte de Capa Enlazada**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("ejemplo.psd"))

            {

                Layer[] layers = psd.Layers;

                // enlazar todas las capas en un grupo enlazado

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // obtener ID para una capa

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId y linkGroupId no son iguales.");

                }

                // obtener todas las capas enlazadas por ID de grupo de enlace.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // desenlazar cada capa del grupo

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // recuperar NULL para un ID de grupo de enlace que no tiene capas en el grupo.

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("El campo linkedLayers no es NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. Soporte de SoCoResource**

{{< highlight java >}}

      // Soporte de SoCoResource

    string nombreArchivoOrigen = "ColorFillLayer.psd";

    string rutaExportación = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(nombreArchivoOrigen);

    using (im)

    {

        foreach (var capa in im.Layers)

        {

            if (capa is FillLayer)

            {

                var fillLayer = (FillLayer)capa;

                foreach (var recurso in fillLayer.Resources)

                {

                    if (recurso is SoCoResource)

                    {

                        var recursoSoCo = (SoCoResource)recurso;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), recursoSoCo.Color);

                        recursoSoCo.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            im.Save(rutaExportación);

        }

    }

{{< /highlight >}}

**PSDNET-115. Se agregan saltos de línea a los saltos de línea existentes si la capa de texto se actualiza con una cadena**

{{< highlight java >}}

           const string NuevoTexto = "abcdef\rzxcvbn";

        string rutaArchivoOrigen = "ArchivoPruebaParaCaracteresAsiáticos.psd");

        string rutaArchivoSalida = "resultado.psd";

        using (var imagen = (PsdImage)Image.Load(rutaArchivoOrigen))

        {

            var capa = (TextLayer)imagen.Layers[0];

            var opcionesImagen = new PsdOptions(imagen);

            capa.UpdateText(NuevoTexto);

            imagen.Save(rutaArchivoSalida, opcionesImagen);

        }

        using (var imagenCreada = (PsdImage)Image.Load(rutaArchivoSalida))

        {

            var capaCreada = (TextLayer)imagenCreada.Layers[0];

            if (NuevoTexto != capaCreada.Text)

            {

                throw new InvalidDataException("El texto actualizado no es válido");

            }

        }

{{< /highlight >}}

**PSDNET-157. Congelación al guardar PSB como PNG**

{{< highlight java >}}

       // Guardar PSB como PNG 

    string nombreArchivoOrigen = "muestra.psb";

    string nombreArchivoSalida = "muestra.png";

    using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoOrigen))

    {

        PngOptions opciones = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        imagen.Save(nombreArchivoSalida, opciones);

    }

{{< /highlight >}}



` `**PSDNET-250. Excepción al cargar archivo PSD CMYK sin capa con compresión RLE**

{{< highlight java >}}

     void LoadRawDataFromPsd()

        {

            string rutaOrigen = "CianConAlfa.psd";

            using (RasterImage imagen = (RasterImage)Image.Load(rutaOrigen))

            {

                var configuracionesRawData = imagen.RawDataSettings;

                RawDataTester cargador = new RawDataTester();

                imagen.LoadRawData(imagen.Bounds, configuracionesRawData, cargador);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle rectángulo, byte[] píxeles, Point inicio, Point fin)

            {

            }

            public void Process(Rectangle rectángulo, byte[] píxeles, Point inicio, Point fin, LoadOptions opcionesCarga)

            {

            }

        }

{{< /highlight >}}

` `**PSDNET-161. Excepción al actualizar capas de texto**

{{< highlight java >}}

      // Cargar un archivo PSD como imagen y convertirlo en PsdImage

    using (PsdImage imagenPsd = (PsdImage)Image.Load("ejemplo.psd"))

    {

        foreach (var capa in imagenPsd.Layers)

        {

            if (capa is TextLayer)

            {

                TextLayer capaTexto = capa as TextLayer;

                capaTexto.UpdateText("actualización de prueba", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        imagenPsd.Save("ActualizarCapaTextoEnArchivoPSD_salida.psd");

    }

{{< /highlight >}}



**PSDNET-222. Redimensionar algunos archivos PSD con máscaras de capa funciona incorrectamente**

{{< highlight java >}}

     int escala = 2;

        string[] nombres = {

                             "UnaRegularYUnaAjusteConVectorYMáscaraDeCapa",

                             "CapaDeNivelesConMáscaraDeCapaRgb",

                             "CapaDeNivelesConMáscaraDeCapaCmyk",

                             "CapaDeAjusteDeBalanceDeColor"

                         };

        for (int i = 0; i < nombres.Length; i++)

        {

            string rutaArchivoOrigen = nombres[i] + ".psd";

            string rutaArchivoSalida = "salida_" + rutaArchivoOrigen;

            string rutaArchivoPngSalida = "salida_" + nombres[i] + ".png";

            var opcionesCargaPsd = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage imagen = (PsdImage)Image.Load(rutaArchivoOrigen, opcionesCargaPsd))

            {

                imagen.Resize(imagen.Width * escala, imagen.Height * escala);

                imagen.Save(rutaArchivoSalida, new PsdOptions());

                imagen.Save(rutaArchivoPngSalida, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}



**PSDNET-244. Guardar PSD con ciertas  Globalization.CultureInfo.CurrentCulture conduce a excepciones al cargar**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string nombreArchivoOrigen = string.Format("ejemplo-{0}.psd", i);

            var opcionesCargaPsd = new PsdLoadOptions() { LoadEffectsResource = true };

            var opcionesGuardadoPsd = new PsdOptions();

            var cultura = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = cultura;

            System.Threading.Thread.CurrentThread.CurrentUICulture = cultura;

            string nombreArchivoSalida = "salida-" + nombreArchivoOrigen;

            // Cargar un archivo PSD como imagen y convertirlo en PsdImage

            using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoOrigen, opcionesCargaPsd))

            {

                imagen.Resize(160, 120);

                imagen.Save(nombreArchivoSalida, opcionesGuardadoPsd);

            }

            cultura = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = cultura;

            System.Threading.Thread.CurrentThread.CurrentUICulture = cultura;

            // Cargar un archivo PSD como imagen y convertirlo en PsdImage

            using (PsdImage imagen2 = (PsdImage)Image.Load(nombreArchivoOrigen, opcionesCargaPsd))

            {

                imagen2.Resize(160, 120);

                imagen2.Save(nombreArchivoSalida, opcionesGuardadoPsd);

            }

        }

{{< /highlight >}}

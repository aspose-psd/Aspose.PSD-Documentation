---
title: Notas de la versión de Aspose.PSD para .NET 18.8
type: docs
weight: 50
url: /es/net/aspose-psd-for-net-18-8-release-notes/
---

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-68|Soporte de la propiedad LayerCreationDateTime.|Característica|
|PSDNET-67|Soporte de SheetColor Highlighting|Característica|
|PSDNET-66|Capacidad de fusionar capas una con otra|Característica|
|PSDNET-65|Agregar soporte parcial de la propiedad Text Layer BoundBox|Característica|
|PSDNET-64|Agregar soporte para IopaResource|Característica|
|PSDNET-56|Soporte de efectos de capas para formato PSD|Característica|
|PSDNET-55|Soporte InterruptMonitor para .Net|Característica|
|PSDNET-50|Hacer posible aplanar capas|Característica|
|PSDNET-49|Agregar la representación de la propiedad de opacidad de relleno en capas.|Característica|
|PSDNET-43|Implementar la representación de la capa de ajuste Curvas|Característica|
|PSDNET-42|Agregar soporte de capa de ajuste Curvas|Característica|
|PSDNET-41|Implementar la representación de la capa de ajuste Niveles|Característica|
|PSDNET-40|Agregar soporte de la capa de ajuste Niveles|Característica|
|PSDNET-37|Agregar soporte de capa de ajuste Mezclador de Canales|Característica|
|PSDNET-35|Agregar soporte de capa de ajuste Tono/Saturación|Característica|
|PSDNET-34|Implementar la representación de la capa de ajuste de Exposición para exportación.|Característica|
|PSDNET-31|Agregar soporte de representación para exportación de capas de ajuste ChannelMixer|Característica|
|PSDNET-26|Agregar soporte de máscara de recorte|Característica|
|PSDNET-13|Agregar soporte de la máscara de capa|Característica|
|PSDNET-9|Agregar soporte de capa de ajuste Filtro fotográfico|Característica|
|PSDNET-8|Agregar soporte de capa de ajuste Mezclador de Canales|Característica|
|PSDNET-7|Agregar soporte de capa de ajuste de Exposición|Característica|
|PSDNET-6|Agregar soporte de capa de ajuste Brillo/Contraste|Característica|
|PSDNET-5|Agregar soporte parcial de capas de ajuste|Característica|
|PSDNET-3|Agregar soporte para la opción de texto PSD NoBreak|Característica|
|PSDNET-2|Capacidad de agregar capa de texto en tiempo de ejecución|Característica|
|PSDNET-62|El Códec TIFF no puede guardar imágenes de canales de 16 bits|Mejora|
|PSDNET-61|La realización de imágenes PSD produce colores de imagen no válidos|Mejora|
|PSDNET-60|La coordenada de la esquina superior izquierda es incorrecta al actualizar|Mejora|
|PSDNET-59|Excepción al actualizar capas de texto|Mejora|
|PSDNET-58|Exponer la propiedad Codec de la imagen JPEG2000 al público|Mejora|
|PSDNET-57|Corregir la configuración de opciones de 24bpp para exportar a BMP|Mejora|
|PSDNET-46|La capa de ajuste se ignoró para la conversión de PSD CMYK a TIFF o JPG|Mejora|

## **Ejemplos de uso:**

**PSDNET-68 Soporte de la propiedad LayerCreationDateTime**

{{< highlight java >}}

 // Ejemplo de propiedad LayerCreationDateTime

string nombreArchivoFuente = "CapaUno.psd";

using (var im = (PsdImage)(Image.Load(nombreArchivoFuente)))

{

    var capa = im.Layers[0];

    var fechaCreacion = capa.LayerCreationDateTime;

    var fechaHoraEsperada = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(fechaHoraEsperada, fechaCreacion);

    var ahora = DateTime.Now;

    var capaCreada = im.AddLevelsAdjustmentLayer();

    // Verificar si la Fecha y Hora de Creación se actualizó en las nuevas capas creadas

    Assert.True(ahora <= capaCreada.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Soporte de SheetColor Highlighting**

{{< highlight java >}}

 // Uso del ejemplo de la propiedad SheetColorHighlight

string nombreArchivoFuente = "EjemploHojaColorResaltado.psd";

string rutaExportación = "EjemploHojaColorResaltadoCambiado.psd";

using (var im = (PsdImage)(Image.Load(nombreArchivoFuente)))

{

    var capa1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, capa1.SheetColorHighlight);

    var capa2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, capa2.SheetColorHighlight);



    capa1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(rutaExportación);	

}

{{< /highlight >}}

**PSDNET-66 Capacidad de fusionar capas una con otra**

{{< highlight java >}}

 // Ejemplo de fusionar dos capas

var archivoFuente1 = "MuestraOpacidadRelleno.psd";

var archivoFuente2 = "TresCapasRegularesSemitransparente.psd";

var rutaExportación = "CapasFusionadasDeDosPsdDiferentes.psd";

using (var im1 = (PsdImage)(Image.Load(archivoFuente1)))

{

    var capa1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(archivoFuente2))

    {

        var capa2 = im2.Layers[0];

        capa1.MergeLayerTo(capa2);

	    im2.Save(rutaExportación);	

    }

}

{{< /highlight >}}

**PSDNET-65 Agregar soporte parcial de la propiedad Text Layer BoundBox**

{{< highlight java >}}

 // Ejemplo de cuadro de texto

string nombreArchivoFuente = "CapaConTexto.psd";

var tamañoÓpticoCorrecto = new Size(127, 45);

var cuadroLímiteCorrecto = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(nombreArchivoFuente))

{

    var capaTexto = (TextLayer)im.Layers[1];

    // El tamaño de la capa es el tamaño del área renderizada

    var tamañoÓptico = capaTexto.Size;

    Assert.AreEqual(tamañoÓpticoCorrecto, tamañoÓptico);

    // TextBoundBox es el tamaño máximo de la capa para la capa de texto.

    // En esta área PS intentará ajustar tu texto

    var cuadroLímite = capaTexto.TextBoundBox;

    Assert.AreEqual(cuadroLímiteCorrecto, cuadroLímite);

}

{{< /highlight >}}

**PSDNET-64 Agregar soporte para IopaResource**

{{< highlight java >}}

 // Cambiar la propiedad de Opacidad de Relleno mediante el cambio de IopaResource

string nombreArchivoFuente = "MuestraOpacidadRelleno.psd";

string rutaExportación = "MuestraOpacidadRellenoCambiada.psd";

using (var im = (PsdImage)(Image.Load(nombreArchivoFuente))

{

    var capa = im.Layers[2];



    var recursos = capa.Resources;

    foreach (var recurso in recursos)

    {

        if (recurso is IopaResource)

        {

            var recursoIopa = (IopaResource)recurso;

            recursoIopa.FillOpacity = 200;

        }

    }



    im.Save(rutaExportación);	

}

{{< /highlight >}}

**PSDNET-56 Soporte de efectos de capas para formato PSD**

{{< highlight java >}}

 using (

    PsdImage imagen =

        (PsdImage)

        Aspose.PSD.Image.Load(

            nombreArchivoFuente,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    imagen.Save(

                salida,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 Soporte InterruptMonitor para .Net**

{{< highlight java >}}

         public void PruebaMonitorInterrupción(string dir, string dirSalida)

        {

            ImageOptionsBase opcionesGuardar = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "gran.psb", dir + "gran_salida.png", opcionesGuardar, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // El tiempo de espera debe ser menor que el tiempo requerido para la conversión de la imagen completa (sin interrupción).

                System.Threading.Thread.Sleep(3000);

                // Interrumpir el proceso

                monitor.Interrupt();

                System.Console.WriteLine("Interrumpiendo el hilo de guardado #{0} en {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Esperar la interrupción...

                thread.Join();

            }

            finally

            {

                // Si el archivo a borrar no existe, no se produce ninguna excepción.

                System.IO.File.Delete(dir + "gran_salida.png");

            }

        }

        /// <summary>

        /// Inicia la conversión de imagen y espera su interrupción.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// La ruta de la imagen de entrada.

            /// </summary>

            private readonly string rutaEntrada;

            /// <summary>

            /// La ruta de la imagen de salida.

            /// </summary>

            private readonly string rutaSalida;

            /// <summary>

            /// El monitor de interrupción.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Las opciones de guardado.

            /// </summary>

            private readonly ImageOptionsBase opcionesGuardar;

            /// <summary>

            /// Inicializa una nueva instancia de la clase <see cref="SaveImageWorker" />.

            /// </summary>

            /// <param name="rutaEntrada">La ruta de la imagen de entrada.</param>

            /// <param name="rutaSalida">La ruta de la imagen de salida.</param>

            /// <param name="opcionesGuardar">Las opciones de guardado.</param>

            /// <param name="monitor">El monitor de interrupción.</param>

            public SaveImageWorker(string rutaEntrada, string rutaSalida, ImageOptionsBase opcionesGuardar, Multithreading.InterruptMonitor monitor)

            {

                this.rutaEntrada = rutaEntrada;

                this.rutaSalida = rutaSalida;

                this.opcionesGuardar = opcionesGuardar;

                this.monitor = monitor;

            }

            /// <summary>

            /// Intenta convertir una imagen de un formato a otro. Maneja la interrupción.

            /// </summary>

            public void ThreadProc()

            {

                using (Image imagen = Image.Load(this.rutaEntrada))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        imagen.Save(this.rutaSalida, this.opcionesGuardar);

                        Assert.Fail("Se esperaba una interrupción.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("El hilo de guardado #{0} finaliza en {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    finally

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}
---
title: Notas de Lanzamiento de Aspose.PSD para .NET 22.9
type: docs
weight: 40
url: /es/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}
Esta página contiene las notas de lanzamiento para [Aspose.PSD para .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)
{{% /alert %}}

{{% alert color="warning" %}}
- Esta versión tiene una regresión en el caso de exportaciones de 16 bits, por lo que recomendamos precaución al usar esta función en este lanzamiento.
Por favor, no actualice Aspose.PSD a la versión 22.9 si el procesamiento de imágenes de 16 bits es su funcionalidad principal.
- Para varias versiones de Photoshop, los usuarios pueden encontrar una ventana con un error de lectura de capa, esto no afectará el trabajo con el archivo PSD.

Estamos trabajando en soluciones para estos problemas.

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-1237|Crear el modelo interno LayerStyleFX que contendrá efectos y datos relacionados para usar el modelo único en los recursos de efectos Lfx2, lmfx, y mlst|Mejora|
|PSDNET-1227|Agregar lectura y escritura de estructuras 'Lefx' con información de efectos para estados de capa en modelos de Línea de Tiempo|Característica|
|PSDNET-1230|Aplicar estado de capa de Línea de Tiempo a capa en PsdImage|Característica|
|PSDNET-1072|Transparencia incorrecta al guardar archivo PSD (RGB/16 bits) en la exportación a 8 bits|Error|
|PSDNET-1140|Excepción al cargar paso de recursos de capa global al abrir documento PSB|Error|
|PSDNET-1266|Fuga de memoria en el procesamiento de archivos específicos|Error|


## **Cambios en la API Pública**
# **APIs Agregadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **APIs Eliminadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Ejemplos de Uso:**

**PSDNET-1072. Transparencia incorrecta al guardar archivo PSD (RGB/16 bits) en la exportación a 8 bits**

{{< highlight csharp >}}
string archivoPsdEntrada = "8bitConTransparencia.psd";
string archivoPsdSalida = "16bitConTransparencia.psd";
string archivoImagenSalida = "SalidaConTransparencia.png";

using (var img = Image.Load(archivoPsdEntrada))
{
    // Opciones de guardado de 16 bits
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(archivoPsdSalida, p16);
}
using (var img = Image.Load(archivoPsdSalida))
{
    // Guardar imagen con colores de 16 bits
    img.Save(archivoImagenSalida, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Excepción al cargar paso de recursos de capa global al abrir documento PSB**

{{< highlight csharp >}}
string archivoPsdOrigen = "entrada.psb";
string archivoImagenSalida = "salida.png";

using (var imagen = (PsdImage)Image.Load(archivoPsdOrigen))
{
    // Aquí no debería haber excepción.
    imagen.Save(archivoImagenSalida, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Agregar lectura y escritura de estructuras 'Lefx' con información de efectos para estados de capa en modelos de Línea de Tiempo**

{{< highlight csharp >}}
string archivoFuente = "4_animado.psd";
string archivoSalida = "salida.psd";

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    TimeLine lineaDeTiempo = TimeLine.InitializeFrom(imagenPsd);
    int[] idsCapa = lineaDeTiempo.LayerIds;

    var efectosEstadoCapa11 = lineaDeTiempo.Frames[1].LayerStates[idsCapa[1]].StateEffects;

    efectosEstadoCapa11.AddDropShadow();
    efectosEstadoCapa11.AddGradientOverlay();

    var efectosEstadoCapa21 = lineaDeTiempo.Frames[2].LayerStates[idsCapa[1]].StateEffects;
    efectosEstadoCapa21.AddStroke(FillType.Color);
    efectosEstadoCapa21.IsVisible = false;

    lineaDeTiempo.ApplyTo(imagenPsd);

    imagenPsd.Save(archivoSalida);
}
{{< /highlight >}}

**PSDNET-1230. Aplicar estado de capa de Línea de Tiempo a capa en PsdImage**

{{< highlight csharp >}}
string archivoFuente = "3_animado.psd";
string archivoPsdSalida = "salida.psd";
string archivoPngSalida = "salida.png";

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine lineaDeTiempo = TimeLine.InitializeFrom(imagenPsd);
    var idsCapa = lineaDeTiempo.LayerIds;

    var estadoCapa11 = lineaDeTiempo.Frames[1].LayerStates[idsCapa[1]];

    lineaDeTiempo.Frames[1].LayerStates[idsCapa[1]].StateEffects.AddPatternOverlay();
    estadoCapa11.BlendMode = BlendMode.Multiply;

    // Cambiar el fotograma activo de 0 a 1 para activar la aplicación de LayerState a Layer
    lineaDeTiempo.ActiveFrame = 1;

    // Aplicar cambios a PsdImage
    lineaDeTiempo.ApplyTo(imagenPsd);

    imagenPsd.Save(archivoPsdSalida);
    imagenPsd.Save(archivoPngSalida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Fuga de memoria en el procesamiento de archivos específicos**

{{< highlight csharp >}}
string[] archivosParaCargar = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int numeroEntrada = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(numeroEntrada, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double contadorMemoria = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total de bytes utilizados antes de la prueba: {0:N2} MiB", contadorMemoria);

double maximo = contadorMemoria;

for (int i = 0; i < 50; i++)
{
    int indiceArchivo = i % numeroEntrada;
    string archivoFuente = Path.Combine(baseFolder, archivosParaCargar[indiceArchivo]);

    // VerificarAperturaGuardado
    using (MemoryStream flujoSalida = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(flujoSalida, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(numeroEntrada, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    contadorMemoria = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    maximo = Math.Max(maximo, contadorMemoria);
}

contadorMemoria = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total de bytes utilizados después de la prueba: {0:N2} MiB", contadorMemoria);
Assert.IsTrue(Math.Abs(contadorMemoria - maximo) < 20, "¡Fuga de memoria encontrada en funcionalidad base!"); 
{{< /highlight >}}

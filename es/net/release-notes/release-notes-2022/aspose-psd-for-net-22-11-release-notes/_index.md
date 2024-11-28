---
title: Notas de la versión de Aspose.PSD para .NET 22.11
type: docs
weight: 20
url: /es/net/aspose-psd-para-net-22-11-notas-de-la-version/
---

{{% alert color = "primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color = "warning" %}}

- Esta versión tiene una regresión en el caso de exportaciones de 16 bits, por lo que recomendamos precaución al usar esta característica en esta versión.
Por favor, no actualice Aspose.PSD a 22.9-22.11 si el procesamiento de imágenes de 16 bits es su funcionalidad principal.

Estamos trabajando en soluciones para estos problemas.

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-1320|No se pueden exportar archivos PSB extremadamente grandes|Mejora|
|PSDNET-659|Hacer el centro del degradado radial móvil|Característica|
|PSDNET-1330|Método de compresión ZipWithoutPrediction no soportado para archivos específicos|Característica|
|PSDNET-735|Después de usar un método de transformación solo para una capa, la capa guardada tiene una caja delimitadora incorrecta|Error|
|PSDNET-1234|Excepción al cargar una imagen PSD con patrón|Error|
|PSDNET-1244|Error en la exportación de imagen (IndexOutOfRangeException) al guardar un archivo PSD con símbolos chinos|Error|
|PSDNET-1303|El marco activo de la línea de tiempo se aplica de forma incorrecta|Error|
|PSDNET-1307|Regresión 22.7: representación incorrecta de texto con caracteres árabes|Error|
|PSDNET-1321|La máscara vectorial en la capa de grupo funciona de manera incorrecta. La imagen final tiene el agujero negro pero no debería|Error|


## **Cambios en la API Pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDNET-659. Hacer el centro del degradado radial móvil**

{{< highlight csharp >}}
string archivoFuente = "psdnet659.psd";
string archivoSalida = "salida.png";

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    FillLayer capaRadial = (FillLayer)imagenPsd.Layers[5];
    GradientFillSettings ajustes = (GradientFillSettings)capaRadial.FillSettings;

    // Actualizar el punto de desplazamiento
    ajustes.HorizontalOffset = 10;
    ajustes.VerticalOffset = -25;

    imagenPsd.Save(archivoSalida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Después de usar un método de transformación solo para una capa, la capa guardada tiene una caja delimitadora incorrecta**

{{< highlight csharp >}}
string nombreArchivoFuente = @"TextLayer.psd";
string archivoSalida = "TextLayerRedimensionada_output.psd";

using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente, new PsdLoadOptions()))
{
    TextLayer capaTexto = (TextLayer)imagen.Layers[1];

    // Establece el nuevo tamaño de la capa de texto
    const int NuevoAncho = 250;
    const int NuevaAltura = 250;

    // Establece el mecanismo de cómo la función de redimensionamiento cambiará el tamaño de la capa (valor predeterminado)
    ResizeType tipoRedimensionamiento = ResizeType.NearestNeighbourResample;

    // Nuevo mecanismo de redimensionamiento para la capa de texto se utiliza aquí
    // No solo la capa sino también la matriz de transformación de la capa de texto se cambiarán
    capaTexto.Resize(NuevoAncho, NuevaAltura, tipoRedimensionamiento);

    imagen.Save(archivoSalida, new PsdOptions(imagen));
}

using (PsdImage imagen = (PsdImage)Image.Load(archivoSalida, new PsdLoadOptions()))
{
    TextLayer capaTxt = (TextLayer)imagen.Layers[1];

    // La razón del delta es una fuente predeterminada diferente
    if (capaTxt.TransformMatrix[4] >= 65 
        && capaTxt.TransformMatrix[4] <= 67
        && capaTxt.TransformMatrix[5] >= 234
        && capaTxt.TransformMatrix[5] <= 237)
    {
        // Todo está correcto
    }
    else
    {
        throw new Exception("El punto de ubicación es incorrecto");
    }
}
{{< /highlight >}}

**PSDNET-1234. Excepción al cargar una imagen PSD con patrón**

{{< highlight csharp >}}
string archivoFuente = "test.psd";
string salida = "salida1234.png";

using (PsdImage imagenPsd = (PsdImage)PsdImage.Load(archivoFuente,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions opcionesPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    imagenPsd.Save(salida, opcionesPng);
}
{{< /highlight >}}

**PSDNET-1244. Error en la exportación de imagen (IndexOutOfRangeException) al guardar un archivo PSD con símbolos chinos**

{{< highlight csharp >}}
string archivoFuente = "input.psd";
string rutaSalida = "output.psd";

var opcionesCarga = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var imagen = (PsdImage)Image.Load(archivoFuente, opcionesCarga))
{
    foreach (var capa in imagen.Layers)
    {
        if (capa.Name == "1")
        {
            var capaTxt = (TextLayer)capa;

            capaTxt.UpdateText("测试测试");
        }
    }

    // Aquí no debería haber excepción.
    imagen.Save(rutaSalida, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. El marco activo de la línea de tiempo se aplica de forma incorrecta**

{{< highlight csharp >}}
string fuente = "timeline1303.psd";
string salida = "salida_timeline.psd";

using (var imagenPsd = (PsdImage)Image.Load(fuente))
{
    TimeLine lineaTiempo = TimeLine.InitializeFrom(imagenPsd);

    lineaTiempo.ActiveFrame = 2;
    lineaTiempo.ApplyTo(imagenPsd);

    imagenPsd.Save(salida);
}
{{< /highlight >}}

**PSDNET-1307. Regresión 22.7: representación incorrecta de texto con caracteres árabes**

{{< highlight csharp >}}
string carpetaFuentesPrueba = "Fuentes";
FontSettings.SetFontsFolder(carpetaFuentesPrueba);
FontSettings.UpdateFonts();

string rutaArchivoFuente = "sarbarg.fin12.psd";
string rutaArchivoSalida = "resultado.tiff";

using (var imagenPsd = (PsdImage)Image.Load(rutaArchivoFuente))
{
    imagenPsd.Save(rutaArchivoSalida, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. No se pueden exportar archivos PSB extremadamente grandes**

{{< highlight csharp >}}
string archivoFuente = "hf-mim-liman-han-guc-art-kuvvet.psb";
string rutaExportacionPsd = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    imagen.Save(rutaExportacionPsd, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. La máscara vectorial en la capa de grupo funciona de manera incorrecta. La imagen final tiene el agujero negro pero no debería**

{{< highlight csharp >}}
string archivoFuente = "demo.psd";
string salida = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(archivoFuente))
{
    PngOptions opcionesPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(salida, opcionesPng);
}
{{< /highlight >}}

**PSDNET-1330. Método de compresión ZipWithoutPrediction no soportado para archivos específicos**

{{< highlight csharp >}}
string archivoFuente = "20221017_220706_0000.psd";
string archivoSalida = "20221017_220706_0000.jpg";

using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase opcionesBase = new JpegOptions() { Quality = 80 };
    imagen.Save(archivoSalida, opcionesBase);
}
{{< /highlight >}}

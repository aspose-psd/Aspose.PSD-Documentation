---
title: Notas de la versión de Aspose.PSD para .NET 22.12
type: docs
weight: 10
url: /es/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión para [Aspose.PSD for .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- En esta versión se corrigió una regresión con la exportación de 16 bits.

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-1336|Agregar la propiedad editable TextOrientation a la interfaz IText|Característica|
|PSDNET-725|Redimensionar el archivo PSD especificado con una máscara de capa produce una máscara incorrecta|Error|
|PSDNET-1277|Agregar la capacidad de guardar y cargar una máscara para 16 imágenes|Error|
|PSDNET-1281|Transparencia incorrecta al guardar una imagen de 16 bits a una imagen de 16 o 8 bits|Error|
|PSDNET-1375|Corregir CMYK en color de 16 bits|Error|


## **Cambios en la API pública**
# **APIs agregadas:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDNET-725. Redimensionar el archivo PSD especificado con una máscara de capa produce una máscara incorrecta**

{{< highlight csharp >}}
string archivoFuente = "fuente.psd";
string rutaExportacionPSD = "salida.psd";
string rutaExportacionPNG = "salida.png";

// Abre el archivo PSD de origen
using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    const int Escala = 4;

    int nuevoAncho = imagen.Ancho * Escala;
    int nuevaAltura = imagen.Alto * Escala;

    // Realiza el redimensionamiento
    imagen.Redimensionar(nuevoAncho, nuevaAltura);
    imagen.Guardar(rutaExportacionPSD, new PsdOptions(imagen));
}

// Abre un archivo PSD redimensionado
using (PsdImage imagen = (PsdImage)Image.Load(rutaExportacionPSD))
{
    // Renderiza a PNG
    imagen.Guardar(rutaExportacionPNG, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Agregar la capacidad de guardar y cargar una máscara para 16 imágenes**

{{< highlight csharp >}}
string archivoPsd8bitsFuente = @"archivoEntrada_8bitColor.psd";
string archivoPsd16bitsSalida = @"archivoSalida_16bitColor.psd";

using (var imagen = (PsdImage)Image.Load(archivoPsd8bitsFuente))
{
    // Las opciones permiten guardar 16 bits de color
    PsdOptions opciones16 = new PsdOptions { ConteoBitsCanal = 16, ModoColor = ColorModes.Rgb};

    // El archivo PSD se guardará con transparencia
    imagen.Guardar(archivoPsd16bitsSalida, opciones16);
}
{{< /highlight >}}

**PSDNET-1281. Transparencia incorrecta al guardar una imagen de 16 bits a una imagen de 16 o 8 bits**

{{< highlight csharp >}}
string archivoFuente = @"Ejemplo_16bit.psd";
string archivoReGuardado = @"ReGuardar_16bit.psd";
string archivoImagen = @"ImagenTotal_16bit.png";

// Se abrirá y guardará un archivo PSD de 16 bits de color (con transparencia) a 16 bits de color
using (var imagen = (PsdImage)Image.Load(archivoFuente))
{
    PsdOptions opciones16 = new PsdOptions() { ConteoBitsCanal = 16, ModoColor = ColorModes.Rgb };
    imagen.Guardar(archivoReGuardado, opciones16);
}

// El archivo PSD guardado de 16 bits de color se renderizará a archivo PNG con transparencia
using (var imagen = (PsdImage)Image.Load(archivoReGuardado))
{
    imagen.Guardar(archivoImagen, new PngOptions() { TipoColor = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Agregar la propiedad editable TextOrientation a la interfaz IText**

{{< highlight csharp >}}
// El siguiente código demuestra la capacidad de editar la nueva propiedad TextOrientation.
// Esto no afecta la representación en este momento, solo le permite editar el valor de la propiedad.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var imagen = (PsdImage)Image.Load(src))
{
    var capaTexto = imagen.Layers[1] as TextLayer;
    if (capaTexto.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Lectura correcta
    }
    else
    {
        throw new Exception("Lectura incorrecta del valor de la propiedad TextOrientation");
    }

    capaTexto.TextData.TextOrientation = TextOrientation.Horizontal;
    capaTexto.TextData.UpdateLayerData();

    imagen.Guardar(output);
}

using (var imagen = (PsdImage)Image.Load(output))
{
    var capaTexto = imagen.Layers[1] as TextLayer;
    if (capaTexto.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Lectura correcta
    }
    else
    {
        throw new Exception("Lectura incorrecta del valor de la propiedad TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Corregir CMYK en color de 16 bits**

{{< highlight csharp >}}
string archivoFuente = @"ClippingMaskRegular.psd";
string rutaExportacion = @"exportar.psd";
string rutaExportacionPNG = @"exportar.png";

// Establece las opciones de conversión
PsdOptions opcionesPsd = new PsdOptions()
{
    ModoColor = ColorModes.Cmyk,
    ConteoBitsCanal = 16,
    ConteoCanales = 5,
    MétodoCompresión = CompressionMethod.Raw
};

// Convierte y guarda
using (var imagen = (PsdImage)Image.Load(archivoFuente))
{
    imagen.Convertir(opcionesPsd);
    imagen.Guardar(rutaExportacion);
}

// Abre el archivo convertido y lo renderiza a PNG
using (PsdImage imagen = (PsdImage)Image.Load(rutaExportacion))
{
    imagen.Guardar(rutaExportacionPNG, new PngOptions() { TipoColor = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

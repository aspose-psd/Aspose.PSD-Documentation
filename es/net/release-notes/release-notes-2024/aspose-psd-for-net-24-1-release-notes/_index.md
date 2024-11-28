---
title: Notas de la versión de Aspose.PSD para .NET 24.1
type: docs
weight: 120
url: /es/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                      | **Categoría** |
|:------------|:------------------------------------------------------------------------------------------------- |:------------|
| PSDNET-1835 | [AI Format] Agregar manejo básico para imágenes AI de varias páginas                              |   Función   |
| PSDNET-718  | El efecto de texto curvado no se aplica al texto                                                  |     Error    |
| PSDNET-1620 | Renderizado incorrecto de la máscara en el archivo específico                                     |     Error    |
| PSDNET-1855 | NullReferenceException en Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor   |     Error    |
| PSDNET-1883 | [AI Format] Corregir el uso de memoria en AiExporterUtils                                         |     Error    |



## **Cambios en la API pública**
# **APIs Añadidas:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs Eliminadas:**
- Ninguna


## **Ejemplos de uso**

**PSDNET-718. El efecto de texto curvado no se aplica al texto**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "texto_curvado.psd");
string archivoSalida = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(archivoFuente, opt))
{
    img.Save(archivoSalida, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Renderizado incorrecto de la máscara en el archivo específico**

{{< highlight csharp >}}
string archivoFuente1 = Path.Combine(baseFolder, "problema_mascara.psd");
string archivoFuente2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string archivoSalida1 = Path.Combine(outputFolder, "export_mascara.png");
string archivoSalida2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(archivoFuente1, opt))
{
    img.Save(archivoSalida1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(archivoFuente2, opt))
{
    img.Save(archivoSalida2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [AI Format] Agregar manejo básico para imágenes AI de varias páginas**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "tresPaginas.ai");
string primerArchivoSalidaPng = Path.Combine(outputFolder, "primerArchivoSalida.png");
string segundoArchivoSalidaPng = Path.Combine(outputFolder, "segundoArchivoSalida.png");
string tercerArchivoSalidaPng = Path.Combine(outputFolder, "tercerArchivoSalida.png");

// Cargar la imagen de AI.
using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    // Por defecto, ActivePageIndex es 0.
    // Por lo tanto, si guarda la imagen de AI sin cambiar esta propiedad, se representará y guardará la primera página.
    imagen.Save(primerArchivoSalidaPng, new PngOptions());

    // Cambiar el índice de página activa a la segunda página.
    imagen.ActivePageIndex = 1;

    // Guardar la segunda página de la imagen de AI como una imagen PNG.
    imagen.Save(segundoArchivoSalidaPng, new PngOptions());

    // Cambiar el índice de página activa a la tercera página.
    imagen.ActivePageIndex = 2;

    // Guardar la tercera página de la imagen de AI como una imagen PNG.
    imagen.Save(tercerArchivoSalidaPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException en Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string carpetaFuentes = Path.Combine(baseFolder, "Fuentes");
FontSettings.SetFontsFolders(new string[] { carpetaFuentes }, true);

string archivoEntrada = Path.Combine(baseFolder, "1.psd");
string archivoSalida = Path.Combine(outputFolder, "out_1855.png");
using (var imagenPsd = (PsdImage)Image.Load(archivoEntrada))
{
    imagenPsd.Save(archivoSalida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [AI Format] Corregir el uso de memoria en AiExporterUtils**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "tresPaginas.ai");
string primerArchivoSalidaPng = Path.Combine(outputFolder, "primerArchivoSalida.png");
string segundoArchivoSalidaPng = Path.Combine(outputFolder, "segundoArchivoSalida.png");
string tercerArchivoSalidaPng = Path.Combine(outputFolder, "tercerArchivoSalida.png");

const double LímiteMemoria = 220;
double memoriaUtilizada = double.MaxValue;

// Cargar la imagen de AI.
using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    // Guardar la primera página de la imagen de AI como imagen PNG.
    imagen.Save(primerArchivoSalidaPng, new PngOptions());

    // Cambiar el índice de página activa a la segunda página.
    imagen.ActivePageIndex = 1;

    // Guardar la segunda página de la imagen de AI como imagen PNG.
    imagen.Save(segundoArchivoSalidaPng, new PngOptions());

    // Cambiar el índice de página activa a la tercera página.
    imagen.ActivePageIndex = 2;

    // Guardar la tercera página de la imagen de AI como imagen PNG.
    imagen.Save(tercerArchivoSalidaPng, new PngOptions());
}

GC.Collect();

memoriaUtilizada = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoriaUtilizada > LímiteMemoria)
{
    throw new Exception("Uso de memoria es demasiado grande. " + memoriaUtilizada + " en lugar de " + LímiteMemoria.ToString("F1"));
}
{{< /highlight >}}

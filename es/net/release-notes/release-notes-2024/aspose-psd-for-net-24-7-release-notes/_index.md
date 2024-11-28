---
title: Notas de la versión de Aspose.PSD para .NET 24.7
type: docs
weight: 60
url: /es/net/aspose-psd-para-net-24-7-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                       | **Categoría** |
|:------------|:--------------------------------------------------------------------------------------------------|:--------------|
| PSDNET-1029 | Excepción de "Fallo al cargar la imagen" al abrir documento AI                                     | Error         |
| PSDNET-2022 | Texto renderizado incorrectamente en archivos PDF de salida                                         | Error         |
| PSDNET-2061 | Corregir ImageSaveException: Falló la exportación de la imagen para el archivo dado en Linux       | Error         |
| PSDNET-2080 | Corregir carga de fuentes al usar Aspose.Drawing                                                    | Error         |
| PSDNET-2085 | 'La operación aritmética resultó en un desbordamiento' al crear una capa de objeto inteligente usando un JPEG grande | Error         |
| PSDNET-2100 | El archivo AI no se puede convertir en un archivo JPG                                               | Error         |

## **Cambios en la API pública**
# **APIs agregadas:**
- Ninguna

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-1029. Excepción de "Fallo al cargar la imagen" al abrir documento AI**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string archivoSalida = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    imagen.Save(archivoSalida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Texto renderizado incorrectamente en archivos PDF de salida**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var imagenPsd = (PsdImage)Image.Load(src))
{
    PdfOptions opcionesGuardado = new PdfOptions();
    opcionesGuardado.PdfCoreOptions = new PdfCoreOptions();

    imagenPsd.Save(output, opcionesGuardado);
}
{{< /highlight >}}

**PSDNET-2061. Corregir ImageSaveException: Falló la exportación de la imagen para el archivo dado en Linux**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string archivoSalida = Path.Combine(outputFolder, "output.jpg");

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var opcionesGuardado = new JpegOptions() { Quality = 70 };
    imagenPsd.Save(archivoSalida, opcionesGuardado);
}
{{< /highlight >}}

**PSDNET-2080. Corregir carga de fuentes al usar Aspose.Drawing**

{{< highlight csharp >}}
using (var fuentesInstaladas = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Antes de actualizar. Cantidad de fuentes instaladas: " + fuentesInstaladas.Families.Length);
    Console.WriteLine("- Plataforma: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Actualizar la caché de fuentes intentando obtener el nombre de fuente de Adobe para 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Después de actualizar. Cantidad de fuentes instaladas: " + fuentesInstaladas.Families.Length);

    Assert.Greater(fuentesInstaladas.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'La operación aritmética resultó en un desbordamiento' al crear una capa de objeto inteligente usando un JPEG grande**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "source.psd");
string imagenJpg = Path.Combine(baseFolder, "test.jpg");

using (var imagen = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imagenJpg, FileMode.Open))
    {
        var capaAgregada = new SmartObjectLayer(stream);
        capaAgregada.Name = "Capa de prueba";
        imagen.AddLayer(capaAgregada);
    }
}
{{< /highlight >}}

**PSDNET-2100. El archivo AI no se puede convertir en un archivo JPG**

{{< highlight csharp >}}
string archivoFuente = Path.Combine(baseFolder, "aaa.ai");
string archivoSalida = Path.Combine(outputFolder, "aaa.png");

using (AiImage imagen = (AiImage)Image.Load(archivoFuente))
{
    imagen.Save(archivoSalida, new PngOptions());
}
{{< /highlight >}}

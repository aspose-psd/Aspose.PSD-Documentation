---
title: Notas de la versión de Aspose.PSD para .NET 23.9
type: docs
weight: 40
url: /es/net/aspose-psd-for-net-23-9-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                                           | **Categoría** |
|:------------|:----------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | Implementar la creación de una máscara para las nuevas capas de ajuste                                                 | Función  |
| PSDNET-1654 | Agregar soporte para Capas Recortadas mezcladas como opción de mezcla de Grupo                                        | Función  |
| PSDNET-1194 | Los archivos PSD con modo de color de 16 bits no aplican la máscara para las capas de ajuste                           | Error   |
| PSDNET-1235 | Renderizado incorrecto de los corchetes en la capa de texto                                                             | Error   |
| PSDNET-1559 | No se pueden actualizar los estilos en las capas de texto                                                               | Error   |
| PSDNET-1583 | Después de exportar un archivo PSD con CMYK, los colores se rompen en el PSD exportado                                | Error   |
| PSDNET-1619 | Un archivo PSB específico arroja la excepción "El rectángulo no tiene un área de procesamiento común"               | Error   |
| PSDNET-1648 | Falla al cargar la imagen. OverflowError: La operación aritmética produjo un desbordamiento                          | Error   |


## **Cambios en la API Pública**
# **APIs Agregadas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **APIs Eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDNET-1638. Implementar la creación de una máscara para las nuevas capas de ajuste**

{{< highlight csharp >}}
string archivoFuente = "zendeya_BW.psd";
string archivoDestino = "zendeya_BW_salida.psd";

using (var im = (PsdImage)Image.Load(archivoFuente))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(archivoDestino);
}

using (var im = (PsdImage)Image.Load(archivoDestino))
{
    Layer capa = im.Layers[1];

    AssertAreEqual((ushort)5, capa.ChannelsCount);
    AssertAreEqual((short)-2, capa.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Agregar soporte para Capas Recortadas mezcladas como opción de mezcla de Grupo**

{{< highlight csharp >}}
string archivoFuente = "ejemplo_fuente.psd";
string archivoPsdSalida = "ejemplo_salida.psd";
string archivoPngSalida = "ejemplo_salida.png";

using (var imagen = (PsdImage)Image.Load(archivoFuente))
{
    imagen.Layers[1].BlendClippedElements = false;
    imagen.Save(archivoPsdSalida);
    imagen.Save(archivoPngSalida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. Los archivos PSD con modo de color de 16 bits no aplican la máscara para las capas de ajuste**

{{< highlight csharp >}}
string archivoFuente = "fuente.psd";
string archivoPngSalida = "actual.png";

using (var imagen = (PsdImage)Image.Load(archivoFuente))
{
    imagen.Save(archivoPngSalida, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Renderizado incorrecto de los corchetes en la capa de texto**

{{< highlight csharp >}}
string archivo = "archivo1.psd";
string salida = "salida_1235.png";

using (var psdImage = (PsdImage)Image.Load(archivo))
{
    foreach (var capa in psdImage.Layers)
    if (capa is TextLayer capaTexto)
    capaTexto.TextData.UpdateLayerData();

    var opcionesImagen = new PsdOptions(psdImage);
    psdImage.Save(salida, opcionesImagen);
}
{{< /highlight >}}

**PSDNET-1559. No se pueden actualizar los estilos en las capas de texto**

{{< highlight csharp >}}
string archivoFuente = "Ejemplo_TamañoFuente.psd";
string archivoSalida = "salida_Ejemplo_TamañoFuente.psd";

using (var psdImage = (PsdImage)Image.Load(archivoFuente, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdImage.Layers[4];
    var l2 = (TextLayer)psdImage.Layers[5];

    var elementosTexto1 = l1.TextData.ProducePortions(new string[] { "texto1", "texto2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var elemento in elementosTexto1)
    {
        l1.TextData.AddPortion(elemento);
    }

    var elementosTexto2 = l2.TextData.ProducePortions(new string[] { "capa de texto 1", "capa de texto 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var elemento in elementosTexto2)
    {
        l2.TextData.AddPortion(elemento);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdImage.Save(archivoSalida);
}
{{< /highlight >}}

**PSDNET-1583. Después de exportar un archivo PSD con CMYK, los colores se rompen en el PSD exportado**

{{< highlight csharp >}}
string archivoFuente = "cañón.psd";
string archivoSalidaPng = "salida_cañón.png";

using (var flujoSalida = new MemoryStream())
{
    using (var psdImage = (PsdImage)Image.Load(archivoFuente))
    {
        psdImage.Save(flujoSalida);
    }

    flujoSalida.Position = 0;
    using (var psdImage = (PsdImage)Image.Load(flujoSalida))
    {
        psdImage.Save(archivoSalidaPng, new PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. Un archivo PSB específico arroja la excepción "El rectángulo no tiene un área de procesamiento común"**

{{< highlight csharp >}}
var entrada = "1619_src.psb";
var salida = "1619_salida.png";
using (PsdImage img = (PsdImage)Image.Load(entrada, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(salida,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Falla al cargar la imagen. OverflowError: La operación aritmética produjo un desbordamiento**

{{< highlight csharp >}}
string archivoFuente = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(archivoFuente))
{
    Layer capa = im.Layers[28];
    GrdmResource recursoGrdm = (GrdmResource)capa.Resources[0];

    AssertAreEqual("自定", recursoGrdm.GradientName);
}

void AssertAreEqual(object esperado, object actual, string mensaje = null)
{
    if (!object.Equals(esperado, actual))
    {
        throw new Exception(mensaje ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

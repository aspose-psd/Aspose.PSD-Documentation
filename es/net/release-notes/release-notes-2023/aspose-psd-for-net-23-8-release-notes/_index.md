---
title: Notas de la versión de Aspose.PSD para .NET 23.8
type: docs
weight: 50
url: /es/net/aspose-psd-para-net-23-8-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                                  | **Categoría**|
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Agregar nuevo tipo de deformación (Flag) | Característica|
| PSDNET-1621 | Agregar nuevos tipos de deformación: arco hacia arriba, arco hacia abajo, esfera | Característica|
| PSDNET-1682 | Implementar nuevo método PsdImage.AddPosterizeAdjustmentLayer para agregar nueva capa de posterización | Característica|
| PSDNET-913  | Información de PSD perdida solo al abrir y guardar | Error     |
| PSDNET-1352 | Error al cargar la imagen | Error     |
| PSDNET-1553 | Error al cargar la imagen: No se puede convertir el objeto de tipo UnknownStructure al tipo DescriptorStructure | Error     |
| PSDNET-1631 | El archivo modificado en la biblioteca de terceros corrompe el archivo PSD pero se puede abrir en Photoshop | Error     |


## **Cambios en la API pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDNET-913. Información de PSD perdida solo al abrir y guardar**

{{< highlight csharp >}}
string src = "Archivo original.psd";
string outputPsd = "out_Archivo original.psd";
string outputPng = "out_Archivo original.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Error al cargar la imagen**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Error al cargar la imagen: No se puede convertir el objeto de tipo UnknownStructure al tipo DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Debería cargar correctamente
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. El archivo modificado en la biblioteca de terceros corrompe el archivo PSD pero se puede abrir en Photoshop**

{{< highlight csharp >}}
string sourceFile = "salida.psd";
string outputFile = "exportar.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Agregar nuevo tipo de deformación (Flag)**

{{< highlight csharp >}}
string sourceFile = "deformacion_bandera.psd";
string outputFile = "exportar_bandera.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Agregar nuevos tipos de deformación: arco hacia arriba, arco hacia abajo, esfera**

{{< highlight csharp >}}
string sourceFileArcUpper = "arco_superior_deformacion.psd";
string sourceFileArcLower = "arco_inferior_deformacion.psd";
string sourceFileBulge =  "deformacion_bulbo.psd";

string outputFileArcUpper ="Exportar_arco_superior.png";
string outputFileArcLower = "Exportar_arco_inferior.png";
string outputFileBulge = "Exportar_bulbo.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Implementar nuevo método PsdImage.AddPosterizeAdjustmentLayer para agregar nueva capa de posterización**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Comprobar cambios guardados
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Los objetos no son iguales.");
    }
}
{{< /highlight >}}

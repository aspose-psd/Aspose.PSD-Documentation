---
title: Notas de la versión de Aspose.PSD para .NET 24.3
type: docs
weight: 100
url: /es/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                          | **Categoría** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [Formato AI] Reducir el tiempo de carga de imágenes AI multipágina grandes         |     Mejora     |
| PSDNET-1905 | El archivo PSD después de la conversión de 8 bits a 16 bits se volvió ilegible |     Error     |
| PSDNET-1906 | El archivo PSD después de la conversión de 8 bits a 32 bits se volvió ilegible |     Error     |
| PSDNET-1921 | [Formato AI] Corregir la representación de curva corta en archivo AI       |     Error     |

## **Cambios en la API Pública**
# **APIs Añadidas:**
- Ninguna

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-1905. El archivo PSD después de la conversión de 8 bits a 16 bits se volvió ilegible**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // está bien
    }
    else
    {
        throw new Exception("Recurso global incorrecto, el primer recurso debería ser Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. El archivo PSD después de la conversión de 8 bits a 32 bits se volvió ilegible**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // está bien
    }
    else
    {
        throw new Exception("Recurso global incorrecto, el primer recurso debería ser Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [Formato AI] Corregir la representación de la curva corta en el archivo AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

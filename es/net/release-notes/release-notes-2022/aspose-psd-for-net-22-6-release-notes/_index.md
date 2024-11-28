---
title: Notas de la versión de Aspose.PSD para .NET 22.6
type: docs
weight: 70
url: /es/net/aspose-psd-para-net-22-6-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-940|Crear API para obtener el hash único de capas similares en diferentes archivos|Mejora|
|PSDNET-678|Renderizado incorrecto de FillLayer con patrón en el caso de que haya más de un patrón y se cambie el orden de las capas|Error|
|PSDNET-1125|Excepción al cargar un archivo PSD específico con modo de color CMYK|Error|


## **Cambios en la API Pública:**
# **APIs Agregadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **APIs Eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDNET-678. Renderizado incorrecto de FillLayer con patrón en el caso de que haya más de un patrón y se cambie el orden de las capas**

{{< highlight csharp >}}
string archivoFuente = "badPattern.psd";
string salidaPng = "out_678.png";

using (var imagenPsd = (PsdImage)Image.Load(archivoFuente))
{
    FillLayer capa1 = (FillLayer)imagenPsd.Layers[1];
    FillLayer capa2 = (FillLayer)imagenPsd.Layers[2];

    capa1.Update();
    capa2.Update();

    imagenPsd.Save(salidaPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Crear API para obtener el hash único de capas similares en diferentes archivos**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    //... Código omitido para resumir ...
}
{{< /highlight >}}

**PSDNET-1125. Excepción al cargar un archivo PSD específico con modo de color CMYK**

{{< highlight csharp >}}
string archivoFuente = "02_alpha-channels.psd";
string salidaPng = "out_1125.png";

using (PsdImage imagen = (PsdImage)Image.Load(archivoFuente))
{
    imagen.Save(salidaPng, new PngOptions());
}
{{< /highlight >}}
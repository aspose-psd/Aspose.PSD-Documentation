---
title: Aspose.PSD para .NET 21.6 - Notas de Lanzamiento
type: docs
weight: 70
url: /es/net/aspose-psd-para-net-21-6-notas-de-lanzamiento/
---

{{% alert color="primary" %}} 

Esta página contiene notas de lanzamiento para [Aspose.PSD para .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-546|La máscara de recorte para un grupo no se renderiza correctamente|Error|
|PSDNET-547|La máscara regular o vectorial para un grupo de capas se ignora al renderizar|Error|
|PSDNET-647|La imagen PSD con máscaras de capa vectoriales deshabilitadas al guardar habilita las máscaras vectoriales|Error|
|PSDNET-786|Excepción al crear una TextLayer con texto de más de 255 caracteres|Error|
|PSDNET-900|El texto de la capa de texto no se puede renderizar en Linux|Mejora|

## **Cambios en la API pública**
# **APIs agregadas:**
- Ninguna

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-546. La máscara de recorte para un grupo no se renderiza correctamente**

{{< highlight csharp >}}
            string nombreArchivoFuente = "AppleClip.psd";
            string nombreArchivoSalida = "resultado.png";

            using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))
            {
                imagen.Save(nombreArchivoSalida, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. La máscara regular o vectorial para un grupo de capas se ignora al renderizar**

{{< highlight csharp >}}
        string nombreArchivoFuente = "Stripes3Mask.psd";
        string nombreArchivoSalida = "SalidaStripes3Mask.png";
        using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))
        {
            imagen.Save(nombreArchivoSalida, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. La imagen PSD con máscaras de capa vectoriales deshabilitadas al guardar habilita las máscaras vectoriales**

{{< highlight csharp >}}
            string nombreArchivoFuente = "FourWithMasksVd.psd";
            string nombreArchivoSalida = "FourWithMasksVdOutput.psd";

            using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))
            {
                imagen.Save(nombreArchivoSalida);
            }
{{< /highlight >}}

**PSDNET-786. Excepción al crear una TextLayer con texto de más de 255 caracteres**

{{< highlight csharp >}}
            string salida = "salida.psd";

            using (var imagen = new PsdImage(100, 100))
            {
                string texto = new string('a', 256);
                imagen.AddTextLayer(texto, Rectangle.Empty);

                imagen.Save(salida);
            }
{{< /highlight >}}

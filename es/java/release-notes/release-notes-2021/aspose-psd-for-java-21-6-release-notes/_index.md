---
title: Notas de la versión Aspose.PSD para Java 21.6
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-21-6-notas-de-la-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión de [Aspose.PSD para Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-351|La máscara de recorte para un grupo no se renderiza correctamente|Error|
|PSDJAVA-352|La máscara regular o vectorial para un grupo de capas se ignora al renderizar|Error|
|PSDJAVA-353|La imagen PSD con máscaras de capa vectoriales deshabilitadas al guardar activa las máscaras vectoriales|Error|
|PSDJAVA-354|Excepción al crear una capa de texto con un texto de más de 255 caracteres|Error|

# **Cambios en la API Pública**
# **APIs Agregadas:**
- Ninguna

# **APIs Eliminadas:**
- Ninguna

# **Ejemplos de uso:**

**PSDJAVA-351. La máscara de recorte para un grupo no se renderiza correctamente**

{{< highlight java >}}
        String nombreArchivoFuente = "AppleClip.psd";
        String nombreArchivoSalida = "resultado.png";

        PsdImage imagen = (PsdImage) Image.load(nombreArchivoFuente);
        try
        {
            imagen.save(nombreArchivoSalida, new PngOptions());
        }finally {
            imagen.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. La máscara regular o vectorial para un grupo de capas se ignora al renderizar**

{{< highlight java >}}
        String nombreArchivoFuente = "Stripes3Mask.psd";
        String nombreArchivoSalida = "SalidaStripes3Mask.png";

        PsdImage imagen = (PsdImage)Image.load(nombreArchivoFuente);
        try
        {
            imagen.save(nombreArchivoSalida, new PngOptions());
        }finally {
            imagen.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. La imagen PSD con máscaras de capa vectoriales deshabilitadas al guardar activa las máscaras vectoriales**

{{< highlight java >}}
        String nombreArchivoFuente = "FourWithMasksVd.psd";
        String nombreArchivoSalida = "FourWithMasksVdOutput.psd";

        PsdImage imagen = (PsdImage) Image.load(nombreArchivoFuente);
        try
        {
            imagen.save(nombreArchivoSalida);
        }finally {
            imagen.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Excepción al crear una capa de texto con un texto de más de 255 caracteres**

{{< highlight java >}}
        String salida = "salida.psd";

        PsdImage imagen = new PsdImage(100, 100);
        try
        {
            char[] caracteres = new char[256];
            Arrays.fill(caracteres, '*');
            String texto = new String(caracteres);
            imagen.addTextLayer(texto, Rectangle.getEmpty());

            imagen.save(salida);
        }finally {
            imagen.dispose();
        }
{{< /highlight >}}

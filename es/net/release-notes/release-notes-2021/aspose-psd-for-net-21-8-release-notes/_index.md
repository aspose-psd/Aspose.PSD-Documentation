---
title: Notas de la versión de Aspose.PSD para .NET 21.8
type: docs
weight: 50
url: /es/net/aspose-psd-para-net-21-8-notas-de-version/
---

{{% alert color="primary" %}} 

Esta página contiene notas de la versión de [Aspose.PSD para .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-698|Soporte de métodos de compresión ZipWithPrediction|Característica|
|PSDNET-663|El espaciado del texto es incorrecto en PSD generado|Error|
|PSDNET-685|Excepción al guardar PSD|Error|
|PSDNET-927|Distancia incorrecta entre líneas y símbolos en Aspose.PSD cuando se usa sin licencia|Error|

## **Cambios en la API pública**
# **APIs Agregadas:**
- Ninguna

# **APIs Eliminadas:**
- Ninguna

## **Ejemplos de uso:**

**PSDNET-663. El espaciado del texto es incorrecto en PSD generado**

{{< highlight csharp >}}
            string nombreArchivoFuente = "fuente.psd";
            string nombreArchivoSalida = "salida.png";

            using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))
            {
                imagen.Save(nombreArchivoSalida, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Excepción al guardar PSD**

{{< highlight csharp >}}
            string nombreArchivoFuente = "Archivo.psd";
            string nombreArchivoSalida = "Archivo2.psd";

            using (PsdImage imagen = (PsdImage)Image.Load(nombreArchivoFuente))
            {
                var capa1 = (TextLayer)imagen.Layers[1];
                capa1.TextData.UpdateLayerData();

                imagen.Save(nombreArchivoSalida);
            }
{{< /highlight >}}

**PSDNET-698. Soporte de métodos de compresión ZipWithPrediction**

{{< highlight csharp >}}
            string rutaArchivoEntrada = "zipTest698.psd";

            string archivoSalidaPng = "salida.png";
            string archivoSalidaRaw = "salida_Raw.psd";
            string archivoSalidaZip = "salida_Zip.psd";

            using (Image imagen = Image.Load(rutaArchivoEntrada))
            {
                imagen.Save(archivoSalidaPng, new PngOptions());

                imagen.Save(archivoSalidaRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                imagen.Save(archivoSalidaZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Distancia incorrecta entre líneas y símbolos en Aspose.PSD cuando se usa sin licencia**

{{< highlight csharp >}}
            bool[] estadosLicencia = new bool[] { false, true };
            for (int i = 0; i < estadosLicencia.Length; i++)
            {
                bool pruebadeLicencia = estadosLicencia[i];
                if (pruebadeLicencia)
                {
                    License licencia = new License();
                    licencia.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string archivoFuente = "psdnetTest927.psd";
                string archivoSalida = "out_" + pruebadeLicencia.ToString() + "_psdnetTest927.png";

                using (var imagen = (PsdImage)Image.Load(archivoFuente))
                {
                    imagen.Save(archivoSalida, new PngOptions());
                }
            }
{{< /highlight >}}

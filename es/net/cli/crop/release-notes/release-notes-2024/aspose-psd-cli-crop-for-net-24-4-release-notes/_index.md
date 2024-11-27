---
title: Aspose.PSD CLI Recorte para .NET 24.4 - Notas de Lanzamiento
type: docs
weight: 90
url: /es/net/cli/recorte/aspose-psd-cli-recorte-para-net-24-4-notas-de-lanzamiento/
---

{{% alert color="primary" %}}

Esta página contiene notas de lanzamiento para [Aspose.PSD CLI Recorte para .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Clave**   | **Resumen**                                            | **Categoría** |
|:------------|:-------------------------------------------------------|:-------------|
| PSDNET-2025 | Lanzamiento inicial de la Aplicación de Recorte CLI de Aspose.PSD  | Mejora  |


## **Ejemplos de Uso:**

**PSDNET-2023. Lanzamiento inicial de la Aplicación de Recorte CLI de Aspose.PSD**

**Uso desde la línea de comandos:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input foto1.jpg --output foto_recortada.png --format png --izquierda 10 --arriba 35 --ancho 250 --alto 300 --tipoRecorte rect --licencia Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso desde el código de comando:**

{{< highlight csharp >}}
var opciones = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    RutaDeEntrada = "foto1.jpg",
    TipoRecorte = CropType.Rect,
    Izquierda = 10,
    Arriba = 35,
    Ancho = 250,
    Alto = 300,
    RutaDeSalida = "foto_recortada.png",
    FormatoSalida = "png"
};


if (estaLicenciado)
{
    opciones.RutaDeLicencia = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Aplicar(opciones);
{{< /highlight >}}

---
title: Notas de la versión de Aspose.PSD CLI Crop para .NET 24.6
type: docs
weight: 90
url: /es/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD CLI Crop para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                  | **Categoría** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Versión Inicial de las Aplicaciones Aspose.PSD CLI: Aspose.PSD.CLI.Export y Aspose.PSD.CLI.NLP.Editor | Mejora |


## **Ejemplos de uso:**

**PSDNET-2110. Versión inicial de la aplicación Aspose.PSD CLI Crop**

**Uso desde la línea de comandos:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input foto1.jpg --output foto_recortada.png --format png --izquierda 10 --arriba 35 --ancho 250 --alto 300 --tipoRecorte rectángulo --licencia Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso desde el código de comando:**

{{< highlight csharp >}}
var opciones = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    RutaEntrada = "foto1.jpg",
    TipoRecorte = CropType.Rect,
    Izquierda = 10,
    Arriba = 35,
    Ancho = 250,
    Alto = 300,
    RutaSalida = "foto_recortada.png",
    FormatoSalida = "png"
};


si (tieneLicencia)
{
    opciones.RutaLicencia = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Aplicar(opciones);
{{< /highlight >}}

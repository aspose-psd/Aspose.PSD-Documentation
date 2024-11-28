---
title: Aspose.PSD CLI Convert para .NET 24.4 - Notas de la versión
type: docs
weight: 90
url: /es/net/cli/conversion/aspose-psd-conversion-cli-app-para-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión para [Aspose.PSD CLI Convert para .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Clave**   | **Resumen**                                               | **Categoría** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Lanzamiento inicial de la aplicación de conversión Aspose.PSD CLI | Mejora |


## **Ejemplos de uso:**

**PSDNET-2023. Lanzamiento inicial de la aplicación de conversión Aspose.PSD CLI**

**Uso desde la línea de comandos:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso desde el código de comando:**

{{< highlight csharp >}}
var opciones = new Aspose.PSD.CLI.Convert.CommandLineOptions.ConversionOptions
{
    InputFiles = new List<string> { "photo_1.jpg", "photo_2.jpg", "photo_3.jpg", "photo_4.jpg", "photo_5.jpg", "photo_6.jpg" },
    OutputPath = "result.zip",
    OutputFormat = "png"
};


if (estaLicenciado)
{
    opciones.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Apply(opciones);
{{< /highlight >}}

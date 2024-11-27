---
title: Notas de versión de Aspose.PSD CLI Convert para .NET 24.6
type: docs
weight: 90
url: /es/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de versión para [Aspose.PSD CLI Convert para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                  | **Categoría** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lanzamiento inicial de las aplicaciones Aspose.PSD CLI: Aspose.PSD.CLI.Export y Aspose.PSD.CLI.NLP.Editor |  Mejora       |


## **Ejemplos de uso:**

**PSDNET-2110. Lanzamiento inicial de las aplicaciones Aspose.PSD CLI: Aspose.PSD.CLI.Export y Aspose.PSD.CLI.NLP.Editor**

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


if (isLicensed)
{
    opciones.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Apply(opciones);
{{< /highlight >}}

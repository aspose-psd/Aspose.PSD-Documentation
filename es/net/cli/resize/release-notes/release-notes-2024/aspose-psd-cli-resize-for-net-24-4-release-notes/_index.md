---
title: Notas de la versión de Aspose.PSD CLI Resize para .NET 24.4
type: docs
weight: 90
url: /es/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD CLI Resize para .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Clave**     | **Resumen**                                          | **Categoría** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Lanzamiento inicial de la Aplicación de Redimensionamiento Aspose.PSD CLI|  Mejora |


## **Ejemplos de uso:**

**PSDNET-2026. Lanzamiento inicial de la Aplicación de Redimensionamiento Aspose.PSD CLI**

**Uso desde la línea de comandos:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso desde el código:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Scale = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(options);

{{< /highlight >}}

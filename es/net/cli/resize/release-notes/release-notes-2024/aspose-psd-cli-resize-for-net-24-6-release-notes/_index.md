---
title: Notas de la versión de Aspose.PSD CLI Resize para .NET 24.6
type: docs
weight: 90
url: /es/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD CLI Resize para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}


| **Clave**    | **Resumen**                                                                                 | **Categoría** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lanzamiento inicial de las aplicaciones Aspose.PSD CLI: Aspose.PSD.CLI.Export y Aspose.PSD.CLI.NLP.Editor |  Mejora |


## **Ejemplos de uso:**

**PSDNET-2110. Lanzamiento inicial de la Aplicación Aspose.PSD CLI Resize**

**Uso desde la línea de comandos:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso desde el código:**

{{< highlight csharp >}}

var opciones = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Escalar = 200,
    FormatoSalida = "png"
};


if (estaLicenciado)
{
    opciones.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(opciones);

{{< /highlight >}}

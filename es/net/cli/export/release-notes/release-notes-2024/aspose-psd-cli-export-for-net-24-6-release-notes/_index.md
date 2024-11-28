---
title: Notas de la versión Aspose.PSD CLI Export para .NET 24.6
type: docs
weight: 90
url: /es/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión para [Aspose.PSD CLI Export para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Clave**   | **Resumen**                                                                                  | **Categoría** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lanzamiento inicial de las aplicaciones Aspose.PSD CLI: Aspose.PSD.CLI.Export y Aspose.PSD.CLI.NLP.Editor |  Mejora |


## **Ejemplos de uso:**

**PSDNET-2110. Lanzamiento inicial de la aplicación Aspose.PSD CLI Export**

**Uso desde la línea de comandos:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso desde el código:**

{{< highlight csharp >}}

var opciones = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    RutaDeImagenDeEntrada = "photo1.jpg",
    RutaDeImagenDeSalida = "exported.png",
    FormatoDeSalida = "png",
    NombreDeCapa = "Layer1"
};


if (tieneLicencia)
{
    opciones.RutaDeLicencia = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Aplicar(opciones);

{{< /highlight >}}

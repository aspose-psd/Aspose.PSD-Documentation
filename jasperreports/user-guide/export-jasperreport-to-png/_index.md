---
title: Export JasperReport to PNG
type: docs
weight: 90
url: /jasperreports/export-jasperreport-to-png
---

{{% alert color="primary" %}}

Aspose.PSD for JasperReports provides a class named ASPngExporter for exporting JasperReport to PNG.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to PNG.

**Java**

{{< highlight java >}}

ASPngExporter pngExporter = new ASPngExporter();
ASPngExportConfigurationImpl pngExportConfiguration = new ASPngExportConfigurationImpl();
pngExportConfiguration.setColorType(PngColorType.Grayscale);
pngExportConfiguration.setBitDepth((byte) 8);
pngExporter.setConfiguration(pngExportConfiguration);

ASExportInputImpl exporterInput = new ASExportInputImpl(jasperPrint);
pngExporter.setExporterInput(exporterInput);

ASExporterOutputImpl exporterOutput = new ASExporterOutputImpl(destFile);
pngExporter.setExporterOutput(exporterOutput);

pngExporter.exportReport();

{{< /highlight >}}

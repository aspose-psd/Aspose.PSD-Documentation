---
title: Export JasperReport to GIF
type: docs
weight: 90
url: /jasperreports/export-jasperreport-to-gif
---

{{% alert color="primary" %}}

Aspose.PSD for JasperReports provides a class named ASGifExporter for exporting JasperReport to GIF.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to GIF.

**Java**

{{< highlight java >}}

ASGifExporter gifExporter = new ASGifExporter();
ASGifExportConfigurationImpl gifExportConfiguration = new ASGifExportConfigurationImpl();
gifExportConfiguration.setDoPaletteCorrection(true);
gifExportConfiguration.setInterlaced(true);
gifExporter.setConfiguration(gifExportConfiguration);

ASExportInputImpl exporterInput = new ASExportInputImpl(jasperPrint);
gifExporter.setExporterInput(exporterInput);

ASExporterOutputImpl exporterOutput = new ASExporterOutputImpl(destFile);
gifExporter.setExporterOutput(exporterOutput);

gifExporter.exportReport();

{{< /highlight >}}

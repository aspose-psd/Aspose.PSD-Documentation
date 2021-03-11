---
title: Export JasperReport to JPEG2000
type: docs
weight: 80
url: /jasperreports/export-jasperreport-to-jpeg2000
---

{{% alert color="primary" %}}

Aspose.PSD for JasperReports provides a class named ASJpeg2000Exporter for exporting JasperReport to JPEG2000.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to JPEG2000.

**Java**

{{< highlight java >}}

ASJpeg2000Exporter jpeg2000Exporter = new ASJpeg2000Exporter();
ASJpeg2000ExportConfigurationImpl jpeg2000ExportConfiguration = new ASJpeg2000ExportConfigurationImpl();
jpeg2000ExportConfiguration.setIrreversible(true);
jpeg2000ExportConfiguration.setCodec(Jpeg2000CodecEnum.J2K);
jpeg2000Exporter.setConfiguration(jpeg2000ExportConfiguration);

exporterInput = new ASExportInputImpl(jasperPrint);
jpeg2000Exporter.setExporterInput(exporterInput);

exporterOutput = new ASExporterOutputImpl("shapesExample.jp2");
jpeg2000Exporter.setExporterOutput(exporterOutput);

jpeg2000Exporter.exportReport();

{{< /highlight >}}

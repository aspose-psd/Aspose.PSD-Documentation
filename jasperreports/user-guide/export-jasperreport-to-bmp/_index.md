---
title: Export JasperReport to BMP
type: docs
weight: 90
url: /jasperreports/export-jasperreport-to-bmp
---

{{% alert color="primary" %}}

Aspose.PSD for JasperReports provides a class named ASBmpExporter for exporting JasperReport to BMP.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to BMP.

**Java**

{{< highlight java >}}

ASBmpExporter bmpExporter = new ASBmpExporter();
ASBmpExportConfigurationImpl bmpExportConfiguration = new ASBmpExportConfigurationImpl();
bmpExportConfiguration.setCompression(BitmapCompression.Rgb);
bmpExportConfiguration.setBitsPerPixel(16);
bmpExportConfiguration.setTextRenderingHintEnum(TextRenderingHintEnum.AntiAlias);
bmpExporter.setConfiguration(bmpExportConfiguration);

exporterInput = new ASExportInputImpl(jasperPrint);
bmpExporter.setExporterInput(exporterInput);

exporterOutput = new ASExporterOutputImpl("shapesExample.bmp");
bmpExporter.setExporterOutput(exporterOutput);

bmpExporter.exportReport();

{{< /highlight >}}

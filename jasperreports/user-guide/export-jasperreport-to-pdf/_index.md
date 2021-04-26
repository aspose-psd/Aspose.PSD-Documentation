---
title: Export JasperReport to PDF
type: docs
weight: 90
url: /jasperreports/export-jasperreport-to-pdf
---

{{% alert color="primary" %}}

Aspose.PSD for JasperReports provides a class named ASPdfExporter for exporting JasperReport to PDF.

{{% /alert %}}

The following code snippet demonstrates how to export the JasperReport to PDF.

**Java**

{{< highlight java >}}

ASPdfExporter pdfExporter = new ASPdfExporter();
ASPdfExportConfigurationImpl pdfExportConfiguration = new ASPdfExportConfigurationImpl();
pdfExportConfiguration.setAuthor("John Smith");
pdfExportConfiguration.setSubject("pdf export example");
pdfExportConfiguration.setTitle("Report");
pdfExportConfiguration.setImageCompression(ImageCompressionEnum.Ccitt4);
pdfExportConfiguration.setJpegQuality(90);
pdfExportConfiguration.setPdfCompliance(PdfComplianceEnum.Pdf15);
pdfExportConfiguration.setTextCompression(TextCompressionEnum.Flate);
pdfExporter.setConfiguration(pdfExportConfiguration);

ASExportInputImpl exporterInput = new ASExportInputImpl(jasperPrint);
pdfExporter.setExporterInput(exporterInput);

ASExporterOutputImpl exporterOutput = new ASExporterOutputImpl(destFile);
pdfExporter.setExporterOutput(exporterOutput);

pdfExporter.exportReport();

{{< /highlight >}}

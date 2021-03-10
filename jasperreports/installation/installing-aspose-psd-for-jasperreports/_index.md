---
title: Installing Aspose.PSD for JasperReports
type: docs
weight: 20
url: /jasperreports/installing-aspose-psd-for-jasperreports/
---

To use **Aspose.PSD for JasperReports** from your application, copy **aspose-psd-jasperreports-xx.x.jar** from the \lib folder of **aspose-psd-jasperreports-xx.x.zip** to the JasperReports\lib directory or to a library folder of your application. After that, you can access the exporters programmatically.

The following example shows the typical code needed to export a report to an TIFF file using Aspose.PSD for JasperReports. More examples can be found in the demo reports included in the product archive.

**Java**

{{< highlight java >}}
    ASTiffExporter tiffExporter = new ASTiffExporter();
    ASTiffExportConfigurationImpl tiffExportConfiguration = new ASTiffExportConfigurationImpl(TiffExpectedFormatEnum.TiffDeflateRgb);
    tiffExportConfiguration.setArtist("John Smith");
    tiffExportConfiguration.setDateTime("12.08.2020");
    tiffExportConfiguration.setCompression(TiffCompressionsEnum.AdobeDeflate);
    tiffExporter.setConfiguration(tiffExportConfiguration);

    exporterInput = new ASExportInputImpl(jasperPrint);
    tiffExporter.setExporterInput(exporterInput);

    exporterOutput = new ASExporterOutputImpl("shapesExample.tiff");
    tiffExporter.setExporterOutput(exporterOutput);

    tiffExporter.exportReport();
{{< /highlight >}}

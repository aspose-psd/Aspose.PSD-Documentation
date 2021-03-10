---
title: Aspose.PSD for JasperReports 21.3 Release Notes
type: docs
weight: 10
url: /jasperreports/aspose-psd-for-jasperreports-21-3-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for Aspose.PSD for JasperReports 21.3.

{{% /alert %}}

{{% alert color="primary" %}}
Please welcome our brand-new product, Aspose.PSD for JasperReports 21.3! Aspose.PSD for JasperReports is the unique solution on the market that makes possible exporting reports from JasperReports to various image file formats.

The export formats currently include: BMP, GIF JPEG, JPEG2000, PNG, PSD, TIFF, PDF.
{{% /alert %}}

## Features

The first release of the product supports the following features:

- Easy and Lightweight Deployment - Aspose.PSD for JasperReports is written purely in Java and is provided as a single JAR file that can easily be deployed on the machines running JasperReports.
- High Fidelity to Report Design - Aspose.PSD for JasperReports exports reports in such a way that they look identical to reports exported by the built-in exporters of JasperReports.
- Multipage export -  Aspose.PSD for JasperReports supports multipage export to the following formats:  Gif,  Tiff, Pdf.
- Batch export - Aspose.PSD for JasperReports supports export reports from JasperReports in batch mode. Each page of the report will be saved as a separate file.

## Usage Examples

{{< highlight java >}}

//      Prepare JasperPrint for export.

        JasperReport jasperReport = JasperCompileManager.compileReport("shapesReport.jrxml");
        JasperPrint jasperPrint = JasperFillManager.fillReport(jasperReport, null, new JREmptyDataSource());

//      Use of ASJpeg2000Exporter to export JasperReport to JPEG2000 file format

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

//      Use of ASPsdExporter to export JasperReport to PSD file format

        ASPsdExporter psdExporter = new ASPsdExporter();
        ASPsdExportConfigurationImpl psdExportConfiguration = new ASPsdExportConfigurationImpl();
        psdExportConfiguration.setColorMode(ColorModesEnum.Rgb);
        psdExportConfiguration.setPsdVersion(PsdVersionEnum.Psd);
        psdExportConfiguration.setCompressionMethod(CompressionMethodEnum.Raw);
        psdExporter.setConfiguration(psdExportConfiguration);

        exporterInput = new ASExportInputImpl(jasperPrint);
        psdExporter.setExporterInput(exporterInput);

        exporterOutput = new ASExporterOutputImpl("shapesExample.psd");
        psdExporter.setExporterOutput(exporterOutput);

        psdExporter.exportReport();

//      Use of ASTiffExporter to export JasperReport to TIFF file format

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

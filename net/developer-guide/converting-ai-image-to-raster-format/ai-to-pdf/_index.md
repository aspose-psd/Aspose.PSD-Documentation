---
title: Ai to PDF
type: docs
weight: 20
url: /net/ai-to-pdf/
---

Aspose.PSD provides functionality to convert AI files to PDF files. For Ai export you need to use the following code snippet:

Below provided sample code demonstrates how to export the AI file to PDF with the [File Format Manipulation API](/psd/net/manipulate-different-image-file-formats/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-AI-AIToPDF-AIToPDF.cs" >}}

You can specify additional PDF parameters in [PdfOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pdfoptions), like Author, Keywords, Subject, Title.

Mass server processing of AI files to PDF can be useful for business automation. PDF format can not be edited as a PSD file. PDF Format can not be changed, so you can use it as an unchangeable format to work with your customers or partners.

## Additional Example

Here is another example demonstrating how to export an AI file to PDF with specific PDF compliance settings:

```csharp
string sourceFile = "patternstokOnePage.ai";
string outputFile = "output_raw.pdf";

var pdfOptions = new PdfOptions();
pdfOptions.PdfCoreOptions = new PdfCoreOptions();
pdfOptions.PdfCoreOptions.PdfCompliance = PdfComplianceVersion.PdfA1a;

using (var aiImage = (AiImage)Image.Load(sourceFile))
{
    aiImage.Save(outputFile, pdfOptions);
}
```

The PdfComplianceVersion.PdfA1a option ensures that the generated PDF meets the PDF/A-1a standard, which is a part of the PDF/A family of ISO-standardized PDF specifications. PDF/A-1a is designed for long-term archiving of electronic documents and ensures that the PDF is self-contained, including all information necessary for displaying the document in the same manner regardless of the tools used.
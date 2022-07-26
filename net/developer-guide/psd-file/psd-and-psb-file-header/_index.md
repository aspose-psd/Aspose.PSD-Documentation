---
title: PSD and PSB File Header
type: docs
weight: 40
url: /net/psd-and-psb-file-header/
---

## **Description**
Adobe Photoshop File header contains information about the version of File (1 for PSD and 2 for PSB), Count of Channels, Color Mode and Bit Depth.

You can learn supported by Aspose.PSD Combinations of Color Mode and Bit Depth from the related article.


The file header contains the basic properties of the image.

|**Length**|**Description**|
| :- | :- |
|4|Signature: always equal to *"8BPS"*|
|2|[PSD Version](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): always equal to 1 for PSD Files and 2 for PSB Files. Aspose.PSD can detect a version of File Format and read it correctly.|
|6|Reserved: must be zero.|
|2|The number of channels in the image, including any alpha channels. The supported range is 1 to 56.|
|4|The height of the image in pixels. The supported range is 1 to 30,000. PSB File supports height up to 300,000 pixels. PSB Files are supported by Aspose.PSD too|
|4|The width of the image in pixels. The supported range is 1 to 30,000. PSB File supports width up to 300,000 pixels. Batch processing of big PSD/PSB files also supported by Aspose.PSD|
|2|Depth: the number of bits per channel. Supported values are 1, 8, 16 and 32. But not every Color Mode works with every depth.|
|2|The [PSD color mode](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes) of the file. Supported values are: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multichannel = 7; Duotone = 8; Lab = 9.|
You can check our [PSD API Reference](https://reference.aspose.com/psd) for it.

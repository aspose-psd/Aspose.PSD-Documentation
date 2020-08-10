---
title: PSD Format overview
type: docs
weight: 60
url: /net/psd-format-overview/
---

### **Description**
PSD, Photoshop Document, represents Adobe Photoshop's native file format used for graphics designing and development.
### **File Format Specifications**
Data in a PSD file is stored in big-endian byte order. This implies swapping the short and long integers when reading or writing on the Windows platform. The Photoshop file format is divided into five major parts. It has many length markers that can be used to move from one section to the next. The length markers are usually padded with bytes to round to the nearest 2 or 4-byte interval. The five major parts are:

- File Header
- Color Mode Data
- Image Resources
- Layer and Mask Information
- Image Data

For conformance, data should be written to all these fields in the section, as Photoshop may try to read the entire section. It also implies that zeroes be written to skipped fields while writing to a file. The length field in the length-delimited sections should be used to decide when to stop reading. In most cases, the length field indicates the number of bytes, not records, following. The following points need to be remembered while reading a file.

- The values in the "Length" column in all tables are in bytes.
- All values defined as Unicode string consist of:
- A 4-byte length field, representing the number of characters in the string (not bytes).
- The string of Unicode values, two bytes per character.
### **Features of format**
PSD files may include image layers, adjustment layers, layer masks, annotations, file information, keywords, and other Photoshop-specific elements. Photoshop files have default extension as.PSD and have a maximum height and width of 30,000 pixels, and a length limit of two gigabytes
### **How it can be used**
1. An instrument for PSD Slicing.
1. [Converting PSD](/psd/net/converting-psd-image-to-raster-format/) to HTML
1. Using [PSD as a Template](/psd/net/using-psd-files-as-templates-for-automation-business-cards-case/) for Email
1. PSD to specific CMS HTML
1. Identikit in PSD File (Police Sketch)
1. Create pseudo-3D preview images using Smart Objects for such goods as bottles, cups, t-shirts, etc.
1. Quick edit of PSD: Auto-tone, Presets, Smart Object, Text Layer Image Cutout

And much more. If you made something great with Aspose.PSD, please share with us your case study using [Aspose Forums](https://forum.aspose.com/).



Additional examples you can learn from:

- [Case Studies](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Showcases](/psd/net/showcases-html/)

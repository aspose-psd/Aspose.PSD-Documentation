---
title: List of the Supported PSD Global Image Resources
type: docs
weight: 30
url: /net/list-of-the-supported-psd-global-image-resources/
---

## **Aspose.PSD supports the Low-Level editing of Image Resources.**
List of fully supported Image Resources, you can find in Aspose.PSD .Net [API Reference](https://reference.aspose.com/psd/net)

According to Adobe® Photoshop® format specification: Image resources use several standard ID numbers, as shown in the Image resource IDs. Not all file formats use all ID's. Some information may be stored in other sections of the file.

For those resource IDs that have been added since Photoshop 3.0. the entry indicates the version in which they were introduced, e.g. (*Photoshop 6.0).*

Image resource ID.

|**ID**|**Description**|
| :- | :- |
|**Decimal**||
|1000|*(Obsolete--Photoshop 2.0 only*) Number of channels, rows, columns, depth, and mode|
|1001|Macintosh print manager print info record|
|1002|Macintosh page format information. No longer read by Photoshop. *(Obsolete)*|
|1003|*(Obsolete--Photoshop 2.0 only*) Indexed color table|
|1005|[ResolutionInfo structure](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource).|
|1006|Names of the alpha channels as a series of Pascal strings.|
|1007|*(Obsolete) See ID 1077 DisplayInfo* structure.|
|1008|The caption as a Pascal string.|
|1009|[Border information.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource) Contains a fixed number (2 bytes real, 2 bytes fraction) for the border width, and 2 bytes for border units (1 = inches, 2 = cm, 3 = points, 4 = picas, 5 = columns).|
|1010|[Background color. ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|Print flags. A series of one-byte boolean values: labels, crop marks, color bars, registration marks, negative, flip, interpolate, caption, print flags.|
|1012|Grayscale and multichannel halftoning information|
|1013|[Color halftoning information](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|Duotone halftoning information|
|1015|Grayscale and multichannel transfer function|
|1016|[Color transfer functions](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188)|
|1017|Duotone transfer functions|
|1018|Duotone image information|
|1019|Two bytes for the effective black and white values for the dot range|
|1020|*(Obsolete)*|
|1021|EPS options|
|1022|[Quick Mask information](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource). Quick Mask channel ID; 1- byte boolean indicating whether the mask was initially empty.|
|1023|*(Obsolete)*|
|1024|[Layer state information](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource).|
|1025|Working path (not saved). Path resource format.|
|1026|[Layers group information](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource). 2 bytes per layer containing a group ID for the dragging groups. Layers in a group have the same group ID.|
|1027|*(Obsolete)*|
|1028|IPTC-NAA record. Contains the *File Info...* information.|
|1029|Image mode for raw format files|
|1030|JPEG quality. Private.|
|1032|*(Photoshop 4.0) [Grid and guides information.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)*|
|1033|*(Photoshop 4.0) [](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[Thumbnail resource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[for Photoshop 4.0](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* only|
|1034|*(Photoshop 4.0)* Copyright flag. Boolean indicating whether image is copyrighted.|
|1035|*(Photoshop 4.0)* URL. Handle of a text string with uniform resource locator*.*|
|1036|*(Photoshop 5.0)[Thumbnail resource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)* (supersedes resource 1033).|
|1037|*(Photoshop 5.0) [Global Angle](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*. 4 bytes that contain an integer between 0 and 359, which is the global lighting angle for effects layer. If not present, assumed to be 30.|
|1038|*(Obsolete) See ID 1073 below. (Photoshop 5.0)* Color samplers resource.|
|1039|*(Photoshop 5.0) [ICC Profile](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*. The raw bytes of an ICC (International Color Consortium) format profile.*  |
|1040|*(Photoshop 5.0) [Watermark](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*.|
|1041|*(Photoshop 5.0) [ICC Untagged Profile](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*. 1 byte that disables any assumed profile handling when opening the file. 1 = intentionally untagged.|
|1042|*(Photoshop 5.0)* Effects visible. 1-byte global flag to show/hide all the effects layer. Only present when they are hidden.|
|1043|*(Photoshop 5.0)* Spot Halftone. 4 bytes for version, 4 bytes for length, and the variable length data.|
|1044|*(Photoshop 5.0)[Document-specific IDs](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)* seed number. 4 bytes: Base value, starting at which layer IDs will be generated (or a greater value if existing IDs already exceed it). Its purpose is to avoid the case where we add layers, flatten, save, open, and then add more layers that end up with the same IDs as the first set.|
|1045|*(Photoshop 5.0) [Unicode Alpha Names](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*.|
|1046|*(Photoshop 6.0)* Indexed Color Table Count. 2 bytes for the number of colors in table that are actually defined|
|1047|*(Photoshop 6.0)* [Transparency Index](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource).|
|1049|*(Photoshop 6.0)* [Global Altitude.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* Slices.|
|1051|*(Photoshop 6.0)* Workflow URL.|
|1052|*(Photoshop 6.0)* Jump To XPEP. 2 bytes major version, 2 bytes minor version, 4 bytes count. Following is repeated for count: 4 bytes block size, 4 bytes key, if key = *'jtDd'* , then next is a Boolean for the dirty flag; otherwise it's a 4 byte entry for the mod date.|
|1053|*(Photoshop 6.0)* Alpha Identifiers.|
|1054|*(Photoshop 6.0)[URL List](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*.|
|1057|*(Photoshop 6.0)* [Version Info](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource).|
|1058|*(Photoshop 7.0)* EXIF data 1.|
|1059|*(Photoshop 7.0)* EXIF data 3*.*|
|1060|*(Photoshop 7.0)* [XMP metadata](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource). File info as XML description.|
|1061|*(Photoshop 7.0)[Caption digest](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)*. 16 bytes: RSA Data Security, MD5 message-digest algorithm|
|1062|*(Photoshop 7.0)[Print scale](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)*. (0 = centered, 1 = size to fit, 2 = user defined). 4 bytes x location (floating point). 4 bytes y location (floating point). 4 bytes scale (floating point)|
|1064|*(Photoshop CS)* [Pixel Aspect Ratio](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource).|
|1065|*(Photoshop CS)* Layer Comps.|
|1066|*(Photoshop CS)* Alternate Duotone Colors. This resource is not read or used by Photoshop.|
|1067|*(Photoshop CS)*Alternate Spot Colors. This resource is not read or used by Photoshop.|
|1069|*(Photoshop CS2)* [Layer Selection ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerselectionidsresource)(s). 2 bytes count, following is repeated for each count: 4 bytes layer ID|
|1070|*(Photoshop CS2)* HDR Toning information|
|1071|*(Photoshop CS2)* Print info|
|1072|*(Photoshop CS2)* [Layer Groups Enabled ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource). 1 byte for each layer in the document, repeated by length of the resource. NOTE: Layer groups have start and end markers|
|1073|*(Photoshop CS3)* Color samplers resource. Also see ID 1038 for old format.|
|1074|*(Photoshop CS3)* Measurement Scale.|
|1075|*(Photoshop CS3)* Timeline Information.|
|1076|*(Photoshop CS3)* Sheet Disclosure.|
|1077|*(Photoshop CS3) DisplayInfo* structure to support floating point clors. Also see ID 1007.|
|1078|*(Photoshop CS3)* Onion Skins.|
|1080|*(Photoshop CS4)* Count Information.|
|1082|*(Photoshop CS5)* Print Information.|
|1083|*(Photoshop CS5)* Print Style. The printing marks, labels, ornaments, etc.|
|1084|*(Photoshop CS5)* Macintosh NSPrintInfo. Variable OS specific info for Macintosh.|
|1085|*(Photoshop CS5)* Windows DEVMODE. Variable OS specific info for Windows.|
|1086|*(Photoshop CS6)* Auto Save File Path.|
|1087|*(Photoshop CS6)* Auto Save Format. |
|1088|*(Photoshop CC)* Path Selection State.|
|2000-2997|Path Information (saved paths).|
|2999|Name of clipping path.|
|3000|*(Photoshop CC)* Origin Path Info|
|4000-4999|Plug-In resource(s). Resources added by a plug-in.|
|7000|Image Ready variables. XML representation of variables definition|
|7001|Image Ready data sets|
|7002|Image Ready default selected state|
|7003|Image Ready 7 rollover expanded state|
|7004|Image Ready rollover expanded state|
|7005|Image Ready save layer settings|
|7006|Image Ready version|
|8000|*(Photoshop CS3)* Lightroom workflow, if present the document is in the middle of a Lightroom workflow.|
|10000|[Print flags information](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printflagsresource).|


Aspose.PSD supports some of these resources. If Resource hasn't its own Class, you can use [UnknownResource ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unknownresource)from Aspose.PSD API Reference.

PSD Global Image Resources can be used for a big amount of cases. You can get specific Low-Level Data, that you cannot obtain in Adobe Photoshop.

Also, be free to report about Image Resources that you need.[Aspose Forum for PSD](https://forum.aspose.com/c/psd) can help.

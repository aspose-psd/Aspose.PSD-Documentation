---
title: Supported combination of Color Modes And Bit Depth in PSD
type: docs
weight: 80
url: /net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **Description**
Aspose.PSD Supports opening of PSD Files with any combination of Color Mode and Bit Depths in Adobe Photoshop PSD Files. You can open such files and use Low-Level API to modify the content of the file. But for some less popular combination can be specific issues, some of them related to Color Modes Limitation.
## **Supported export combination of Color Modes And Bit Depth in PSD in read-only mode**

| |Bitmap|Grayscale|Indexed|RGB|CMYK|Multichannel|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Depth 1|Yes[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Depth 8|-|Yes|Yes|Yes|Yes|No Q3-Q4|No Q3-Q4|Yes[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Depth 16|-|Yes|-|Yes|Yes|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|No (Q3-Q4)|
|Depth 32|-|Yes*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Yes*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Minor issues in some cases
## **Supported export combination of Color Modes And Bit Depth in PSD in editable mode**

| |Bitmap|Grayscale|Indexed|RGB|CMYK|Multichannel|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Depth 1|Yes|-|-|-|-|-|-|-|
|Depth 8|-|Yes|No|Yes|Yes|No Q3-Q4|No Q3-Q4|Yes*|
|Depth 16|-|Yes|-|Yes|Yes*|-|-|No (Q3-Q4)|
|Depth 32|-|No (Q3-Q4)|-|No (Q3-Q4)|-|-|-|-|
\* Minor issues in some cases



If you need the support of specific Color Mode / Bit Depth Combination, you can post on [Aspose Forums](https://forum.aspose.com/c/psd)




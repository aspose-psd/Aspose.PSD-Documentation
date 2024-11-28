---
title: PSD和PSB文件头部
type: docs
weight: 40
url: /zh/net/psd-and-psb-file-header/
---

## **描述**
Adobe Photoshop文件头部包含有关文件的版本信息（PSD为1，PSB为2），通道数量，颜色模式和位深度。

您可以从相关文章中了解由Aspose.PSD支持的颜色模式和位深度的组合。

文件头包含图像的基本属性。

|**长度**|**描述**|
| :- | :- |
|4|签名：始终等于*"8BPS"*|
|2|[PSD 版本](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion)：PSD文件为1，PSB文件为2。Aspose.PSD能够检测文件格式的版本并正确读取。|
|6|保留：必须为零。|
|2|图像中的通道数，包括任何Alpha通道。支持范围为1到56。|
|4|图像的高度（以像素为单位）。支持范围为1到30,000像素。PSB文件支持高达300,000像素的高度。Aspose.PSD也支持PSB文件。|
|4|图像的宽度（以像素为单位）。支持范围为1到30,000像素。PSB文件支持高达300,000像素的宽度。Aspose.PSD也支持对大型PSD/PSB文件的批处理。|
|2|深度：每个通道的位数。支持的值为1, 8, 16和32。但并非每种颜色模式都适用于每种深度。|
|2|文件的[PSD颜色模式](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes)。支持的值为：位图 = 0；灰度 = 1；索引 = 2；RGB = 3；CMYK = 4；多通道 = 7；双色调 = 8；Lab = 9。|
您可以查看我们的[PSD API参考](https://reference.aspose.com/psd)以了解更多。


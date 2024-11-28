---
title: 当在压缩图像上绘制时避免性能下降
type: docs
weight: 10
url: /zh/net/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **当在压缩图像上绘制时避免性能下降**
有时您想要在压缩图像上执行非常复杂的图形操作。当Aspose.PSD需要动态压缩和解压图像时，性能下降可能会发生。在压缩图像上绘制也可能会带来性能惩罚。
### **解决方案**
为避免性能下降，我们建议在执行图形操作之前，将图像转换为未压缩或原始格式。
### **使用文件路径**
在接下来的示例中，将一个PSD图像转换为原始格式（无压缩）并保存到磁盘。然后重新加载未压缩图像，才能在其上执行图形操作。相同的技术也适用于BMP和GIF文件。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **使用流对象**
下面的代码片段向您展示如何将PSD图像转换为原始格式（无压缩）并使用MemoryStream保存到磁盘。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}

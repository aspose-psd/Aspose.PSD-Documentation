---
title: 在绘制的压缩图像上避免性能降级
type: docs
weight: 40
url: /zh/java/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **在绘制的压缩图像上避免性能降级**
有时候，您可能希望在压缩图像上执行非常复杂的图形操作。当 Aspose.PSD 需要在运行时压缩和解压图像时，性能可能会下降。在压缩图像上绘制也可能会导致性能损失。
### **解决方案**
为了避免性能下降，我们建议在执行图形操作之前将图像转换为未压缩或原始格式。
### **使用文件路径**
在接下来的示例中，一个 PSD 图像被转换为原始格式（无压缩）并保存到磁盘。然后在执行图形操作之前重新加载未压缩的图像。相同的技术适用于 BMP 和 GIF 文件。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **使用流对象**
下面的代码片段展示了如何将 PSD 图像转换为原始格式（无压缩）并使用 Stream 保存到磁盘。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}

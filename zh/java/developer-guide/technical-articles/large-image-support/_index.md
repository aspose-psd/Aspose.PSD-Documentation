---
title: 大图支持
type: docs
weight: 60
url: /zh/java/large-image-support/
---

## **大图支持**
由于标准 Java 库在处理图像大小方面存在一些限制，我们引入了一种新的机制来支持处理大图。新方法克服了这些限制，但由于数据大小限制，对于创建和加载的最大支持尺寸为 2,147,483,647 x 2,147,483,647 像素。
### **处理大图**
Aspose.PSD 提升了对大图的性能和支持。数百兆字节大小的图像不再是问题，因此您可以在这些图像上创建、加载和绘制。但是，由于部分处理和处理 OutOfMemoryException 异常，对于非常大的图像，性能可能会非常低。这是因为 Aspose.PSD 尝试重新分配较小数量的数据进行处理，每次重新分配步骤的成本非常高。新架构的优势明显：

- 没有图像大小限制。
- 您不受计算机可用内存的限制。

如果您遇到处理缓慢的情况，建议增加总 RAM 量以将所有像素适应内存。如果不这样做，处理仍然是可能的，但速度较慢。操作方法如下：

- 调用 LoadPartialPixels 方法，并提供所需的矩形和委托以接收加载的指定像素。

Aspose.PSD 尝试加载整个矩形。

- 如果有足够的内存来适应所有像素，则所有像素只需返回给调用者。
- 如果没有足够的内存，调用者将从指定矩形内部收到部分像素。当这些像素被处理后，调用者将收到下一个矩形。处理将在整个矩形被处理完成时结束。

Aspose.PSD 尝试提取尽可能多的行。如果没有足够的内存适应一个像素行，那么一个像素行将被分成符合高度为 1 的矩形的部分。您还可以在大图上绘制。绘制过程试图影响整个所需的矩形。如果没有足够的内存，绘画将在部分矩形上执行，直到整个区域被绘制。此外，Aspose.PSD 支持保存和导出大图。将源图像保存到磁盘或导出至另一种文件格式。如果需要，保存或导出过程将使用部分矩形执行。 
### **支持的图像格式**
以下格式支持处理大图像：

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

上述格式可以安全地通过创建、修改、应用绘图操作、保存到磁盘或导出的方式进行处理，无论图像大小如何。

. 

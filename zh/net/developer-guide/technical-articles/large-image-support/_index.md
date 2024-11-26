---
title: 大图支持
type: docs
weight: 40
url: /zh/net/large-image-support/
---

## **大图支持**
由于标准.NET库存在一些关于可以处理的图像大小的限制，我们引入了一种新的机制来支持大图像。这种新方法克服了这些限制，但由于数据大小限制，用于创建和加载的最大支持尺寸为2,147,483,647 x 2,147,483,647像素。
### **处理大图像**
Aspose.PSD在处理大图像方面性能和支持得到改善。数百兆字节大小的图像现在不再是问题，因此您可以在这些图像上创建、加载和绘制。然而，由于部分处理和处理OutOfMemoryException异常，对于非常大的图像，性能可能会很低。这是因为Aspose.PSD尝试重新分配更少的数据以进行处理，而每个重新分配步骤的成本非常高。新架构的好处是显而易见的：

- 没有图像大小的限制。
- 您不受PC可用内存的限制。

如果您遇到处理速度较慢的情况，建议增加总RAM量以使所有像素适应内存。如果不这样做，处理仍然可行，但速度较慢。处理方法如下：

- 调用 [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) 方法，并使用所需的矩形和代理来接收指定的加载像素。

Aspose.PSD会尝试加载整个矩形。

- 如果有足够的内存容纳所有像素，那么所有像素将简单地返回给调用者。
- 如果内存不足，调用者将从指定矩形的内部接收一部分像素。当这些像素被处理后，调用者将接收下一个矩形。处理结束时，整个矩形都被处理。

Aspose.PSD试图提取尽可能多的行。如果没有足够的内存来容纳一个像素行，则一行将被分割成符合高度为1的矩形的部分。您还可以在大图像上绘制。绘图过程试图影响整个所需的矩形。如果内存不足，绘制将在部分矩形上进行，直到整个区域被绘制。此外，Aspose.PSD支持保存和导出大图像。将源图像保存到磁盘或将其导出为另一种文件格式。如果需要，保存或导出过程是通过使用部分矩形执行的。 
### **支持的图像格式**
以下格式支持大图像处理：

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

以上格式可以安全地通过创建、修改、应用绘图操作、保存到磁盘或导出成另一种图像格式，进行无视图像大小的处理。

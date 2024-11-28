---
title: 原始数据处理
type: docs
weight: 50
url: /zh/net/raw-data-processing/
---

## **原始数据处理**
为了提高 Aspose.PSD API 的性能，我们在版本2.4.0中引入了一种用于原始数据处理的方法。原始数据处理现在在内部使用，并具有外部API，因此可以从库外部使用以提高整体性能。有时处理会有些棘手，并需要一些解释。目前，原始数据处理仅适用于BMP格式。

为了帮助开发人员获得最佳性能，Aspose.PSD API提供了一个原始数据处理系统，该系统具有用于定制的外部API。开发人员调用[LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) 和[SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) 方法族来使用原始数据处理。这些方法还需要使用[RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings)类设置所需的原始数据格式。RawDataSettings类允许开发人员指定任何原始数据格式。然而，为了实现最佳性能，您需要使用数据存储的原始数据格式。[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 类中定义的RawDataSettings有助于确定图像的原始[数据格式](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat)。将RawDataSettings实例传递给LoadRawData方法时，数据会如实返回，不会应用任何转换，这可能会提高性能。另一方面，您需要关注所有可能有些复杂的原始数据格式布局。

为了简化处理过程，可能需要一些性能损失，您可以通过实例化并初始化带有所需原始数据设置的类来指定所需的RawDataSettings。在某些情况下，无法以指定格式返回原始数据（例如，在版本2.4.0中无法从CMYK颜色空间转换为RGB）。此外，有时对于某些图像格式根本不支持原始数据处理。要确定是否可以使用LoadRawData 和 SaveRawData 方法族，您需要查询[IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable)属性。

### **洞察**
对于RGB[像素数据格式](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat)，存在索引（基于调色板）和基于RGB的原始数据格式。索引原始数据格式包含0..(2^比特计数 - 1)范围内的调色板条目索引。索引原始数据格式为每像素1、2、4和8位。其余为基于RGB的原始数据格式。在加载原始数据时，要注意是否有足够的字节可用于加载数据，否则将抛出适当的异常。您可以通过将行大小乘以所需行数来简单估算字节数组大小。行大小可能会有所不同，这取决于原始数据存储格式。

为了获得最佳性能，请始终使用与[RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize)属性值相等的原始数据行大小。但有时可能需要向原始数据行添加额外填充，或者减少填充，当这种情况发生时可能需要使用不同的行大小。如果需要图像边界矩形的子集，则必须考虑索引RGB像素格式可能发生的位移。例如，假设图像的尺寸为100x100像素，每像素1比特的原始数据格式。您想要加载一个从位置(7,0)到(2,1)尺寸的原始数据矩形，或者换句话说，您需要从x=7和y=0开始的2像素。在这种情况下，您应该接收以下数据布局：



![todo:image_alt_text](raw-data-processing_1.png)

这意味着您将收到2个字节，第一个字节包含7个不需要的像素，然后是1个期望的像素，第二个字节包含1个期望的像素，然后是7个不需要的像素。您可能会问为什么我们没有执行数据位移，将这两个像素放入单个字节中？答案很简单：为了保持性能高。所有内部处理通常是从第一个像素开始并以最后一个可用像素结束。只有在需要像素子集的情况下才会出现少见的情况。此外，我们不知道这些像素之后将如何处理，因此转移会降低性能并使代码变得不必要复杂。始终估算出需要的正确位（无需确定正确的字节，因为数据总是以填充的第一个字节）的位置，以便找到要求的像素。可以使用一个简单的公式来计算正确的位：（rect.Left * 比特计数）% 8。
### **索引RGB颜色转换**
为了实现尽可能的高性能，请始终使用相同的源和目标原始数据设置、像素格式和行大小。但是，有时可能需要执行数据转换。例如，您可以加载每像素1位的RGB图像，并以每像素2位保存它，或加载每像素4位的RGB图像，并将其颜色范围降级为每像素2位。在任一情况下，应用颜色转换。有时候，对索引RGB图像进行转换可能会有些棘手，并且可能无法在不应用一些设置的情况下进行。我们需要确定源颜色范围如何映射到目标颜色空间。为了完成这项任务，我们有不同的[模式](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods)：

- 调色板映射（DitheringMethods.PaletteConversion）
- 原始数据映射（DitheringMethods.PaletteIgnore）
- 自定义转换（DitheringMethods.CustomConverter）

使用调色板转换时，源颜色空间尝试尽可能接近目标颜色空间。例如，让我们假设我们有一个具有以下颜色的4位图像：
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

源图像如下所示：



![todo:image_alt_text](raw-data-processing_2.png)

然后我们将4位图像转换为以下调色板颜色定义的1位图像：

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

在调色板转换模式下，转换器会读取源颜色并使用目标调色板的[GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index)方法确定目标索引。如果调色板的GetNearestColorIndex方法给出超出范围的索引，则将使用[RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex)属性值。这将将源颜色转换为在强度值方面尽可能接近的目标颜色。您可以看到以下结果：



![todo:image_alt_text](raw-data-processing_3.png)

在原始数据映射模式下使用了不同的场景。简单地忽略了源和目标色彩调色板，并将源索引映射到目标索引。当发现一个值无法映射到目标范围（降低位数时）时，将使用RasterImage.RawFallbackIndex属性值。默认值为0，将映射到目标调色板中的第一种颜色。如果此属性值位于目标范围之外，将抛出适当的异常。这会导致结果不太可预测，可以在以下图像中显示：



![todo:image_alt_text](raw-data-processing_4.png)

调色板转换模式是解决颜色映射问题的更正确的解决方案，但完成时间可能稍长，因为需要执行计算来估算正确的调色板映射。 （两种方法之间通常几乎没有性能差异。）另一方面，原始映射模式执行速度更快，可用于颜色转换粗糙时使用更少的颜色映射的情况。例如，有时源调色板已经被修剪，并且可以安全地转换为较小的位数，因为额外的位数根本没有被使用。

要使用这些方法中的任何一种，使用RasterImage类的RawDitheringMethod属性。默认情况下，设置为调色板转换方法以实现最佳外观结果。您可以在进行任何转换之前更改此属性（例如，当将图像保存到流时）。请注意，如果您加载了一个图像并重写了一些原始像素数据，那么调色板忽略和调色板转换抖动方法就不会发生，因为新数据会存储在缓存中，缓存会以最大的可用格式32ARGB（截至2.4.0，可能会更改）存储数据。此格式用于应对加载和保存图像的可能不同颜色范围的问题。此外，当以RGB模式加载图像并将其转换为索引模式，或反之亦然时，将忽略调色板忽略和调色板转换抖动方法。
### **自定义颜色转换器**
有时仅使用标准颜色转换方法是不够的。您可能希望使用自定义算法来在使用颜色转换例程时获得完全自由。当源图像和目标图像的像素格式都是索引RGB格式时，可使用更简单的接口[IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter)。您需要将[RasterImage.RawIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawindexedcolorconverter)属性设置为IIndexedColorConverter接口的实例，并将[DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter设置为RawDitheringMethod属性的值。在此情况下，任何索引颜色转换都通过指定的IIndexedColorConverter实例进行。自定义索引颜色转换器定义了以下方法：



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



在需要从索引RGB图像转换为索引RGB图像格式（将1, 2, 4或8位计数之一转换为另一个位数）时，将调用FillIndexedtoIndexedMap方法。该映射数组的长度为所有可能的源格式条目计数。您需要填充该数组以从源颜色调色板条目到目标颜色调色板条目的映射。请注意，目标索引值在0..（位计数 - 1）范围内，否则会抛出适当的异常。

如果需要执行更自定义的颜色转换场景，则应将[RasterImage.RawCustomColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawcustomcolorconverter)属性设置为[IColorConverter](https://reference.aspose.com/psd/net/aspose.psd/icolorconverter)接口的实例。如果同时设置了RawCustomColorConverter属性和RawIndexedColorConverter属性，前者将始终重写后者，此时不会使用索引颜色转换器。IColorConverter具有一个方法：



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}


每次需要颜色转换时，都会调用Convert方法。该方法接收源格式的原始数据，并具有一个输出缓冲区，用于接收转换为目标格式的颜色。目标缓冲区应足以容纳转换后的数据（如果Aspose.PSD库内部调用接口调用），并且应在调用方法返回时包含转换后的原始数据。可能会多次调用Convert方法，直到覆盖整个源数据。
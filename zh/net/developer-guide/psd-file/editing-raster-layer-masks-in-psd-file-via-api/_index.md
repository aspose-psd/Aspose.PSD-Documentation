---
title: 通过 API 在 PSD 文件中编辑光栅图层蒙版
type: docs
weight: 20
url: /zh/net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **概述**
**为了自动化 PSD 格式的编辑并在没有 Adobe® Photoshop® 的情况下更改 PSD 文件，您可以使用下面提供的 Aspose.PSD API。以下是可以帮助您修改 PSD 文件的 C# 和 .NET 代码片段。**

使用 PSD 图层和矢量蒙版，我们能够在不永久删除它们的情况下隐藏和显示图层像素。光栅蒙版也称为图层蒙版或用户蒙版。在 Aspose.PSD 中，可以通过[LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata)图层属性访问光栅和矢量蒙版，它可以是 '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' 和 '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' 类的实例，这些类是抽象 'LayerMaskData' 类的子类。如果一个图层同时具有光栅和矢量蒙版，则会提供[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)实例。如果一个图层只有光栅蒙版或矢量蒙版，则会提供[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)实例。如果 LayerMaskData 属性为 null，则表示该图层没有蒙版或仅有一个禁用的矢量蒙版。


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>一个光栅蒙版和一个禁用的矢量蒙版 LayerMaskDataShort</p><p>一个禁用的光栅蒙版 LayerMaskDataShort</p><p>一个光栅蒙版和一个矢量蒙版 LayerMaskDataFull</p><p>一个光栅蒙版 LayerMaskDataShort</p><p>一个矢量蒙版 LayerMaskDataShort</p><p>一个禁用的矢量蒙版 null（但矢量资源存在）</p>|
| :- | :- |

## **如何在 PSD 文件中获取图层光栅蒙版？**
首先，我们应该查找图层是否同时具有矢量和图层蒙版：

以下提供的示例代码演示了如何获取图层光栅蒙版

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

否则，LayerMaskData 图层属性的类型为 LayerMaskDataShort。在这种情况下，让我们检查图层是否只有一个光栅蒙版，方法是检查 Flags 属性。它不应该包含 [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData** 标志，否则该蒙版是矢量蒙版缓存。

获取蒙版代码段：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

如果需要**提取光栅蒙版**作为 LayerMaskDataShort（用于进一步操作），即使两种蒙版都存在，也应提取并转换为 LayerMaskDataShort。下面的代码可以同时用于这两种情况：

从 PSD 中提取光栅蒙版

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}

## **如何检查 PSD 文件中的图层是否具有光栅蒙版？**
以下的 C# 代码可能会帮助您检查图层是否具有光栅蒙版：

如何知道是否将光栅蒙版应用于[PSD 图层](/psd/zh/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}

## **如何在 PSD 文件中删除 / 添加 / 更新图层光栅蒙版？**
仅删除 / 添加 / 更新 LayerMaskData 是不够的以便正确保存，因为通道不会被更新；尽管它可能提供正确的渲染。这并不会更改蒙版通道：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

我们应该使用 layer AddLayerMask 方法来删除 / 添加 / 更新。

这会同时添加 / 更新蒙版和通道：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

这会同时删除蒙版和通道：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}

## **在 PSD 图像中删除图层光栅蒙版**
首先，我们检查蒙版是否处于短格式，并且如果不是矢量蒙版，我们可以只调用 AddLayerMask 方法并输入 null 来删除光栅蒙版。但如果蒙版处于完整格式，我们必须将其转换为短格式，仅保留矢量蒙版。要删除图层蒙版，可以使用以下 C# .NET 代码段：

代码段如何从 PSD 文件中删除图层蒙版。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

## **更新 PSD 图像中的图层光栅蒙版**
这很简单：如果蒙版处于短格式，则必须根据需要更改 ImageData 和 MaskRectangle。否则，[UserMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)和[UserMaskRectangle](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)应更改。以下的 C# .NET 代码段可用于更新图层蒙版：

使用 C# 更新 PSD 图层蒙版

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

这是一个可能改变光栅蒙版的示例操作。这个操作反转了图层用户蒙版：

使用 C# 更新 PSD 图层蒙版

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}

## **更新 PSD 文件中的图层光栅蒙版时如何处理矢量蒙版存在的情况**
假设用户已经更改了矢量路径资源。然后，它可以通过调用[AddLayerMask](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask)图层方法简单地更新矢量蒙版：

使用 C# 更新[PSD 图层矢量蒙版](/psd/zh/net/layer-vector-mask/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}

## **在 PSD 文件中添加图层光栅蒙版**
如果一个图层没有蒙版，我们可以通过调用 AddLayerMask 图层方法简单地添加给定的光栅蒙版。

如果这个蒙版没有[UserMaskFromRenderingOtherData**](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)标志，那么它已经有一个光栅蒙版，并且我们必须像上面描述的方式更新它。否则，如果这个蒙版是短格式，我们将其转换为完整格式。否则，我们将其原样使用。然后根据给定的蒙版属性更新 UserMaskData、UserMaskRectangle 和其他属性。以下的 C# .NET 代码段可用于添加（更新）图层蒙版：

将新的图层蒙版添加到 PSD 文件

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **如何检查图层蒙版是否启用？**
要了解图层光栅蒙版的启用状态，我们可以检查 LayerMaskDataShort 的 Flags 属性或 LayerMaskDataFull 的 RealFlags 中的 LayerMaskFlags.Disabled 标志状态。以下的 C# .NET 代码段可用于获取图层蒙版的启用状态：

检查蒙版是否启用：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}

## **如何启用或禁用光栅图层蒙版？**
要启用或禁用图层光栅蒙版，我们可以更改 LayerMaskDataShort 的 Flags 属性或 LayerMaskDataFull 的 RealFlags 中的 LayerMaskFlags.Disabled 标志状态。以下的 C# .NET 代码段可用于更改图层蒙版的启用状态：

启用或禁用光栅图层蒙版：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}

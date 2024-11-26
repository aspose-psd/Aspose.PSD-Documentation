---
title: 使用PSD文件作为模板进行自动化处理 - 商业名片案例
type: docs
weight: 10
url: /zh/net/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **概述**
本文描述了在需要通过编程方式更新[PSD文件](https://wiki.fileformat.com/image/psd/)中的一些图层时经常使用的情况，其中PSD/PSB文件具有某种已知的类似模板的结构。这可用于为不同人群创建大量的名片（商业名片案例）。或者您需要将PSD文件翻译成不同语言，并用其中的一些图形素材替换之。

阅读本文后，您将了解如何实现以下操作：

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)

## **简单情况**
例如，您有一个包含已知图层名称的PSD模板。因此，您需要通过C#更改、更新或替换PSD图层。首先，您需要使用Aspose.PSD打开模板文件。

如何通过C#打开PSD文件？

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)


然后，我们需要根据名称查找要替换的图层。以下是此功能的简单实现。

如何通过其名称在PSD文件中找到图层

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}



找到图层后，我们可以按通用方法更新它，使用[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)：

如何在PSD图层上绘制

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

在这种情况下，我们在现有PSD图层上绘制了新加载的[PNG图像](https://wiki.fileformat.com/image/png/)，因此旧数据将在新文件中丢失。

但如果我们还需要更新文本怎么办？过程类似。通过其名称查找[文本图层](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)，然后我们以编程方式[更新Photoshop文件的文本图层](/psd/zh/net/render-text-with-different-colors-in-text-layer/)。

如何使用C#在Photoshop中更新文本图层

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



最后，我们需要保存更改：

如何使用[Aspose.PSD](https://products.aspose.com/psd/net)保存更改的PSD文件

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



最终的图像是：

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **具有附加功能的复杂情况**
以上我们展示了在PSD文件的图层中替换图像的最简单方式。

但是Aspose.PSD可以提供更复杂的附加功能，如添加新图层、移除旧图层，并使用不同的样式在多行文本中更新文本图层。

我们可以找到要替换的[图层](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer)，然后在图层列表中找到其索引，将其删除，并在从[Jpeg文件](https://wiki.fileformat.com/image/jpeg/)创建新图层后插入到相同位置。

从文件创建新图层并将其插入到PSD图像中使用[Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



在此文件代码片段的末尾，我们校正图层位置并将新图层数组保存到Psd图像中。

如何复制[PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)图层属性

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



最后，我们需要通过C#更新现有PSD图像中的文本图层。Aspose.PSD支持[按部分更新文本图层](/psd/zh/net/working-with-text-layers/)。每个[文本部分](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion)具有唯一的样式和段落属性组合。

如何复制[PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)图层属性

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



结果，我们通过代码更改了PSD模板，添加了来自Jpeg、Png、J2k、Bmp、Gif或Tiff文件的新图层和不同风格的多行[文本](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs)。


![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)

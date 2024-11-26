---
title: 如何在Java中以编程方式创建YouTube缩略图生成器
type: docs
weight: 10
url: /zh/java/how-to-create-youtube-thumbnail-generator-programmatically-in-java/
---

## **介绍**
该文档的目的是演示在一个真实例子中使用[Aspose.PSD for Java](https://products.aspose.com/psd/java)的一些组合工具的API用法。在本文中，将编写和解释一个**生成YouTube缩略图的简单Java程序**，该缩略图用于[DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q)频道。选择了来自现实世界的该频道，因为其缩略图相当标准，并且展示了Aspose.PSD for Java的一些流行组合工具的使用（例如[投影效果](/psd/zh/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)、径向渐变填充、绘制文本和形状）：

![待办：图片替换文本](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **工作原理概述**
一个简单的Java程序以两个参数为输入：标题和图像。使用Aspose.PSD for Java从输入生成**内存中的Photoshop文档（PSD）**。随后，程序将文档从PSD转换为PNG文件格式，以获得尺寸为1280x720像素的YouTube缩略图。输出图像看起来与以下类似：

![待办：图片替换文本](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **技术要求**
要成功运行本文代码，需要以下技术：

- Java 6+
- [Aspose.PSD for Java](/psd/zh/java/installation/)（最新版）

## **入门**
如前所述，该程序使用内存中的PSD生成缩略图。因此，让我们**首先创建一个PSD文档**：

```java
PsdImage psdImage = new PsdImage(1280, 720);
```

如果你仔细看上面的YouTube缩略图，你可能会注意到**它由几个组件组成**：

1. 一个背景图像（印刷遮罩）
2. 一个径向PSD渐变（突出显示右上角的区域）
3. 一个带有阴影效果的标识
4. 一个标题和一个简单的绘图（蓝色矩形）

让我们深入研究如何在接下来的部分中使用Aspose.PSD for Java实现其中的每个组件。

## **1. 添加背景图像**
图层的顺序很重要。因此，必须先添加背景图像，以免重叠其他图层。请注意，目前仅支持[光栅文件格式](/psd/zh/java/supported-file-formats/)。

### **1.1. 将背景图像添加到Photoshop图层**
为了**将栅格图像添加到PSD**，在构建图层时必须传递输入流作为参数（查看更多[加载栅格图像的示例](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)）：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}
```

### **1.2. 将背景图像适应到画布**
以下两个操作（调整大小、定位）对于图像大小与画布大小不同时非常有用，尽管本文中的图像与画布大小相同（假设不总是这样）。

确保载入的图像**适合画布大小**（查看更多[调整大小的示例](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)）：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}
```

调整大小后，图像位置会改变。因此，为了**重置图像位置**，将调整后的图像移动到左上角：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}
```

## **2. 添加径向渐变**
有两种方式添加径向渐变，使用：

- 现有图层上的[渐变叠加效果](/psd/zh/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163)（将渐变效果绑定到当前图层并应用于其内容）
- 新的[渐变填充图层](/psd/zh/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill)（保留独立梯度设置的单独图层）

对于本例，使用渐变填充图层就足够了。然而，为了使本文更有趣和有用，**使用了渐变填充图层**，因为所有图层效果都以类似的方式应用，下一节将使用另一个图层效果。

### **2.1. 添加径向渐变填充图层**
添加新的渐变填充图层的过程包括以下2个步骤：

\1. 必须**声明渐变填充设置**，因为没有预定义的设置。最低要求的配置如下（意味着需要渐变类型、比例、颜色和透明度点）：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}
```

上面的配置声明了一个在边缘为透明且在中心为深蓝色的径向渐变。默认情况下，渐变位置在画布的中间。

要颠倒渐变填充并略微位移到右上角，请使用相应的可选属性：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}
```


\2. 配置完成后，将渐变填充图层和其设置添加到PSD中：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}
```

## **添加带阴影的标识**
**投影效果**是一种允许沿物体（图像、文本等）轮廓添加自定义阴影的效果。

### **3.1. 将标识添加到Photoshop图层**
与1.1节中的方法相同，可用来**将标识添加到PSD**中：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
```

### **3.2. 定位标识**
默认情况下，载入的图像与左上角紧密贴合。然而，为了看起来像频道上的原始YouTube缩略图，需要添加一些**边缘间距**，因此，图像位置应该从图层边缘偏移：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
```

### **3.3. 为标识添加投影效果**
如果使用浅色背景图像，标识可能会不可见。因此，最好通过[混合选项属性](/psd/zh/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)为标识**添加投影效果**：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}
```

由于默认配置（类似于Photoshop的配置），投影效果并不具有必要的属性。不过，上述阴影已经修改，使其看起来像在边缘模糊的半透明边框。

## **4. 添加文本和形状的绘制**
### **4.1. 创建图形图层**
直接在常规图层上不支持绘图。因此，除了图层外，使用**图形引擎**进行绘图（查看更多[绘图示例](/psd/zh/java/drawing-images-using-graphics/)）：

```java
Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
```

### **4.2. 绘制多行文本**
有经验的读者可能会问：为什么不使用文本图层添加文本？原因有几条：在这种情况下不需要文本编辑，因为每次从头开始生成PSD；目前的[文本API](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers)尚不支持字体自定义（在撰写本文时的版本为v20.6）。

要**绘制一些使用自定义字体的文本**，只需实例化一个期望的字体并从图形引擎中调用相应方法即可。不过，要制作一个（详细内容请参见下一节）根据文本行数自动更改高度的矩形稍微困难。首先必须先计算所有行的确切高度：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}
```

其中1.15是行高，3是文本间距。

### **4.3. 绘制一个矩形**
即使使用渐变刷子，绘制一个矩形也很容易（只需设置要绘制的区域和颜色范围）。当已知文本的高度时，计算矩形的大小和位置。为了在PSD中**绘制填充的矩形**（而不仅仅是一个框），从图形引擎中调用相应方法并附上这些内容：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}
```

` `其中40, 15, 25是缩进。

## **结果**
缩略图的形状已经完成。因此，现在是将缩略图**导出为一种栅格文件格式**（例如PNG）以供进一步分发的时候：

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}
```

## **结论**
在本文中，我们为DW Documentary频道创建了一个YouTube缩略图生成器，并解释了如何使用一些流行的组合工具，例如投影效果、径向渐变填充、绘制文本和形状。

## **完整示例**
您可以[下载Aspose.PSD SDK](https://products.aspose.com/psd/net)

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
```
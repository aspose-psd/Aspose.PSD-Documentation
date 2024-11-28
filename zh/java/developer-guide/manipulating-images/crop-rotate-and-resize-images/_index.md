---
title: 裁剪、旋转和调整图像大小
type: docs
weight: 40
url: /zh/java/crop-rotate-and-resize-images/
---

## **裁剪图像**
图像裁剪通常指的是去除图像的外部部分以帮助改善构图。裁剪也可以用于剪切图像的某些部分，以便增加对特定区域的关注。Aspose.PSD API支持两种不同的图像裁剪方法：通过偏移和矩形。
### **通过偏移裁剪**
RasterImage类提供了一个重载版本的Crop方法，该方法接受4个整数值，表示左、右、上和下。基于这四个值，Crop方法将移动图像边界向图像中心移动，同时丢弃外部部分。以下代码片段演示了如何通过偏移裁剪图像。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **通过矩形裁剪**
RasterImage类提供了另一个重载版本的Crop方法，该方法接受Rectangle类的实例。您可以通过为Rectangle对象提供所需的边界来切除图像的任何部分。以下代码片段演示了如何通过矩形裁剪任何图像。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **旋转和翻转图像**
Aspose.PSD for Java是一个易于使用的库，因为它提供了简单的方法来执行复杂的操作。例如，如果应用程序需要旋转图像，则Aspose.PSD for Java已为其基类Image提供了RotateFlip方法。无论图像格式如何，该库都可以在其上执行特定的旋转和翻转过程。
### **旋转图像**
Image.RotateFlip方法可用于将图像逆时针或顺时针旋转90/180/270度，并水平或垂直翻转图像。Image.RotateFlip方法接受一个RotateFlipType参数，该参数指定要应用于图像的旋转和翻转类型。执行旋转和翻转的步骤如下简单，

1. 使用Image类公开的工厂方法Load加载图像。
1. 调用Image.RotateFlip方法，同时指定适当的RotateFlipType。
1. 保存结果。

以下代码示例演示了如何设置图像的RotateFlip属性和RotateFlipType枚举。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **在特定角度上旋转图像**
Aspose.PSD for Java API公开了RasterImage.Rotate方法，以方便希望在特定角度上旋转图像的用户。与RasterImage.RotateFlip方法不同，RasterImage.Rotate方法接受三个参数：

1. 旋转角度：float类型参数，指定要将图像旋转到的旋转角度。正值顺时针旋转图像；负值逆时针旋转图像。
1. 等比缩放：布尔类型参数，指定图像大小是否根据旋转后的矩形（角点）投影进行更改。如果设置为false，则图像尺寸将保持不变，仅旋转内部图像内容。
1. 背景颜色：Color类型参数，指定要填充在旋转图像背景中的颜色。

以下代码片段演示了RasterImage.Rotate方法的用法。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **调整图像大小**
本文演示了如何使用Aspose.PSD for Java对图像执行调整大小操作。Aspose.PSD API已公开了高效且易于使用的方法来实现此目标。Aspose.PSD for Java已为Image类暴露了Resize方法，可用于实时调整现有图像的大小。有两种Resize方法的重载以满足应用程序需求。
### **简单调整大小**
执行调整大小操作的步骤如下简单：

1. 使用Image类公开的工厂方法Load加载图像。
1. 调用Image.Resize方法，同时指定新的高度和宽度。
1. 保存结果。

以下代码示例演示了如何调整图像大小。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **使用ResizeType枚举调整大小**
Aspose.PSD API已公开了ResizeType枚举，可与Image.Resize一起使用以实现所需的结果。下面提供的代码片段演示了ResizeType枚举的用法，而ResizeType枚举成员的详细信息可以在本页底部找到。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



如果您想在应用重设大小后获得高质量的结果，则建议始终使用ResizeType.LanczosResample，因为它将输出非常高质量的结果，但可能比ResizeType.NearestNeighbourResample工作慢。另一方面，ResizeType.NearestNeighbourResample算法专为快速调整大小而设计，而牺牲图像质量。该方法可能适用于实时缩略图生成或需要性能的类似流程。
## **等比例调整图像大小**
您可以通过将新的高度和宽度值作为参数传递给Image.Resize方法来调整图像大小，但在这种情况下，您必须自己计算纵横比。这是因为当图像的宽度或高度改变时，图像会以填充新尺寸或缩小以适应新尺寸。如果图像的宽度和高度的更改不成比例，这可能导致拉伸和扭曲的结果。本文演示了如何使用Aspose.PSD for Java API调整图像大小，只需通过传递新的高度或宽度，同时允许API自动计算其他成比例的值。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **ResizeType枚举**
ResizeType确定根据所选滤镜在图像上执行的调整大小类型。

ResizeType枚举成员

|**成员名称**|**值**|**描述**|
| :- | :- | :- |
|LeftTopToLeftTop|0|新图像的左上点将与原始图像的左上点重叠。如果需要，将进行裁剪。|
|RightTopToRightTop|1|新图像的右上点将与原始图像的右上点重叠。如果需要，将进行裁剪。|
|RightBottomToRightBottom|2|新图像的右下点将与原始图像的右下点重叠。如果需要，将进行裁剪。|
|LeftBottomToLeftBottom|3|新图像的左下点将与原始图像的左下点重叠。如果需要，将进行裁剪。|
|CenterToCenter|4|新图像的中心将与原始图像的中心重叠。如果需要，将进行裁剪。|
|LanczosResample|5|使用7x7掩模的Lanczos算法重新采样。|
|NearestNeighbourResample|6|使用最近邻居算法重新采样。|

---
title: 裁剪、旋转和调整图像大小
type: docs
weight: 40
url: /zh/net/crop-rotate-and-resize-images/
---

## **裁剪图像**
图像裁剪通常指的是删除图像的外部部分，以帮助改善构图。裁剪也可用于剪切图像的某些部分，以增强对特定区域的关注。Aspose.PSD API支持两种不同的图像裁剪方法：通过偏移和矩形。
### **通过偏移裁剪**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)类提供了Crop方法的重载版本，该方法接受4个整数值，分别表示左、右、上和下。根据这四个值，Crop方法将移动图像边界向图像中心移动，同时丢弃外部部分。以下代码段演示了如何通过偏移裁剪图像。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **通过矩形裁剪**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)类还提供了另一个重载版本的Crop方法，该方法接受一个Rectangle类的实例。您可以通过向Rectangle对象提供所需的边界来剪切图像的任何部分。以下代码段演示了如何通过矩形裁剪任何图像。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **旋转和翻转图像**
Aspose.PSD for .NET是一个易于使用的库，因为它提供了执行复杂操作的简单方法。例如，如果应用程序需要旋转图像，则Aspose.PSD for .NET为其基类图像提供了RotateFlip方法。无论图像格式如何，该库都可以针对图像执行特定的旋转和翻转过程。
### **旋转图像**
Image.RotateFlip方法可用于将图像旋转90/180/270度，并在水平或垂直方向翻转图像。Image.RotateFlip方法接受一个RotateFlipType参数，该参数指定要应用于图像的旋转和翻转类型。执行旋转和翻转的步骤如下简单，


1. 使用Image类公开的工厂方法Load加载图像。
1. 调用Image.RotateFlip方法，并指定适当的RotateFlipType。
1. 保存结果。

以下代码示例演示了如何设置图像的RotateFlip属性以及RotateFlipType枚举。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **以特定角度旋转图像**
Aspose.PSD for .NET API公开了[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate方法，以便为希望将图像旋转到特定角度的用户提供支持。与[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip方法不同，[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate方法接受三个参数：

1. 旋转角度：float类型的参数，指定图像要旋转的角度。正值顺时针旋转图像；负值逆时针旋转图像。
1. 等比例调整大小：布尔类型参数，指定图像大小是否根据旋转后的矩形（角点）投影进行更改。如果设置为false，则图像尺寸将保持不变，只有内部图像内容会旋转。
1. 背景颜色：Color类型参数，指定旋转图像的背景填充颜色。

以下代码段演示了[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate方法的用法。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **调整图像大小**
本文介绍了使用Aspose.PSD for .NET执行图像调整操作的方法。Aspose.PSD API提供了高效且易于使用的方法来实现此目标。Aspose.PSD for .NET为Image类公开了Resize方法，可用于动态调整现有图像的大小。Resize方法有两个重载，以满足应用程序的需求。
### **简单调整大小**
执行调整大小的步骤如下简单，


1. 使用Image类公开的工厂方法Load加载图像。
1. 调用Image.Resize方法，并指定新的高度和宽度。
1. 保存结果。

以下代码示例演示了如何调整图像大小。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **使用ResizeType枚举调整大小**
Aspose.PSD API公开了ResizeType枚举，可与Image.Resize一起使用以实现所需的结果。下面提供的代码段演示了ResizeType枚举的用法，而ResizeType枚举成员的详细信息可以在本页底部找到。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



如果希望在应用重新调整大小后获得高质量结果，则建议始终使用ResizeType.LanczosResample，因为它将输出高质量结果，但可能比ResizeType.NearestNeighbourResample慢。另一方面，ResizeType.NearestNeighbourResample算法专门用于快速调整大小，同时在图像质量上作出妥协。此方法可能适用于实时缩略图生成或类似流程中需要性能的场景。
## **等比例调整图像大小**
您可以通过将新的高度和宽度值作为参数传递给Image.Resize方法来调整图像大小，但在这种情况下，您必须自己计算纵横比。这是因为当改变图像的宽度或高度时，图像会被缩放或缩小以填充新尺寸。如果图像的宽度和高度的改变不成比例，这可能导致拉伸和畸变的结果。本文演示了使用Aspose.PSD for .NET API来调整图像大小的用法，其中可以传递新的高度或宽度，同时允许API自动计算其他比例值。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **ResizeType枚举**
ResizeType根据所选滤镜确定在图像上执行的调整大小的类型。

[ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)枚举的成员

|**成员名称**|**值**|**描述**|
| :- | :- | :- |
|LeftTopToLeftTop|0|新图像的左上点将与原始图像的左上点重合。如有必要，将裁剪。|
|RightTopToRightTop|1|新图像的右上点将与原始图像的右上点重合。如有必要，将裁剪。|
|RightBottomToRightBottom|2|新图像的右下点将与原始图像的右下点重合。如有必要，将裁剪。|
|LeftBottomToLeftBottom|3|新图像的左下点将与原始图像的左下点重合。如有必要，将裁剪。|
|CenterToCenter|4|新图像的中心将与原始图像的中心重合。如有必要，将裁剪。|
|LanczosResample|5|使用7x7掩模使用Lanczos算法重新采样。|
|NearestNeighbourResample|6|使用最近邻算法重新采样。|

---
title: 如何在Aspose.PSD中使用Warp
type: docs
weight: 40
url: /zh/net/how-to-use-warp-in-aspose-psd/
---

## **第1部分 - 使用Warp效果渲染PSD文件**

Photoshop在应用Warp效果后保存渲染图像。我们的库可以重现或重新渲染带有Warp效果的图像。要启用此功能，只需在打开PSD文件时将AllowWarpRepaint标志设置为true。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-1.cs" >}}

结果:
![Aspose.PSD for .NET Warp Result 1](warp1.png)

除了为SmartLayers渲染Warp效果外，我们的库还支持TextLayers的Warp效果。实现代码保持不变，唯一的区别在于文件名。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-2.cs" >}}

结果:
![Aspose.PSD for .NET Warp Result 2](warp2.png)

**! 注意: ** 目前，我们的库支持渲染自定义Warp*（用户操作网格点）和所有标准Warp类型。
* - 目前，我们的库支持带有标准网格的自定义Warp，并且我们正在积极扩展支持以包括未来所有网格类型。


## **第2部分 - 修改Warp效果**

我们的库允许您不仅进行渲染，还可以修改（添加）Warp效果。
这些修改通过**WarpParams**类的功能实现。

| **特征**    | **描述**                                                              | 
|:-------------|:-----------------------------------------------------------------------|
| Bounds       | 返回扭曲图像的边界。                                                   |
| MeshPoints   | 一个点数组，每个点表示扭曲网格的一个顶点。                           |
| Value        | 非自定义Warp效果的扭曲效果的值。                                       |
| WarpRotates  | 定义非自定义Warp效果方向的枚举。                                       |
| WarpStyles   | 定义Warp效果类型的枚举。                                               |

下面的代码示例演示了如何确定Smart Layer的Warp效果类型，并调整效果的类型和变形程度。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-3.cs" >}}

结果:
![Aspose.PSD for .NET Warp Result 3](warp3.png)

## **第3部分 - 添加Warp效果**

下面的代码示例演示了如何向Smart Layer添加标准的Warp效果。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-4.cs" >}}

结果:
![Aspose.PSD for .NET Warp Result 4](warp4.png)

下面的代码示例演示了如何向Smart Layer添加自定义Warp效果。
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

结果:
![Aspose.PSD for .NET Warp Result 5](warp5.png)

下面的代码示例演示了如何向Text Layer添加Warp效果。
**! 注意:** 根据Photoshop的标准，Text Layers的Warp效果通常限于标准类型。但是，我们的库支持使用两种类型的Warp效果。请注意，此类文件可能与Photoshop不完全兼容。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

结果:
![Aspose.PSD for .NET Warp Result 6](warp6.png)

我们不断完善和扩展我们的Warp效果的功能，重点是提高其速度、质量和支持的功能。请关注我们每月发布的最新动态。
您的Aspose.PSD团队

---
title: Aspose.PSD适配器.NET 24.4 - 发布说明
type: docs
weight: 100
url: /zh/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

本页面包含 [Aspose.PSD适配器.NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/) 的发布说明

{{% /alert %}}

| **关键**     | **摘要**                                    | **类别**     |
|:------------|:-------------------------------------------|:------------|
| PSDNET-1985 | 将Aspose.PSD.Adapters.Imaging初次发布至Nuget   | 功能增强    |


## **公共API更改**
# **新增API:**
- 无

# **移除API:**
- 无

## **使用示例:**

请查看 [Aspose.PSD.Adapters文档页面](/zh/psd/net/adapters)

**PSDNET-1985. 使用Aspose.PSD.Adapters的最完整示例**

{{< highlight csharp >}}
// 在初始化配置中添加适配器启用
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// 还可以额外启用导出器
Aspose.PSD.Adapters.Imaging.EnableExporters();

// 要使用适配器，您需要同时拥有Aspose.PSD和适配者的许可证
// 这是如何应用Aspose.PSD许可证
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// 这是应用Aspose.Imaging的适配者许可证的示例
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// 然后您可以运行任何适配器或PSD或Imaging库的代码

// 之后，所有这些文件都可以被Aspose.PSD打开，而无需任何额外的代码，只需使用
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // 执行此代码后，您将获得从WEBP创建的PSD文件，并且可以应用任何Aspose.PSD滤镜、图层和调整，包括扭曲转换
}

// 您还可以将适配器的导出适配者图像创建为PSD格式
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // 使用Aspose.Imaging API编辑带有Imaging特定特性的WEBP文件
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // 然后只需使用 ToPsdImage() 方法并像使用Photoshop一样编辑文件，包括图层、智能滤镜和智能对象。
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // 使用Aspose.PSD保存最终的PSD文件
        psdImage.Save("output.psd");
    }
}

// 如果您不需要使用适配器提供的加载器或导出器，只需将它们禁用
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}

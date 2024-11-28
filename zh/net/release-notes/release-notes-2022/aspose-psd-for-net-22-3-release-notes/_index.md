---
title: Aspose.PSD for .NET 22.3 - 发布说明
type: docs
weight: 100
url: /zh/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

本页面包含 [Aspose.PSD for .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明。

{{% /alert %}}

|**键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-210|为图层组添加属性 IsOpen|功能|
|PSDNET-643|带栅格图层蒙版的 PSD 图像在保存为 16 位 PSD 图像时丢失蒙版|错误|
|PSDNET-899|溶解混合模式不适用于带蒙版的文件夹|错误|
|PSDNET-1047|在通过 Aspose.PSD 21.11 保存后 Photoshop 无法打开特定文件|错误|
|PSDNET-1068|具有线性减淡（添加）混合模式的图层呈现不正确|错误|
|PSDNET-1069|加载后图案填充图层更新时引发异常|错误|


## **公共 API 更改**
# **新增的 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **移除的 API:**
- 无


## **使用示例:**

**PSDNET-210. 为图层组添加属性 IsOpen**

{{< highlight csharp >}}
// 在运行时读取和写入 IsOpen 属性的示例。
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. 带栅格图层蒙版的 PSD 图像在保存为 16 位 PSD 图像时丢失蒙版**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. 溶解混合模式不适用于带蒙版的文件夹**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. 在通过 Aspose.PSD 21.11 保存后 Photoshop 无法打开特定文件**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // 需要手动用 Photoshop 打开输出的 PSD。

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // 不会引发异常。
            }
{{< /highlight >}}

**PSDNET-1068. 具有线性减淡（添加）混合模式的图层呈现不正确**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. 加载后图案填充图层更新时引发异常**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}

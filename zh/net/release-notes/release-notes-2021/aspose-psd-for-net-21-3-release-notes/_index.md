---
title: Aspose.PSD为.NET 21.3版 - 发布说明
type: docs
weight: 100
url: /zh/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}}

本页包含[Aspose.PSD为.NET 21.3版](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明

{{% /alert %}}

|**主题**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-823|添加SectionDividerLayer以改善图层组的体验|增强功能|
|PSDNET-694|在读取PattResource时，宽度和高度被交换|错误|
|PSDNET-789|多个图层效果的混合不正确|错误|
|PSDNET-805|存在多个图层效果时，混合顺序和逻辑不正确|错误|
|PSDNET-842|描边效果属性未保存到PSD文件|错误|

## **公共API更改**
# **已添加的API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **已移除的API:**
- 无

## **使用示例:**

**PSDNET-694. 在读取PattResource时，宽度和高度被交换**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // 调用模式渲染

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. 多个图层效果的混合不正确**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // 寻找文本图层
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "最佳";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // 以这种方式保存已更改的PSD文件
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. 存在多个图层效果时，混合顺序和逻辑不正确**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // 以这种方式保存已更改的PSD文件
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. 添加SectionDividerLayer以改善图层组的体验**

{{< highlight csharp >}}
            // 以下代码演示SectionDividerLayer图层以及如何获取相关的LayerGroup。

            // 图层层次结构
            //    [0]: '</图层组>' Group 1的SectionDividerLayer
            //    [1]: '图层 1' 普通图层
            //    [2]: '</图层组>' Group 2的SectionDividerLayer
            //    [3]: '</图层组>' Group 3的SectionDividerLayer
            //    [4]: 'Group 3' GroupLayer
            //    [5]: 'Group 2' GroupLayer
            //    [6]: 'Group 1' GroupLayer

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "对象不相等。");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // 创建图层层次结构
                // 添加图层组 'Group 1'
                LayerGroup group1 = image.AddLayerGroup("Group 1", 0, true);
                // 添加普通图层
                Layer layer1 = new Layer();
                layer1.DisplayName = "图层 1";
                group1.AddLayer(layer1);
                // 添加图层组 'Group 2'
                LayerGroup group2 = group1.AddLayerGroup("Group 2", 1);
                // 添加图层组 'Group 3'
                LayerGroup group3 = group2.AddLayerGroup("Group 3", 0);

                // 获取SectionDividerLayer的实例
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // 使用SectionDividerLayer.GetRelatedLayerGroup()方法，获取相关的LayerGroup实例。
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // 同一个LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // 同一个LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // 同一个LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Group 1' 包含5个图层
            }
{{< /highlight >}}

**PSDNET-842. 描边效果属性未保存到PSD文件**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "对象不相等。");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // 不会抛出ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // 检查保存的值
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}

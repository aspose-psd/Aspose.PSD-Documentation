---
title: Aspose.PSD for .NET 21.1 - 发行说明
type: docs
weight: 120
url: /zh/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}}

本页面包含 [Aspose.PSD for .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明。

{{% /alert %}}

| **关键** | **摘要** | **类别** |
| :- | :- | :- |
| PSDNET-766 | Aspose.PSD 20.10: 尝试将特定 PSD 文件转换为 PNG 时出现异常 | 错误 |
| PSDNET-792 | 保存具有智能对象的 PSD 时出现异常 | 错误 |

## **公共 API 变更**
# **已添加的 API:**
- 无

# **已移除的 API:**
- 无

## **使用示例:**
**PSDNET-766. Aspose.PSD 20.10: 尝试将特定 PSD 文件转换为 PNG 时出现异常**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. 保存具有智能对象的 PSD 时出现异常**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // 查找智能对象
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // 我们正在从内存流中加载智能对象图层，
                        // 但我们可以使用 smart.ExportContents(somePath) 导出智能对象到文件
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // 查找文本图层
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // 我们可以使用简单的 UpdateText，但这种方式可以让我们分部编辑文本
                                        // 创建多行文本图层和其他文本和段落样式特性
                                        // 请小心。如果智能对象内容不是 PSD，您不能使用此文本编辑方式
                                        // 在这种情况下，您应该使用 Graphic API: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "最佳";

                                        // 如果要使图像看起来良好，您应该更改文本的大小。
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // 最好使用 ReplaceContents。它会自动重新渲染智能对象
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // 这样可以保存更改后的 PSD 文件
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

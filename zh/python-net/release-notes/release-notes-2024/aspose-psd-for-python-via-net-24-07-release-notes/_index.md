---
title: Aspose.PSD for Python via .NET 24.7 - 发行说明
type: docs
weight: 10
url: /zh/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

此页面包含[Aspose.PSD for Python via .NET 24.7](https://pypi.org/project/aspose-psd/)的发行说明。

{{% /alert %}}

| **关键**     | **摘要**                                                                                                           | **类别** |
|:------------|:-------------------------------------------------------------------------------------------------------------------|:---------|
| PSDPYTHON-86 | 打开 AI 文档时出现“图像加载失败。”异常                                                                  | 错误  |
| PSDPYTHON-87 | 输出 PDF 文件中的文本呈现不正确                                                                          | 错误  |
| PSDPYTHON-88 | 在 Linux 上为给定文件修复 ImageSaveException: 图像导出失败                             | 错误  |
| PSDPYTHON-89 | 使用 Aspose.Drawing 时修复字体加载                                                                  | 错误  |
| PSDPYTHON-90 | 使用大型 JPEG 创建智能对象图层时出现“算术运算导致溢出”                               | 错误  |
| PSDPYTHON-91 | AI 文件无法转换为 JPG 文件                                                                                | 错误  |

## **公共 API 更改**
# **已添加的 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **已移除的 API:**
- 无

## **用法示例:**

**PSDPYTHON-86. 打开 AI 文档时出现“图像加载失败。”异常**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. 输出 PDF 文件中的文本呈现不正确**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. 修复 ImageSaveException: 在 Linux 上为给定文件导出失败**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. 当使用 Aspose.Drawing 时修复字体加载**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- 更新前。已安装字体数: " + str(len(installedFonts.families)))
            print("- 通过尝试获取 'Arial' 的 Adobe 字体名称来刷新字体缓存：")
            FontSettings.get_adobe_font_name("Arial")
            print("- 更新后。已安装字体数: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 使用大型 JPEG 创建智能对象图层时出现“算术运算导致溢出”**
{{< highlight python >}}
        # 修复已完成，但是 Aspose.PSD for Python 中存在另一个问题，限制了此测试
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "测试图层"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. AI 文件无法转换为 JPG 文件**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

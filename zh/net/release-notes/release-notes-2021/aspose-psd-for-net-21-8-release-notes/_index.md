---
title: Aspose.PSD for .NET 21.8 - 更新说明
type: docs
weight: 50
url: /zh/net/aspose-psd-for-net-21-8-release-notes/
---

{{% alert color="primary" %}} 

此页面包含 [Aspose.PSD for .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/) 的更新说明。

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-698|支持使用 ZipWithPrediction 压缩方法|功能|
|PSDNET-663|生成的 PSD 中文本间距不正确|错误|
|PSDNET-685|保存 PSD 时出现异常|错误|
|PSDNET-927|在没有许可证的情况下使用 Aspose.PSD 时符号间和行间的距离不正确|错误|

## **公共 API 更改**
# **新增的 API:**
- 无

# **移除的 API:**
- 无

## **使用示例:**

**PSDNET-663. 生成的 PSD 中文本间距不正确**

{{< highlight csharp >}}
            string sourceFileName = "source.psd";
            string outputFileName = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. 保存 PSD 时出现异常**

{{< highlight csharp >}}
            string sourceFileName = "File.psd";
            string outputFileName = "File2.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                var layer1 = (TextLayer)image.Layers[1];
                layer1.TextData.UpdateLayerData();

                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-698. 支持使用 ZipWithPrediction 压缩方法**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";

            string outputPng = "output.png";
            string outputRaw = "out_Raw.psd";
            string outputZip = "out_Zip.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(outputPng, new PngOptions());

                image.Save(outputRaw, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                image.Save(outputZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. 在没有许可证的情况下使用 Aspose.PSD 时符号间和行间的距离不正确**

{{< highlight csharp >}}
            bool[] licenseStates = new bool[] { false, true };
            for (int i = 0; i < licenseStates.Length; i++)
            {
                bool testLicense = licenseStates[i];
                if (testLicense)
                {
                    License license = new License();
                    license.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string sourceFile = "psdnetTest927.psd";
                string outputFile = "out_" + testLicense.ToString() + "_psdnetTest927.png";

                using (var image = (PsdImage)Image.Load(sourceFile))
                {
                    image.Save(outputFile, new PngOptions());
                }
            }
{{< /highlight >}}

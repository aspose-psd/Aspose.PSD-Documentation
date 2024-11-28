---
title: Aspose.PSD for .NET 21.9 - 发行说明
type: docs
weight: 40
url: /zh/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

本页包含[Aspose.PSD for .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-574|使RLE压缩成为PSD保存的默认选项，以避免输出PSD过大|特性|
|PSDNET-747|支持PSD文件中的多通道颜色模式叠加图案图层效果|特性|
|PSDNET-951|在创建新图层后，其资源属性为空，阻止了操作（例如调整大小）|错误|
|PSDNET-955|不支持8位ZipWithPrediction压缩方法|错误|

## **公共 API 更改**
# **已添加的 API:**
- 无

# **已移除的 API:**
- 无

## **使用示例:**

**PSDNET-574. 使RLE压缩成为PSD保存的默认选项，以避免输出PSD过大**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. 支持PSD文件中的多通道颜色模式叠加图案图层效果**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // 不应抛出异常
            using (var im = Image.Load(fileName, loadOptions))
            {
                // 不应抛出异常
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. 在创建新图层后，其资源属性为空，阻止了操作（例如调整大小）**

{{< highlight csharp >}}
            string PSDFile = "Layer1.psd";
            string layer1File = "Layer2.png";
            string layer2File = "Layer3.png";
            string outFileName = "finaloutput.psd";

            void ReplaceColor(RasterImage image, Color oldColor, int diff, Color newColor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var length = pixels.Length;

                var oldR = oldColor.R;
                var oldG = oldColor.G;
                var oldB = oldColor.B;
                var newColorValue = newColor.ToArgb();

                for (int i = 0; i < length; i++)
                {
                    // 红色
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // 绿色
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // 蓝色
                    var b = (byte)(pixels[i] & 0xff);

                    int actualDiff = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (actualDiff <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Layer2 = null;
            Layer Layer3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region 添加图层 1

                using (var stream = new FileStream(layer1File, FileMode.Open))
                {
                    Layer2 = new Layer(stream);

                    Layer2.Resize(image.Width, image.Height);
                    var width = Layer2.Width;
                    var height = Layer2.Height;

                    Layer2.Left = 675;
                    Layer2.Top = 0;

                    Layer2.Right = Layer2.Left + width;
                    Layer2.Bottom = Layer2.Top + height;

                    image.AddLayer(Layer2);
                }

                #endregion

                using (var stream = new FileStream(layer2File, FileMode.Open))
                {
                    Layer3 = new Layer(stream);
                    // 用透明颜色替换白色
                    ReplaceColor(Layer3, Color.White, 256, Color.Transparent);
                    Layer2.DrawImage(new Point(0, 0), Layer3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. 不支持8位ZipWithPrediction压缩方法**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}

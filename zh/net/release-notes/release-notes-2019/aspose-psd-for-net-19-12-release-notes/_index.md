---
title: Aspose.PSD for .NET 19.12 - 发布说明
type: docs
weight: 10
url: /zh/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD for .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明。

{{% /alert %}}

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-11|支持链接图层|功能|
|PSDNET-131|支持 Soco 资源|功能|
|PSDNET-115|如果更新 TextLayer 的字符串，则向现有 LineBreaks 添加 LineBreaks|错误|
|PSDNET-157|将 PSB 另存为 PNG 会冻结|错误|
|PSDNET-250|在不带使用 RLE 压缩的层的 CMYK PSD 文件加载时出现异常|错误|
|PSDNET-161|更新文本图层时会出现异常|错误|
|PSDNET-222|调整一些带有图层蒙版的 PSD 文件存在问题|错误|
|PSDNET-244|保存带有某些 Globalization.CultureInfo.CurrentCulture 的 PSD 会导致加载异常|错误|

## **公共 API 更改**
# **新增的 API:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **已移除的 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **用法示例：**
**PSDNET-11. 支持链接图层**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("example.psd"))

            {

                Layer[] layers = psd.Layers;

                //将所有图层链接到一个链接组

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                //获取一个图层的ID

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId 与 linkGroupId 不相等。");

                }

                //通过链接组ID获取所有链接图层。

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                //从组中分离每个图层

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                //检索一个空链接组ID，该组中没有图层。

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("linkedLayers 字段不为空。");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. 支持 Soco 资源**

{{< highlight java >}}

      // 支持 Soco 资源

    string sourceFileName = "ColorFillLayer.psd";

    string exportPath = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        foreach (var layer in im.Layers)

        {

            if (layer is FillLayer)

            {

                var fillLayer = (FillLayer)layer;

                foreach (var resource in fillLayer.Resources)

                {

                    if (resource is SoCoResource)

                    {

                        var socoResource = (SoCoResource)resource;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), socoResource.Color);

                        socoResource.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            im.Save(exportPath);

        }

    }

{{< /highlight >}}

**PSDNET-115. 如果更新 TextLayer 的字符串，则向现有 LineBreaks 添加 LineBreaks**

{{< highlight java >}}

           const string NewText = "abcdef\rzxcvbn";

        string sourceFilePath = "TestFileForAsianChars.psd");

        string outputFilePath = "result.psd";

        using (var image = (PsdImage)Image.Load(sourceFilePath))

        {

            var layer = (TextLayer)image.Layers[0];

            var imageOptions = new PsdOptions(image);

            layer.UpdateText(NewText);

            image.Save(outputFilePath, imageOptions);

        }

        using (var createdImage = (PsdImage)Image.Load(outputFilePath))

        {

            var createdLayer = (TextLayer)createdImage.Layers[0];

            if (NewText != createdLayer.Text)

            {

                throw new InvalidDataException("更新的文本无效");

            }

        }

{{< /highlight >}}

**PSDNET-157. 将 PSB 另存为 PNG 会冻结**

{{< highlight java >}}

       // 将 PSB 另存为 PNG

    string sourceFileName = "sample.psb";

    string outFileName = "sample.png";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(outFileName, options);

    }

{{< /highlight >}}

**PSDNET-250. 在不带使用 RLE 压缩的层的 CMYK PSD 文件加载时出现异常**

{{< highlight java >}}

     void LoadRawDataFromPsd()

        {

            string sourcePath = "CmykWithAlpha.psd";

            using (RasterImage image = (RasterImage)Image.Load(sourcePath))

            {

                var rawDataSettings = image.RawDataSettings;

                RawDataTester loader = new RawDataTester();

                image.LoadRawData(image.Bounds, rawDataSettings, loader);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end)

            {

            }

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions)

            {

            }

        }

{{< /highlight >}}

**PSDNET-161. 更新文本图层时会出现异常**

{{< highlight java >}}

      // 将 PSD 文件作为图像加载并转换为 PsdImage

    using (PsdImage psdImage = (PsdImage)Image.Load("example.psd"))

    {

        foreach (var layer in psdImage.Layers)

        {

            if (layer is TextLayer)

            {

                TextLayer textLayer = layer as TextLayer;

                textLayer.UpdateText("test update", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        psdImage.Save("UpdateTextLayerInPSDFile_out.psd");

    }

{{< /highlight >}}

**PSDNET-222. 调整一些带有图层蒙版的 PSD 文件存在问题**

{{< highlight java >}}

     int scale = 2;

        string[] names = {

                             "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

                             "LevelsLayerWithLayerMaskRgb",

                             "LevelsLayerWithLayerMaskCmyk",

                             "ColorBalanceAdjustmentLayer"

                         };

        for (int i = 0; i < names.Length; i++)

        {

            string sourceFilePath = names[i] + ".psd";

            string outputFilePath = "output_" + sourceFilePath;

            string outputPngFilePath = "output_" + names[i] + ".png";

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, psdLoadOptions))

            {

                image.Resize(image.Width * scale, image.Height * scale);

                image.Save(outputFilePath, new PsdOptions());

                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}

**PSDNET-244. 保存带有某些 Globalization.CultureInfo.CurrentCulture 的 PSD 会导致加载异常**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string sourceFileName = string.Format("example-{0}.psd", i);

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            var psdSaveOptions = new PsdOptions();

            var culture = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            string outputFileName = "output-" + sourceFileName;

            // 将 PSD 文件作为图像加载并转换为 PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image.Resize(160, 120);

                image.Save(outputFileName, psdSaveOptions);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            // 将 PSD 文件作为图像加载并转换为 PsdImage

            using (PsdImage image2 = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image2.Resize(160, 120);

                image2.Save(outputFileName, psdSaveOptions);

            }

        }

{{< /highlight >}}

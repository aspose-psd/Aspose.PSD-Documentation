---
title: Aspose.PSD for .NET 19.8 - 发行说明
type: docs
weight: 50
url: /zh/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

此页面包含 Aspose.PSD for .NET 19.8 的发行说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-184|从流加载 JPEG、PNG 和其他图像文件到 PsdImage|功能|
|PSDNET-134|实现填充图层：渐变的渲染|功能|
|PSDNET-166|将 PSD 保存为 PDF 时不提供可选择的文本|功能|
|PSDNET-158|支持将 PSB 另存为 PDF|功能|
|PSDNET-189|在只读模式下加载 PSD 时内存使用较高|增强功能|
|PSDNET-171|创建新 TextLayer 后，PSD 文件对于 PS 变得无法读取|错误|
|PSDNET-156|加载 PSD 时出现异常|错误|

## **公共 API 变更**
# **已添加的 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **已移除的 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **使用示例:**
**PSDNET-184. 从流加载 JPEG、PNG 和其他图像文件到 PsdImage**

{{< highlight java >}}

    // load JPEG,PNG and other image files to PsdImage from stream

    string outputFilePath = "PsdResult.psd";

    var filesList = new string[]

    {

        "PsdExample.psd",

        "BmpExample.bmp",

        "GifExample.gif",

        "Jpeg2000Example.jpf",

        "JpegExample.jpg",

        "PngExample.png",

        "TiffExample.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. 实现填充图层：渐变的渲染**

{{< highlight java >}}

             // Implement rendering of Fill Layer: Gradient

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. 将 PSD 保存为 PDF 时不提供可选择的文本**

{{< highlight java >}}

  // Saving PSD into PDF does not provide selectable text

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. 创建新 TextLayer 后，PSD 文件对于 PS 变得无法读取**

{{< highlight java >}}

 // After the creation of new TextLayer on Build Server, PSD File became unreadable for PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Some text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. 加载 PSD 时出现异常**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. 在只读模式下加载 PSD 时内存使用较高**

{{< highlight java >}}

 // High memory usage of Aspose.PSD on loading of PSD with ReadOnly Mode

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // 此示例的内存使用量必须小于 100 MB

            if (memoryUsed > 100)

            {

                throw new Exception("内存使用过大");

            }

{{< /highlight >}}

**PSDNET-158. 支持将 PSB 另存为 PDF**

{{< highlight java >}}

 // Support saving PSB as PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

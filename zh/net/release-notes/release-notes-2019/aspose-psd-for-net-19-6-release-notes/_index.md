---
title: Aspose.PSD for .NET 19.6 - 发行说明
type: docs
weight: 70
url: /zh/net/aspose-psd-for-net-19-6-release-notes/
---

{{% alert color="primary" %}} 

此页面包含 [Aspose.PSD for .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-127|能够将 PSD 文件转换为 PSB 反之亦然|功能|
|PSDNET-154|将 Aspose.Imaging 19.5 源码移植到 Aspose.PSD 中|改进|
|PSDNET-155|清理与 Aspose.PSD 相关的公共 API|改进|
|PSDNET-159|移除属性 IsLicensed|改进|
|PSDNET-102|从 PSB 转换为 JPG 时挂起|错误|
|PSDNET-150|Photoshop 中编辑时新增的文本图层位置会发生偏移|错误|

## **公共 API 更改**
# **新增的 API:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- F:Aspose.PSD.FileFormat.Cdr
- F:Aspose.PSD.FileFormat.Cmx
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.PsbResourceSignature
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerLockType.LockAll
- P:Aspose.PSD.Image.BufferSizeHint
- P:Aspose.PSD.ImageOptions.JpegOptions.ResolutionUnit
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.TextRenderingHint
- M:Aspose.PSD.ImageOptions.VectorRasterizationOptions.CopyTo(Aspose.PSD.ImageOptions.VectorRasterizationOptions)
- P:Aspose.PSD.LoadOptions.BufferSizeHint
- T:Aspose.PSD.MemoryManagement.Configuration
- P:Aspose.PSD.MemoryManagement.Configuration.BufferSizeHint
- T:Aspose.PSD.ResolutionUnit
- F:Aspose.PSD.ResolutionUnit.None
- F:Aspose.PSD.ResolutionUnit.Inch
- F:Aspose.PSD.ResolutionUnit.Cm
# **已移除的 API:**
- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapHeight
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapPlanes
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitsPerPixel
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapCoreHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.Os22XBitmapHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.Os22XBitmapHeaderFullSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSize
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV2
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV3
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV4
- F:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapInfoHeaderSizeV5
- T:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapCompression
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapImageSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapXPelsPerMeter
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapYPelsPerMeter
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapColorsUsed
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.BitmapColorsImportant
- P:Aspose.PSD.FileFormats.Bmp.BitmapInfoHeader.ExtraBitMasks
- T:Aspose.PSD.FileFormats.Bmp.BitmapV4Header
- P:Aspose.PSD.FileFormats.Bmp.BitmapV4Header.RedMask
...

## **用法示例:**
**PSDNET-127. 能够将 PSD 文件转换为 PSB 反之亦然**

{{< highlight java >}}

 // 能够将 PSD 文件转换为 PSB 反之亦然

            string sourceFilePathPsb = "2layers.psb";

            string outputFilePathPsd = "ConvertFromPsb.psd";

            using (Image img = Image.Load(sourceFilePathPsb))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psd };

                img.Save(outputFilePathPsd, options);

            }

            string sourceFilePathPsd = "2layers.psd";

            string outputFilePathPsb = "ConvertFromPsd.psb";

            using (Image img = Image.Load(sourceFilePathPsd))

            {

                var options = new PsdOptions((PsdImage)img) { FileFormatVersion = FileFormatVersion.Psb };

                img.Save(outputFilePathPsb, options);

            }

{{< /highlight >}}

**PSDNET-102. 从 PSB 转换为 JPG 时挂起**

{{< highlight java >}}

  // 从 PSB 转换为 JPG 时挂起          

            string[] sourceFileNames = new string[] { 

                //Test files with layers

                "Little",

                "Simple",

                //Test files without layers

                "psb",

                "psb3"

            };

            var options = new PsdLoadOptions();

            foreach (var fileName in sourceFileNames)

            {

                var sourceFileName = fileName + ".psb";

                using (PsdImage image = (PsdImage)Image.Load(sourceFileName, options))

                {

                    // All jpeg and psd files must be readable

                    image.Save(fileName + "_output.jpg", new JpegOptions() { Quality = 95 });

                    image.Save(fileName + "_output.psb");

                }

            }             

{{< /highlight >}}

**PSDNET-150: Photoshop 中编辑时新增的文本图层位置会发生偏移**

{{< highlight java >}}

             // Photoshop 中编辑时新增的文本图层位置会发生偏移

    string sourceFileName = "OneLayer.psd";

    string exportPath = "OneLayer_Edited.psd";

    int leftPos = 99;

    int topPos = 47;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        im.AddTextLayer("Some text", new Rectangle(leftPos, topPos, 99, 47));

        TextLayer textLayer = (TextLayer)im.Layers[1];

        if (textLayer.Left != leftPos || textLayer.Top != topPos) 

        {

            throw new Exception("Was created incorrect Text Layer");

        }

        // We can't test Transform Matrix with a public API,

        // but if we start edit text layer in PSD we should get the same bounds as we created

        im.Save(exportPath);

    }

{{< /highlight >}}```json

```
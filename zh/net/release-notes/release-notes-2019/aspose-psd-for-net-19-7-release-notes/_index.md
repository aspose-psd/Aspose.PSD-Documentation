---
title: Aspose.PSD for .NET 19.7 - 发行说明
type: docs
weight: 60
url: /zh/net/aspose-psd-for-net-19-7-release-notes/
---

{{% alert color="primary" %}}

本页面包含[Aspose.PSD for .NET 19.7](https://www.nuget.org/packages/Aspose.PSD/)的发行说明

{{% /alert %}}

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-126|支持图层矢量蒙版处理|特性|
|PSDNET-130|为PSD文件实现正确的调整大小方法|特性|
|PSDNET-165|添加支持将PSD导出为PDF|特性|
|PSDNET-186|添加支持将AI格式（版本2和3）导出到其他格式|特性|

## **公共API更改**
# **已添加的API:**
- F:Aspose.PSD.FileFormat.Ai
- T:Aspose.PSD.FileFormats.Ai.AiDataSection
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Dispose
- T:Aspose.PSD.FileFormats.Ai.AiFinalizeSection
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- T:Aspose.PSD.FileFormats.Ai.AiFormatVersion
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.PsAdobe20
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.PsAdobe30
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf14
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf15
- T:Aspose.PSD.FileFormats.Ai.AiHeader
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Creator
- P:Aspose.PSD.FileFormats.Ai.AiHeader.For
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Title
- P:Aspose.PSD.FileFormats.Ai.AiHeader.CreationDate
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentProcessColors
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentProcSets
- P:Aspose.PSD.FileFormats.Ai.AiHeader.BoundingBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.ColorUsage
- P:Aspose.PSD.FileFormats.Ai.AiHeader.TemplateBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.TileBox
- P:Aspose.PSD.FileFormats.Ai.AiHeader.DocumentPreview
- P:Aspose.PSD.FileFormats.Ai.AiHeader.Item(System.String)
- T:Aspose.PSD.FileFormats.Ai.AiImage
- M:Aspose.PSD.FileFormats.Ai.AiImage.#ctor
- P:Aspose.PSD.FileFormats.Ai.AiImage.FileFormat
- P:Aspose.PSD.FileFormats.Ai.AiImage.Version
- P:Aspose.PSD.FileFormats.Ai.AiImage.Header
- P:Aspose.PSD.FileFormats.Ai.AiImage.SetupSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.FinalizeSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.DataSection
- P:Aspose.PSD.FileFormats.Ai.AiImage.IsCached
- P:Aspose.PSD.FileFormats.Ai.AiImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Ai.AiImage.Width
- P:Aspose.PSD.FileFormats.Ai.AiImage.Height
- M:Aspose.PSD.FileFormats.Ai.AiImage.CacheData
- M:Aspose.PSD.FileFormats.Ai.AiImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Ai.AiImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Ai.AiImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Ai.AiImage.SetPalette(Aspose.PSD.IColorPalette,System.Boolean)
- T:Aspose.PSD.FileFormats.Ai.AiSetupSection
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData
- P:Aspose.PSD.ImageOptions.PdfOptions.PageSize

# **已移除的API:**
- 无

## **使用示例:**
**PSDNET-126. 支持图层矢量蒙版处理**

{{< highlight java >}}

             string sourceFileName = "DifferentLayerMasks_Source.psd";

            string exportPath = "DifferentLayerMasks_Export.psd";

            string exportPathPng = "DifferentLayerMasks_Export.png";

            // 读取

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                // 对矢量路径点进行更改

                foreach (var layer in image.Layers)

                {

                    foreach (var layerResource in layer.Resources)

                    {

                        var resource = layerResource as VectorPathDataResource;

                        if (resource != null)

                        {

                            foreach (var pathRecord in resource.Paths)

                            {

                                var bezierKnotRecord = pathRecord as BezierKnotRecord;

                                if (bezierKnotRecord != null)

                                {

                                    Point p0 = bezierKnotRecord.Points[0];

                                    bezierKnotRecord.Points[0] = bezierKnotRecord.Points[2];

                                    bezierKnotRecord.Points[2] = p0;

                                    break;

                                }

                            }

                        }

                    }

                }

                // 导出

                image.Save(exportPath);

                image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-130. 为PSD文件实现正确的调整大小方法**

{{< highlight java >}}

              // 为PSD文件实现正确的调整大小方法

            string sourceFileName = "1.psd";

            string exportPathPsd = "ResizeTest.psd";

            string exportPathPng = "ResizeTest.png";

            using (RasterImage image = Image.Load(sourceFileName) as RasterImage)

            {

                image.Resize(160, 120);

                image.Save(exportPathPsd, new PsdOptions());

                image.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }           

{{< /highlight >}}

**PSDNET-165. 添加支持将PSD导出为PDF**

{{< highlight java >}}

   // 添加支持将PSD导出为PDF

    string[] sourcesFiles = new string[]

    {

        @"1.psd",

        @"little.psb",

        @"psb3.psb",

        @"inRgb16.psd",

        @"ALotOfElementTypes.psd",

        @"ColorOverlayAndShadowAndMask.psd",

        @"ThreeRegularLayersSemiTransparent.psd"

    };

    for (int i = 0; i < sourcesFiles.Length; i++)

    {

        string sourceFileName = sourcesFiles[i];

        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

        {

           string outFileName = "PsdToPdf" + i + ".pdf";

           image.Save(outFileName, new PdfOptions());

        }

    }

{{< /highlight >}}

**PSDNET-186. 添加支持将AI格式（版本2和3）导出到其他格式**

{{< highlight java >}}

 // 添加支持将AI格式（版本2和3）导出到其他格式

            string[] sourcesFiles = new string[]

            {

                @"34992OStroke",

                @"rect2_color",

            };

            for (int i = 0; i < sourcesFiles.Length; i++)

            {

                string name = sourcesFiles[i];

                string sourceFileName = @"testdata\Images\Ai\" + name + ".ai";

                ImageOptionsBase options;

                string outFileName;

                using (AiImage image = (AiImage)Image.Load(sourceFileName))

                {

                    outFileName = name + ".psd";

                    options = new PsdOptions();

                    image.Save(outFileName, options);

                    outFileName = name + ".png";

                    options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

                    image.Save(outFileName, options);

                    outFileName = name + ".jpg";

                    options = new JpegOptions() { Quality = 85 };

                    image.Save(outFileName, options);

                    outFileName = name + ".gif";

                    options = new GifOptions() { DoPaletteCorrection = false };

                    image.Save(outFileName, options);

                    outFileName = name + ".tif";

                    options = new TiffOptions(TiffExpectedFormat.TiffDeflateRgba);

                    image.Save(outFileName, options);

                    outFileName = name + ".psd";

                    options = new PsdOptions();

                    image.Save(outFileName, options);

                }

            }

{{< /highlight >}}

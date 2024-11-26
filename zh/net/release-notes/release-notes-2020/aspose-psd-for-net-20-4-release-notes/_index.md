---
title: Aspose.PSD for .NET 20.4 - 发行说明
type: docs
weight: 90
url: /zh/net/aspose-psd-for-net-20-4-release-notes/
---

{{% alert color="primary" %}} 

本页面包含了 [Aspose.PSD for .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-567|支持“矢量起源数据”资源|功能|
|PSDNET-373|支持 lclrResource（图层颜色设置）|功能|
|PSDNET-563|支持长度记录数据中的属性。（路径操作（布尔运算），图层中形状的索引，贝塞尔结记录数量）|功能|
|PSDNET-425|支持图像区域资源＃1010 背景颜色|功能|
|PSDNET-530|在运行时添加填充图层|功能|
|PSDNET-424|支持Image Section Resource＃1009边框信息|功能|
|PSDNET-592|支持AI格式文件中的图层|功能|
|PSDNET-256|支持渐变叠加图层效果的读取和编辑|功能|
|PSDNET-257|渐变叠加图层效果的呈现|功能|
|PSDNET-585|Photoshop 中未显示 GradientOverlayEffect.BlendMode 属性更改|错误|
|PSDNET-561|修复将灰度 ColorMode 和每通道 16 位保存为灰度 PSD 格式的 PSD 图像|错误|
|PSDNET-560|修复将灰度 ColorMode 和每通道 16 位保存为 PNG 格式的 PSD 图像|错误|

## **公共 API 更改**
# **新增的 API：**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **移除的 API：**
- 无

## **使用示例:**
**PSDNET-567.支持“矢量起源数据”资源**

{{< highlight java >}}

         // VogkResource 支持

        static void ExampleOfVogkResourceSupport()

        {

            string fileName = "VectorOriginationDataResource.psd";

            string outFileName = "out_VectorOriginationDataResource_.psd";

            using (var psdImage = (PsdImage)Image.Load(fileName))

            {

                var resource = GetVogkResource(psdImage);

                // 读取

                if (resource.ShapeOriginSettings.Length != 1 ||

                    !resource.ShapeOriginSettings[0].IsShapeInvalidated ||

                    resource.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource were read wrong.");

                }

                // 编辑

                resource.ShapeOriginSettings = new[]

                {

                    resource.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                psdImage.Save(outFileName);

            }

        }

        static VogkResource GetVogkResource(PsdImage image)

        {

            var layer = image.Layers[1];

            VogkResource resource = null;

            var resources = layer.Resources;

            for (int i = 0; i < resources.Length; i++)

            {

                if (resources[i] is VogkResource)

                {

                    resource = (VogkResource)resources[i];

                    break;

                }

            }

            if (resource == null)

            {

                throw new Exception("VogkResource未找到.");

            }

            return resource;

        }   

{{< /highlight >}}

**PSDNET-373. 支持 lclr 资源（表格颜色设置）**

{{< highlight java >}}

         static void CheckSheetColorsAndRerverse(SheetColorHighlightEnum[] sheetColors, PsdImage img)

        {

            int layersCount = img.Layers.Length;

            for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

            {

                Layer layer = img.Layers[layerIndex];

                LayerResource[] resources = layer.Resources;

                foreach (LayerResource layerResource in resources)

                {

                    // lclr 资源总是存在于 psd 文件资源列表中。

                    LclrResource resource = layerResource as LclrResource;

                    if (resource != null)

                    {

                        if (resource.Color != sheetColors[layerIndex])

                        {

                            throw new Exception("Sheet Color has been read wrong");

                        }

                        // 风格表格颜色的反转。设置图层颜色高亮。

                        resource.Color = sheetColors[layersCount - layerIndex - 1];

                        break;

                    }

                }

            }

        }

            string sourceFilePath = "AllLclrResourceColors.psd";

            string outputFilePath = "AllLclrResourceColorsReversed.psd";

            // 在文件中，图层高亮的颜色的顺序如下

            SheetColorHighlightEnum[] sheetColors = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Red,

                SheetColorHighlightEnum.Orange,

                SheetColorHighlightEnum.Yellow,

                SheetColorHighlightEnum.Green,

                SheetColorHighlightEnum.Blue,

                SheetColorHighlightEnum.Violet,

                SheetColorHighlightEnum.Gray,

                SheetColorHighlightEnum.NoColor

            };            

            // 图层表格颜色用于视觉突出显示图层。

            // 例如，您可以更新 PSD 中的一些图层，然后通过颜色将要引起注意的图层进行突出显示。

            using (PsdImage img = (PsdImage)Image.Load(sourceFilePath))

            {

                CheckSheetColorsAndRerverse(sheetColors, img);

                img.Save(outputFilePath, new PsdOptions());

            }

            using (PsdImage img = (PsdImage)Image.Load(outputFilePath))

            {

                // 颜色应该是颠倒的

                Array.Reverse(sheetColors);

                CheckSheetColorsAndRerverse(sheetColors, img);

            }

{{< /highlight >}}

**PSDNET-563. 支持从 LengthRecord 数据中的属性（路径操作（布尔操作），图层中形状的索引，贝塞尔结记录数）**

{{< highlight java >}}

            string fileName = "PathOperationsShape.psd";

            using (var im = (PsdImage)Image.Load(fileName))

            {

                VsmsResource resource = null;

                foreach (var layerResource in im.Layers[1].Resources)

                {

                    if (layerResource is VsmsResource)

                    {

                        resource = (VsmsResource)layerResource;

                        break;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)resource.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)resource.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)resource.Paths[11];

                // 这里我们更改了形状之间组合的方式。

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                im.Save("out_" + fileName);

            }

{{< /highlight >}}

**PSDNET-425. 支持图像区域资源＃1010 背景颜色**

{{< highlight java >}}

             string sourceFile = "input.psd";

            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                ResourceBlock[] imageResources = image.ImageResources;

                BackgroundColorResource backgroundColorResource = null;

                foreach (var imageResource in imageResources)

                {

                    if (imageResource is BackgroundColorResource)

                    {

                        backgroundColorResource = (BackgroundColorResource)imageResource;

                        break;

                    }

                }

                // 更新 BackgroundColorResource

                backgroundColorResource .Color = Color.DarkRed;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-530. 在运行时添加填充图层**

{{< highlight java >}}

             string outputPsd = "output.psd";

            using (var image = new PsdImage(100, 100))

            {

                FillLayer colorFillLayer = FillLayer.CreateInstance(FillType.Color);

                colorFillLayer.DisplayName = "Color Fill Layer";

                image.AddLayer(colorFillLayer);

                FillLayer gradientFillLayer = FillLayer.CreateInstance(FillType.Gradient);

                gradientFillLayer.DisplayName = "Gradient Fill Layer";

                image.AddLayer(gradientFillLayer);

                FillLayer patternFillLayer = FillLayer.CreateInstance(FillType.Pattern);

                patternFillLayer.DisplayName = "Pattern Fill Layer";

                patternFillLayer.Opacity = 50;

                image.AddLayer(patternFillLayer);

                image.Save(outputPsd);

            }

{{< /highlight >}}

**PSDNET-424. 支持图像区域资源＃1009 边框信息**

{{< highlight java >}}

             string sourceFile = "input.psd";

            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                ResourceBlock[] imageResources = image.ImageResources;

                BorderInformationResource borderInfoResource = null;

                foreach (var imageResource in imageResources)

                {

                    if (imageResource is BorderInformationResource)

                    {

                        borderInfoResource = (BorderInformationResource)imageResource;

                        break;

                    }

                }

                // 更新 BorderInformationResource

                borderInfoResource.Width = 0.1;

                borderInfoResource.Unit = PhysicalUnit.Inches;

                image.Save(outputFile);

            }

{{< /highlight >}}

**PSDNET-592. 支持 AI 格式文件中的图层**

{{< highlight java >}}

         void AssertIsTrue(bool condition, string message)

        {

            if (!condition)

            {

                throw new FormatException(message);

            }

        }

        string sourceFileName = "form_8_2l3_7.ai";

        string outputFileName = "form_8_2l3_7_export";

        using (AiImage image = (AiImage)Image.Load(sourceFileName))

        {

            AiLayerSection layer0 = image.Layers[0];

            AssertIsTrue(layer0 != null, "Layer 0 should be not null.");

            AssertIsTrue(layer0.Name == "Layer 4", "The Name property of the layer 0 should be Layer 4");

            AssertIsTrue(!layer0.IsTemplate, "The IsTemplate property of the layer 0 should be false.");

            AssertIsTrue(layer0.IsLocked, "The IsLocked property of the layer 0 should be true.");

            AssertIsTrue(layer0.IsShown, "The IsShown property of the layer 0 should be true.");

            AssertIsTrue(layer0.IsPrinted, "The IsPrinted property of the layer 0 should be true.");

            AssertIsTrue(!layer0.IsPreview, "The IsPreview property of the layer 0 should be false.");

            AssertIsTrue(layer0.IsImagesDimmed, "The IsImagesDimmed property of the layer 0 should be true.");

            AssertIsTrue(layer0.DimValue == 51, "The DimValue property of the layer 0 should be 51.");

            AssertIsTrue(layer0.ColorNumber == 0, "The ColorNumber property of the layer 0 should be 0.");

            AssertIsTrue(layer0.Red == 79, "The Red property of the layer 0 should be 79.");

            AssertIsTrue(layer0.Green == 128, "The Green property of the layer 0 should be 128.");

            AssertIsTrue(layer0.Blue == 255, "The Blue property of the layer 0 should be 255.");

            AssertIsTrue(layer0.RasterImages.Length == 0, "The pixels length property of the raster image in the layer 0 should equals 0.");

            AiLayerSection layer1 = image.Layers[1];

            AssertIsTrue(layer1 != null, "Layer 1 should be not null.");

            AssertIsTrue(layer1.Name == "Layer 1", "The Name property of the layer 1 should be Layer 1");

            AssertIsTrue(layer1.RasterImages.Length == 1, "The length property of the raster images in the layer 1 should equals 1.");

            AiRasterImageSection rasterImage = layer1.RasterImages[0];

            AssertIsTrue(rasterImage != null, "The raster image in the layer 1 should be not null.");

            AssertIsTrue(rasterImage.Pixels != null, "The pixels property of the raster image in the layer 1 should be not null.");

            AssertIsTrue(string.Empty == rasterImage.Name, "The Name property of the raster image in the layer 1 should be empty");

            AssertIsTrue(rasterImage.Pixels.Length == 100, "The pixels length property of the raster image in the layer 1 should equals 100.");

            image.Save(outputFileName + ".psd", new PsdOptions());

            image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

        }

{{< /highlight >}}

**PSDNET-256. 支持渐变叠加图层效果的读取和编辑**

{{< highlight java >}}

             // 创建/获取并编辑图层中
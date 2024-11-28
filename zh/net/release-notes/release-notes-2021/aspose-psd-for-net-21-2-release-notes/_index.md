---
title: Aspose.PSD for .NET 21.2 - 发布说明
type: docs
weight: 110
url: /zh/net/aspose-psd-for-net-21-2-release-notes/
---

{{% alert color="primary" %}} 

此页面包含 [Aspose.PSD for .NET 21.2](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-404|支持 vogkResource|功能|
|PSDNET-809|替换智能对象内容时，智能对象图层边界不正确，其内容与具有不同尺寸和分辨率的文件替换时|功能|
|PSDNET-752|无法将 FillLayer 转换为 SmartObjectLayer|错误|
|PSDNET-778|LayerGroup 添加新图层的顺序颠倒|错误|
|PSDNET-790|在 SmartObject 图层中导入图像会导致 PSD 损坏|错误|
|PSDNET-810|加载文件时出现异常|错误|
|PSDNET-824|加载和保存具有形状图层和矢量路径的 PSD 图像后，加载错误的 vogk 资源|错误|
|PSDNET-827|加载 ReferenceStructure 和 EnumeratedReferenceStructure 结构时出现异常|错误|

## **公共 API 更改**
# **已添加的 API：**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginType
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginResolution
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginShapeBox
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginRadiiRectangle
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidatedPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginIndexPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginTypePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginResolutionPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginRadiiRectanglePresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginShapeBBoxPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Left
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Top
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Right
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bottom
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.QuadVersion
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.Bounds
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.TopRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomRight
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.BottomLeft
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeRadiiRectangle.QuadVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.String,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(Aspose.PSD.Image,Aspose.PSD.ResolutionSetting)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(System.String,Aspose.PSD.ResolutionSetting)

# **已删除的 API：**
- 无

## **使用示例:**

**PSDNET-404. 支持 vogkResource**

{{< highlight csharp >}}
            // 此示例演示了加载和保存具有形状图层和矢量路径的 PSD 图像的工作方式。
            string dataDir = "PSDNET404_1";
            string sourcePath = Path.Combine(dataDir, "vectorShapes.psd");
            string outputFilePath = Path.Combine(dataDir, "output_vectorShapes.psd");
            using (PsdImage image = (PsdImage)Image.Load(sourcePath))
            {
                var resource = GetVogkResource(image);
                AssertAreEqual(1, resource.ShapeOriginSettings.Length);
                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, setting.OriginIndex);
                var originalSetting = resource.ShapeOriginSettings[0];
                originalSetting.IsShapeInvalidated = true;
                resource.ShapeOriginSettings = new[]
                {
                    originalSetting,
                    new VectorShapeOriginSettings()
                    {
                        OriginIndex = 1,
                        OriginResolution = 144,
                        OriginType = 4,
                        OriginShapeBox = new VectorShapeBoundingBox()
                        {
                            Bounds = Rectangle.FromLeftTopRightBottom(10, 15, 40, 70)
                        }
                    },
                    new VectorShapeOriginSettings()
                    {
                        OriginIndex = 2,
                        OriginResolution = 301,
                        OriginType = 5,
                        OriginRadiiRectangle = new VectorShapeRadiiRectangle()
                        {
                            TopLeft = 2,
                            TopRight = 6,
                            BottomLeft = 23,
                            BottomRight = 42,
                            QuadVersion = 1
                        }
                    }
                };

                image.Save(outputFilePath, new PsdOptions());
            }

            using (PsdImage image = (PsdImage)Image.Load(outputFilePath))
            {
                var resource = GetVogkResource(image);
                AssertAreEqual(3, resource.ShapeOriginSettings.Length);

                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(true, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, setting.OriginIndex);
                AssertAreEqual(true, setting.IsShapeInvalidated);

                setting = resource.ShapeOriginSettings[1];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(1, setting.OriginIndex);
                AssertAreEqual(144.0, setting.OriginResolution);
                AssertAreEqual(4, setting.OriginType);
                AssertAreEqual(Rectangle.FromLeftTopRightBottom(10, 15, 40, 70), setting.OriginShapeBox.Bounds);

                setting = resource.ShapeOriginSettings[2];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(false, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(true, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(2, setting.OriginIndex);
                AssertAreEqual(301.0, setting.OriginResolution);
                AssertAreEqual(5, setting.OriginType);
                AssertAreEqual(2.0, setting.OriginRadiiRectangle.TopLeft);
                AssertAreEqual(6.0, setting.OriginRadiiRectangle.TopRight);
                AssertAreEqual(23.0, setting.OriginRadiiRectangle.BottomLeft);
                AssertAreEqual(42.0, setting.OriginRadiiRectangle.BottomRight);
                AssertAreEqual(1, setting.OriginRadiiRectangle.QuadVersion);
            }

            VogkResource GetVogkResource(PsdImage image)
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
                    throw new Exception("未找到 VogkResource。");
                }

                return resource;
            }

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "对象不相等。");
                }
            }
{{< /highlight >}}

**PSDNET-752. 错误：无法将 FillLayer 转换为 SmartObjectLayer**

{{< highlight csharp >}}
            string sourceFilePath = "effectlost.psd";
            string outputFilePath = "output.psd";

            using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFilePath))
            {
                SmartObjectLayer smartObject = psdImage.SmartObjectProvider.ConvertToSmartObject(0);

                psdImage.Save(outputFilePath);
            }
{{< /highlight >}}

**PSDNET-778. LayerGroup 添加新图层的顺序颠倒**

{{< highlight csharp >}}
            void AreEqual(string expected, string actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("值不相等。");
                }
            }

            string outputFile = "output.psd";

            PsdOptions psdOptions = new PsdOptions();
            psdOptions.Source = new StreamSource(new MemoryStream());
            using (PsdImage psdImage = (PsdImage)Image.Create(psdOptions, 100, 100))
            {
                LayerGroup layerGroup = psdImage.AddLayerGroup("Folder", 0, true);
                layerGroup.AddLayer(new Layer() { DisplayName = "Layer 1" });
                layerGroup.AddLayer(new Layer() { DisplayName = "Layer 2" });

                AreEqual("Layer 1", layerGroup.Layers[0].DisplayName);
                AreEqual("Layer 2", layerGroup.Layers[1].DisplayName);

                psdImage.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-790. 在 SmartObject 图层中导入图像会导致 PSD 损坏**

{{< highlight csharp >}}
            const string baseFolder = "PSDNET790_1\\";
            const string outputFolder = baseFolder + "output\\";

            // 测试从图像导入的图层是否转换为智能对象图层，并保存的 PSD 文件是正确的。
            using (PsdImage image = (PsdImage)Image.Load(baseFolder + @"layerTest1.psd"))
            {

                string layerFilePath = baseFolder + @"picture.jpg";
                string outputFilePath = outputFolder + "layerTest2.psd";
                string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
                using (var stream = new FileStream(layerFilePath, FileMode.Open))
                {
                    Layer layer = null;
                    try
                    {
                        layer = new Layer(stream);
                        image.AddLayer(layer);
                    }
                    catch (Exception)
                    {
                        if (layer != null)
                        {
                            layer.Dispose();
                        }

                        throw;
                    }

                    var layer2 = image.Layers[2];
                    var layer3 = image.SmartObjectProvider.ConvertToSmartObject(image.Layers.Length - 1);
                    var bounds = layer3.Bounds;
                    layer3.Left = (image.Width - layer3.Width) / 2;
                    layer3.Top = layer2.Top;
                    layer3.Right = layer3.Left + bounds.Width;
                    layer3.Bottom = layer3.Top + bounds.Height;

                    image.Save(outputFilePath);
                    image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}

**PSDNET-809. 替换智能对象内容时，智能对象图层边界不正确，其内容与具有不同尺寸和分辨率的文件替换时**

{{< highlight csharp >}}
            // 此示例演示了在新内容文件具有不同分辨率时，ReplaceContents 方法的正确工作方式。
            const string baseFolder = "PSDNET809_1\\";
            const string outputFolder = baseFolder + "output\\";
            const string fileName = "CommonPsb.psd";
            const string filePath = baseFolder + fileName; // 原始 PSD 图像
            const string newContentPath = baseFolder + "image.jpg"; // 智能对象的新内容文件
            const string outputFilePath = outputFolder + "ChangedPsd";
            const string pngOutputPath = outputFilePath + ".png"; // 输出的 PNG 文件
            const string psdOutputPath = outputFilePath + ".psd"; // 输出的 PSD 文件
            using (PsdImage psd = (PsdImage)Image.Load(filePath))
            {
                for (int i = 0; i < psd.Layers.Length; i++)
                {
                    var layer = psd.Layers[i];
                    SmartObjectLayer smartObjectLayer = layer as SmartObjectLayer;
                    if (smartObjectLayer != null)
                    {
                        smartObjectLayer.ReplaceContents(newContentPath);

                        psd.Save(psdOutputPath);
                        psd.Save(pngOutputPath, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
                    }
                }
            }
{{< /highlight >}}

**PSDNET-810. 加载文件时出现异常**

{{< highlight csharp >}}
            string testFile1 = "face.psd";
            string testFile2 = "BigFile2.psd";

            using (var psdImage = (PsdImage)Image.Load(testFile1))
            {
                // 文件成功加载
            }

            using (var psdImage = (PsdImage)Image.Load(testFile2))
            {
                // 文件成功加载
            }
{{< /highlight >}}

**PSDNET-824. 加载和保存具有形状图层和矢量路径的 PSD 图像后，加载错误的 vogk 资源**

{{< highlight csharp >}}
            // 此示例演示了加载和保存具有形状图层和矢量路径的 PSD 图像后，加载错误的 vogk 资源的正确工作方式，以及保留 Live Shape Properties。
            string dataDir = "PSDNET824_1\\";
            string srcFile = dataDir + "vectorShapes.psd";
            string outputFilePath = dataDir + "\\output\\vectorShapes.psd";
            using (PsdImage psd = (PsdImage)Image.Load(srcFile))
            {
                psd.Save(outputFilePath);
            }

            // 检查 Adobe® Photoshop® 中输出的 PSD 文件中是否存在 Live Shape Properties。
{{< /highlight >}}

**PSDNET-827. 加载 ReferenceStructure 和 EnumeratedReferenceStructure 结构时出现异常**

{{< highlight csharp >}}
            string srcFile = "sourceFile.psd";
            string output = "output.psd";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                // 文件成功加载

                SmartObjectLayer layer = (SmartObjectLayer)psdImage.Layers[1];
                SoLdResource resource = (SoLdResource)layer.Resources[9];

                DescriptorStructure struct1 = (DescriptorStructure)resource.Items[15];
                ListStructure struct2 = (ListStructure)struct1.Structures[5];
                DescriptorStructure struct3 = (DescriptorStructure)struct2.Types[1];
                DescriptorStructure struct4 = (DescriptorStructure)struct3.Structures[6];
                ListStructure struct5 = (ListStructure)struct4.Structures[1];
                DescriptorStructure struct6 = (DescriptorStructure)struct5.Types[0];

                // 加载 ReferenceStructure 和 EnumeratedReferenceStructure
                ReferenceStructure referenceStruct = (ReferenceStructure)struct6.Structures[0];
                EnumeratedReferenceStructure enumRefStruct = (EnumeratedReferenceStructure)referenceStruct.Items[0];

                // 成功加载 ReferenceStructure 和 EnumeratedReferenceStructure

                psdImage.Save(output);
            }
{{< /highlight >}}
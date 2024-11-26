---
title: Aspose.PSD for .NET 21.4 - 发行说明
type: docs
weight: 90
url: /zh/net/aspose-psd-for-net-21-4-release-notes/
---

{{% alert color="primary" %}} 

该页面包含了 [Aspose.PSD for .NET 21.4](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}} 

|**关键字**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-259|图案叠加图层效果的渲染|功能|
|PSDNET-861|添加未知的Vogk资源属性以支持在PSD图像中大小调整带有矢量路径的形状图层|功能|
|PSDNET-90|未能正确将PSD转换为PDF|错误|
|PSDNET-830|保存特定PSD文件带有文本图层时出现异常|错误（此前已修复）

## **公共 API 更改**
# **已添加 API:**
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginBoxCorners
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.Transform
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginBoxCornersPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsTransformPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Xx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Xy
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Yx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Yy
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Tx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Ty

# **已移除 API:**
- 无

## **使用示例:**

**PSDNET-90. 未能正确将PSD转换为PDF**

{{< highlight csharp >}}
            string srcFile = "psd_magical.psd";
            string outputJpg = "output.jpg";
            string outputPdf = "output.pdf";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                JpegOptions jpgOptions = new JpegOptions();
                PdfOptions pdfOptions = new PdfOptions();

                psdImage.Save(outputJpg, jpgOptions);
                psdImage.Save(outputPdf, pdfOptions);
            }
{{< /highlight >}}

**PSDNET-259. 图案叠加层效果的渲染**

{{< highlight csharp >}}
            string sourceFile = "imageWithPattern.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-861. 添加未知的Vogk资源属性以支持在PSD图像中大小调整带有矢量路径的形状图层**

{{< highlight csharp >}}
            // 本示例展示如何获取和设置PSD文件中FillLayer的Vogk资源的ShapeOriginSettings的新Transform和OriginBoxCorners属性
            string sourceFileName = Path.Combine("PSDNET861_1", "vectorShape_25_50.psd");
            string outputPath = Path.Combine("PSDNET861_1", "result.psd");

            VectorShapeOriginSettings originalSetting;
            const int layerIndex = 0;

            // 加载原始图像
            using (PsdImage image = (PsdImage)Image.Load(sourceFileName)) 
            {
                AssertIsTrue(layerIndex < image.Layers.Length);
                var layer = image.Layers[layerIndex];
                AssertIsTrue(layer is FillLayer);
                var resource = GetVogkResource((FillLayer)layer);
                AssertAreEqual(1, resource.ShapeOriginSettings.Length);

                // 读取后断言
                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(0, setting.OriginIndex);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(5, setting.OriginType);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(Rectangle.FromLeftTopRightBottom(3, 7, 10, 22), setting.OriginShapeBox.Bounds);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(300d, setting.OriginResolution);

                // 断言新属性
                AssertAreEqual(true, setting.IsTransformPresent);
                AssertAreEqual(0d, setting.Transform.Tx);
                AssertAreEqual(0d, setting.Transform.Ty);
                AssertAreEqual(0.050000000000000003d, setting.Transform.Xx);
                AssertAreEqual(0d, setting.Transform.Yx);
                AssertAreEqual(0d, setting.Transform.Xy);
                AssertAreEqual(0.1d, setting.Transform.Yy);
                AssertAreEqual(true, setting.IsOriginBoxCornersPresent);
                AssertAreEqual(2.9000000000000004d, setting.OriginBoxCorners[0]);
                AssertAreEqual(7.3000000000000007d, setting.OriginBoxCorners[1]);
                AssertAreEqual(10.450000000000001d, setting.OriginBoxCorners[2]);
                AssertAreEqual(7.3000000000000007d, setting.OriginBoxCorners[3]);
                AssertAreEqual(10.450000000000001d, setting.OriginBoxCorners[4]);
                AssertAreEqual(22.400000000000002d, setting.OriginBoxCorners[5]);
                AssertAreEqual(2.9000000000000004d, setting.OriginBoxCorners[6]);
                AssertAreEqual(22.400000000000002d, setting.OriginBoxCorners[7]);

                // 设置新属性
                originalSetting = resource.ShapeOriginSettings[0];
                originalSetting.Transform.Tx = 0.2d;
                originalSetting.Transform.Ty = 0.3d;
                originalSetting.Transform.Xx = 0.4d;
                originalSetting.Transform.Xy = 0.5d;
                originalSetting.Transform.Yx = 0.6d;
                originalSetting.Transform.Yy = 0.7d;
                originalSetting.OriginBoxCorners = new double[8] { 9, 8, 7, 6, 5, 4, 3, 2 };

                // 保存具有更改属性的PSD图像
                image.Save(outputPath, new PsdOptions(image));
            }

            // 使用具有更改属性的已保存PSD图像
            using (PsdImage image = (PsdImage)Image.Load(outputPath))
            {
                var layer = image.Layers[layerIndex];
                AssertIsTrue(layer is FillLayer);
                var resource = GetVogkResource((FillLayer)layer);
                AssertAreEqual(1, resource.ShapeOriginSettings.Length);

                // 断言属性已正确保存和加载
                var setting = resource.ShapeOriginSettings[0];
                AssertAreEqual(true, setting.IsOriginIndexPresent);
                AssertAreEqual(false, setting.IsShapeInvalidatedPresent);
                AssertAreEqual(true, setting.IsOriginResolutionPresent);
                AssertAreEqual(true, setting.IsOriginTypePresent);
                AssertAreEqual(true, setting.IsOriginShapeBBoxPresent);
                AssertAreEqual(false, setting.IsOriginRadiiRectanglePresent);
                AssertAreEqual(0, setting.OriginIndex);
                AssertAreEqual(true, setting.IsTransformPresent);
                AssertAreEqual(0.2d, setting.Transform.Tx);
                AssertAreEqual(0.3d, setting.Transform.Ty);
                AssertAreEqual(0.4d, setting.Transform.Xx);
                AssertAreEqual(0.5d, setting.Transform.Xy);
                AssertAreEqual(0.6d, setting.Transform.Yx);
                AssertAreEqual(0.7d, setting.Transform.Yy);
                AssertAreEqual(true, setting.IsOriginBoxCornersPresent);
                AssertAreEqual(originalSetting.OriginBoxCorners[0], setting.OriginBoxCorners[0]);
                AssertAreEqual(originalSetting.OriginBoxCorners[1], setting.OriginBoxCorners[1]);
                AssertAreEqual(originalSetting.OriginBoxCorners[2], setting.OriginBoxCorners[2]);
                AssertAreEqual(originalSetting.OriginBoxCorners[3], setting.OriginBoxCorners[3]);
                AssertAreEqual(originalSetting.OriginBoxCorners[4], setting.OriginBoxCorners[4]);
                AssertAreEqual(originalSetting.OriginBoxCorners[5], setting.OriginBoxCorners[5]);
                AssertAreEqual(originalSetting.OriginBoxCorners[6], setting.OriginBoxCorners[6]);
                AssertAreEqual(originalSetting.OriginBoxCorners[7], setting.OriginBoxCorners[7]);
            }

            VogkResource GetVogkResource(FillLayer layer)
            {
                if (layer == null)
                {
                    throw new PsdImageArgumentException("参数 layer 不应为空.");
                }

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
                    throw new PsdImageException("未找到 VogkResource.");
                }

                return resource;
            }

            void AssertIsTrue(bool condition)
            {
                if (!condition)
                {
                    throw new FormatException(string.Format("预期为 true"));
                }
            }

            void AssertAreEqual(object actual, object expected)
            {
                if (!object.Equals(actual, expected))
                {
                    throw new FormatException(string.Format("实际值 {0} 与预期值 {1} 不相等.", actual, expected));
                }
            }
{{< /highlight >}}
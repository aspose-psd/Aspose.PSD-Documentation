---
title: Aspose.PSD cho .NET 22.1 - Ghi chú phát hành
type: docs
weight: 120
url: /vi/net/aspose-psd-cho-net-22-1-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 22.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-1017|PatternOverlay chỉ có thể được áp dụng một lần|Lỗi|
|PSDNET-1056|Tập tin tạm tràn khi mở một tập tin từ luồng|Lỗi|
|PSDNET-991|Tối ưu hóa vẽ cho bộ lọc thông minh Gaussian blur|Tính năng|
|PSDNET-1044|Hỗ trợ nhiều dữ liệu mẫu tại PattResource|Tính năng|


## **Thay Đổi API Công Khai**
# **API Thêm Mới:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Patterns
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey2
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey3
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.ImageMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Height
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Save(Aspose.PSD.StreamContainer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.SetPattern(System.Int32[],Aspose.PSD.Rectangle)


# **API Loại Bỏ:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)


## **Ví dụ về Sử dụng:**
**PSDNET-1017. PatternOverlay chỉ có thể được áp dụng một lần**
{{< highlight csharp >}}
            string outputPsd = "output_1017.psd";
            string outputPng = "output_1017.png";

            using (var psdImage = (PsdImage)Image.Create(new PsdOptions() { Source = new StreamSource(new MemoryStream()), }, 500, 500))
            {
                FillLayer layer = FillLayer.CreateInstance(FillType.Color);
                psdImage.AddLayer(layer);
                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(layer);
                vectorPath.FillColor = Color.Yellow;
                PathShape shape2 = new PathShape();
                shape2.Points.Add(new BezierKnot(new PointF(300, 150), true));
                shape2.Points.Add(new BezierKnot(new PointF(350, 200), true));
                shape2.Points.Add(new BezierKnot(new PointF(250, 200), true));
                shape2.IsClosed = false;
                vectorPath.Shapes.Add(shape2);

                VectorDataProvider.UpdateLayerFromVectorPath(layer, vectorPath, true);

                PatternOverlayEffect patternOverlay = layer.BlendingOptions.AddPatternOverlay();
                var newPattern = new int[]
                                        {
                                Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(),
                                Color.Aqua.ToArgb(), Color.Aqua.ToArgb(), Color.White.ToArgb(),
                                Color.White.ToArgb(), Color.Aqua.ToArgb(),
                                        };

                var newPatternBounds = new Rectangle(0, 0, 4, 2);
                patternOverlay.Settings.PatternData = newPattern;
                patternOverlay.Settings.PatternWidth = newPatternBounds.Width;
                patternOverlay.Settings.PatternHeight = newPatternBounds.Height;
                patternOverlay.Settings.HorizontalOffset = newPatternBounds.X;
                patternOverlay.Settings.VerticalOffset = newPatternBounds.Y;

                layer.Update();

                var layer2 = FillLayer.CreateInstance(FillType.Color);
                psdImage.AddLayer(layer2);
                VectorPath vectorPath2 = VectorDataProvider.CreateVectorPathForLayer(layer2);
                vectorPath2.FillColor = Color.Blue;
                PathShape shape3 = new PathShape();
                shape3.Points.Add(new BezierKnot(new PointF(400, 450), true));
                shape3.Points.Add(new BezierKnot(new PointF(100, 400), true));
                shape3.Points.Add(new BezierKnot(new PointF(250, 100), true));
                shape3.IsClosed = false;
                vectorPath2.Shapes.Add(shape3);

                VectorDataProvider.UpdateLayerFromVectorPath(layer2, vectorPath2, true);

                PatternOverlayEffect patternOverlay2 = layer2.BlendingOptions.AddPatternOverlay();
                var newPattern2 = new int[]
                                        {
                                Color.Green.ToArgb(), Color.Purple.ToArgb(), Color.Purple.ToArgb(),
                                Color.Green.ToArgb(), Color.Green.ToArgb(), Color.Black.ToArgb(),
                                Color.Black.ToArgb(), Color.Green.ToArgb(),
                                        };

                var newPatternBounds2 = new Rectangle(0, 0, 4, 2);
                patternOverlay2.Settings.PatternData = newPattern2;
                patternOverlay2.Settings.PatternWidth = newPatternBounds2.Width;
                patternOverlay2.Settings.PatternHeight = newPatternBounds2.Height;
                patternOverlay2.Settings.HorizontalOffset = newPatternBounds2.X;
                patternOverlay2.Settings.VerticalOffset = newPatternBounds2.Y;

                psdImage.Save(outputPsd);
                psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
{{< /highlight >}}

**PSDNET-1056. Tập tin tạm tràn khi mở một tập tin từ luồng**
{{< highlight csharp >}}

            using (var memStream = new MemoryStream())
            {
                byte[] fileBytes = new byte[3];
                memStream.Write(fileBytes, 0, fileBytes.Length);

                // kiểm tra hành vi
                Exception exception = null;
                try
                {
                    using (var image = Image.Load(memStream))
                    {
                    }
                }
                catch (CoreExceptions.ImageLoadException mainEx)
                {
                    // tìm kiếm ngoại lệ cấp thấp nhất
                    exception = mainEx;
                    while (exception.InnerException != null)
                    {
                        exception = exception.InnerException;
                    }
                }

                // kiểm tra ngoại lệ
                string typeName = exception.GetType().Name; // cho mục đích debug
                if (exception is CoreExceptions.ImageLoadException)
                {
                    // OK
                }
                else
                {
                    // Không ổn
                    throw exception;
                }
            }
{{< /highlight >}}

**PSDNET-991. Tối ưu hóa vẽ cho bộ lọc thông minh Gaussian blur**
{{< highlight csharp >}}
          string sourceFilte = "psdnet991_layers.psd";
            string outputPsd = "out_psdnet991_layers.psd";
            string outputPng = "out_psdnet991_layers.png";

            using (var image = (PsdImage)Image.Load(sourceFilte))
            {
                SmartObjectLayer smartLayer = (SmartObjectLayer)image.Layers[1];
                Layer maskLayer = image.Layers[2];
                Layer regularLayer = image.Layers[3];

                GaussianBlurSmartFilter gaussianBlur = new GaussianBlurSmartFilter();
                gaussianBlur.Radius = 10;

                // Áp dụng bộ lọc vào SmartObject
                gaussianBlur.Apply(smartLayer);
                smartLayer.SmartFilters.UpdateResourceValues();
                smartLayer.UpdateModifiedContent();

                // Áp dụng bộ lọc vào layer mask
                gaussianBlur.ApplyToMask(maskLayer);

                //Áp dụng bộ lọc vào layer
                gaussianBlur.Apply(regularLayer);

                image.Save(outputPsd);
                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-1044. Hỗ trợ nhiều dữ liệu mẫu tại PattResource**
{{< highlight csharp >}}
            string src = "psdnet1044.psd";
            string output = "out_psdnet1044.psd";

            using (var image = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                PattResource pattResource = (PattResource)image.GlobalLayerResources[0];

                if (pattResource.Patterns.Length == 2)
                {
                    Console.WriteLine("Đọc chính xác các mục PattResourceData.");
                }

                var fillLayer = FillLayer.CreateInstance(FillType.Color);
                image.AddLayer(fillLayer);

                IPatternFillSettings pattSetting = fillLayer.BlendingOptions.AddPatternOverlay().Settings;

                pattSetting.PatternWidth = 3;
                pattSetting.PatternHeight = 3;
                pattSetting.PatternData = new int[]
                {
                    Color.White.ToArgb(), Color.White.ToArgb(), Color.Red.ToArgb(),
                    Color.White.ToArgb(), Color.Green.ToArgb(), Color.White.ToArgb(),
                    Color.Blue.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(),
                };

                image.Save(output);
            }
{{< /highlight >}}
---
title: Aspose.PSD cho .NET 19.10 - Ghi chú phiên bản
type: docs
weight: 30
url: /vi/net/aspose-psd-cho-net-19-10-ghi-chu-phien-ban/
---

{{% alert color="primary" %}}

Trang này chứa ghi chú cho phiên bản Aspose.PSD cho .NET 19.10

{{% /alert %}}

| **Khóa** | **Tóm tắt** | **Danh mục** |
| :- | :- | :- |
| PSDNET-207 | [Hỗ trợ Layer Điều chỉnh Cân Bằng Màu](/psd/vi/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer) | Tính năng |
| PSDNET-145 | [Hỗ trợ Layer Điều chỉnh Đảo Ngược](/psd/vi/net/modifying-images/#modifyingimages-invertadjustmentlayer) | Tính năng |
| PSDNET-139 | [Triển khai Bộ lọc Bicubic](/psd/vi/net/modifying-images/#modifyingimages-implementbicubicresampling) | Tính năng |
| PSDNET-169 | [Thêm hỗ trợ xuất PSD sang PDF với Clipping Mask](/psd/vi/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask) | Tính năng |
| PSDNET-168 | [Thêm hỗ trợ xuất PSD sang PDF với Adjustment Layers](/psd/vi/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer) | Tính năng |
| PSDNET-179 | Vấn đề lấy Layer DropShadowEffect | Cải tiến |
| PSDNET-203 | Khi văn bản được cập nhật với ký tự / (gạch chéo xuống), tệp không thể được mở trong Photoshop | Lỗi |
| PSDNET-199 | Tệp PSD không thể được lưu khi lớp văn bản chỉ chứa dòng linebreak | Lỗi |
| PSDNET-185 | Cỡ chữ Font bị trích xuất sai | Lỗi |

## **Thay đổi API Công cộng**
# **API Đã Thêm:**
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F:Aspose.PSD.ResizeType.CatmullRom
- F:Aspose.PSD.ResizeType.CubicConvolution
- F:Aspose.PSD.ResizeType.CubicBSpline
- F:Aspose.PSD.ResizeType.Mitchell
- F:Aspose.PSD.ResizeType.SinC
- F:Aspose.PSD.ResizeType.Bell
# **Đã Gỡ Bỏ APIs:**
- Không

## **Ví dụ về việc sử dụng:**
**PSDNET-207. Hỗ trợ Layer Điều chỉnh Cân Bằng Màu**

{{< highlight java >}}

            var filePath = "ColorBalance.psd";

            var outputPath = "ColorBalance_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                foreach (var layer in im.Layers)

                {

                    var cbLayer = layer as ColorBalanceAdjustmentLayer;

                    if (cbLayer != null)

                    {

                        cbLayer.ShadowsCyanRedBalance = 30;

                        cbLayer.ShadowsMagentaGreenBalance = -15;

                        cbLayer.ShadowsYellowBlueBalance = 40;

                        cbLayer.MidtonesCyanRedBalance = -90;

                        cbLayer.MidtonesMagentaGreenBalance = -25;

                        cbLayer.MidtonesYellowBlueBalance = 20;

                        cbLayer.HighlightsCyanRedBalance = -30;

                        cbLayer.HighlightsMagentaGreenBalance = 67;

                        cbLayer.HighlightsYellowBlueBalance = -95;

                        cbLayer.PreserveLuminosity = true;

                    }

                }

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-145. Hỗ trợ Layer Điều chỉnh Đảo Ngược**

{{< highlight java >}}

            var filePath = "InvertStripes_before.psd";

            var outputPath = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-139. Triển khai Bộ lọc Bicubic**

{{< highlight java >}}

             string sourceFile = "sample.psd";

            string destName = "ResamplerCubicConvolutionStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicConvolution);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCatmullRomStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CatmullRom);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerMitchellStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Mitchell);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerCubicBSplineStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.CubicBSpline);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerSinCStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.SinC);

                image.Save(destName, new PsdOptions(image));

            }

            string sourceFile = "sample.psd";

            string destName = "ResamplerBellStripes_after.psd";

            // Load an existing image into an instance of PsdImage class

            using (PsdImage image = (PsdImage)Image.Load(sourceFile))

            {

                image.Resize(300, 300, ResizeType.Bell);

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-169. Thêm hỗ trợ xuất PSD sang PDF với Clipping Mask**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-168. Thêm hỗ trợ xuất PSD sang PDF với Adjustment Layers**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("example.psd"))

    {

      image.Save("document.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. Khi văn bản được cập nhật với / (gạch chéo xuống), tệp không thể mở trong Photoshop**

{{< highlight java >}}

         var psdImage = (PsdImage)image;

        var layers = psdImage.Layers;

        for (var index = layers.Length - 1; index >= 0; index--)

        {

            var layer = layers[index];

            if (!(layer is TextLayer)) continue;

            var textLayer = (TextLayer)layer;

            textLayer.UpdateText("/");

        }

        var imageOptions = new PsdOptions(psdImage);

        var fileName = Path.GetFileName(filePath);

        var outputFilePath = Path.GetDirectoryName(filePath) + "\\target_" + fileName;

        psdImage.Save(outputFilePath, imageOptions);



{{< /highlight >}}

**PSDNET-199. Tệp PSD không thể lưu khi lớp văn bản chỉ chứa dòng linebreak**

{{< highlight java >}}

 string filePath = "testLineBreaks2.psd";

string outputPath = "testLineBreaks2_changed.psd";

var newText = "\r";

        using (var image = Image.Load(filePath))

        {

            var psdImage = image as PsdImage;

            if (image == null)

            {

                return;

            }

            var layers = psdImage.Layers;

            for (var index = layers.Length - 1; index >= 0; index--)

            {

                var layer = layers[index] as TextLayer;

                if (layer == null)

                {

                    continue;

                }

                layer.UpdateText(newText);

            }

            var imageOptions = new PsdOptions(psdImage);

            psdImage.Save(outputPath, imageOptions);

        }

{{< /highlight >}}

**PSDNET-185. Cỡ chữ Font bị trích xuất sai**

{{< highlight java >}}

             // Trích xuất sai cỡ chữ Font 

            string filePath = "直播+电商.psd";

            var tolerance = 0.001;

            using (var image = Image.Load(filePath))

            {

                int layerIndex = 22;

                // API cũ (Sử dụng cỡ chữ đoạn văn bản đầu tiên)

                PsdImage psdImage = image as PsdImage;

                double[] matrix = ((TextLayer)psdImage.Layers[layerIndex]).TransformMatrix;

                double baseFontSize = ((TextLayer)psdImage.Layers[layerIndex]).Font.Size;

                double fontSize = matrix[0] * baseFontSize;

                // Kiểm tra cỡ chữ font cơ sở

                if (Math.Abs(100.0 - baseFontSize) > tolerance)

                {

                    throw new Exception("Cỡ chữ Font đã đọc sai");

                }

                // Kiểm tra cỡ chữ font thực sự

                if (Math.Abs(88.425 - fontSize) > tolerance)

                {

                    throw new Exception("TransformMatrix đã đọc sai");

                }

                // API mới (Một lớp văn bản có thể chứa bất kỳ số lượng cỡ chữ font nào)

                ITextPortion[] portions = ((TextLayer)psdImage.Layers[layerIndex]).TextData.Items;

                ITextStyle style = portions[0].Style;

                double fontSizeOfPortion = matrix[0] * style.FontSize;

                // Kiểm tra cỡ chữ font đoạn cơ sở

                if (Math.Abs(100.0 - style.FontSize) > tolerance)

                {

                    throw new Exception("Cỡ chữ Font đã đọc sai");

                }

                // Kiểm tra cỡ chữ font thực sự của đoạn

                if (Math.Abs(88.425 - fontSizeOfPortion) > tolerance)

                {

                    throw new Exception("TransformMatrix đã đọc sai");

                }

            }

{{< /highlight >}}

**PSDNET-179. Vấn đề Lấy Layer DropShadowEffect**

{{< highlight java >}}

       // Khi thuộc tính DropShadowEffect.UseGlobalLight là 'true', thì đối tượng DropShadowEffect sẽ sử dụng giá trị góc từ thuộc tính PsdImage.GlobalAngle.

		using (PsdImage image = (PsdImage)Image.Load("4.psd"))

		{

    		image.GlobalAngle = 30;

    		image.Save("output.psd");

		}

{{< /highlight >}}


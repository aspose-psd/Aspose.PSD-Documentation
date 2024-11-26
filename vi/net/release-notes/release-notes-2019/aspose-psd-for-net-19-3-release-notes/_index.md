---
title: Aspose.PSD cho .NET 19.3 - Ghi chú phát hành
type: docs
weight: 100
url: /vi/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho Aspose.PSD cho .NET 19.3

{{% /alert %}}

|**Khóa**|**Tóm Tắt**|**Danh Mục**|
| :- | :- | :- |
|PSDNET-104|Rendering của lớp văn bản quay bởi Ma trận Biến đổi|Tính năng|
|PSDNET-96|Thực hiện rendering của hiệu ứng Stroke với Màu Fill cho xuất khẩu|Tính năng|
|PSDNET-112|Các Bộ biến áp InnerData làm hỏng một số lớp với mặt nạ vector|Mắc lỗi|
|PSDNET-113|Cập nhật lớp văn bản cho hình ảnh PSD gây lỗi khi mở trong Photoshop|Mắc lỗi|

## **Thay Đổi API Công Khai**
# **API Đã Thêm:**
- Không có
# **API Đã Xóa:**
- Không có

## **Ví dụ sử dụng:**
**PSDNET-104. Rendering của lớp văn bản quay bởi Ma trận Biến đổi**

{{< highlight java >}}

 string sourceFileName = "TransformedText.psd";

string exportPath = "TransformedTextExport.psd";

string exportPathPng = "TransformedTextExport.png";

var im = (PsdImage) Image.Load(sourceFileName);

using(im) {

 im.Save(exportPath);

 im.Save(exportPathPng, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Thực hiện rendering của hiệu ứng Stroke với Màu Fill cho xuất khẩu**

{{< highlight java >}}

  // Thực hiện rendering của hiệu ứng Stroke với Màu Fill cho xuất khẩu

 string sourceFileName = "StrokeComplex.psd";

 string exportPath = "StrokeComplexRendering.psd";

 string exportPathPng = "StrokeComplexRendering.png";

 var loadOptions = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(sourceFileName, loadOptions)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var effect = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var settings = (ColorFillSettings) effect.FillSettings;

   settings.Color = Color.DeepPink;

  }

  // Lưu psd

  im.Save(exportPath, new PsdOptions());

  // Lưu png

  im.Save(exportPathPng, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. Các Bộ biến áp InnerData làm hỏng một số lớp với mặt nạ vector**

{{< highlight java >}}

 // Các Bộ biến áp InnerData làm hỏng một số lớp với mặt nạ vector

var sourceFile = "1.psd";

var pngPath = "RotateFlipTest2617.png";

var psdPath = "RotateFlipTest2617.psd";

var flipType = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(sourceFile))) {

 im.RotateFlip(flipType);

 im.Save(pngPath, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 im.Save(psdPath);

}

{{< /highlight >}}

**PSDNET-113. Cập nhật lớp văn bản cho hình ảnh PSD gây lỗi khi mở trong Photoshop**

{{< highlight java >}}

 string sourceFileName = "Test.psd";

string exportPath = "Result.psd";

using(Image image = Image.Load(sourceFileName)) {

 if (!(image is PsdImage)) {

 

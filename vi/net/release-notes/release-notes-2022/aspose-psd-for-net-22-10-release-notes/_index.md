---
title: Ghi chú phát hành Aspose.PSD cho .NET 22.10
type: docs
weight: 30
url: /vi/net/aspose-psd-cho-net-22-10-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Phiên bản này có sự suy giảm trong trường hợp xuất 16 bit, vì vậy chúng tôi khuyến nghị cẩn thận khi sử dụng tính năng này trong phiên bản này.
Vui lòng không cập nhật Aspose.PSD lên 22.9-22.10 nếu xử lý hình ảnh 16 bit là chức năng chính của bạn.

Chúng tôi đang làm việc để tìm giải pháp cho những vấn đề này.

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-1287|Loại bỏ các thuộc tính lỗi thời trong Lfx2Resource|Cải tiến|
|PSDNET-1071|Aspose.PSD không thể mở file PSD (RGB/16 bit) với nén ZipWithoutPrediction|Lỗi|
|PSDNET-1257|Các hiệu ứng thời gian biến mất và hiển thị một cách lạ (trong Photoshop)|Lỗi|
|PSDNET-1278|Độ trong suốt không hoạt động đúng cho hiệu ứng Stroke với Inside Position|Lỗi|
|PSDNET-1279|Sự suy giảm: Lỗi khi mở File PSD|Lỗi|
|PSDNET-1284|Cập nhật văn bản thất bại với một số ký tự châu Á. Lỗi khi phân tích ký tự cụ thể|Lỗi|
|PSDNET-1291|Cập nhật văn bản thất bại với một số ký tự châu Á. Lỗi khi hiển thị ký tự cụ thể|Lỗi|
|PSDNET-1292|Lỗi khi mở tệp xuất bởi Photoshop sau lưu một số ký tự châu Á cụ thể|Lỗi|


## **Thay đổi API công khai**
# **API được thêm:**
- Không có

# **API bị loại bỏ:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Ví dụ về cách sử dụng:**

**PSDNET-1071. Aspose.PSD không thể mở file PSD (RGB/16 bit) với nén ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Các hiệu ứng thời gian biến mất và hiển thị một cách lạ (trong Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Tạo timeline với vài khung.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. Độ trong suốt không hoạt động đúng cho hiệu ứng Stroke với Inside Position**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Sự suy giảm: Lỗi khi mở File PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Cập nhật văn bản thất bại với một số ký tự châu Á. Lỗi khi phân tích ký tự cụ thể**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // Chọn ký tự gây ra vấn đề

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Loại bỏ các thuộc tính lỗi thời trong Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Cập nhật lựa chọn BlendMode của hiệu ứng
    effect.BlendMode = BlendMode.Darken;

    // Cập nhật lựa chọn Độ mờ của hiệu ứng
    effect.Opacity = 128; // 50%

    // Cập nhật lựa chọn màu fill cho hiệu ứng vẽ Stroke
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Cập nhật văn bản thất bại với một số ký tự châu Á. Lỗi khi hiển thị ký tự cụ thể**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // Chọn các ký tự gây ra vấn đề

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Lỗi khi mở tệp xuất bởi Photoshop sau lưu một số ký tự châu Á cụ thể**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}

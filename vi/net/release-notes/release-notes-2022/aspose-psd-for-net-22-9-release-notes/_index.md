---
title: Ghi chú phát hành Aspose.PSD cho .NET 22.9
type: docs
weight: 40
url: /vi/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Bản phát hành này có một sự suy giảm trong trường hợp xuất 16-bit, vì vậy chúng tôi khuyên bạn cẩn thận khi sử dụng tính năng này trong bản phát hành này.
Vui lòng không cập nhật Aspose.PSD lên phiên bản 22.9 nếu xử lý hình ảnh 16-bit là tính năng chính của bạn.
- Đối với một số phiên bản của Photoshop, người dùng có thể gặp cửa sổ hiển thị thông báo lỗi đọc lớp, điều này sẽ không ảnh hưởng đến việc làm việc với tệp PSD.

Chúng tôi đang làm việc để giải quyết các vấn đề này.

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-1237|Tạo mô hình LayerStyleFX nội bộ sẽ chứa hiệu ứng và dữ liệu liên quan để sử dụng mô hình duy nhất trong tài nguyên hiệu ứng Lfx2, lmfx và mlst|Cải tiến|
|PSDNET-1227|Thêm đọc và viết các cấu trúc 'Lefx' với thông tin hiệu ứng cho các trạng thái lớp trong mô hình TimeLine|Tính năng|
|PSDNET-1230|Áp dụng trạng thái lớp TimeLine vào lớp trong PsdImage|Tính năng|
|PSDNET-1072|Độ trong suốt không chính xác khi lưu tệp PSD (RGB/16-bit) khi xuất sang 8-bit|Lỗi|
|PSDNET-1140|Ngoại lệ khi tải bước tài nguyên lớp toàn cầu khi mở tài liệu PSB|Lỗi|
|PSDNET-1266|Rò rỉ bộ nhớ khi xử lý các tệp cụ thể|Lỗi|


## **Thay đổi trong API công cộng**
# **Các API được Thêm:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **Các API Đã Loại bỏ:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Ví dụ về việc sử dụng:**

**PSDNET-1072. Độ trong suốt không chính xác khi lưu tệp PSD (RGB/16-bit) khi xuất sang 8-bit**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // Tùy chọn lưu 16 bit
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // Lưu hình ảnh với màu 16 bit
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Ngoại lệ khi tải bước tài nguyên lớp toàn cầu khi mở tài liệu PSB**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // Không nên có ngoại lệ ở đây.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Thêm đọc và viết các cấu trúc 'Lefx' với thông tin hiệu ứng cho các trạng thái lớp trong mô hình TimeLine**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] layerIds = timeLine.LayerIds;

    var layerStateEffects11 = timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects;

    layerStateEffects11.AddDropShadow();
    layerStateEffects11.AddGradientOverlay();

    var layerStateEffects21 = timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects;
    layerStateEffects21.AddStroke(FillType.Color);
    layerStateEffects21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1230. Áp dụng trạng thái lớp TimeLine vào lớp trong PsdImage**

{{< highlight csharp >}}
string sourceFile = "3_animated.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var layerState11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    layerState11.BlendMode = BlendMode.Multiply;

    // Thay đổi khung hoạt động từ 0 thành 1 để kích hoạt việc áp dụng LayerState vào Layer
    timeLine.ActiveFrame = 1;

    // Áp dụng các thay đổi vào PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Rò rỉ bộ nhớ khi xử lý các tệp cụ thể**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Tổng số byte được sử dụng trước thử nghiệm: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // Kiểm tra Mở và Lưu
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(inputNumber, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, memCount);
}

memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Tổng số byte được sử dụng sau thử nghiệm: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "Phát hiện rò rỉ bộ nhớ trong chức năng cơ bản!");
{{< /highlight >}}

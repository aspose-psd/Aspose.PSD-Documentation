---
title: Aspose.PSD cho .NET 22.8 - Ghi chú Phát hành
type: docs
weight: 50
url: /vi/net/aspose-psd-cho-net-22-8-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-1225|Điều tra và sửa các vấn đề trong trình cài đặt|Cải tiến|
|PSDNET-800|Hỗ trợ của Khung Thời gian từ Tệp PSD|Tính năng|
|PSDNET-1219|Hỗ trợ của tài nguyên 'mlst' chứa trong ShmdResource như là một tài nguyên con|Tính năng|
|PSDNET-814|Băm của Thay đổi Lớp nếu chúng ta gọi layer.BlendingOptions.Effects|Lỗi|


## **Thay đổi API công cộng**
# **APIs Thêm vào:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Delay
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.LayerStates
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.DisposalMethod
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Automatic
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.DoNotDispose
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Dispose
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.HorizontalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.VerticalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.FillOpacity
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.DescriptorVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.SubResourcesx


# **APIs Đã loại bỏ:**
- None


## **Ví dụ về cách sử dụng:**

**PSDNET-800. Hỗ trợ Khung thời gian từ Tệp PSD**

{{< highlight csharp >}}
string sourceFile = "image1219.psd";
string outputPsd = "output_image800.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    // Thay đổi phương pháp tiêu hủy của khung 1
    timeLine.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;

    // Thay đổi độ trễ của khung 2
    timeLine.Frames[1].Delay = 15;

    // Thay đổi độ mờ của 'Lớp 1' trên khung 2
    LayerState layerState11 = timeLine.Frames[1].LayerStates[timeLine.LayerIds[1]];
    layerState11.Opacity = 50;

    // di chuyển 'Lớp 1' đến góc dưới bên trái trên khung 3
    LayerState layerState21 = timeLine.Frames[2].LayerStates[timeLine.LayerIds[1]];
    layerState21.Offset = new Point(-50, 230);

    // Thêm khung mới
    List<Frame> frames = new List<Frame>(timeLine.Frames);
    frames.Add(new Frame(timeLine));
    timeLine.Frames = frames.ToArray();

    // Thay đổi chế độ trộn của 'Lớp 1' trên khung 4
    LayerState layerState31 = timeLine.Frames[3].LayerStates[timeLine.LayerIds[1]];
    layerState31.BlendMode = BlendMode.Dissolve;

    // Áp dụng các thay đổi trở lại đối tượng PsdImage
    timeLine.ApplyTo(psdImage);
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-814. Băm của Thay đổi Lớp nếu chúng ta gọi layer.BlendingOptions.Effects**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layer = image.Layers[0];
    var startHash = layer.GetHashCode();
    var effects = layer.BlendingOptions.Effects;
    var endHash = layer.GetHashCode();

    if (startHash != endHash)
    {
        throw new Exception("Băm không được thay đổi");
    }
}
{{< /highlight >}}

**PSDNET-1219. Hỗ trợ của tài nguyên 'mlst' chứa trong ShmdResource như là một tài nguyên con**

{{< highlight csharp >}}
string sourceFile = "image1219.psd";
string outputPsd = "output_image1219.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    Layer layer1 = image.Layers[1];
    ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
    MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];

    ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
    DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
    BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];

    // Vô hiệu hóa lớp 1 trên khung 1
    layerEnabled.Value = false;

    image.Save(outputPsd);
}
{{< /highlight >}}

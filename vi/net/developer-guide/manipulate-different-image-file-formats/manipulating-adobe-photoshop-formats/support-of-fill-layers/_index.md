---
title: Hỗ trợ các lớp Fill
type: docs
weight: 90
url: /vi/net/support-of-fill-layers/
---

## **Các Lớp Fill Với Mẫu Fill**
Bài viết này demo cách điền [PSD](https://wiki.fileformat.com/image/psd/) lớp với mẫu fill. Một Pattern* *là một hình ảnh, màu sắc, bóng hoặc đường dùng để fill một khu vực của một hình ảnh. Vui lòng sử dụng Aspose.PSD.FileFormats.Psd.Layers.FillLayer để thêm Pattern vào lớp PSD. Đoạn mã dưới đây tải một tệp PSD, truy cập lớp Filllayer và thiết lập Mẫu bằng thuộc tính [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}


Dưới đây là một ví dụ khác mô tả cách [Aspose.PSD](https://products.aspose.com/psd/net) vẽ mẫu bằng cách sử dụng [FillLayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) và [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Các Lớp Fill Với Màu Gradient Fill**
Bài viết này demo cách sử dụng fill Gradient để fill lớp PSD. Aspose.PSD APIs đã tiết lộ các phương pháp hiệu quả & dễ sử dụng để đạt được mục tiêu này. Aspose.PSD đã tiết lộ các lớp [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) và [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) để thêm hiệu ứng Gradient vào một lớp.


Các bước fill lớp PSD bằng Gradient fill đơn giản như sau:

- Tải một tệp PSD như một hình ảnh sử dụng phương thức [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) được tiết lộ bởi lớp [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Thiết lập các thuộc tính settings của đối tượng [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Tạo một danh sách [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) với các màu cần thiết và vị trí của màu.
- Tạo một danh sách điểm trong suốt với độ mờ cần thiết và vị trí của điểm trong suốt.
- Gọi phương thức [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Lưu kết quả.



Đoạn mã dưới đây cho thấy cách thêm Gradient fill để fill lớp PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**Dưới đây là một ví dụ khác sử dụng thuộc tính [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** để fill lớp PSD bằng Gradient fill. Aspose.PSD hỗ trợ các loại Gradient sau thông qua Enumeration GradientType:

- **GradientType.Linear:**       Trong Gradient tuyến tính, màu chuyển tiếp từ màu xuất phát đến màu cuối cùng theo một đường thẳng.
- **GradientType.Radial:**       Trong Gradient hình tròn, các màu mở rộ từ điểm bắt đầu theo một mẫu tròn.
- **GradientType.Angle:**        Trong Gradient góc, một Gradient góc xoay ngược chiều kim đồng hồ xung quanh điểm xuất phát.
- **GradientType.Reflected:** Trong Gradient phản chiếu, màu được phản chiếu cả hai bên của điểm bắt đầu.
- **GradientType.Diamond:**   Gradient kim cương tạo ra một hình dạng kim cương từ điểm bắt đầu.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Hỗ Trợ Thuộc Tính Scale cho Lớp Gradient Fill**
Bài viết này demo cách scale FillLayer với Gradient fill bằng Aspose.PSD cho .NET. Với mục đích này, một thuộc tính mới [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) đã được thêm vào [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings).


Dưới đây là đoạn mã demo thể hiện cách sử dụng thuộc tính **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Các Lớp Fill Với Màu Fill**
Bài viết này demo cách fill [PSD](https://wiki.fileformat.com/image/psd/) lớp với Màu. Vui lòng sử dụng lớp [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) để thêm Màu vào lớp PSD. Đoạn mã dưới đây tải một tệp PSD, truy cập lớp Fill và thiết lập màu bằng thuộc tính [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}



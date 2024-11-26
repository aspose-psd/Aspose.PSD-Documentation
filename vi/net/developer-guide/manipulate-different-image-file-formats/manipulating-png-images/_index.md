---
title: Xóa đổi ảnh PNG
type: docs
weight: 40
url: /vi/net/manipulating-png-images/
---

## **Xác định Độ trong suốt cho Ảnh PNG**
Một trong những ưu điểm của việc lưu ảnh dưới định dạng PNG là PNG có thể có nền trong suốt. Aspose.PSD cho .NET cung cấp tính năng xác định độ trong suốt cho Ảnh PNG & Ảnh raster như được minh họa trong phần dưới đây. Aspose.PSD cho .NET API có thể được sử dụng để thiết lập bất kỳ màu nào là trong suốt khi tạo ảnh PNG mới hoặc chuyển đổi các ảnh hiện có sang định dạng PNG. Với mục đích này, Aspose.PSD cho .NET API đã tiếp cận [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) property và [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) enumerated mà có thể thiết lập để chỉ định bất kỳ màu nào sẽ được hiển thị như là trong suốt trong ảnh PNG. Đoạn mã mẫu dưới đây minh họa cách chuyển đổi một ảnh PSD hiên có sang ảnh PNG bằng cách xác định màu mong muốn là trong suốt.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **Thiết lập Độ phân giải cho Ảnh PNG**
Aspose.PSD cho .NET mở ra lớp ResolutionSetting mà có thể được sử dụng để thiết lập độ phân giải cho tất cả định dạng ảnh bao gồm cả PNG. Bài viết này minh họa cách sử dụng Aspose.PSD cho .NET API để thiết lập thông số độ phân giải ngang & dọc cho định dạng ảnh PNG. Đoạn mã dưới đây tải một ảnh PSD hiện có và chuyển đổi nó sang định dạng PNG đồng thời thay đổi độ phân giải.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **Nén Tập tin PNG**
Portable Network Graphic (PNG) là một định dạng nén không mất dữ liệu cho việc truyền một dạng bitmap qua mạng. Khi bạn lưu một ảnh dưới dạng tập tin PNG trong bất kỳ chương trình nào, bạn có thể được yêu cầu chọn một mức nén trong một phạm vi từ 0 đến mức cao nhất. Thiết lập giá trị này thực sự nén kích thước tập tin và không giảm chất lượng hình ảnh. Bài viết này mô tả cách Aspose.PSD APIs cho phép bạn kiểm soát kích thước tập tin PNG. Aspose.PSD APIs có thể được sử dụng để thiết lập Cấp độ Nén cho định dạng tập tin PNG bằng cách sử dụng lớp PngOptions có một property [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) kiểu int. Property này chấp nhận một giá trị từ 0 đến 9 với 9 là mức nén cao nhất. Đoạn mã dưới đây minh họa cách thiết lập Cấp độ Nén bằng cách sử dụng Aspose.PSD cho .NET API.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **Xác định Độ sâu Bit cho Ảnh PNG**
Độ sâu Bit trong hình ảnh là số bit được sử dụng để chỉ định màu sắc của một pixel duy nhất trong một hình ảnh bitmap. Giống như tất cả các định dạng bitmap khác, độ sâu màu của PNG cũng được biểu diễn bằng bit như 1-bit (2 màu), 2-bit (4 màu), 4-bit (16 màu) và 8-bit (256 màu). Aspose.PSD cho .NET API có thể được sử dụng để thiết lập độ sâu bit cho ảnh PNG bằng cách sử dụng [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) property mà được tiết lộ bởi lớp PngOptions. Hiện tại, property BitDepth có thể thiết lập 1, 2, 4 hoặc 8 bit cho các loại màu xám và màu chiếm chỉ số. Đối với tất cả các loại màu khác, chỉ có 8 bit được hỗ trợ. Đoạn mã dưới đây minh họa cách thiết lập Độ sâu Bit cho một ảnh PNG.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **Ứng dụng Phương pháp Lọc trên Ảnh PNG**
Độ sâu Bit trong hình ảnh là số bit được sử dụng để chỉ định màu sắc của một pixel duy nhất trong một hình ảnh bitmap. Giống như tất cả các định dạng bitmap khác, độ sâu màu của PNG cũng được biểu diễn bằng bit như 1-bit (2 màu), 2-bit (4 màu), 4-bit (16 màu) và 8-bit (256 màu). Aspose.PSD cho .NET API có thể được sử dụng để thiết lập độ sâu bit cho ảnh PNG bằng BitDepth property tiết lộ bởi lớp PngOptions. Hiện tại, property BitDepth có thể thiết lập 1, 2, 4 hoặc 8 bit cho các loại màu xám và màu chiếm chỉ số. Đối với tất cả các loại màu khác, chỉ có 8 bit được hỗ trợ. Đoạn mã dưới đây minh họa cách thiết lập Độ sâu Bit cho ảnh PNG.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **Thay đổi Màu Nền của Ảnh PNG trong suốt**
Ảnh định dạng PNG có thể có nền trong suốt. Aspose.PSD cho .NET cung cấp tính năng thay đổi màu nền của ảnh PNG có nền trong suốt. Aspose.PSD cho .NET API có thể được sử dụng để thiết lập/thay đổi màu của một ảnh PNG trong suốt. Đoạn mã dưới đây minh họa cách thiết lập/thay đổi màu nền của ảnh PNG trong suốt.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}

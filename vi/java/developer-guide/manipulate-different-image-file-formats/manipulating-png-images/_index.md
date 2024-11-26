---
title: Xử lý Hình Ảnh PNG
type: docs
weight: 30
url: /vi/java/manipulating-png-images/
---

## **Xác định độ trong suốt cho Hình Ảnh PNG**
Một trong những ưu điểm của việc lưu hình ảnh dưới định dạng PNG là PNG có thể có nền trong suốt. Aspose.PSD cho Java cung cấp tính năng để xác định độ trong suốt cho các lớp PngImage & RasterImage như được minh họa trong phần dưới đây. Aspose.PSD cho Java API có thể được sử dụng để đặt bất kỳ màu nào là trong suốt trong quá trình tạo hình ảnh PNG mới hoặc chuyển đổi hình ảnh hiện có sang định dạng PNG. Vì mục đích này, Aspose.PSD cho Java API đã tiết lộ thuộc tính TransparentColor và kiểu liệt kê PngColorType mà có thể được đặt để xác định màu nào sẽ được hiển thị trong suốt trong hình ảnh PNG. Đoạn mã dưới đây minh họa cách chuyển đổi hình ảnh PSD hiện có thành hình ảnh PNG bằng cách sử dụng constructor nạp chồng PngImage và xác định màu mong muốn là trong suốt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Đặt Độ phân giải cho Hình Ảnh PNG**
Aspose.PSD cho Java tiết lộ lớp ResolutionSetting mà có thể được sử dụng để đặt độ phân giải cho tất cả các định dạng hình ảnh bao gồm cả PNG. Bài viết này minh họa việc sử dụng Aspose.PSD cho Java API để đặt các tham số độ phân giải ngang & dọc cho định dạng hình ảnh PNG. Đoạn mã dưới đây tải một hình ảnh PSD hiện có và chuyển đổi sang định dạng PNG cũng thay đổi độ phân giải.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **Nén Các Tập Tin PNG**
Định dạng Hình ảnh Mạng Ngang (PNG) là một định dạng nén mất không chất lượng để truyền một bitmap qua mạng. Khi bạn lưu một hình ảnh dưới dạng tệp PNG trong bất kỳ chương trình nào, bạn có thể được yêu cầu chọn mức nén trong khoảng từ 0 đến mức tối đa nào đó. Đặt giá trị này thực sự nén kích thước tệp và không làm giảm chất lượng hình ảnh. Bài viết này mô tả cách Aspose.PSD APIs cho phép bạn kiểm soát kích thước tập tin PNG. Các APIs Aspose.PSD có thể được sử dụng để thiết lập Các Mức Nén cho định dạng tập tin PNG bằng cách sử dụng lớp PngOptions có thuộc tính CompressionLevel kiểu int. Thuộc tính này chấp nhận một giá trị từ 0 đến 9 trong đó 9 là mức nén cao nhất. Đoạn mã dưới đây minh họa cách thiết lập Các Mức Nén bằng cách sử dụng Aspose.PSD cho Java API.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Xác định Độ Sâu Bit cho Hình Ảnh PNG**
Độ sâu bit trong hình ảnh là số bit được sử dụng để chỉ định màu của một pixel duy nhất trong hình ảnh bitmap. Giống như tất cả các định dạng hình ảnh bitmap khác, độ sâu màu của PNG cũng được biểu diễn bằng bit như 1 bit (2 màu), 2 bit (4 màu), 4 bit (16 màu) và 8 bit (256 màu). Aspose.PSD cho Java API có thể được sử dụng để đặt độ sâu bit cho hình ảnh PNG bằng cách sử dụng thuộc tính BitDepth được tiết lộ bởi lớp PngOptions. Hiện tại, thuộc tính BitDepth có thể được thiết lập thành 1, 2, 4 hoặc 8 bit cho kiểu màu xám và màu chỉ mục. Đối với tất cả các kiểu màu khác, chỉ 8 bit được hỗ trợ. Đoạn mã dưới đây minh họa cách đặt Độ Sâu Bit cho hình ảnh PNG.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Áp Dụng Các Phương Pháp Lọc cho Hình Ảnh PNG**
Aspose.PSD cho Java tiết lộ liệt kê PngFilterType mà có thể được sử dụng để đặt loại bộ lọc cho hình ảnh PNG. Đoạn mã dưới đây minh họa cách áp dụng bộ lọc lên tệp PSD hiện có để chuyển đổi sang hình ảnh PNG bằng cách sử dụng PngFilterType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Thay Đổi Màu Nền của Hình Ảnh PNG Trong Suốt**
Hình ảnh định dạng PNG có thể có nền trong suốt. Aspose.PSD cho Java cung cấp tính năng thay đổi màu nền của một hình ảnh PNG có nền trong suốt. Aspose.PSD cho Java API có thể được sử dụng để đặt/thay đổi màu của một hình ảnh PNG trong suốt. Đoạn mã dưới đây minh họa cách đặt/thay đổi màu nền của một hình ảnh PNG trong suốt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}

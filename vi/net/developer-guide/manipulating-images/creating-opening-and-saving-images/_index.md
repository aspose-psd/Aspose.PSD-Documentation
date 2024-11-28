---
title: Tạo, Mở và Lưu Hình Ảnh
type: docs
weight: 30
url: /vi/net/tao-mo-va-luu-hinh-anh/
---

## **Tạo Tệp Hình Ảnh**
Aspose.PSD cho .NET cho phép nhà phát triển tạo ra các hình ảnh của riêng mình. Sử dụng phương thức Create tĩnh được tiết lộ bởi lớp Image để tạo ra các hình ảnh mới. Bạn chỉ cần cung cấp đối tượng thích hợp của một trong các lớp từ không gian tên ImageOptions cho định dạng hình ảnh đầu ra mong muốn. Để tạo một tệp hình ảnh, trước tiên hãy tạo một phiên bản của một trong các lớp từ không gian tên ImageOptions. Các lớp này xác định định dạng hình ảnh đầu ra. Dưới đây là một số lớp từ không gian tên ImageOptions (lưu ý rằng chỉ các định dạng tệp PSD đang được hỗ trợ cho việc tạo ra):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) đặt các tùy chọn cho việc tạo tệp PSD. Tệp hình ảnh có thể được tạo bằng cách thiết lập một đường dẫn đầu ra hoặc bằng cách thiết lập một luồng.
### **Tạo bằng Cách Thiết lập Đường Dẫn**
Tạo PsdOptions từ không gian tên [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) và thiết lập các thuộc tính khác nhau. Thuộc tính quan trọng nhất cần thiết là Source. Thuộc tính này chỉ ra nơi dữ liệu hình ảnh đặt (trong một tệp hoặc một luồng). Trong ví dụ dưới đây, nguồn là một tệp. Sau khi thiết lập các thuộc tính, truyền đối tượng đến một trong các phương thức tĩnh [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) cùng với tham số chiều rộng và chiều cao. Chiều rộng và chiều cao được xác định theo pixel.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Tạo Bằng Cách Sử Dụng Luồng**
Quy trình để tạo một hình ảnh bằng cách sử dụng một luồng tương tự như sử dụng đường dẫn. Sự khác biệt duy nhất là bạn cần tạo một phiên bản của [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) bằng cách truyền một đối tượng Stream vào hàm tạo của nó và gán nó cho thuộc tính Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Mở Tệp Hình Ảnh**
Các nhà phát triển có thể sử dụng Aspose.PSD cho API .NET để mở các tệp hình ảnh PSD hiện có cho mục đích khác nhau, như thêm hiệu ứng vào hình ảnh hoặc chuyển đổi một tệp hiện có sang một định dạng khác. Dù mục đích là gì, Aspose.PSD cung cấp hai cách tiêu chuẩn để mở các tệp hiện có: từ tệp hoặc từ một luồng.
### **Mở từ Ổ Đĩa**
Mở một tệp hình ảnh bằng cách truyền đường dẫn và tên tệp làm tham số cho phương thức tĩnh Load được tiết lộ bởi lớp Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Mở bằng Cách Sử Dụng Một Luồng**
Đôi khi hình ảnh mà chúng ta cần mở được lưu trữ dưới dạng một luồng. Trong trường hợp đó, sử dụng phiên bản nạp chồng của phương thức Load. Điều này chấp nhận một đối tượng Stream làm đối số để mở hình ảnh.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Nạp Hình Ảnh Như Một Lớp**
Bài viết này thể hiện cách sử dụng Aspose.PSD để nạp một hình ảnh như một lớp. Aspose.PSD đã tiết lộ phương pháp AddLayer của lớp PsdImage để thêm một hình ảnh vào một tệp PSD như một lớp.

Các bước để nạp một hình ảnh vào PSD như một lớp dễ như sau:

- Tạo một phiên bản của một hình ảnh bằng lớp PsdImage với chiều rộng và chiều cao cụ thể. 
- Nạp một tệp PSD như một hình ảnh sử dụng phương thức nhà máy Load được tiết lộ bởi lớp Image.
- Tạo một phiên bản của lớp Layer và gán lớp hình ảnh PSD cho nó.
- Thêm lớp được tạo bằng phương thức AddLayer được tiết lộ bởi lớp PsdImage.
- Lưu kết quả.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Nạp Hình Ảnh Như Lớp từ Một Luồng**
Bài viết này thể hiện cách sử dụng Aspose.PSD để nạp một hình ảnh như một lớp từ một luồng. Để nạp một hình ảnh từ một luồng, chỉ cần truyền một đối tượng luồng chứa một hình ảnh vào hàm tạo của lớp Layer. Thêm lớp đã tạo bằng phương thức AddLayer được tiết lộ bởi lớp PsdImage và lưu kết quả.


Dưới đây là mã mẫu.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Lưu Tệp Hình Ảnh**
Aspose.PSD cho phép bạn tạo tệp hình ảnh từ đầu. Nó cũng cung cấp các phương tiện để chỉnh sửa các tệp hình ảnh hiện có. Sau khi hình ảnh được tạo hoặc chỉnh sửa, tệp thường được lưu vào ổ đĩa. Aspose.PSD cung cấp cho bạn các phương pháp để lưu hình ảnh vào ổ đĩa bằng cách chỉ định một đường dẫn hoặc sử dụng một đối tượng Luồng.
### **Lưu vào Ổ Đĩa**
Lớp Image đại diện cho một đối tượng hình ảnh, vì vậy lớp này cung cấp tất cả các công cụ cần thiết để tạo, nạp và lưu hình ảnh. Sử dụng phương thức Save của lớp Image để lưu hình ảnh. Một phiên bản nạp chồng của phương thức Save chấp nhận vị trí tệp dưới dạng chuỗi.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Lưu vào Một Luồng**
Một phiên bản nạp chồng khác của phương thức Save chấp nhận đối tượng Stream như một đối số và lưu tệp hình ảnh vào luồng.

Nếu hình ảnh được tạo bằng cách chỉ định bất kỳ CreateOptions nào trong hàm tạo Image, hình ảnh sẽ được lưu tự động vào đường dẫn hoặc luồng được cung cấp trong quá trình khởi tạo của lớp Image bằng cách gọi phương thức Save mà không chấp nhận bất kỳ tham số nào.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Thiết Lập để Thay Thế Font Bị Thiếu**
Các nhà phát triển có thể sử dụng Aspose.PSD cho API .NET để tải các tệp hình ảnh PSD hiện có cho mục đích khác nhau, ví dụ, để đặt tên phông chữ mặc định khi lưu tài liệu PSD dưới dạng hình ảnh raster (sang các định dạng PNG, JPG và BMP). Phông chữ mặc định này nên được sử dụng làm phông chữ thay thế cho tất cả các phông chữ bị thiếu (phông chữ không được tìm thấy trong Hệ điều hành hiện tại). Sau khi hình ảnh được chỉnh sửa, tệp sẽ được lưu vào ổ đĩa.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}

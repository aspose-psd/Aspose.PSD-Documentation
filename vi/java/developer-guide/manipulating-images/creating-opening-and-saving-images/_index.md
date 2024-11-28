---
title: Tạo, Mở và Lưu Hình Ảnh
type: docs
weight: 30
url: /vi/tạo-mở-và-lưu-hình-ảnh/
---

## **Tạo Tập Tin Hình Ảnh**
Aspose.PSD cho Java cho phép nhà phát triển tạo ra các hình ảnh của riêng mình. Sử dụng phương thức Create tĩnh mà lớp Hình ảnh (Image) cung cấp để tạo các hình ảnh mới. Bạn chỉ cần cung cấp một đối tượng phù hợp từ một trong các lớp trong không gian tên ImageOptions cho định dạng hình ảnh đầu ra mong muốn. Để tạo một tập tin hình ảnh, trước tiên hãy tạo một phiên bản của một trong các lớp trong không gian tên ImageOptions. Các lớp này xác định định dạng hình ảnh đầu ra. Dưới đây là một số lớp từ không gian tên ImageOptions (lưu ý rằng hiện chỉ có các định dạng tệp PSD được hỗ trợ cho việc tạo): 

PsdOptions đặt các tùy chọn cho việc tạo một tệp PSD. Tệp hình ảnh có thể được tạo bằng cách đặt một đường dẫn đầu ra hoặc bằng cách thiết lập một luồng.
### **Tạo bằng Cách Đặt Đường Dẫn**
Tạo PsdOptions từ không gian tên ImageOptions và đặt các thuộc tính khác nhau. Thuộc tính quan trọng nhất cần đặt là thuộc tính Source. Thuộc tính này xác định nơi dữ liệu hình ảnh đặt (trong tệp hoặc một luồng). Trong ví dụ dưới đây, nguồn là một tệp. Sau khi đặt các thuộc tính, truyền đối tượng này tới một trong các phương thức Create tĩnh cùng với thông số chiều rộng và chiều cao. Chiều rộng và chiều cao được xác định tính bằng pixel.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Tạo Bằng Cách Sử Dụng Luồng**
Quá trình tạo một hình ảnh bằng cách sử dụng một luồng giống như việc sử dụng một đường dẫn. Sự khác biệt duy nhất là bạn cần tạo một phiên bản của StreamSource bằng cách truyền một đối tượng Stream tới hàm dựng của nó và gán nó vào thuộc tính Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Mở Tập Tin Hình Ảnh**
Nhà phát triển có thể sử dụng API Aspose.PSD cho Java để mở các tệp hình ảnh PSD hiện có cho các mục đích khác nhau, như thêm hiệu ứng vào hình ảnh hoặc chuyển đổi một tệp hiện có sang một định dạng khác. Dù mục đích là gì, Aspose.PSD cung cấp hai cách tiêu chuẩn để mở các tệp hiện có: từ tệp hoặc từ một luồng.
### **Mở từ Ổ Đĩa**
Mở một tập tin hình ảnh bằng cách truyền đường dẫn và tên tệp như một tham số tới phương thức tĩnh Load mà lớp Image cung cấp.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Mở bằng Cách Sử Dụng Một Luồng**
Đôi khi hình ảnh mà chúng ta cần mở được lưu trữ dưới dạng một luồng. Trong trường hợp này, hãy sử dụng phiên bản nạp chồng của phương thức Load. Nó chấp nhận một đối tượng Stream làm đối số để mở hình ảnh.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Nạp Hình Ảnh Như Một Lớp**
Bài viết nàydemonstrates cách sử dụng Aspose.PSD để tải một hình ảnh như một lớp. Aspose.PSD APIs đã bật các phương thức hiệu quả & dễ sử dụng để đạt được mục tiêu này. Aspose.PSD đã bật phương thức AddLayer của lớp PsdImage để thêm một hình ảnh vào một tệp PSD như một lớp.

Các bước để tải một hình ảnh vào PSD như một lớp như sau:

- Tạo một phiên bản hình ảnh sử dụng lớp PsdImage với chiều rộng và chiều cao được chỉ định.
- Nạp một tệp PSD như một hình ảnh sử dụng phương thức tạo mà lớp Image bật ra.
- Tạo một phiên bản của lớp Layer và gán hình ảnh PSD lớp vào đó.
- Thêm lớp đã tạo bằng phương thức AddLayer được bật ra bởi lớp PsdImage
- Lưu các kết quả.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Lưu Tập Tin Hình Ảnh**
Aspose.PSD cho phép bạn tạo các tệp hình ảnh từ đầu. Nó cũng cung cấp phương tiện để chỉnh sửa các tệp hình ảnh hiện có. Khi hình ảnh được tạo hoặc chỉnh sửa, tệp thường được lưu vào ổ đĩa. Aspose.PSD cung cấp cho bạn các phương thức để lưu hình ảnh vào ổ đĩa bằng cách chỉ định một đường dẫn hoặc sử dụng một đối tượng Luồng.
### **Lưu vào Ổ Đĩa**
Lớp Image đại diện cho đối tượng hình ảnh, vì vậy lớp này cung cấp tất cả các công cụ cần thiết để tạo, nạp và lưu một tập tin hình ảnh. Sử dụng phương thức Save của lớp Image để lưu hình ảnh. Một phiên bản nạp chồng của phương thức Save chấp nhận địa chỉ tệp dưới dạng một chuỗi.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Lưu vào Một Luồng**
Một phiên bản nạp chồng khác của phương thức Save chấp nhận đối tượng Luồng làm đối số và lưu tệp hình ảnh vào luồng.

Nếu hình ảnh được tạo bằng cách chỉ định bất kỳ CreateOptions nào trong hàm dựng của Image, hình ảnh sẽ tự động được lưu vào đường dẫn hoặc luồng được cung cấp trong quá trình khởi tạo của lớp Image bằng cách gọi phương thức Save không chấp nhận bất kỳ tham số nào.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Cài Đặt Để Thay Thế Font Thiếu**
Nhà phát triển có thể sử dụng API Aspose.PSD cho Java để nạp các tệp hình ảnh PSD hiện có cho các mục đích khác nhau, ví dụ như đặt tên font mặc định khi lưu tài liệu PSD dưới dạng hình ảnh raster (sang định dạng PNG, JPG và BMP). Font mặc định này sẽ được sử dụng để thay thế cho tất cả các font thiếu (font không tìm thấy trên hệ điều hành hiện tại). Khi hình ảnh đã được chỉnh sửa, tệp sẽ được lưu vào ổ đĩa.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}



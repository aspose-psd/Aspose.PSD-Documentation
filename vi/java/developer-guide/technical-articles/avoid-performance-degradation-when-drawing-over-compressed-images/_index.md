---
title: Tránh Sự Suy Giảm Hiệu Suất Khi Vẽ Trên Hình Ảnh Nén
type: docs
weight: 40
url: /vi/java/tranh-su-suy-giam-hieu-suat-khi-ve-tren-hinh-anh-nen/
---

## **Tránh Sự Suy Giảm Hiệu Suất Khi Vẽ Trên Hình Ảnh Nén**
Có những lúc bạn muốn thực hiện các hoạt động đồ họa cực kỳ phức tạp trên một hình ảnh đã nén. Khi Aspose.PSD phải nén và giải nén hình ảnh ngay lập tức, sự suy giảm hiệu suất có thể xảy ra. Việc vẽ trên hình ảnh nén cũng có thể mang theo một khoản phạt về hiệu suất.
### **Giải Pháp**
Để tránh sự suy giảm hiệu suất, chúng tôi khuyên bạn nên chuyển đổi hình ảnh sang định dạng không nén, hoặc định dạng nguyên thô, trước khi thực hiện các hoạt động đồ họa.
### **Sử Dụng Đường Dẫn Tệp**
Trong ví dụ sau, một hình ảnh PSD được chuyển đổi sang định dạng nguyên thô (không nén) và lưu vào đĩa. Hình ảnh không nén được tải lại trước khi thực hiện các hoạt động đồ họa trên đó. Cùng kỹ thuật áp dụng cho các tệp BMP và GIF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Sử Dụng Một Đối Tượng Luồng**
Đoạn mã sau cho bạn thấy cách hình ảnh PSD được chuyển đổi sang định dạng nguyên thô (không nén) và lưu vào đĩa bằng Stream.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}


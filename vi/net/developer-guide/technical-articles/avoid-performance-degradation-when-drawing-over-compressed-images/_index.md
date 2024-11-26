---
title: Tránh Sự Suy Giảm Hiệu Suất Khi Vẽ Trên Hình Ảnh Nén
type: docs
weight: 10
url: /vi/net/tranh-su-su-giam-hieu-suat-khi-ve-tren-hinh-anh-nen/
---

## **Tránh Sự Suy Giảm Hiệu Suất Khi Vẽ Trên Hình Ảnh Nén**
Đôi khi bạn muốn thực hiện các thao tác đồ họa cực kỳ phức tạp trên một hình ảnh được nén. Khi Aspose.PSD phải nén và giải nén hình ảnh ngay lập tức, có thể xảy ra sự suy giảm hiệu suất. Vẽ trên hình ảnh nén cũng có thể gây ra một khoản phí về hiệu suất.
### **Giải Pháp**
Để tránh sự suy giảm hiệu suất, chúng tôi khuyến nghị rằng bạn chuyển đổi hình ảnh sang định dạng không nén, hoặc thô, trước khi thực hiện các thao tác đồ họa.
### **Sử Dụng Đường Dẫn Tệp**
Trong ví dụ sau, một hình ảnh PSD được chuyển đổi sang định dạng thô (không nén) và được lưu vào đĩa. Sau đó, hình ảnh không nén được tải trở lại trước khi thực hiện các thao tác đồ họa trên nó. Cùng một kỹ thuật áp dụng cho các tập tin BMP và GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **Sử Dụng Đối Tượng Luồng**
Đoạn mã sau cho bạn biết cách chuyển đổi hình ảnh PSD sang định dạng thô (không nén) và lưu vào đĩa bằng MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}

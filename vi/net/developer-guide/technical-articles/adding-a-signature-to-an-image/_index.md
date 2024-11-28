---
title: Thêm Chữ Ký vào Hình Ảnh
type: docs
weight: 70
url: /vi/net/them-chu-ky-vao-hinh-anh/
---

## **Thêm Chữ Ký**


Việc thêm chữ ký vào hình ảnh đôi khi cần thiết để ký số hình ảnh và tránh việc làm giả. Một ý tưởng khác có thể là xem xét hình ảnh như nó đang được hiển thị trong một phòng tranh. Dù lý do là gì, API của Aspose.PSD cung cấp tính năng để thêm chữ ký vào hình ảnh bằng cách đơn giản nhất như được giải thích dưới đây. Lưu ý, ví dụ này sử dụng lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) để vẽ một hình ảnh khác với chữ ký vào bề mặt hình ảnh ban đầu. Để thể hiện thao tác, chúng ta sẽ tải một hình ảnh PSD từ ổ đĩa và vẽ một hình ảnh khác được chữ ký lên bề mặt hình ảnh ban đầu bằng cách sử dụng phương thức [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) của lớp Graphics. Chúng ta sẽ lưu hình ảnh kết quả dưới dạng PNG bằng cách sử dụng lớp [PngOptions](https://reference.aspose.com/psd/net/aspose.psd/imageoptions/pngoptions). Dưới đây là ví dụ mã mà thể hiện cách thêm chữ ký vào một hình ảnh. Mã ví dụ đã được chia thành các phần để dễ theo dõi. Từng bước, ví dụ cho thấy cách:

- Tải hình ảnh chính và hình ảnh phụ (chữ ký).
- Tạo và khởi tạo một đối tượng Graphics.
- Vẽ hình ảnh bằng cách sử dụng phương thức DrawImage của lớp Graphics.
- Lưu kết quả dưới dạng PNG.
### **Mẫu Chương Trình**
#### **Tải Hình Ảnh**
Đầu tiên, tạo các phiên bản của lớp Image để tải các hình ảnh mẫu từ ổ đĩa.
#### **Tạo và Khởi Tạo Đối Tượng Đồ Họa**
Sau khi tải các hình ảnh, tạo và khởi tạo một đối tượng lớp Graphics trong khi sử dụng đối tượng của hình ảnh chính.
#### **Vẽ Hình Ảnh Phụ Lên Hình Ảnh Chính**
Sau đó, sử dụng phương thức DrawImage của lớp Graphics, thêm hình ảnh phụ vào hình ảnh chính. Có nhiều phiên bản của phương thức DrawImage mà chấp nhận một đối tượng Image làm tham số đầu tiên trong khi tất cả các tham số khác tương ứng với vị trí mà hình ảnh cần được vẽ. Để minh họa, mã sau đây sử dụng phiên bản của DrawImage chấp nhận một đối tượng của điểm làm tham số thứ hai và cố gắng vẽ chữ ký ở góc dưới bên phải của hình ảnh chính.
#### **Lưu Hình Ảnh**
Cuối cùng, lưu hình ảnh trở lại ổ đĩa cục bộ dưới dạng tệp PNG bằng cách sử dụng lớp PngOptions.
#### **Mã Nguồn Đầy Đủ**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}

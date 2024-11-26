---
title: Thêm Chữ Ký vào Hình Ảnh
type: docs
weight: 10
url: /vi/them-chu-ky-vao-anh/
---

## **Thêm Chữ Ký**


Việc thêm chữ ký vào hình ảnh đôi khi cần thiết để ký số vào hình ảnh để tránh hàng giả. Một ý kiến khác có thể là để xem xét hình ảnh giống như nó đang được trưng bày trong một phòng tranh. Bất kể lí do nào đi chăng nữa, API của Aspose.PSD cung cấp tính năng để thêm chữ ký vào hình ảnh bằng cách đơn giản nhất như được giải thích dưới đây. Vui lòng lưu ý, ví dụ này sử dụng lớp Graphics để vẽ một hình ảnh khác có chữ ký vào bề mặt của hình ảnh gốc. Để thực hiện thao tác này, chúng ta sẽ tải một hình ảnh PSD từ ổ đĩa và vẽ một hình ảnh khác như chữ ký vào bề mặt của hình ảnh gốc bằng cách sử dụng phương thức DrawImage của lớp Graphics. Chúng ta sẽ lưu kết quả hình ảnh dưới dạng PNG bằng cách sử dụng lớp PngOptions. Dưới đây là một ví dụ code mô tả cách thêm chữ ký vào hình ảnh. Mã nguồn ví dụ đã được chia thành các phần để dễ theo dõi. Bước từng bước, ví dụ cho thấy cách:

- Tải các hình ảnh chính và phụ (chữ ký).
- Tạo và khởi tạo một đối tượng Graphics.
- Vẽ hình ảnh bằng cách sử dụng phương thức DrawImage của lớp Graphics.
- Lưu kết quả dưới dạng PNG.
### **Mẫu Chương Trình**
#### **Tải Hình Ảnh**
Đầu tiên, tạo các trường hợp của lớp Image để tải các hình ảnh mẫu từ ổ đĩa.
#### **Tạo và Khởi Tạo Đối Tượng Graphic**
Sau khi tải hình ảnh, tạo và khởi tạo một đối tượng lớp Graphics khi sử dụng đối tượng của hình ảnh chính.
#### **Vẽ Hình Ảnh Phụ lên Hình Ảnh Chính**
Sau đó, sử dụng phương thức DrawImage của lớp Graphics, thêm hình ảnh phụ vào hình ảnh chính. Có nhiều phiên bản của phương thức DrawImage chấp nhận một đối tượng Image làm tham số đầu tiên trong khi tất cả các tham số khác tương ứng với vị trí mà hình ảnh cần được vẽ. Vì mục đích minh họa, đoạn mã sau sử dụng phiên bản nạp quá tải của DrawImage mà chấp nhận một đối tượng Point làm tham số thứ hai và cố gắng vẽ chữ ký ở góc dưới bên phải của hình ảnh chính.
#### **Lưu Hình Ảnh**
Cuối cùng, lưu hình ảnh trở lại ổ đĩa cục bộ dưới dạng tệp PNG bằng cách sử dụng lớp PngOptions.
#### **Toàn Bộ Mã Nguồn**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}

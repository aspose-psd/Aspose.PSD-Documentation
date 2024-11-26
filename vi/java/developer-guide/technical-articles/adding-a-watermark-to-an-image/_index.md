---
title: Thêm Watermark vào ảnh
type: docs
weight: 20
url: /vi/them-watermark-vao-anh/
---

## **Thêm Watermark vào ảnh**
Tài liệu này giải thích cách thêm watermark vào ảnh bằng cách sử dụng Aspose.PSD. Việc thêm watermark vào ảnh là một yêu cầu phổ biến trong các ứng dụng xử lý ảnh. Ví dụ này sử dụng lớp Graphics để vẽ một chuỗi trên bề mặt ảnh.

### **Thêm Watermark**
Để minh họa hoạt động, chúng ta sẽ tải một ảnh BMP từ ổ đĩa và vẽ một chuỗi làm watermark trên bề mặt ảnh bằng cách sử dụng phương thức DrawString của lớp Graphics. Chúng ta sẽ lưu ảnh dưới định dạng PNG bằng lớp PngOptions. Dưới đây là một ví dụ mã mà minh họa cách thêm watermark vào ảnh. Mã nguồn ví dụ đã được chia thành các phần để dễ theo dõi. Bước theo bước, các ví dụ cho thấy cách:

1. Tải ảnh.
1. Tạo và khởi tạo đối tượng Graphics.
1. Tạo và khởi tạo đối tượng Font và SolidBrush.
1. Vẽ một chuỗi như watermark bằng cách sử dụng phương thức DrawString của lớp Graphics.
1. Lưu ảnh dưới định dạng PNG.

Đoạn mã sau đây cho thấy cách thêm watermark vào ảnh.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}

### **Thêm Watermark Chéo**
Thêm watermark chéo vào ảnh tương tự như thêm watermark ngang như đã thảo luận ở trên, với một số sự khác biệt. Để minh họa hoạt động, chúng ta sẽ tải một ảnh JPG từ ổ đĩa, thêm các biến đổi bằng cách sử dụng một đối tượng của lớp Matrix và vẽ một chuỗi làm watermark trên bề mặt ảnh bằng cách sử dụng phương thức DrawString của lớp Graphics. Dưới đây là một ví dụ mã mà minh họa cách thêm watermark chéo vào ảnh. Mã nguồn ví dụ đã được chia thành các phần để dễ theo dõi. Bước theo bước, các ví dụ cho thấy cách:

1. Tải ảnh.
1. Tạo và khởi tạo đối tượng Graphics.
1. Tạo và khởi tạo đối tượng Font và SolidBrush.
1. Lấy kích thước của ảnh trong đối tượng SizeF.
1. Tạo một thể hiện của lớp Matrix và thực hiện biến đổi hợp thành.
1. Gán biến đổi cho đối tượng Graphics.
1. Tạo và khởi tạo đối tượng StringFormat.
1. Vẽ một chuỗi làm watermark bằng cách sử dụng phương thức DrawString của lớp Graphics.
1. Lưu ảnh kết quả.

Đoạn mã sau đây cho thấy cách thêm watermark chéo vào ảnh.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}

---
title: Thêm Watermark vào một Hình ảnh
type: tài liệu
weight: 30
url: /vi/net/them-watermark-vao-mot-hinh-anh/
---

## **Thêm Watermark vào một Hình ảnh**
Tài liệu này giải thích cách thêm watermark vào một hình ảnh bằng cách sử dụng Aspose.PSD. Thêm watermark vào một hình ảnh là một yêu cầu phổ biến cho các ứng dụng xử lý hình ảnh. Ví dụ này sử dụng lớp Graphics để vẽ một chuỗi trên bề mặt hình ảnh.
### **Thêm Watermark**
Để minh họa hoạt động, chúng tôi sẽ tải một hình ảnh BMP từ đĩa và vẽ một chuỗi như watermark trên bề mặt hình ảnh bằng cách sử dụng phương thức DrawString của lớp Graphics. Chúng tôi sẽ lưu hình ảnh dưới định dạng PNG bằng cách sử dụng lớp PngOptions. Dưới đây là một đoạn mã mẫu minh họa cách thêm watermark vào một hình ảnh. Mã nguồn mẫu đã được chia thành các phần để dễ dàng theo dõi. Từng bước, các ví dụ cho thấy cách thêm watermark vào một hình ảnh:

1. [Tải](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) một hình ảnh.
1. Tạo và khởi tạo một đối tượng [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. Tạo và khởi tạo các đối tượng Font và [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. Vẽ một chuỗi như watermark bằng cách sử dụng phương thức [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) của lớp Graphics.
1. Lưu hình ảnh dưới định dạng PNG.

Đoạn mã sau cho thấy cách thêm watermark lên hình ảnh.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Thêm Watermark đường chéo**
Thêm watermark đường chéo vào một hình ảnh tương tự như việc thêm watermark ngang như đã thảo luận ở trên, chỉ khác biệt một vài điểm. Để minh họa hoạt động, chúng tôi sẽ tải một hình ảnh JPG từ đĩa, thêm các biến đổi bằng cách sử dụng một đối tượng của lớp [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) và vẽ một chuỗi như watermark trên bề mặt hình ảnh bằng cách sử dụng phương thức DrawString của lớp Graphics. Dưới đây là một đoạn mã mẫu minh họa cách thêm watermark đường chéo vào một hình ảnh. Mã nguồn mẫu đã được chia thành các phần để dễ dàng theo dõi. Từng bước, các ví dụ cho thấy cách thêm watermark đường chéo vào một hình ảnh:

1. Tải một hình ảnh.
1. Tạo và khởi tạo một đối tượng Graphics.
1. Tạo và khởi tạo các đối tượng [Font](https://reference.aspose.com/psd/net/aspose.psd/font) và SolidBrush.
1. Lấy kích thước của hình ảnh trong đối tượng [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. Tạo một thể hiện của lớp Matrix và thực hiện biến đổi hợp thành.
1. Gán biến đổi cho đối tượng Graphics.
1. Tạo và khởi tạo một đối tượng [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. Vẽ một chuỗi như watermark bằng cách sử dụng phương thức DrawString của lớp Graphics.
1. Lưu hình ảnh kết quả.

Đoạn mã sau cho thấy cách thêm watermark đường chéo.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}

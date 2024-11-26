---
title: Tổng quan về Định dạng PSD
type: docs
weight: 60
url: /vi/net/psd-format-overview/
---

## **Mô tả**
PSD, Photoshop Document, đại diện cho định dạng tệp nguyên thủy của Adobe Photoshop được sử dụng cho thiết kế đồ họa và phát triển.
## **Thông số Định dạng Tệp**
Dữ liệu trong tệp PSD được lưu trữ theo thứ tự byte big-endian. Điều này ngụ ý việc hoán đổi các số nguyên ngắn và dài khi đọc hoặc ghi trên nền tảng Windows. Định dạng tệp Photoshop chia thành năm phần chính. Nó chứa nhiều đánh dấu chiều dài có thể được sử dụng để di chuyển từ một phần sang phần tiếp theo. Đánh dấu chiều dài thường được đệm bằng byte để làm tròn đến gần kích thước 2 hoặc 4 byte. Năm phần chính bao gồm:

- Đầu tệp
- Dữ liệu Chế độ Màu
- Tài nguyên Hình ảnh
- Thông tin Lớp và Mặt Nạ
- Dữ liệu Hình ảnh

Để tuân thủ, dữ liệu nên được ghi vào tất cả các trường trong phần này, vì Photoshop có thể thử đọc toàn bộ phần đó. Nó cũng ngụ ý rằng phải ghi các số không vào các trường bị bỏ qua khi ghi vào một tệp. Trường chiều dài trong các phần giới hạn bởi chiều dài nên được sử dụng để quyết định khi nào ngừng đọc. Trong hầu hết các trường hợp, trường chiều dài chỉ ra số byte, không phải số bản ghi, đang theo sau. Cần nhớ các điểm sau khi đọc một tệp.

- Các giá trị trong cột "Chiều Dài" trong tất cả các bảng đều theo byte.
- Tất cả các giá trị được định nghĩa là chuỗi Unicode bao gồm:
- Một trường chiều dài 4 byte, đại diện cho số ký tự trong chuỗi (không phải byte).
- Chuỗi giá trị Unicode, hai byte cho mỗi ký tự.
## **Tính năng của định dạng**
Tệp PSD có thể bao gồm các lớp hình ảnh, lớp điều chỉnh, mặt mặt nạ, chú thích, thông tin tệp, từ khóa và các yếu tố cụ thể của Photoshop khác. Tệp Photoshop có phần mở rộng mặc định là .PSD và có giới hạn chiều cao và chiều rộng tối đa là 30.000 pixel, và giới hạn chiều dài hai gigabyte.
## **Cách sử dụng**
1. Một công cụ để Cắt PSD.
1. [Chuyển đổi PSD](/psd/vi/net/converting-psd-image-to-raster-format/) sang HTML
1. Sử dụng [PSD làm Mẫu](/psd/vi/net/using-psd-files-as-templates-for-automation-business-cards-case/) cho Email
1. PSD thành HTML CMS cụ thể
1. Identikit trong Tệp PSD (Phác thảo Cảnh sát)
1. Tạo hình ảnh xem trước giả 3D bằng cách sử dụng Các Đối tượng Thông minh cho các mặt hàng như chai lọ, cốc, áo thun, v.v.
1. Chỉnh sửa nhanh của PSD: Tự động tông màu, Thiết lập, Đối tượng Thông minh, Tách hình ảnh Lớp Văn bản

Và nhiều hơn nữa. Nếu bạn đã tạo điều gì đó lớn với Aspose.PSD, vui lòng chia sẻ với chúng tôi trường hợp sử dụng của bạn bằng [Diễn đàn Aspose](https://forum.aspose.com/).


Các ví dụ bổ sung bạn có thể học từ:

- [Các trường hợp nghiên cứu](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Trưng bày](/psd/vi/net/showcases-html/)

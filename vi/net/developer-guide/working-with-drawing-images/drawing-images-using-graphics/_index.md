---
title: Vẽ Hình Ảnh bằng Đồ Họa
type: docs
weight: 20
url: /vi/net/drawing-images-using-graphics/
---

## **Vẽ Hình Ảnh bằng Đồ Họa**
Với thư viện Aspose.PSD, bạn có thể vẽ các hình dạng đơn giản như đường thẳng, hình chữ nhật và hình tròn, cũng như các hình dạng phức tạp như da giác, đường cong, cung và hình dạng Bézier. Thư viện Aspose.PSD tạo ra các hình dạng bằng Các object [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) mà thuộc về không gian tên Aspose.PSD. Các đối tượng Graphics chịu trách nhiệm thực hiện các hoạt động vẽ khác nhau trên một hình ảnh, từ đó thay đổi bề mặt của hình ảnh. Lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sử dụng một loạt các đối tượng trợ giúp để tăng cường các hình dạng:

·         Bút, để vẽ đường, đường viền hình dạng hoặc tạo các biểu diễn hình học khác.

·         Cọ, để xác định cách điền vào khu vực.

·         Phông chữ, để xác định hình dạng của các ký tự văn bản.
### **Vẽ với Lớp Graphics**
Dưới đây là một ví dụ mã nguồn minh họa việc sử dụng lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Mã nguồn ví dụ đã được chia thành nhiều phần để giữ nó đơn giản và dễ theo dõi. Từng bước, các ví dụ cho thấy cách:

1. Tạo một hình ảnh.
1. Tạo và khởi tạo đối tượng Graphics.
1. Xóa bề mặt.
1. Vẽ một hình bầu dục.
1. Vẽ một đa giác đã được điền và lưu hình ảnh.
### **Mẫu Lập Trình**
#### **Tạo Một Hình Ảnh**
Bắt đầu bằng cách tạo một hình ảnh bằng cách sử dụng bất kỳ phương pháp nào được mô tả trong Tạo Tập Tin.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Tạo và Khởi Tạo Đối Tượng Graphics**
Tiếp theo, tạo và khởi tạo một đối tượng Graphics bằng cách chuyển đối tượng Hình ảnh cho nó vào hàm tạo.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Xóa Bề Mặt**
Xóa bề mặt của Graphics bằng cách gọi phương thức Xóa của lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) và chuyển màu làm tham số. Phương thức này điền vào bề mặt của Graphics với màu được chuyển vào như một đối số.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Vẽ Một Hình Bầu Dục**
Bạn có thể thấy rằng lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) đã hiển thị nhiều phương thức để vẽ và điền các hình dạng. Bạn sẽ tìm thấy danh sách đầy đủ các phương thức trong Tài liệu tham chiếu API của Aspose.PSD cho .NET. Có một số phiên bản nạp chồng của phương thức Vẽ hình bầu dục được hiển thị bởi lớp Graphics. Tất cả các phương pháp này chấp nhận một đối tượng Bút như đối số đầu tiên. Các tham số sau được chuyển để xác định hình chữ nhật giới hạn xung quanh hình bầu dục. Ví dụ này, sử dụng phiên bản chấp nhận đối tượng Hình chữ nhật làm tham số thứ hai để vẽ một hình bầu dục bằng đối tượng Bút trong màu bạn muốn.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Vẽ Một Đa Giác Đã Được Điền**
Tiếp theo, vẽ một đa giác sử dụng Brush Tuyến tính và một mảng điểm. Lớp Graphics đã hiển thị nhiều phiên bản nạp chồng của phương thức FillPolygon(). Tất cả các phiên bản này chấp nhận một đối tượng Cọ như đối số đầu tiên, xác định các đặc tính của điền. Tham số thứ hai là một mảng điểm. Xuất hiện lưu ý, mỗi hai điểm liền kề trong mảng chỉ định một cạnh của đa giác.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Vẽ Hình Ảnh bằng Đồ Họa : Toàn Bộ Nguồn**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Tất cả các lớp mà thực hiện IDisposable và truy cập tài nguyên không quản lý được khởi tạo trong một câu lệnh Sử dụng để đảm bảo rằng chúng được xử lý đúng cách khi bị loại bỏ.

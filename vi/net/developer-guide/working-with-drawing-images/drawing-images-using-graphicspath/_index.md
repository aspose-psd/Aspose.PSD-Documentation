---
title: Vẽ Hình Ảnh bằng GraphicsPath
type: docs
weight: 30
url: /vi/net/drawing-images-using-graphicspath/
---

## **Vẽ Hình Ảnh bằng GraphicsPath**
Lớp [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) chịu trách nhiệm cho việc tạo và duy trì một đường dẫn đồ họa. GraphicsPath không có tham chiếu đến một hình ảnh và không thay đổi hình ảnh chính nó, thay vào đó, nó có thể được xem xét như một đối tượng chứa dữ liệu mô tả các đường dẫn mà lớp Graphics có thể vẽ. Lớp GraphicsPath sử dụng các hình dạng; mỗi hình dạng hoặc được tạo bởi một chuỗi liên kết các đường và cong hoặc một hình học cơ bản. Mỗi hình dạng có thể được chia thành các đoạn hình. Bạn có thể thêm, xóa và thay đổi các hình hoặc hình dạng khác nhau vào một đối tượng GraphicsPath. Khi GraphicsPath đã được mô tả đầy đủ, sử dụng các phương thức tương ứng của lớp Graphics (Vẽ Đường và Đổ Màu cho Đường) để vẽ hoặc đổ màu cho các đường. Lớp Graphics sẽ lấy từng đoạn hình dạng và vẽ chúng để tạo ra hình ảnh cuối cùng.
### **Vẽ bằng lớp GraphicsPath**
Dưới đây là một ví dụ minh họa việc sử dụng lớp [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath). Mã nguồn ví dụ đã được chia thành nhiều phần để giữ cho nó đơn giản và dễ theo dõi. Từng buớc, các ví dụ sẽ cho bạn thấy cách:

- Tạo một hình ảnh.
- Khởi tạo một đối tượng Graphics.
- Xóa bề mặt.
- Tạo một thể hiện của [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Tạo một hình dạng.
- Thêm các hình vào hình dạng.
- Tạo một mảng hình dạng.
- Vẽ đường dẫn.
- Đổ màu cho đường dẫn.


### **Vẽ Hình Ảnh bằng GraphicsPath: Mẫu Lập Trình**
#### **GraphicsPath : Tạo Một Hình Ảnh**
Bắt đầu bằng cách tạo một hình ảnh bằng bất kỳ phương pháp nào được mô tả trong Đang Tạo Tập Tin.
#### **GraphicsPath : Khởi tạo Một Đối Tượng Graphics**
Tạo và khởi tạo một đối tượng Graphics bằng cách chuyển đối tượng Image vào hàm dựng của nó.
#### **GraphicsPath : Xóa Bề Mặt**
Xóa bề mặt Graphics bằng cách gọi phương thức Clear của lớp Graphics và truyền một Màu làm tham số. Phương thức này điền bề mặt Graphics với màu được truyền vào như đối số.
#### **GraphicsPath : Tạo Một Thể Hiện Của GraphicsPath**
Tạo một thể hiện của GraphicsPath với GraphicsPath được thiết lập là Đối Lập theo mặc định. Chế độ này xác định cách điền nội vi của một hình kín. Giá trị GraphicsPath khác có thể là Winding.
#### **GraphicsPath : Tạo Một Hình Dạng**
Tạo một thể hiện của lớp Figure. Như đã thảo luận trước đó, Figure có thể chứa Shapes và các hình dạng đóng cư trú trong không gian tên Aspose.PSD.Shapes.
#### **GraphicsPath : Thêm Hình vào Hình Dạng**
Phương thức Thêm Hình mở ra bởi lớp Figure cho phép bạn thêm hình vào hình dạng. Trong các ví dụ mã dưới đây, một số hình dạng được thêm vào một đối tượng Figure.
#### **GraphicsPath : Thêm Hình vào Mảng**
Nhiều hình có thể được thêm vào một đối tượng GraphicsPath bằng cách sử dụng phương thức AddFigures mở ra bởi lớp GraphicsPath. Phương thức này chấp nhận một mảng hình như tham số.
#### **GraphicsPath : Vẽ Các Đường Dẫn**
Vẽ GraphicsPath bằng cách sử dụng phương thức DrawPath mở ra bởi lớp Graphics. Phương thức này chấp nhận hai tham số. Tham số đầu tiên là một đối tượng của lớp Pen, xác định màu sắc, độ rộng và kiểu của đường dẫn. Tham số thứ hai là đối tượng của lớp GraphicsPath, đại diện cho đường dẫn chính nó.
#### **GraphicsPath : Đổ Màu cho Các Đường Dẫn**


Bạn có thể điền vào một đường dẫn bằng cách truyền một đối tượng GraphicsPath tới phương thức Fill Paths mở ra bởi lớp Graphics. Phương thức Fill Paths điền đường dẫn theo chế độ điền (đối lập hoặc vòng quanh) hiện tại được thiết lập cho đường dẫn. Nếu đường dẫn có bất kỳ hình đóng nào, đường dẫn sẽ được điền như thể những hình đóng đó đã được đóng lại.

Phương thức Fill Paths chấp nhận hai tham số. Tham số đầu tiên là một đối tượng của bất kỳ lớp chổi nào từ không gian tên Aspose.PSD.Brushes. Tham số thứ hai là đường dẫn chính nó. Ví dụ này, sử dụng HatchBrush, một chổi hình chữ nhật với kiểu hatch, màu trước, và màu nền. Trước khi truyền đối tượng HatchBrush vào phương thức Fill Paths, hãy thiết lập các thuộc tính của nó.
### **GraphicsPath : Toàn Bộ Mã Nguồn**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Tất cả các lớp thực hiện IDisposable được khởi tạo trong một câu lệnh Using để đảm bảo rằng chúng được giải phóng đúng cách.


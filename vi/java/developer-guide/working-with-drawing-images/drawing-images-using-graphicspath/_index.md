---
title: Vẽ Ảnh sử dụng GraphicsPath
type: docs
weight: 30
url: /vi/java/drawing-images-using-graphicspath/
---

## **Vẽ Ảnh sử dụng GraphicsPath**
Lớp GraphicsPath là nơi tạo và duy trì một đường dẫn đồ họa. GraphicsPath không có tham chiếu đến một hình ảnh và không thay đổi chính hình ảnh, thay vào đó, nó có thể được coi là một đối tượng chứa siêu dữ liệu mô tả các đường dẫn mà lớp Graphics có thể vẽ. Lớp GraphicsPath sử dụng các hình thể; mỗi hình thể hoặc bao gồm một chuỗi các đường và đường cong được kết nối hoặc một hình học cơ bản. Mỗi hình thể có thể được chia thành các phân đoạn hình thể. Bạn có thể thêm, loại bỏ và thay đổi các hình thể hoặc hình dạng khác nhau trong một đối tượng GraphicsPath. Khi GraphicsPath đã được mô tả hoàn toàn, sử dụng các phương thức tương ứng của lớp Graphics (Vẽ Đường và Đổ Màu Đường) để vẽ hoặc điền đầy các đường. Lớp Graphics lấy mỗi phân đoạn hình thể và vẽ nó để tạo ra hình ảnh cuối cùng.

### **Vẽ sử dụng lớp GraphicsPath**
Dưới đây là một ví dụ minh họa việc sử dụng lớp GraphicsPath. Mã nguồn ví dụ đã được chia thành nhiều phần để giữ nó đơn giản và dễ theo dõi. Từng bước, các ví dụ sẽ chỉ cho bạn cách:

- Tạo một hình ảnh.
- Khởi tạo một đối tượng Graphics.
- Xóa bề mặt.
- Tạo một thể hiện của GraphicsPath.
- Tạo một hình thể.
- Thêm hình dạng vào hình thể.
- Tạo một mảng các hình dạng.
- Vẽ đường dẫn.
- Đổ màu đường dẫn.


### **Vẽ Ảnh sử dụng GraphicsPath: Mẫu Lập Trình**
#### **GraphicsPath : Tạo một Hình Ảnh**
Bắt đầu bằng cách tạo một hình ảnh bằng cách sử dụng bất kỳ phương pháp nào được mô tả trong Việc Tạo Tệp.
#### **GraphicsPath : Khởi tạo Một Đối Tượng Graphics**
Tạo và khởi tạo một đối tượng Graphics bằng cách chuyển đối tượng Hình ảnh vào hàm tạo của nó.
#### **GraphicsPath : Xóa Bề Mặt**
Xóa bề mặt Đồ họa bằng cách gọi phương thức Clear của lớp Graphics và chuyển một Màu làm tham số. Phương thức này điền bề mặt đồ họa bằng màu được chuyển làm đối số.
#### **GraphicsPath : Tạo Một Thể Hiện của GraphicsPath**
Tạo một thể hiện của GraphicsPath với GraphicsPath được đặt thành Alternate theo mặc định. Chế độ này xác định cách điền bên trong của một hình kín. Giá trị GraphicsPath khác có thể là Winding.
#### **GraphicsPath : Tạo Một Hình Thể**
Tạo một thể hiện của lớp Figure. Như đã thảo luận trước đó, Figure có thể chứa Shapes và các hình dạng ở trong không gian tên Aspose.PSD.Shapes.
#### **GraphicsPath : Thêm Hình Dạng vào Hình Thể**
Phương thức Add Shapes được tiết lộ bởi lớp Figure cho phép bạn thêm các hình dạng vào hình thể. Trong các ví dụ mã sau, một số hình dạng được thêm vào một đối tượng Figure.
#### **GraphicsPath : Thêm Hình Thể vào Một Mảng**
Nhiều hình thể có thể được thêm vào một đối tượng GraphicsPath bằng cách sử dụng phương thức AddFigures được tiết lộ bởi lớp GraphicsPath. Phương thức này chấp nhận một mảng các hình thể như tham số.
#### **GraphicsPath : Vẽ Các Đường Dẫn**
Vẽ GraphicsPath bằng cách sử dụng phương thức DrawPath được tiết lộ bởi lớp Graphics. Phương thức chấp nhận hai tham số. Tham số đầu tiên là một đối tượng của lớp Pen, xác định màu sắc, độ rộng và kiểu của đường dẫn. Tham số thứ hai là đối tượng của lớp GraphicsPath, đại diện cho chính đường dẫn.
#### **GraphicsPath : Đổ Màu Đường Dẫn**


Bạn có thể điền một đường dẫn bằng cách chuyển một đối tượng GraphicsPath vào phương thức Fill Paths được tiết lộ bởi lớp Graphics. Phương thức Fill Paths điền đường dẫn theo chế độ điền (alternate hoặc winding) hiện tại được thiết lập cho đường dẫn. Nếu đường dẫn có bất kỳ hình kín nào, đường dẫn sẽ được điền như thể các hình kín đó đã được đóng lại.

Phương thức Fill Paths chấp nhận hai tham số. Tham số thứ nhất là một đối tượng của bất kỳ lớp cọ nào từ không gian tên Aspose.PSD.Brushes. Tham số thứ hai là chính đường dẫn. Để minh họa, hãy sử dụng HatchBrush, một cái chổi hình chữ nhật với một kiểu rồi, một màu nền, và một màu nền. Trước khi chuyển đối tượng HatchBrush vào phương thức Fill Paths, hãy thiết lập các thuộc tính của nó.
### **GraphicsPath : Nguồn Mã Đầy Đủ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



Tất cả các lớp mà triển khai IDisposable đều được khởi tạo trong một câu lệnh Using để đảm bảo rằng chúng được huỷ đúng cách.

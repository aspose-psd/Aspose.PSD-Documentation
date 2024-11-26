---
title: Vẽ Hình Ảnh Sử Dụng Graphics
type: docs
weight: 20
url: /vi/java/drawing-images-using-graphics/
---

## **Vẽ Hình Ảnh Sử Dụng Graphics**

Với thư viện Aspose.PSD, bạn có thể vẽ các hình dạng đơn giản như đường thẳng, hình chữ nhật và hình tròn, cũng như các hình dạng phức tạp như đa giác, đường cong, cung và hình dạng Bézier. Thư viện Aspose.PSD tạo các hình dạng như vậy bằng cách sử dụng lớp Graphics nằm trong không gian tên Aspose.PSD. Đối tượng Graphics chịu trách nhiệm thực hiện các hoạt động vẽ khác nhau trên một hình ảnh, từ đó thay đổi bề mặt của hình ảnh. Lớp Graphics sử dụng một loạt các đối tượng trợ giúp để tăng cường các hình dạng:

- Bút, để vẽ đường, đường viền hình dạng hoặc vẽ các biểu thị hình học khác.
- Cọ, để xác định cách điền vào vùng.
- Phông chữ, để xác định hình dạng của các ký tự văn bản.

### **Vẽ với Lớp Graphics**

Dưới đây là một ví dụ mã nguồn demo về việc sử dụng lớp Graphics. Mã nguồn ví dụ đã được chia thành nhiều phần để giữ nó đơn giản và dễ theo dõi. Từng bước, ví dụ sẽ hướng dẫn cách:

1. Tạo một hình ảnh.
1. Tạo và khởi tạo một đối tượng Graphics.
1. Xóa bề mặt.
1. Vẽ một hình ellipse.
1. Vẽ một đa giác đã tô màu và lưu hình ảnh.

### **Mẫu Lập Trình**

#### **Tạo Một Hình Ảnh**

Bắt đầu bằng cách tạo một hình ảnh bằng cách sử dụng bất kỳ phương pháp nào được mô tả trong Viết Tệp.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

#### **Tạo và Khởi Tạo Một Đối Tượng Graphics**

Tiếp theo, tạo và khởi tạo một đối tượng Graphics bằng cách truyền đối tượng Image vào hàm tạo nó.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

#### **Xóa Bề Mặt**

Xóa bề mặt của Graphics bằng cách gọi phương thức Clear của lớp Graphics và truyền màu là tham số. Phương thức này sẽ lấp đầy bề mặt của Graphics bằng màu được truyền là đối số.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

#### **Vẽ Một Hình Ellipse**

Bạn có thể thấy rằng lớp Graphics đã tiết lộ rất nhiều phương thức để vẽ và tô màu các hình dạng. Bạn sẽ tìm thấy danh sách đầy đủ các phương thức trong Aspose.PSD cho Tài Liệu Tham Khảo API Java. Có một số phiên bản nạp chồng của phương thức DrawEllipse được tiết lộ bởi lớp Graphics. Tất cả các phương thức này chấp nhận một đối tượng Pen là đối số đầu tiên. Các tham số sau đó được truyền để xác định hình chữ nhật bao quanh hình ellipse. Để mục đích của ví dụ này, hãy sử dụng phiên bản chấp nhận một đối tượng Rectangle làm tham số thứ hai để vẽ một hình ellipse bằng đối tượng Pen trong màu bạn muốn.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

#### **Vẽ Một Đa Giác Đã Tô Màu**

Tiếp theo, vẽ một đa giác bằng cách sử dụng LinearGradientBrush và một mảng các điểm. Lớp Graphics đã tiết lộ một số phiên bản nạp chồng của phương thức FillPolygon. Tất cả những phương thức này chấp nhận một đối tượng Brush là đối số đầu tiên, xác định các đặc điểm của lớp fill. Tham số thứ hai là một mảng các điểm. Vui lòng lưu ý rằng mỗi hai điểm liên tiếp trong mảng xác định một cạnh của đa giác.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

### **Vẽ Hình Ảnh Sử Dụng Graphics : Mã Nguồn Đầy Đủ**

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

Tất cả các lớp thực hiện IDisposable và truy cập vào tài nguyên không quản lý được khởi tạo trong một câu lệnh Using để đảm bảo rằng chúng được loại bỏ đúng cách.


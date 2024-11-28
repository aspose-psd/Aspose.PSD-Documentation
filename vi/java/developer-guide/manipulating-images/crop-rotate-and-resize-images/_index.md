---
title: Cắt, Xoay và Thay Đổi Kích Thước Ảnh
type: docs
weight: 40
url: /vi/java/crop-rotate-and-resize-images/
---

## **Cắt Ảnh**
Cắt ảnh thường đề cập đến việc loại bỏ các phần ngoại cùng của một bức ảnh để cải thiện khung hình. Việc cắt ảnh cũng có thể được sử dụng để cắt ra một phần của một bức ảnh để tăng sự tập trung vào một khu vực cụ thể. Aspose.PSD API hỗ trợ hai phương pháp khác nhau để cắt ảnh: thông qua dịch chuyển và hình chữ nhật.
### **Cắt thông qua Dịch Chuyển**
Lớp RasterImage cung cấp một phiên bản nạp chồng của phương thức Crop chấp nhận 4 giá trị số nguyên đại diện cho Trái, Phải, Trên & Dưới. Dựa trên bốn giá trị này, phương thức Crop di chuyển ranh giới ảnh về phía trung tâm của ảnh trong khi loại bỏ phần bên ngoài. Đoạn mã dưới đây minh họa cách cắt ảnh thông qua dịch chuyển.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Cắt thông qua Hình Chữ Nhật**
Lớp RasterImage cung cấp một phiên bản nạp chồng khác của phương thức Crop chấp nhận một thể hiện của lớp Rectangle. Bạn có thể cắt ra bất kỳ phần nào của ảnh bằng cách cung cấp ranh giới mong muốn cho đối tượng Rectangle. Đoạn mã dưới đây minh họa cách Cắt bất kỳ ảnh nào thông qua Hình Chữ Nhật.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Xoay và Lật Ảnh**
Aspose.PSD cho Java là một thư viện dễ sử dụng vì nó cung cấp các phương pháp đơn giản để thực hiện các thao tác phức tạp. Ví dụ, Aspose.PSD cho Java đã cung cấp phương thức RotateFlip cho lớp cơ sở Image nếu ứng dụng cần xoay ảnh. Bất kể định dạng ảnh, thư viện có thể thực hiện quy trình xoay và lật cụ thể trên ảnh.
### **Xoay Ảnh**
Phương thức Image.RotateFlip có thể được sử dụng để xoay ảnh theo 90/180/270 độ và lật ảnh theo chiều ngang hoặc dọc. Phương thức Image.RotateFlip chấp nhận một tham số RotateFlipType xác định loại xoay và lật áp dụng cho ảnh. Các bước để thực hiện xoay và lật đơn giản như sau,

1. Tải ảnh bằng phương thức nhà máy Load được tiếp cận bởi lớp Image.
1. Gọi phương thức Image.RotateFlip trong khi xác định RotateFlipType phù hợp.
1. Lưu kết quả.

Đoạn mã ví dụ dưới đây minh họa cách thiết lập thuộc tính RotateFlip của một ảnh và liệt kê các thành viên của enum RotateFlipType.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Xoay Ảnh Theo Góc Cụ Thể**
Aspose.PSD cho Java API cung cấp phương thức RasterImage.Rotate để hỗ trợ người dùng muốn xoay ảnh theo một góc cụ thể. Khác với phương thức RasterImage.RotateFlip, phương thức RasterImage.Rotate chấp nhận ba tham số:

1. Góc xoay: Một tham số loại float chỉ định góc xoay mà ảnh phải được xoay đến. Giá trị dương xoay ảnh theo chiều kim đồng hồ; giá trị âm thực hiện xoay ngược chiều kim đồng hồ.
1. Thay đổi tỷ lệ: Một tham số loại Boolean chỉ định liệu kích thước ảnh có thay đổi theo chiếu hình chữ nhật đã xoay (điểm góc) hay không. Nếu đặt thành sai, kích thước ảnh sẽ không bị thay đổi và chỉ nội dung ảnh bên trong được xoay.
1. Màu nền: Một tham số loại Color chỉ định màu sẽ được điền vào nền của ảnh sau khi xoay.

Đoạn mã dưới đây minh họa cách sử dụng phương thức RasterImage.Rotate.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Thay Đổi Kích Thước Ảnh**
Bài viết này minh họa cách sử dụng Aspose.PSD cho Java để thực hiện thao tác Thay Đổi Kích Thước trên một bức ảnh. Aspose.PSD API đã tiết lộ các phương pháp hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD cho Java đã tiết lộ phương thức Resize cho lớp ảnh mà có thể được sử dụng để thay đổi kích thước của các hình ảnh hiện có ngay lập tức. Có hai phiên bản của phương thức Resize phù hợp với nhu cầu ứng dụng.
### **Thay Đổi Kích Thước Đơn Giản**
Các bước để thực hiện Thay Đổi Kích Thước như sau:

1. Tải ảnh bằng phương thức nhà máy Load được tiếp cận bởi lớp Image.
1. Gọi phương thức Image.Resize trong khi xác định Chiều Cao & Chiều Rộng mới.
1. Lưu kết quả.

Đoạn mã dưới đây minh họa cách thay đổi kích thước ảnh.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Thay Đổi Kích Thước với Enum ResizeType**
Aspose.PSD API đã tiết lộ liệt kê ResizeType mà có thể được sử dụng với Image.Resize để đạt kết quả mong muốn. Đoạn mã dưới đây minh họa cách sử dụng liệt kê ResizeType, trong khi chi tiết của các thành viên liệt kê ResizeType có thể được tìm thấy ở cuối trang.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



Nếu bạn muốn có kết quả chất lượng sau khi áp dụng thay đổi kích thước thì nên sử dụng ResizeType.LanczosResample vì nó sẽ sản xuất kết quả chất lượng cao nhưng có thể hoạt động chậm hơn so với ResizeType.NearestNeighbourResample. Ngược lại, thuật toán ResizeType.NearestNeighbourResample được sử dụng đặc biệt cho việc thay đổi kích thước nhanh trong khi hi sinh chất lượng ảnh. Phương pháp này có thể hữu ích cho việc tạo ảnh thu nhỏ theo thời gian thực hoặc các quá trình tương tự mà yêu cầu hiệu suất.
## **Thay Đổi Kích Thước Ảnh Tỷ Lệ**
Bạn có thể thay đổi kích thước ảnh bằng cách truyền các giá trị chiều cao và chiều rộng mới như tham số cho phương thức Image.Resize nhưng trong trường hợp đó bạn phải tính tỷ lệ khung hình mình. Điều này là do khi chiều rộng hoặc chiều cao của một ảnh bị thay đổi, ảnh sẽ được thu nhỏ hoặc phóng to để lấp đầy kích thước mới . Nếu các thay đổi đối với chiều rộng và chiều cao của một ảnh không cùng tỷ lệ này có thể dẫn đến kết quả bị kéo dài và biến dạng. Bài viết này minh họa việc sử dụng API Aspose.PSD cho Java để thay đổi kích thước ảnh bằng cách truyền vào chiều cao hoặc chiều rộng mới trong khi cho phép API tự động tính toán giá trị tỷ lệ khác.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **Liệt Kê ResizeType**
ResizeType xác định loại thay đổi kích thước sẽ được thực hiện trên ảnh dựa trên bộ lọc được chọn.

Các Thành viên của Liệt Kê ResizeType

|**Tên Thành Viên**|**Giá Trị**|**Mô Tả**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Điểm góc trên cùng bên trái của ảnh mới sẽ trùng với điểm góc trên cùng bên trái của ảnh gốc. Cắt xra sẽ xảy ra nếu cần.|
|RightTopToRightTop|1|Điểm góc trên cùng bên phải của ảnh mới sẽ trùng với điểm góc trên cùng bên phải của ảnh gốc. Cắt sẽ xảy ra nếu cần.|
|RightBottomToRightBottom|2|Điểm góc dưới cùng bên phải của ảnh mới sẽ trùng với điểm góc dưới cùng bên phải của ảnh gốc. Cắt sẽ xảy ra nếu cần.|
|LeftBottomToLeftBottom|3|Điểm góc dưới cùng bên trái của ảnh mới sẽ trùng với điểm góc dưới cùng bên trái của ảnh gốc. Cắt sẽ xảy ra nếu cần.|
|CenterToCenter|4|Chính giữa của ảnh mới sẽ trùng với chính giữa của ảnh gốc. Cắt sẽ xảy ra nếu cần.|
|LanczosResample|5|Resample bằng thuật toán Lanczos sử dụng bộ lọc 7x7.|
|NearestNeighbourResample|6|Resample bằng thuật toán hàng xóm gần nhất.|

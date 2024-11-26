---
title: Cắt, Xoay và Thay Đổi Kích Thước Hình Ảnh
type: docs
weight: 40
url: /vi/net/crop-rotate-and-resize-images/
---

## **Cắt Hình Ảnh**
Việc cắt hình ảnh thường đề cập đến việc loại bỏ các phần ngoài cùng của một hình ảnh để giúp cải thiện khung hình. Việc cắt ảnh cũng có thể được sử dụng để cắt bớt một phần của hình ảnh để tăng tập trung vào một khu vực cụ thể. Aspose.PSD API hỗ trợ hai phương pháp khác nhau để cắt hình ảnh: bằng dịch chuyển và hình chữ nhật.
### **Cắt bằng Dịch Chuyển**
Lớp [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) cung cấp một phiên bản nạp chồng của phương thức Crop chấp nhận 4 giá trị số nguyên đại diện cho Trái, Phải, Trên và Dưới. Dựa trên bốn giá trị này, phương thức Crop di chuyển ranh giới hình ảnh về phía trung tâm của hình ảnh trong khi loại bỏ phần ngoài cùng. Đoạn mã dưới đây minh họa cách cắt hình ảnh bằng dịch chuyển.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **Cắt bằng Hình Chữ Nhật**
Lớp [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) cung cấp một phiên bản nạp chồng khác của phương thức Crop chấp nhận một thể hiện của lớp Rectangle. Bạn có thể cắt bất kỳ phần nào của hình ảnh bằng cách cung cấp ranh giới mong muốn cho đối tượng Rectangle. Đoạn mã dưới đây minh họa cách Cắt ảnh bất kỳ bằng Hình Chữ Nhật.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **Xoay và Lật Hình Ảnh**
Aspose.PSD cho .NET là một thư viện dễ sử dụng vì nó cung cấp các phương thức đơn giản để thực hiện các hoạt động phức tạp. Ví dụ, Aspose.PSD cho .NET đã cung cấp phương thức RotateFlip cho lớp cơ sở Image nếu một ứng dụng cần xoay một hình ảnh. Bất kể định dạng hình ảnh, thư viện có thể thực hiện thao tác cụ thể Rotate & Flip trên nó.
### **Xoay một Hình Ảnh**
Phương thức Image.RotateFlip có thể được sử dụng để xoay hình ảnh 90/180/270 độ và lật hình ảnh theo chiều ngang hoặc chiều dọc. Phương thức Image.RotateFlip chấp nhận một tham số RotateFlipType chỉ định loại xoay và lật áp dụng cho hình ảnh. Các bước để thực hiện Rotate & Flip như sau,

1. Tải hình ảnh bằng phương thức nhà máy Load được tiết lộ bởi lớp Image.
1. Gọi phương thức Image.RotateFlip trong khi chỉ định RotateFlipType phù hợp.
1. Lưu kết quả.

Ví dụ mã sau minh họa cách thiết lập thuộc tính RotateFlip của một Hình ảnh và liệt kê RotateFlipType.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **Xoay một Hình Ảnh Theo Góc Cụ Thể**
Aspose.PSD cho .NET API tiết lộ phương thức [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate để hỗ trợ người dùng muốn xoay một hình ảnh theo một góc cụ thể. Không giống như phương thức [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip, phương thức [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate chấp nhận ba tham số:

1. Góc xoay: Một tham số kiểu số thực xác định góc quay mà hình ảnh sẽ được xoay đến. Một giá trị dương xoay hình ảnh theo chiều kim đồng hồ; một giá trị âm thực hiện việc xoay ngược chiều kim đồng hồ.
1. Thay đổi kích thước tỷ lệ: Một tham số kiểu Boolean xác định xem kích thước hình ảnh có cần phải thay đổi theo chiều chiếu của hình chữ nhật xoay (các điểm góc). Nếu đặt thành sai, kích thước hình ảnh sẽ không thay đổi và chỉ nội dung hình ảnh bên trong được xoay.
1. Màu nền: Một tham số kiểu Color chỉ định màu được điền vào phần nền của hình ảnh sau khi xoay.

Đoạn mã dưới đây minh họa việc sử dụng phương thức [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **Thay Đổi Kích Thước Hình Ảnh**
Bài viết này minh họa cách sử dụng Aspose.PSD cho .NET để thực hiện thao tác Thay Đổi Kích Thước trên một hình ảnh. Các API Aspose.PSD đã tiết lộ các phương thức hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD cho .NET đã tiết lộ phương thức Resize cho lớp Image mà có thể được sử dụng để thay đổi kích thước hình ảnh hiện có ngay lập tức. Có hai phiên bản của phương thức Resize để phù hợp với nhu cầu ứng dụng.
### **Thay Đổi Kích Thước Đơn Giản**
Các bước để thực hiện Thay Đổi Kích Thước như sau:

1. Tải hình ảnh bằng phương thức nhà máy Load được tiết lộ bởi lớp Image.
1. Gọi phương thức Image.Resize trong khi chỉ định chiều Cao & Rộng mới.
1. Lưu kết quả.

Ví dụ mã sau minh họa cách Thay Đổi Kích Thước một hình ảnh.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **Thay Đổi Kích Thước với Enumeration ResizeType**
Aspose.PSD API đã tiết lộ Enumeration ResizeType có thể được sử dụng với Image.Resize để đạt được các kết quả mong muốn. Đoạn mã cung cấp dưới đây minh họa việc sử dụng Enumeration ResizeType, trong khi chi tiết các thành viên Enumeration ResizeType có thể được tìm thấy dưới cùng trang này.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}

Nếu bạn muốn có kết quả chất lượng sau khi áp dụng thay đổi kích thước thì nên sử dụng ResizeType.LanczosResample vì nó sẽ tạo ra kết quả chất lượng cao nhưng có thể hoạt động chậm hơn so với ResizeType.NearestNeighbourResample. Ngược lại, thuật toán ResizeType.NearestNeighbourResample được sử dụng đặc biệt cho việc thay đổi kích thước nhanh trong khi đánh đổi chất lượng hình ảnh. Phương pháp này có thể hữu ích cho việc tạo hình ảnh xem trước trong thời gian thực hoặc các quy trình tương tự nơi hiệu suất được yêu cầu.
## **Thay Đổi Kích Thước Hình Ảnh Theo Tỷ Lệ**
Bạn có thể thay đổi kích thước hình ảnh bằng cách truyền các giá trị chiều cao & rộng mới như tham số cho phương thức Image.Resize nhưng trong trường hợp đó bạn phải tự tính tỉ lệ khung hình. Điều này bởi khi chiều rộng hoặc cao của một hình ảnh thay đổi, hình ảnh sẽ được thu nhỏ hoặc mở rộng để điền vào kích thước mới. Nếu sự thay đổi về chiều rộng và chiều cao của một hình ảnh không cân xứng này có thể dẫn đến kết quả bị căng và biến dạng. Bài viết này minh họa việc sử dụng Aspose.PSD cho .NET API để thay đổi kích thước hình ảnh bằng cách truyền một trong hai giá trị mới về chiều cao hoặc chiều rộng trong khi cho phép API tự động tính giá trị tỷ lệ khác.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **Enumeration ResizeType**
ResizeType xác định loại thay đổi kích thước được thực hiện trên hình ảnh dựa trên bộ lọc đã chọn.

Các thành viên của Enumeration [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)

|**Tên Thành Viên**|**Giá Trị**|**Mô Tả**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Điểm trái trên của hình ảnh mới sẽ trùng với điểm trái trên của hình ảnh ban đầu. Thu gọn sẽ xảy ra nếu cần.|
|RightTopToRightTop|1|Điểm phải trên của hình ảnh mới sẽ trùng với điểm phải trên của hình ảnh ban đầu. Thu gọn sẽ xảy ra nếu cần.|
|RightBottomToRightBottom|2|Điểm phải dưới của hình ảnh mới sẽ trùng với điểm phải dưới của hình ảnh ban đầu. Thu gọn sẽ xảy ra nếu cần.|
|LeftBottomToLeftBottom|3|Điểm trái dưới của hình ảnh mới sẽ trùng với điểm trái dưới của hình ảnh ban đầu. Thu gọn sẽ xảy ra nếu cần.|
|CenterToCenter|4|Trung tâm của hình ảnh mới sẽ trùng với trung tâm của hình ảnh ban đầu. Thu gọn sẽ xảy ra nếu cần.|
|LanczosResample|5|Thu mẫu sử dụng giải thuật Lanczos sử dụng mặt nạ 7x7.|
|NearestNeighbourResample|6|Thu mẫu sử dụng giải thuật người hàng xóm gần nhất.|

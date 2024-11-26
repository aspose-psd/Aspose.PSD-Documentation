---
title: Chỉnh Sửa Ảnh
type: docs
weight: 50
url: /vi/java/chinh-sua-anh/
---

## **Dithering cho Hình Ảnh Raster**
Dithering là một kỹ thuật tạo ra ảo ảnh màu mới bằng cách thay đổi mẫu các chấm thực sự tạo nên một bức ảnh. Đây là phương pháp phổ biến nhất để giảm phạm vi màu của ảnh xuống còn 256 (hoặc ít hơn). Aspose.PSD cung cấp hỗ trợ dithering cho lớp RasterImage bằng cách giới thiệu phương thức Dither chấp nhận hai tham số. Tham số đầu tiên là kiểu DitheringMethod được áp dụng với hai tùy chọn FloydSteinbergDithering và ThresholdDithering. Tham số thứ hai cho phương thức Dither là BitCount dạng số nguyên. BitCount xác định kích thước lấy mẫu cho kết quả dithering. Giá trị mặc định là 1 đại diện cho đen và trắng, trong khi các giá trị cho phép là 1, 4, 8 tạo ra các bảng màu với 2, 4 và 256 màu tương ứng.



## **Điều chỉnh Độ Sáng, Độ Tương Phản và Gamma**
Điều chỉnh màu sắc trong các hình ảnh số là một trong những tính năng cốt lõi mà hầu hết các thư viện xử lý ảnh cung cấp. Điều chỉnh màu sắc có thể được phân loại theo các mục sau.

1. Độ sáng đề cập đến sự sáng hoặc tối của màu sắc. Tăng độ sáng của một hình ảnh sẽ làm cho tất cả các màu sáng hơn trong khi giảm độ sáng làm tối hơn tất cả các màu sắc.
1. Tương phản đề cập đến việc làm cho các đối tượng hoặc chi tiết trong một hình ảnh rõ ràng hơn. Tăng độ tương phản của một hình ảnh sẽ làm tăng sự khác biệt giữa các khu vực sáng và tối để các khu vực sáng trở nên sáng hơn và khu vực tối trở nên tối hơn. Giảm độ tương phản sẽ khiến cho khu vực sáng và tối ở độ tương tự như nhau nhưng tổng thể hình ảnh trở nên đồng đều hơn.
1. Gamma tối ưu hóa độ tương phản và độ sáng của ánh sáng gián tiếp chiếu sáng một vật trong ảnh.
### **Điều chỉnh Độ Sáng**
Aspose.PSD cho API Java cung cấp phương thức AdjustBrightness cho lớp RasterImage mà có thể được sử dụng để điều chỉnh độ sáng của hình ảnh bằng cách truyền một giá trị số nguyên làm tham số. Giá trị tham số cao nhất đại diện cho một hình ảnh sáng hơn. Dưới đây là hình ảnh gốc và hình ảnh kết quả để so sánh.



### **Điều chỉnh Độ Tương Phản**
Phương thức AdjustContrast được tiết lộ bởi lớp RasterImage có thể được sử dụng để điều chỉnh Độ Tương Phản của một hình ảnh bằng cách truyền một giá trị float làm tham số.

Giá trị tham số cao nhất đại diện cho một độ tương phản cao hơn trong hình ảnh cụ thể. Dưới đây là hình ảnh gốc và hình ảnh kết quả để so sánh.



### **Điều chỉnh Gamma**
Phương thức AdjustGamma được tiết lộ bởi lớp RasterImage có hai phiên bản. Một trong số các phiên bản chấp nhận một giá trị float và thực hiện sự sửa Gamma cho các hệ số kênh đỏ, xanh lá cây và xanh dương. Trong khi phiên bản khác chấp nhận ba tham số float đại diện cho mỗi hệ số màu một cách riêng lẻ. Đoạn mã dưới đây cho thấy cách Điều chỉnh Gamma trên một hình ảnh.



## **Làm Mờ Một Hình Ảnh**
Bài viết này mô tả cách sử dụng Aspose.PSD cho Java để thực hiện hiệu ứng Làm Mờ trên một hình ảnh. API Aspose.PSD đã tiết lộ các phương thức hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD cho Java đã tiết lộ lớp GaussianBlurFilterOptions để tạo ra một hiệu ứng mờ ngay lập tức. Lớp GaussianBlurFilterOptions cần các giá trị bán kính và sigma để tạo ra một hiệu ứng mờ trên một hình ảnh. Các bước để thực hiện Resize đơn giản như sau:

1. Tải một hình ảnh bằng phương thức cung cấp sẵn Load bởi lớp Image.
1. Chuyển đổi hình ảnh thành RasterImage.
1. Tạo một phiên bản của lớp GaussianBlurFilterOptions với hàm tạo mặc định hoặc cung cấp giá trị bán kính và sigma trong hàm tạo.
1. Gọi phương thức RasterImage.Filter trong khi chỉ định hình chữ nhật là ranh giới hình ảnh và phiên bản lớp GaussianBlurFilterOptions.
1. Lưu kết quả.

Đoạn mã dưới đây cho thấy cách tạo hiệu ứng mờ trên một hình ảnh.



## **Xác minh Độ Trong Suốt của Hình Ảnh**
Bài viết này mô tả cách sử dụng Aspose.PSD cho Java để kiểm tra độ trong suốt của hình ảnh. Các bước để kiểm tra độ trong suốt của hình ảnh đơn giản như sau:

1. Tải một hình ảnh bằng phương thức nhà máy Tải được tiết lộ bởi lớp Image.
1. Kiểm tra độ trong suốt hình ảnh, nếu độ trong suốt là không, hình ảnh là trong suốt.
1. Đoạn mã dưới đây cho thấy cách kiểm tra hình ảnh có trong suốt hay không.

## **Thực hiện Máy Nén GIF Mất Số**
Sử dụng Aspose.PSD cho Java, nhà phát triển có thể chỉ định sự khác biệt pixel. Việc nén của GIF dựa trên một "từ điển" các chuỗi các pixel đã thấy. Bộ mã hóa thông thường tìm kiếm từ điển cho chuỗi dài nhất của các pixel khớp hoàn toàn với các pixel trong hình ảnh. Bộ mã hóa mất số chọn chuỗi dài nhất của các pixel là "đủ tương tự" với các pixel trong hình ảnh. Dưới đây là sự thể hiện mã của chức năng nói trên.



## **Thực Hiện Tân Sử Dụng Bicubic**
Tân sử dụng có nghĩa là bạn đang thay đổi kích thước pixel của một hình ảnh. Khi bạn giảm kích thước, bạn đang loại bỏ các pixel và do đó xóa thông tin và chi tiết từ hình ảnh của bạn. Khi bạn tăng kích thước, bạn đang thêm pixel. Photoshop thêm các pixel này bằng cách sử dụng quy tắc lồng tiếp. Bài viết này mô tả cách bạn có thể thực hiện Tân Sử Dụng Bicubic bằng cách sử dụng Aspose.PSD cho Java.

Dưới đây là cuồi mã của chức năng đề cập đến.


## **Tích Hợp Lớp Điều Chỉnh Ngược**
Bài viết này mô tả cách bạn có thể thực hiện **lớp điều chinh ngược** bằng cách sử dụng Aspose.PSD cho Java. Một lớp điều chinh là một loại lớp đặc biệt được sử dụng chủ yếu cho việc sửa màu sắc. Thay vì có một nội dung riêng, chúng điều chỉnh thông tin trên các lớp bên dưới. Lớp điều chinh ngược tạo ra hiệu ứng ảnh âm bằng cách đảo ngược màu sắc của một bức ảnh.

Dưới đây là cuối mã của chức năng đề cập đến.

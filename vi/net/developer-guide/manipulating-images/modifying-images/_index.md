---
title: Chỉnh sửa Ảnh
type: docs
weight: 50
url: /vi/net/chinh-sua-anh/
---

## **Dùng Phương pháp Dithering cho Hình Ảnh Raster**
Dithering là một kỹ thuật tạo ảo giác về màu sắc và bóng bằng cách biến đổi mẫu các chấm thực sự tạo ra một hình ảnh. Đây là phương pháp phổ biến nhất để giảm phạm vi màu sắc của hình ảnh xuống còn 256 (hoặc ít hơn) màu. Aspose.PSD cung cấp việc hỗ trợ dithering cho lớp [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) bằng cách giới thiệu phương thức Dither, nhận hai tham số. Tham số đầu tiên thuộc kiểu DitheringMethod sẽ được áp dụng với hai tùy chọn là FloydSteinbergDithering và ThresholdDithering. Tham số thứ hai cho phương thức [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) là BitCount ở dạng số nguyên. BitCount xác định kích thước mẫu cho kết quả của dithering. Giá trị mặc định là 1 đại diện cho đen và trắng, trong khi các giá trị cho phép khác nhau là 1, 4, 8 tạo ra bảng màu với 2, 4 và 256 màu tương ứng.

## **Điều chỉnh Độ Sáng, Kontrast và Gamma**
Việc điều chỉnh màu sắc trong hình ảnh số là một trong những tính năng chính mà hầu hết các thư viện xử lý hình ảnh cung cấp. Điều chỉnh màu sắc có thể được phân loại như sau.

1. Độ Sáng đề cập đến sự sáng hoặc tối của một màu sắc. Tăng độ sáng của một hình ảnh làm cho tất cả các màu sắc trở nên sáng hơn trong khi giảm độ sáng làm cho tất cả các màu sắc trở nên tối đen.
1. Kontrast đề cập đến việc làm cho các đối tượng hoặc chi tiết trong hình ảnh rõ rệt hơn. Tăng kontrast của một hình ảnh tăng sự khác biệt giữa vùng sáng và tối để vùng sáng trở nên sáng hơn và vùng tối trở nên tối hơn. Giảm kontrast sẽ làm cho vùng sáng và tối duy trì xấp xỉ như nhau nhưng tổng thể hình ảnh trở nên đồng nhất hơn.
1. Gamma tinh chỉnh độ tương phản và độ sáng của ánh sáng gián tiếp đang chiếu sáng vào một đối tượng trong hình ảnh.

### **Điều chỉnh Độ Sáng**
Aspose.PSD cho .NET API cung cấp phương thức [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) cho lớp [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) có thể được sử dụng để điều chỉnh độ sáng của hình ảnh bằng cách truyền 1 giá trị số nguyên làm tham số. Giá trị tham số cao nhất đề cập đến một hình ảnh sáng hơn. Dưới đây là hình ảnh gốc và hình ảnh kết quả để so sánh.

### **Điều chỉnh Kontrast**
Phương thức [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) được tiết lộ bởi lớp [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) có thể được sử dụng để điều chỉnh Kontrast của hình ảnh bằng cách truyền giá trị float làm tham số.

### **Điều chỉnh Gamma**
Phương thức [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) được tiết lộ bởi lớp [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) có hai phiên bản. Một trong số các phiên bản chấp nhận một giá trị float và thực hiện việc hiệu chỉnh Gamma cho các hệ số kênh đỏ, xanh lục và xanh lam. Trong khi phiên bản khác chấp nhận ba tham số float đại diện cho mỗi hệ số màu riêng lẻ. Đoạn mã dưới đây thể hiện cách Điều chỉnh Gamma trên một hình ảnh.

## **Làm Mờ một Hình Ảnh**
Bài viết này thể hiện cách sử dụng Aspose.PSD cho .NET để thực hiện hiệu ứng Làm Mờ trên một hình ảnh. API của Aspose.PSD đã tiết lộ các phương pháp hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD cho .NET đã tiết lộ lớp [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) để tạo hiệu ứng làm mờ ngay lập tức. Lớp [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) cần giá trị bán kính và sigma để tạo hiệu ứng làm mờ trên hình ảnh. Các bước để thực hiện Resize như sau:

1. Tải hình ảnh bằng phương thức tạo mẫu Load được tiết lộ bởi lớp Image.
1. Chuyển đổi hình ảnh thành [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Tạo một thể hiện của lớp [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) với hàm tạo mặc định hoặc cung cấp giá trị bán kính và sigma trong hàm tạo.
1. Gọi phương thức [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter trong khi chỉ định hình chữ nhật là ranh giới hình ảnh và thể hiện của lớp [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Lưu kết quả.

## **Xác minh Độ Trong suốt của Hình Ảnh**
Bài viết này thể hiện cách sử dụng Aspose.PSD cho .NET để kiểm tra độ trong suốt của hình ảnh. Các bước để kiểm tra độ trong suốt của hình ảnh như sau:

1. Tải hình ảnh bằng phương thức tạo Load được tiết lộ bởi lớp [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Kiểm tra độ mờ nếu độ mờ bằng không thì hình ảnh trong suốt.
1. Đoạn mã dưới đây thể hiện cách kiểm tra hình ảnh có trong suốt hay không.

## **Thực hiện Bộ nén GIF mất điểm**
Sử dụng Aspose.PSD cho .NET, nhà phát triển có thể đặt sự khác biệt giữa các điểm ảnh. Nén GIF dựa trên một "từ điển" của chuỗi các điểm ảnh thấy. Bộ mã hóa bình thường tìm kiếm từ điển để tìm chuỗi dài nhất của các điểm ảnh khớp chính xác với các điểm ảnh trong hình ảnh. Bộ mã hóa mất điểm chọn chuỗi dài nhất của các điểm ảnh "đủ giống" với các điểm ảnh trong hình ảnh. Dưới đây là minh họa mã của chức năng này.

## **Thực hiện Bộ lọc Bicubic Resampling**
Resampling đề cập đến việc thay đổi kích thước pixel của một hình ảnh. Khi bạn giảm mẫu, bạn đang loại bỏ các pixel và do đó xóa thông tin và chi tiết khỏi hình ảnh của bạn. Khi bạn tăng mẫu, bạn đang thêm các pixel. Photoshop thêm các pixel này bằng cách sử dụng nội suy. Bài viết này thể hiện cách bạn có thể thực hiện Bộ lọc Bicubic Resampling bằng cách sử dụng Aspose.PSD cho .NET.

## **Lớp Điều chỉnh Cân Bằng Màu Sắc**
Bài viết này thể hiện cách sử dụng Aspose.PSD cho .NET để thực hiện **lớp điều chỉnh cân bằng màu sắc** trên một hình ảnh. Lớp điều chỉnh cân bằng màu sắc cho phép bạn điều chỉnh màu sắc của hình ảnh của họ. Nó hiển thị ba kênh màu và màu bù của chúng và bạn có thể điều chỉnh sự cân bằng của các cặp màu này để thay đổi diện mạo của một bức ảnh.

## **Lớp Điều chỉnh Đảo Ngược**
Bài viết này thể hiện cách bạn có thể thực hiện **lớp điều chỉnh đảo ngược** bằng cách sử dụng Aspose.PSD cho .NET. Lớp điều chỉnh là một loại lớp đặc biệt được sử dụng chủ yếu để hiệu chỉnh màu sắc. Thay vì có nội dung riêng, chúng điều chỉnh thông tin trên các lớp dưới nó. Lớp điều chỉnh Đảo ngược tạo hiệu ứng ảnh âm bằng cách đảo ngược màu sắc của hình ảnh.

---
title: Chuyển đổi hình ảnh
type: docs
weight: 20
url: /vi/java/chuyen-doi-hinh-anh/
---

## **Chuyển đổi hình ảnh thành Đen Trắng và Màu xám**
Đôi khi bạn có thể cần chuyển đổi hình ảnh màu sang Đen Trắng hoặc Màu xám để in ấn hoặc lưu trữ. Bài viết này thể hiện việc sử dụng Aspose.PSD cho API Java để đạt được điều này bằng cách sử dụng hai phương pháp như sau.

- Nhị phân
- Màu xám
### **Nhị phân**
Để hiểu khái niệm Nhị phân, quan trọng là định nghĩa Hình ảnh Nhị phân; đó là một hình ảnh kỹ thuật số chỉ có hai giá trị có thể cho mỗi điểm ảnh. Thông thường, hai màu được sử dụng cho hình ảnh nhị phân là đen và trắng tuy nhiên bất kỳ hai màu nào cũng có thể được sử dụng. Nhị phân là quá trình chuyển đổi hình ảnh thành hai cấp độ nghĩa là mỗi điểm ảnh được lưu trữ dưới dạng một bit duy nhất (0 hoặc 1) trong đó 0 biểu thị sự vắng màu và 1 có nghĩa là có màu. Aspose.PSD cho API Java hiện hỗ trợ hai phương pháp Nhị phân.
#### **Nhị phân với Ngưỡng Cố Định**
Đoạn mã dưới đây cho thấy cách sử dụng nhị phân với ngưỡng cố định có thể được áp dụng cho một hình ảnh.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Nhị phân với Ngưỡng Otsu**
Đoạn mã dưới đây cho thấy cách sử dụng nhị phân với ngưỡng Otsu có thể được áp dụng cho một hình ảnh.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Chuyển đổi Màu xám**
Chuyển đổi Màu xám là quá trình chuyển đổi hình ảnh liên tục sang hình ảnh với các tông màu xám không liên tục. Đoạn mã dưới đây cho thấy cách sử dụng Chuyển đổi Màu xám.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Chuyển đổi Lớp Hình Ở Định dạng GIF Sang Ảnh TIFF**
Đôi khi cần phải trích xuất và chuyển đổi các lớp của một Hình ảnh PSD sang một định dạng ảnh raster khác để đáp ứng nhu cầu của ứng dụng. API Aspose.PSD hỗ trợ tính năng trích xuất và chuyển đổi các lớp của Hình ảnh PSD sang một định dạng ảnh raster khác. Đầu tiên, chúng ta sẽ tạo một thể hiện của hình ảnh và tải hình ảnh PSD từ ổ đĩa cục bộ, sau đó chúng ta sẽ lặp qua từng lớp trong thuộc tính Layer. Sau đó chúng ta sẽ chuyển đổi khối sang hình ảnh TIFF. Đoạn mã dưới đây cho thấy cách chuyển đổi các lớp hình ảnh PSD sang ảnh TIFF.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **Chuyển đổi CMYK PSD thành CMYK TIFF**
Sử dụng Aspose.PSD cho Java, nhà phát triển có thể chuyển đổi tệp CMYK PSD thành định dạng tiff CMYK. Bài viết này thể hiện cách xuất / chuyển đổi tệp CMYK PSD thành định dạng tiff CMYK với Aspose.PSD. Sử dụng Aspose.PSD cho Java, bạn có thể tải hình ảnh PSD và sau đó bạn có thể thiết lập các thuộc tính khác nhau bằng lớp TiffOptions và lưu hoặc xuất hình ảnh. Đoạn mã dưới đây cho thấy cách đạt được tính năng này.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Xuất Ảnh**
Bên cạnh một bộ công cụ xử lý hình ảnh phong phú, Aspose.PSD cung cấp các lớp chuyên biệt để chuyển đổi định dạng tệp PSD sang các định dạng khác. Sử dụng thư viện này, chuyển đổi hình ảnh PSD rất đơn giản và trực quan. Dưới đây là một số lớp chuyên biệt cho mục đích này trong không gian tên ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Dễ dàng xuất ảnh PSD với Aspose.PSD cho API Java. Tất cả những gì bạn cần là một đối tượng của lớp phù hợp từ không gian tên ImageOptions. Bằng cách sử dụng các lớp này, bạn có thể dễ dàng xuất bất kỳ hình ảnh nào được tạo, chỉnh sửa hoặc đơn giản chỉ được tải với Aspose.PSD cho Java sang bất kỳ định dạng nào được hỗ trợ.
## **Kết hợp Hình Ảnh**
Ví dụ này sử dụng lớp Graphics và thể hiện cách kết hợp hai hoặc nhiều hình ảnh thành một hình ảnh hoàn chỉnh duy nhất. Để thể hiện thao tác, ví dụ tạo một PsdImage mới và vẽ hình ảnh trên bề mặt bố cục bằng cách sử dụng phương thức Draw Image được tiết lộ bởi lớp Graphics. Bằng cách sử dụng lớp Graphics, hai hoặc nhiều hình ảnh có thể được kết hợp một cách sao cho hình ảnh kết quả sẽ trông như một hình ảnh hoàn chỉnh không có khoảng trống giữa các phần hình ảnh và không có trang. Kích thước bố cục phải bằng kích thước của hình ảnh kết quả. Dưới đây là đoạn mã thể hiện cách sử dụng phương thức Draw Image của lớp Graphics để kết hợp hình ảnh trong một hình ảnh duy nhất.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Mở rộng và Cắt Hình Ảnh**
Aspose.PSD API cho phép bạn mở rộng hoặc cắt một hình ảnh trong quá trình chuyển đổi hình ảnh. Nhà phát triển cần tạo một hình chữ nhật với tọa độ X và Y và xác định chiều rộng và chiều cao của hộp hình chữ nhật. Tọa độ X, Y và Chiều rộng, Chiều cao của hình chữ nhật sẽ miêu tả việc mở rộng hoặc cắt hình ảnh đã tải. Nếu cần mở rộng hoặc cắt hình ảnh trong quá trình chuyển đổi hình ảnh, thực hiện các bước sau:

1. Tạo một thể hiện của lớp RasterImage và tải hình ảnh hiện có.
1. Tạo một thể hiện của lớp ImageOption.
1. Tạo một thể hiện của lớp Rectangle và khởi tạo tọa độ X,Y và Chiều rộng, Chiều cao của hình chữ nhật.
1. Gọi phương thức Save của lớp RasterImage khi truyền tên tệp đầu ra, các tùy chọn hình ảnh và đối tượng hình chữ nhật làm tham số.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Đọc và Ghi Dữ Liệu XMP Cho Hình Ảnh**
XMP (Extensible Metadata Platform) là một tiêu chuẩn ISO. XMP chuẩn hóa mô hình dữ liệu, định dạng serialization và các thuộc tính cốt lõi cho định nghĩa và xử lý dữ liệu từ tiêu chuẩn. Nó cũng cung cấp hướng dẫn cho việc nhúng thông tin XMP vào hình ảnh phổ biến như JPEG, mà không làm hỏng khả năng đọc của chúng bởi các ứng dụng không hỗ trợ XMP. Sử dụng Aspose.PSD cho API Java, nhà phát triển có thể đọc hoặc ghi siêu dữ liệu XMP vào hình ảnh. Bài viết này thể hiện cách XMP metadata có thể được đọc từ hình ảnh và ghi siêu dữ liệu XMP vào hình ảnh.
### **Tạo Siêu Dữ liệu XMP, Ghi Nó Và Đọc Từ Tệp**
Với sự trợ giúp của không gian tên XMP, nhà phát triển có thể tạo đối tượng dữ liệu XMP metadata và ghi vào hình ảnh. Đoạn mã dưới đây cho thấy cách sử dụng các gói XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage và DublinCorePackage chứa trong không gian tên XMP.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Xuất Ảnh trong Môi trường Đa Luồng**
Aspose.PSD cho Java hiện hỗ trợ chuyển đổi ảnh trong môi trường đa luồng. Aspose.PSD cho Java đảm bảo hiệu suất tối ưu của các hoạt động trong quá trình thực thi mã trong môi trường đa luồng. Tất cả các lớp tùy chọn hình ảnh (ví dụ: BmpOptions, TiffOptions, JpegOptions, v.v.) trong Aspose.PSD cho Java thực thi giao diện IDisposable. Do đó, nhà phát triển cần đánh giá đúng các đối tượng lớp tùy chọn hình ảnh trong trường hợp đã thiết lập thuộc tính Nguồn. Đoạn mã dưới đây thể hiện chức năng đã nêu.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



Aspose.PSD hiện hỗ trợ thuộc tính SyncRoot khi làm việc trong môi trường đa luồng. Nhà phát triển có thể sử dụng thuộc tính này để đồng bộ hóa truy cập đến luồng nguồn. Đoạn mã dưới đây thể hiện cách sử dụng thuộc tính SyncRoot.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

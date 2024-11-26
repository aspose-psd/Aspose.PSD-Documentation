---
title: Chuyển đổi Hình Ảnh
type: docs
weight: 20
url: /vi/net/chuyen-doi-hinh-anh/
---

## **Chuyển Đổi Hình Ảnh Sang Trắng Đen và Nửa Màu**
Đôi khi bạn có thể cần chuyển đổi hình ảnh màu sang trắng đen hoặc nửa màu để in ấn hoặc lưu trữ. Bài viết này thể hiện việc sử dụng Aspose.PSD cho API .NET để đạt được điều này bằng hai phương pháp như dưới đây.

- Nhị phân
- Màu xám
### **Nhị phân**
Để hiểu về khái niệm Nhị phân, quan trọng là xác định Hình ảnh Nhị phân; đó là một hình ảnh kỹ thuật số chỉ có hai giá trị có thể cho mỗi pixel. Thông thường, hai màu sắc được sử dụng cho hình ảnh nhị phân là đen và trắng mặc dù bất kỳ hai màu nào cũng có thể được sử dụng. Nhị phân hóa là quá trình chuyển đổi hình ảnh thành mức nền nghĩa là mỗi pixel được lưu trữ như một bit đơn (0 hoặc 1) với 0 biểu thị sự vắng màu và 1 có nghĩa là sự hiện diện của màu sắc. Aspose.PSD cho API .NET hiện đang hỗ trợ hai phương pháp Nhị phân.
#### **Nhị Phân với Ngưỡng Cố Định**
Snippet mã dưới đây cho bạn thấy cách áp dụng nhị phân hóa với ngưỡng cố định cho một hình ảnh.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Nhị Phân với Ngưỡng Otsu**
Snippet mã dưới đây cho bạn thấy cách áp dụng nhị phân hóa với ngưỡng Otsu cho một hình ảnh.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Màu Xám**
Màu xám là quá trình chuyển đổi hình ảnh liên tục thành hình ảnh với các mảng màu xám không liên tục. Snippet mã dưới đây cho bạn thấy cách sử dụng Màu xám.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}


## **Chuyển Đổi Lớp Hình Ảnh GIF Sang Hình Ảnh TIFF**
Đôi khi cần phải trích xuất và chuyển đổi các lớp của một Hình ảnh PSD sang định dạng hình ảnh raster khác để đáp ứng nhu cầu của ứng dụng. Aspose.PSD API hỗ trợ tính năng trích xuất và chuyển đổi các lớp của Hình ảnh PSD sang định dạng hình ảnh raster khác. Đầu tiên, chúng ta sẽ tạo một đối tượng hình ảnh và tải hình ảnh PSD từ ổ đĩa cục bộ, sau đó chúng ta sẽ lặp qua từng lớp trong thuộc tính Layer. Sau đó, chúng ta sẽ chuyển khối thành hình ảnh TIFF. Snippet mã dưới đây cho bạn thấy cách chuyển đổi các lớp hình ảnh PSD thành hình ảnh TIFF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}


## **Chuyển Đổi PSD CMYK Sang TIFF CMYK**
Sử dụng Aspose.PSD cho .NET, các nhà phát triển có thể chuyển đổi tệp CMYK PSD sang định dạng tiff CMYK. Bài viết này thể hiện cách xuất/chuyển đổi tệp CMYK PSD sang định dạng tiff CMYK với Aspose.PSD. Sử dụng Aspose.PSD cho .NET, bạn có thể tải hình ảnh PSD và sau đó bạn có thể thiết lập các thuộc tính khác nhau bằng cách sử dụng [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) class và lưu hoặc xuất hình ảnh. Snippet mã dưới đây cho bạn thấy cách thực hiện tính năng này.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}


## **Xuất Hình Ảnh**
Bên cạnh một bộ các rutin xử lý hình ảnh phong phú, Aspose.PSD cung cấp các lớp chuyên dụng để chuyển đổi định dạng tệp PSD sang các định dạng khác. Sử dụng thư viện này, việc chuyển đổi hình ảnh PSD rất đơn giản và trực quan. Dưới đây là một số lớp chuyên dụng cho mục đích này trong namespace [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions).

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Việc xuất hình ảnh PSD với Aspose.PSD cho API .NET rất dễ dàng. Bạn chỉ cần một đối tượng của lớp thích hợp từ namespace [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions). Bằng cách sử dụng các lớp này, bạn có thể dễ dàng xuất bất kỳ hình ảnh nào được tạo, chỉnh sửa hoặc đơn giản chỉ được tải với Aspose.PSD cho .NET sang bất kỳ định dạng được hỗ trợ nào.

## **Kết Hợp Hình Ảnh**
Ví dụ này sử dụng lớp Graphics và cho thấy cách kết hợp hai hoặc nhiều hình ảnh thành một hình ảnh hoàn chỉnh. Để thể hiện thao tác, ví dụ tạo một PsdImage mới và vẽ hình ảnh trên bề mặt canvas bằng cách sử dụng phương thức DrawImage được tiết lộ bởi lớp Graphics. Sử dụng lớp Graphics, hai hoặc nhiều hình ảnh có thể được kết hợp một cách sao cho hình ảnh kết quả sẽ trông giống như một hình ảnh hoàn chỉnh không có khoảng trống giữa các phần hình ảnh và không có trang nào. Kích thước bề mặt canvas phải bằng với kích thước của hình ảnh kết quả. Dưới đây là mã thảo luận cho thể hiện cách sử dụng [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) phương thức của lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) để kết hợp hình ảnh thành một hình ảnh duy nhất.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}

## **Mở Rộng và Cắt Hình Ảnh**
Aspose.PSD API cho phép bạn mở rộng hoặc cắt hình ảnh trong quá trình chuyển đổi hình ảnh. Nhà phát triển cần tạo một hình chữ nhật với tọa độ X và Y và chỉ định chiều rộng và chiều cao của hộp hình chữ nhật. X, Y và chiều rộng, chiều cao của hình chữ nhật sẽ miêu tả việc mở rộng hoặc cắt hình ảnh đã tải. Nếu cần phải mở rộng hoặc cắt hình ảnh trong quá trình chuyển đổi hình ảnh, thực hiện các bước sau:

1. Tạo một thể hiện của lớp [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) và tải hình ảnh hiện có.
1. Tạo một thể hiện lớp ImageOption.
1. Tạo một thể hiện của lớp [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) và khởi tạo X, Y và chiều rộng, chiều cao của hình chữ nhật.
1. Gọi phương thức [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) của lớp RasterImage trong khi truyền tên tệp đầu ra, tùy chọn hình ảnh và đối tượng hình chữ nhật làm tham số.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}

## **Đọc và Viết Dữ Liệu XMP Cho Hình Ảnh**
XMP (Extensible Metadata Platform) là một tiêu chuẩn ISO. XMP chuẩn hóa một mô hình dữ liệu, một định dạng serialization và các thuộc tính cốt lõi cho việc xác định và xử lý dữ liệu mở rộng. Nó cũng cung cấp hướng dẫn cho việc nhúng thông tin XMP vào một hình ảnh phổ biến như JPEG, mà không làm hỏng tính đọc bằng các ứng dụng không hỗ trợ XMP. Sử dụng Aspose.PSD cho API .NET, các nhà phát triển có thể đọc hoặc viết dữ liệu XMP vào hình ảnh. Bài viết này thể hiện cách dữ liệu XMP có thể được đọc từ một hình ảnh và viết dữ liệu XMP vào hình ảnh.
### **Tạo Dữ Liệu XMP, Viết Và Đọc Từ Tệp**
Với sự trợ giúp của không gian tên Xmp, nhà phát triển có thể tạo đối tượng dữ liệu XMP metadata và viết nó vào một hình ảnh. Snippet mã dưới đây cho bạn thấy cách sử dụng XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage và DublinCorePackage chứa trong không gian tên [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}


## **Xuất Hình Ảnh Trong Môi Trường Đa Luồng**
Aspose.PSD cho .NET bây giờ hỗ trợ chuyển đổi hình ảnh trong môi trường đa luồng. Aspose.PSD cho .NET đảm bảo hiệu suất tối ưu của các thao tác trong quá trình thực thi mã trong môi trường đa luồng. Tất cả các lớp tùy chọn hình ảnh ([image option](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)) (ví dụ: BmpOptions, TiffOptions, JpegOptions, v.v.) trong Aspose.PSD cho .NET thực thi giao diện IDisposable. Do đó, là bắt buộc phải người phát triển cần phải khử bộ nhớ đúng cách đối với đối tượng lớp tùy chọn hình ảnh nếu thuộc tính Source được thiết lập. Snippet mã dưới đây thể hiện chức năng này.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD bây giờ hỗ trợ thuộc tính SyncRoot khi làm việc trong môi trường đa luồng. Nhà phát triển có thể sử dụng thuộc tính này để đồng bộ hóa truy cập vào luồng nguồn. Snippet mã dưới đây thể hiện cách sử dụng thuộc tính SyncRoot.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}

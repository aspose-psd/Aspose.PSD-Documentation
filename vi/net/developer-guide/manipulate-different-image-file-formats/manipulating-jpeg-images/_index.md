---
title: Xử lý Ảnh JPEG
type: docs
weight: 30
url: /vi/net/manipulating-jpeg-images/
---

## **Sử dụng Lớp ExifData để Đọc và Sửa Đổi Các Thẻ EXIF của Jpeg**
Hầu hết các máy ảnh số (bao gồm cả điện thoại thông minh), máy quét và các hệ thống khác xử lý ảnh lưu ảnh với thông tin EXIF (Exchangeable Image File). Các thiết lập máy ảnh và thông tin về cảnh được ghi lại bởi máy ảnh vào tập tin ảnh. Dữ liệu EXIF cũng bao gồm tốc độ màn trập, ngày và giờ chụp ảnh, tiêu cự, bù sáng, mẫu đo phơi sáng và nếu sử dụng đèn flash. Các API của Aspose.Imaging đã làm cho việc trích xuất thông tin EXIF từ một ảnh cụ thể trở nên dễ dàng và đơn giản. Nhà phát triển cũng có thể viết dữ liệu EXIF vào hình ảnh hoặc sửa đổi thông tin hiện có theo yêu cầu của họ. Aspose.PSD đã cung cấp lớp [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) để đọc, viết và sửa đổi dữ liệu EXIF, trong khi không gian tên [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) chứa các liệt kê liên quan được sử dụng trong quá trình này.
### **Đọc Dữ Liệu EXIF**
Các API Aspose.PSD cung cấp cách để đọc dữ liệu EXIF từ một hình ảnh cụ thể. Các bước được cung cấp dưới đây mô tả cách sử dụng lớp ExifData để đọc thông tin EXIF từ một hình ảnh.

- Tải ảnh PSD bằng phương thức factory Load.
- Tìm hình thu nhỏ Jpeg trong các tài nguyên PSD.
- Trích xuất một phiên bản của lớp ExifData.

Trích xuất thông tin cần thiết và viết nó ra bảng điều khiển.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Một cách khác, nhà phát triển cũng có thể lấy thông tin cụ thể bằng đoạn mã sau.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Viết & Sửa Đổi Dữ Liệu EXIF**
Sử dụng các API Aspose.PSD, nhà phát triển có thể viết thông tin EXIF mới và sửa đổi dữ liệu EXIF hiện có của một ảnh. Cả hai quá trình (Viết & Sửa đổi) đều yêu cầu tải ảnh và lấy dữ liệu EXIF vào một phiên bản của lớp ExifData. Sau đó, người dùng có thể truy cập các thuộc tính được phơi bởi lớp ExifData để thiết lập chúng theo cách tương ứng. Vui lòng lưu ý rằng ảnh để điều chỉnh nên là ảnh Jpeg hoặc Tiff thường là hình thu nhỏ PSD. Mã mẫu để minh họa cách sử dụng như sau:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Trích xuất hình thu nhỏ từ tài nguyên PSD**
Hình thu nhỏ là phiên bản giảm kích thước của hình ảnh, được sử dụng để hiển thị một phần quan trọng của bức hình thay vì toàn bộ khung hình. Một số tập tin ảnh (đặc biệt là những bức ảnh chụp bằng máy ảnh kỹ thuật số) chứa một hình ảnh thu nhỏ được nhúng trong tập tin. API Aspose.PSD cho phép bạn trích xuất hình thu nhỏ tài nguyên PSD và lưu nó riêng lẻ trên ổ đĩa. Tài nguyên hình thu nhỏ chứa thuộc tính ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) có thể truy xuất dữ liệu hình thu nhỏ. Đoạn mã dưới đây mô tả cách sử dụng nó.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Sử dụng phương pháp được thảo luận ở trên để lưu hình thu nhỏ vào các định dạng tập tin hỗ trợ khác. Nếu bạn muốn xuất dữ liệu hình thu nhỏ sang các định dạng ảnh khác như BMP & PNG, vui lòng sử dụng các tùy chọn xuất ảnh khác.
### **Trích xuất hình thu nhỏ từ các phân đoạn JFIF**
Cũng có thể trích xuất hình thu nhỏ từ phân đoạn ExifData hoặc JFIF của tài nguyên hình thu nhỏ PSD. Đoạn mã bên dưới cho thấy cách thực hiện việc trích xuất dữ liệu hình thu nhỏ từ phân đoạn JFIF hoặc ExifData:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Sử dụng phương pháp được thảo luận ở trên để lưu hình thu nhỏ vào các định dạng tập tin hỗ trợ khác. Nếu bạn muốn xuất dữ liệu hình thu nhỏ sang các định dạng ảnh khác như BMP & PNG, vui lòng sử dụng các tùy chọn xuất ảnh khác.
### **Thêm Hình thu nhỏ vào Phân đoạn JFIF**
Đoạn mã dưới đây cho thấy cách sử dụng thuộc tính JFIF.Thumbnail để thêm hình thu nhỏ vào phân đoạn JFIF của hình ảnh PSD đã tải.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Hình thu nhỏ với dữ liệu phân đoạn khác không thể chiếm quá 65,545 byte do quy định về định dạng JPEG. Đối với trường hợp hình ảnh lớn được đặt làm hình thu nhỏ, có thể có trường hợp ngoại lệ xảy ra.
### **Thêm Hình thu nhỏ vào Phân đoạn EXIF**
Đoạn mã dưới đây mô tả cách sử dụng thuộc tính ExifData.Thumbnail để thêm hình thu nhỏ vào phân đoạn EXIF của hình ảnh PSD đã tải.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


Trong trường hợp này, API Aspose.PSD không thể ước lượng kích thước hình thu nhỏ, nhưng nó có thể kiểm tra kích thước của toàn bộ phân đoạn dữ liệu EXIF. Điều này không thể lớn hơn 65,535 byte.
## **Sử dụng Lớp JpegExifData để Đọc và Sửa Đổi Các Thẻ EXIF của Jpeg**
Các API Aspose.PSD cung cấp lớp [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) dành riêng cho định dạng hình ảnh Jpeg để truy xuất và cập nhật thông tin EXIF. Bài viết này mô tả cách sử dụng lớp JpegExifData để đạt được mục tiêu tương tự. Lớp Aspose.PSD.Exif.JpegExifData phục vụ như một container dữ liệu EXIF cho các hình ảnh Jpeg, và cung cấp cách truy xuất các thẻ EXIF Jpeg tiêu chuẩn như được mô tả dưới đây:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Danh Sách Đầy Đủ Các Thẻ EXIF**
Đoạn mã trên đọc một số thẻ EXIF bằng các thuộc tính được cung cấp bởi lớp Aspose.PSD.Exif.JpegExifData. Danh sách đầy đủ các thuộc tính này có sẵn ở đây. Đoạn mã sau sẽ đọc tất cả các thẻ EXIF bằng cách sử dụng lớp [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Tự động Sửa chữa Độ Xoay của Hình ảnh JPEG**


Ảnh có thể được chụp bằng máy ảnh quay ở 90°, 180°, 270° hoặc không (hướng bình thường). Hầu hết các máy ảnh số lưu thông tin hướng cùng với dữ liệu hình ảnh dưới dạng thẻ EXIF của các hình ảnh JEPG. Thông tin này có thể được sử dụng để thực hiện xoay tự động trên các hình ảnh để sửa chữa hướng. API Aspose.PSD cung cấp phương thức AutoRotate cho lớp JpegImage để tự động sửa chữa độ xoay của hình ảnh JPEG. Đây là cách bạn có thể sử dụng phương thức AutoRotate với API Aspose.PSD cho .NET.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Hỗ trợ cho JPEG-LS với mô hình màu CMYK và YCCK**


API Aspose.PSD cho .NET cung cấp hỗ trợ cho các mô hình màu CMYK và YCCK với JPEG-LS. Đoạn mã dưới đây mô tả cách sử dụng hỗ trợ đó cho JPEG-LS.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Hỗ trợ cho Ảnh JPEG-LS với 2-7 bit mỗi mẫu**


API Aspose.PSD cho .NET cung cấp hỗ trợ cho ảnh JPEG-LS với 2-7 bit mỗi mẫu. Đoạn mã dưới đây mô tả cách sử dụng hỗ trợ đó cho JPEG-LS.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Thiết lập Loại Màu và Loại Nén cho hình ảnh JPEG**




API Aspose.PSD cho .NET cung cấp hỗ trợ cho Loại Màu và Loại Nén và thiết lập chúng như màu xám và tiến triển cho hình ảnh JPEG. Đoạn mã dưới đây mô tả cách sử dụng hỗ trợ đó.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}





Đoạn mã dưới đây mô tả cách sử dụng thuộc tính ExifData.Thumbnail để thêm hình thu nhỏ vào phân đoạn EXIF của hình ảnh PSD đã tải.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

Trong trường hợp này, API Aspose.PSD không thể ước lượng kích thước hình thu nhỏ, nhưng nó có thể kiểm tra kích thước của toàn bộ phân đoạn dữ liệu EXIF. Điều này không thể lớn hơn 65,535 byte.


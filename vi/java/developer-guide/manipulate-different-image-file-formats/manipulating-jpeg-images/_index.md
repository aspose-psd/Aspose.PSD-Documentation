---
title: Xử lý hình ảnh JPEG
type: docs
weight: 20
url: /vi/java/manipulating-jpeg-images/
---

## **Sử dụng Lớp ExifData để Đọc và Sửa Đổi Thẻ EXIF của JPEG**

Hầu hết tất cả các máy ảnh kỹ thuật số (bao gồm cả điện thoại thông minh), máy quét và các hệ thống khác xử lý lưu ảnh với thông tin EXIF (Tệp Hình ảnh Giao đổi). Các thiết lập máy ảnh và thông tin cảnh được ghi lại bởi máy ảnh vào tập tin hình ảnh. Dữ liệu EXIF cũng bao gồm tốc độ màn trập, ngày và giờ chụp ảnh, tiêu cự, bù sáng, mẫu đo độ sáng và nếu có sử dụng đèn flash. API Aspose.Imaging đã cho phép trích xuất thông tin EXIF từ một hình ảnh cụ thể một cách dễ dàng và đơn giản. Các nhà phát triển cũng có thể viết dữ liệu EXIF vào hình ảnh hoặc sửa đổi thông tin hiện có theo yêu cầu của mình. Aspose.Imaging đã cung cấp lớp ExifData để đọc, viết và sửa đổi dữ liệu EXIF, trong khi không gian tên Aspose.PSD.Exif.Enums chứa các liệt kê liên quan được sử dụng trong quá trình đó.
### **Đọc Dữ liệu EXIF**
Các API Aspose.PSD cung cấp phương tiện để đọc dữ liệu EXIF từ một hình ảnh cụ thể. Các bước cung cấp dưới đây minh họa cách sử dụng lớp ExifData để đọc thông tin EXIF từ một hình ảnh.

- Tải hình ảnh PSD bằng phương thức factory Load.
- Tìm hình xem trước JPEG trong số tài nguyên PSD.
- Trích xuất một thể hiện của lớp ExifData.

Lấy thông tin cần thiết và ghi nó ra bảng điều khiển.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}

Hoặc, các nhà phát triển cũng có thể nhận thông tin cụ thể bằng mã mẫu sau.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Viết và Sửa Đổi Dữ liệu EXIF**

Bằng cách sử dụng các API Aspose.PSD, các nhà phát triển có thể viết thông tin EXIF mới và sửa đổi dữ liệu EXIF hiện có của hình ảnh. Cả hai quy trình (Viết & Sửa đổi) đều yêu cầu tải một hình ảnh và lấy dữ liệu EXIF vào một thể hiện của lớp ExifData. Sau đó, người dùng có thể truy cập các thuộc tính được tiết lộ bởi lớp ExifData để thiết lập chúng phù hợp. Vui lòng lưu ý rằng các hình ảnh để thao tác nên là hình ảnh JPEG hoặc TIFF thường là hình xem trước PSD. Mã mẫu để minh họa cách sử dụng như sau:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Trích xuất Hình xem trước từ Tài nguyên PSD**
Hình xem trước là phiên bản thu nhỏ của hình ảnh, được sử dụng để hiển thị một phần quan trọng của hình ảnh thay vì toàn bộ khung. Một số tệp hình ảnh (đặc biệt là những tấm chụp bằng máy ảnh kỹ thuật số) có một hình ảnh xem trước được nhúng trong tệp. API Aspose.PSD cho phép bạn trích xuất hình xem trước tài nguyên PSD và lưu nó riêng lẻ trên đĩa. Tài nguyên hình xem trước chứa thuộc tính ExifData.Thumbnail mà có thể truy xuất dữ liệu hình xem trước. Đoạn mã sau minh họa cách sử dụng nó.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}

Sử dụng cách tiếp cận đã thảo luận ở trên để lưu hình xem trước vào các định dạng tệp hỗ trợ khác. Nếu bạn muốn xuất dữ liệu hình xem trước sang các định dạng hình ảnh khác như BMP và PNG, vui lòng sử dụng các tùy chọn xuất hình ảnh khác.
### **Trích xuất Hình xem trước từ các Đoạn JFIF**
Cũng có thể trích xuất hình xem trước từ đoạn ExifData hoặc JFIF của tài nguyên hình xem trước PSD. Đoạn mã sau cho thấy cách thực hiện việc trích xuất dữ liệu hình xem trước từ đoạn JFIF hoặc ExifData:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}

Sử dụng cách tiếp cận đã thảo luận ở trên để lưu hình xem trước vào các định dạng tệp hỗ trợ khác. Nếu bạn muốn xuất dữ liệu hình xem trước sang các định dạng hình ảnh khác như BMP và PNG, vui lòng sử dụng các tùy chọn xuất hình ảnh khác.
### **Thêm Hình xem trước vào Đoạn JFIF**
Đoạn mã dưới đây minh họa cách sử dụng thuộc tính JFIF.Thumbnail để thêm một hình ảnh xem trước vào đoạn JFIF của hình ảnh PSD đã tải.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Hình ảnh xem trước với dữ liệu đoạn khác không thể chiếm hơn 65.545 byte do các quy định định dạng JPEG. Trong trường hợp hình ảnh lớn được đặt làm hình xem trước, có thể xuất hiện ngoại lệ.
### **Thêm Hình xem trước vào Đoạn EXIF**
Đoạn mã dưới đây minh họa cách sử dụng thuộc tính ExifData.Thumbnail để thêm một hình ảnh xem trước vào đoạn EXIF của hình ảnh PSD đã tải.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

Trong trường hợp này, API Aspose.PSD không thể ước lượng kích thước hình ảnh xem trước, nhưng có thể kiểm tra kích thước của toàn bộ đoạn dữ liệu EXIF. Điều này không thể lớn hơn 65.535 byte.
## **Sử dụng Lớp JpegExifData để Đọc và Sửa Đổi Thẻ EXIF của JPEG**
API Aspose.PSD cung cấp lớp JpegExifData dành riêng cho các định dạng hình ảnh JPEG để truy xuất & cập nhật thông tin EXIF. Bài viết này minh họa cách sử dụng lớp JpegExifData để đạt được mục tiêu tương tự. Lớp Aspose.PSD.Exif.JpegExifData phục vụ như hộp dữ liệu EXIF cho hình ảnh JPEG và cung cấp phương tiện để truy xuất các thẻ EXIF chuẩn của JPEG như minh họa dưới đây:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Danh sách đầy đủ các thẻ EXIF**
Đoạn mã trên đọc một số Thẻ EXIF bằng cách sử dụng các thuộc tính được cung cấp bởi lớp Aspose.PSD.Exif.JpegExifData. Danh sách đầy đủ các thuộc tính này có sẵn tại đây. Đoạn mã sau sẽ đọc tất cả các thẻ EXIF bằng cách sử dụng lớp System.Reflection.PropertyInfo.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Tự Điều chỉnh Hướng Ảnh JPEG**
Ảnh có thể được chụp bằng máy ảnh quay 90°, 180°, 270° hoặc không (hướng bình thường). Hầu hết các máy ảnh kỹ thuật số lưu thông tin hướng cùng với dữ liệu hình ảnh dưới dạng thẻ EXIF của các hình ảnh JPEG. Thông tin này có thể được sử dụng để thực hiện tự động quay hình ảnh để điều chỉnh hướng. Các API Aspose.PSD cung cấp phương thức AutoRotate cho lớp JpegImage để tự động điều chỉnh hướng của các hình ảnh JPEG. Dưới đây là cách bạn có thể sử dụng phương thức AutoRotate với Aspose.PSD cho API Java.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Hỗ trợ cho JPEG-LS với CMYK và YCCK**

Aspose.PSD cho API Java cung cấp hỗ trợ cho các mô hình màu CMYK và YCCK với JPEG-LS. Đoạn mã dưới đây minh họa cách sử dụng hỗ trợ đó cho JPEG-LS.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Hỗ trợ cho JPEG-LS với 2-7 bit mỗi mẫu**

Aspose.PSD cho API Java cung cấp hỗ trợ cho hình ảnh JPEG-LS với 2-7 bit mỗi mẫu. Đoạn mã dưới đây minh họa cách sử dụng hỗ trợ đó cho JPEG-LS.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Cài đặt Loại Màu sắc và Loại Nén cho hình ảnh JPEG**

Aspose.PSD cho API Java cung cấp hỗ trợ cho Loại Màu sắc và Loại Nén và thiết lập chúng như mức xám và tiến bộ cho hình ảnh JPEG. Đoạn mã dưới đây minh họa cách sử dụng hỗ trợ đó.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}

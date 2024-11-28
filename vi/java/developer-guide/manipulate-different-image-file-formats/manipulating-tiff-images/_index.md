---
title: Xử lý Ảnh TIFF
type: docs
weight: 40
url: /vi/java/manipulating-tiff-images/
---

## **Thêm Khung với Các Cài Đặt Khác Nhau**
TIFF là một định dạng rất linh hoạt và cho phép thêm các khung khác nhau, với các kích thước, nén và cài đặt khác nhau. Các API Aspose.PSD cho phép bạn thêm bất kỳ khung TIFF nào có bất kỳ kích thước nào giúp tạo tài liệu phức tạp. Nếu có yêu cầu điều chỉnh các khung trong quá trình thêm để làm cho chúng trở nên bằng nhau, thực hiện các bước sau:

- Tạo một khung trống mới với các tùy chọn mong muốn hoặc sao chép khung nguồn với các tùy chọn đầu ra được chỉ định bằng cách sử dụng phương thức CreateFrameFrom.
- Thay đổi kích thước của khung hình/nguồn thành kích thước mong muốn bằng cách sử dụng phương thức Resize.
- Thêm các điểm ảnh của khung hình/nguồn vào khung mới.
- Thêm khung mới vào hình ảnh TIFF đầu ra.

## **Xuất Lớp ảnh PSD sang Định dạng Tệp TIFF Nhiều Trang**
Đôi khi bạn cần xuất các lớp ảnh PSD sang định dạng tệp TIFF nhiều trang. Bài viết này sẽ hướng dẫn cách thực hiện công việc này bằng cách sử dụng API Aspose.PSD cho Java. Đầu tiên, chúng ta sẽ tải ảnh PSD từ ổ đĩa. Sau đó, chúng ta sẽ lặp qua các lớp ảnh PSD và tạo TiffFrame từ các lớp tương ứng. Cuối cùng, chúng ta sẽ lưu hình ảnh TIFF kết quả vào một tệp đơn trên ổ đĩa.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}

## **Cấu hình Tùy chọn TiffOptions**
Nhà phát triển có thể điều chỉnh các thuộc tính khác nhau của lớp Tiffoptions để đạt được kết quả mong muốn. Trong tài liệu này, chúng ta sẽ tập trung vào 4 thuộc tính chính điều khiển các thuộc tính hình ảnh kết quả.

Các thuộc tính này được liệt kê dưới đây.

1. ` `TiffOptions.Photometric
2. TiffOptions.Compression
3. TiffOptions.BitsPerSample
4. TiffOptions.Predictor

Khi khởi tạo một cấu trúc Tiffoptions trống, mỗi tùy chọn được đặt thành giá trị mặc định của nó, ví dụ nén được đặt thành None, BitsPerSample được đặt là 1 và Photometric được đặt là MinIsWhite. Lưu vào định dạng này sẽ làm cho hình ảnh cuối cùng trở nên đen trắng và đây là hành vi dự kiến cho các tùy chọn như vậy. Để có kết quả màu, bạn phải đặt tất cả các thuộc tính được đề cập trên sang các giá trị tương ứng với không gian màu mong muốn hoặc bạn có thể khởi tạo cấu trúc Tiffoptions với các cài đặt được xác định trước như đã thảo luận sau trong bài viết. Bảng dưới đây mô tả các giá trị tham số dự kiến mà bạn có thể đặt để đạt được kết quả mong muốn. Vui lòng lưu ý, bạn nên đặt tất cả 4 cột này thông qua Tiffoptions để lưu bất kỳ hình ảnh nạp/tạo vào định dạng tệp TIFF.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Không nén|1/4/8/16 (bảng màu, chế độ màu) chỉ một kênh|Không|
|MinIsWhite/MinIsBlack|LZW/Không nén|1/4/8/16 (chế độ xám) chỉ một kênh|Không|
|Palette|LZW/Không nén|8 (bảng màu, chế độ màu) chỉ một kênh|Ngang (nén nhiều hơn cho LZW với các mẫu giống nhau)|
|MinIsWhite/MinIsBlack|LZW/Không nén|8 (chế độ xám) chỉ một kênh|Ngang (nén nhiều hơn cho LZW với các mẫu giống nhau)|
|RGB|LZW/Không nén|[8,8,8] (3 kênh RGB)|Không/Ngang|
|RGB|LZW/Không nén|[8,8,8,8] (3 kênh RGB và kênh alpha bổ sung có thể được đặt qua TiffOptions.AlphaStorage) Thực ra bất kỳ số lượng kênh bổ sung nào cũng được hỗ trợ nhưng mỗi kênh phải có kích thước 8 bit như [8,8,8,8,8,8]|Không/Ngang|
Tất cả 4 thuộc tính nên được đặt qua TiffOptions để lưu bất kỳ định dạng hình ảnh nào sang định dạng Tiff. Khi sử dụng các kết hợp khác nhau, một số trình xem (bao gồm Windows Photo Viewer) có thể từ chối hiển thị hình ảnh kết quả do họ chỉ hỗ trợ giới hạn. Trong trường hợp đó, vui lòng chọn trình xem khác cho quá trình kiểm tra của bạn.

### **Cài Đặt Đã Định Sẵn cho Lớp TiffOptions**
Để thuận tiện cho người dùng và tránh sự cấu hình sai của trường hợp Tiffoptions, API Aspose.PSD cho Java đã bật một hàm tạo khác chấp nhận một tham số kiểu TiffExpectedFormat. Dựa trên giá trị được chọn từ liệt kê TiffExpectedFormat, API tự cấu hình tất cả các thuộc tính bắt buộc cho trường hợp Tiffoptions để tạo ra kết quả mong muốn. Trước khi chúng ta chuyển đến đoạn mã minh họa, đây là danh sách các trường TiffExpectedFormat và thông tin chi tiết của chúng để hiểu rõ hơn về cách sử dụng.

- TiffExpectedFormat.Default: Đặt trường này thành Mặc định tương tự như hàm tạo mặc định của lớp Tiffoptions không có nén và BitsPerPixel được đặt thành 1 để tạo ra kết quả đen trắng. Được khuyến khích sử dụng trường này khi các thuộc tính cụ thể của định dạng khác cần được đặt thủ công theo kết quả mong muốn.
- TiffExpectedFormat.TiffCcitRle: Riêng cho mã hóa RLE khi lưu kết quả trong định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffCcittFax3: Riêng cho mã hóa CCITT Fax3 khi lưu kết quả trong định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffCcittFax4: Riêng cho mã hóa CCITT Fax4 khi lưu kết quả trong định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffDeflateBW: Riêng cho nén Deflate khi lưu kết quả trong định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffDeflateRGB: Riêng cho nén Deflate khi lưu kết quả trong định dạng TIFF RGB (màu).
- TiffExpectedFormat.TiffJpegRGB: Riêng cho nén JPEG khi lưu kết quả trong định dạng TIFF RGB (màu).
- TiffExpectedFormat.TiffJpegYCBCR: Riêng cho nén Deflate khi lưu kết quả trong định dạng TIFF YCBCR (màu).
- TiffExpectedFormat.TiffLzwBW: Riêng cho nén LZW khi lưu kết quả trong định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffLzwRGB: Riêng cho nén LZW khi lưu kết quả trong định dạng TIFF RGB (màu).
- TiffExpectedFormat.TiffLzwRGBA: Riêng cho nén LZW khi lưu kết quả trong định dạng TIFF RGBA (màu với độ trong suốt).
- TiffExpectedFormat.TiffNoCompressionBW: Riêng cho định dạng TIFF không nén khi lưu kết quả ở 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffNoCompressionRGB: Riêng cho định dạng TIFF không nén khi lưu kết quả ở RGB (màu).
- TiffExpectedFormat.TiffNoCompressionRGBA: Riêng cho định dạng TIFF không nén khi lưu kết quả ở RGBA (màu với độ trong suốt).

Đoạn mã dưới đây phân tích cụ thể việc sử dụng các trường TiffExpectedFormat khi tạo một thể hiện của lớp Tiffoptions.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}

## **Hỗ Trợ Nén và Nén Adobe Deflate**
Định dạng tệp TIFF (Tagged Image File Format) hỗ trợ các loại nén khác nhau trong đó loại nén được lưu trữ dưới dạng thẻ (một giá trị số nguyên) trong tệp. Một trong những phương pháp nén như vậy là Adobe Deflate (trước đây được biết đến là Deflate). API Aspose.PSD cho Java hỗ trợ phương pháp nén này để xuất & tạo ảnh TIFF.

### **Lưu Ảnh vào TIFF với Nén Deflate**
Chuyển đổi các hình ảnh được tải vào TIFF với nén Deflate/Adobe Deflate là dễ dàng như sau.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}

### **Tạo TiffImage với Nén Adobe Deflate**
Mẫu dưới đây mô tả cách sử dụng API Aspose.PSD cho Java để tạo một hình ảnh từ đầu bằng cách sử dụng phương pháp nén Adobe Deflate.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}

### **Nén Ảnh TIFF**
API Aspose.PSD cho Java có thể được sử dụng để chuyển đổi các hình ảnh PSD sang định dạng ảnh TIFF và thậm chí thay đổi nén của ảnh TIFF kết quả. API cũng có thể được sử dụng để lưu các hình ảnh khác nhau như khung trong một hình ảnh TIFF cho mục đích lưu trữ trong khi nén các hình ảnh để đạt kích thước dữ liệu thấp nhất. Nén hình ảnh trong bất kỳ trường hợp nào cũng nên được thực hiện bằng cách giảm kích thước dữ liệu nguồn mà không xem xét thuật toán nén nào được sử dụng. Để đạt tỷ lệ nén tốt nhất, chúng ta có thể sử dụng không gian màu chỉ số hóa. Đoạn mã dưới đây thực hiện việc nén tốt nhất sử dụng 16 chỉ mục màu và thuật toán nén LZW tuy nhiên các màu nguồn are slightly dithered.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}

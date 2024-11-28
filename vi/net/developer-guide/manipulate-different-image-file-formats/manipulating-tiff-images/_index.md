---
title: Xử lý hình ảnh TIFF
type: docs
weight: 50
url: /vi/net/xu-ly-hinh-anh-tiff/
---

## **Thêm Khung với Các Cài Đặt Khác Nhau**
TIFF là một định dạng rất linh hoạt và cho phép thêm các khung khác nhau, với kích thước, nén và cài đặt khác nhau. APIs của Aspose.PSD cho phép bạn thêm bất kỳ khung TIFF nào với bất kỳ kích thước nào giúp tạo tài liệu phức tạp. Nếu có yêu cầu điều chỉnh các khung trong quá trình thêm để làm cho chúng đều nhau, thực hiện các bước sau:

- Tạo một khung trống mới với các tùy chọn mong muốn hoặc sao chép khung nguồn với các tùy chọn đầu ra được chỉ định bằng cách sử dụng phương thức CreateFrameFrom.
- Thay đổi kích thước khung/hình ảnh nguồn thành kích thước mong muốn bằng cách sử dụng phương thức Resize.
- Thêm các điểm ảnh khung/hình ảnh nguồn vào khung mới.
- Thêm khung mới vào hình ảnh TIFF đầu ra.

## **Xuất các lớp của hình ảnh PSD sang định dạng tệp Multi Page Tiff**
Đôi khi bạn cần xuất các lớp hình ảnh PSD sang định dạng tệp Multi-page TIFF. Bài viết này sẽ thể hiện cách chúng ta có thể thực hiện công việc này bằng cách sử dụng Aspose.PSD cho .NET API. Đầu tiên, chúng ta sẽ tải hình ảnh PSD từ đĩa. Sau đó, chúng ta sẽ lặp qua các lớp hình ảnh PSD và tạo TiffFrame từ các lớp tương ứng. Cuối cùng, chúng ta sẽ lưu hình ảnh Tiff kết quả vào một tệp duy nhất trên đĩa.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}

## **Cấu hình Tùy Chọn TiffOptions**
Nhà phát triển có thể điều chỉnh các thuộc tính khác nhau của [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) class để thu được kết quả mong muốn. Trong văn bản này, chúng ta sẽ tập trung vào 4 thuộc tính chính điều khiển các thuộc tính hình ảnh kết quả.

Các thuộc tính này được liệt kê dưới đây.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Khi chúng ta khởi tạo một cấu trúc TiffOptions trống, mỗi tùy chọn được đặt giá trị mặc định của nó, ví dụ, nén được đặt là None, BitsPerSample được đặt ở 1 và Photometric là MinIsWhite. Lưu vào định dạng này sẽ làm cho hình ảnh cuối cùng trở thành đen trắng và đây là hành vi được mong đợi cho sự kết hợp tùy chọn như vậy. Để có kết quả màu, bạn phải thiết lập tất cả các thuộc tính đã nêu ở trên thành các giá trị tương ứng với không gian màu mong muốn hoặc bạn có thể khởi tạo cấu trúc TiffOptions với các cài đặt được thảo luận sau trong bài viết này. Dưới đây là một bảng mô tả các giá trị tham số mong đợi mà bạn có thể thiết lập để đạt được kết quả mong muốn. Lưu ý, bạn nên thiết lập tất cả 4 cột thông qua TiffOptions để lưu bất kỳ hình ảnh nào được tải/tạo vào định dạng TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Bảng màu|LZW/Uncompressed|1/4/8/16 (bảng màu, chế độ màu) chỉ một kênh|Không|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16 (chế độ xám) chỉ một kênh|Không|
|Bảng màu|LZW/Uncompressed|8 (bảng màu, chế độ màu) chỉ một kênh|Ngang (nén mạnh hơn cho các mẫu LZW giống nhau)|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8 (chế độ xám) chỉ một kênh|Ngang (nén mạnh hơn cho các mẫu LZW giống nhau)|
|RGB|LZW/Uncompressed|[8,8,8] (3 kênh RGB)|Không/Ngang|
|RGB|LZW/Uncompressed|[8,8,8,8] (3 kênh RGB và bổ sung kênh alpha có thể được thiết lập thông qua TiffOptions.AlphaStorage) Thực tế bất kỳ số lượng kênh bổ sung nào cũng được hỗ trợ nhưng mỗi kênh phải có kích thước 8 bit như [8,8,8,8,8,8]|Không/Ngang|
Tất cả 4 thuộc tính cần phải được thiết lập qua TiffOptions để lưu bất kỳ định dạng hình ảnh nào sang định dạng Tiff. Khi sử dụng các kết hợp khác nhau, một số trình xem (bao gồm Trình xem Ảnh trong Windows) có thể từ chối vẽ hình ảnh kết quả do hỗ trợ hạn chế mà họ cung cấp. Trong trường hợp như vậy, hãy chọn trình xem khác cho quá trình kiểm tra của bạn.

### **Cài Đặt Sẵn cho Lớp TiffOptions**
Để hỗ trợ người dùng và tránh sự cấu hình không chính xác của một phiên bản TiffOptions, Aspose.PSD cho .NET API đã tiết lộ một hàm tạo khác chấp nhận một tham số kiểu [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Dựa trên giá trị đã chọn từ liệt kê TiffExpectedFormat, API sẽ tự động cấu hình tất cả các thuộc tính bắt buộc cho phiên bản TiffOptions để tạo ra kết quả mong muốn. Trước khi chúng ta di chuyển đến mã mẫu, đây là danh sách các trường TiffExpectedFormat và chi tiết của chúng để hiểu rõ hơn về cách sử dụng.

- TiffExpectedFormat.Default: Thiết lập trường này thành Mặc định hoạt động tương tự như hàm tạo mặc định của lớp TiffOptions với không nén và BitsPerPixel được thiết lập thành 1 để tạo ra kết quả đen trắng. Được khuyến nghị sử dụng trường này khi các thuộc tính cụ thể của định dạng khác phải được thiết lập thủ công theo kết quả mong muốn.
- TiffExpectedFormat.TiffCcitRle: Đặc biệt cho mã hóa RLE trong khi lưu kết quả dưới định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffCcittFax3: Đặc biệt cho mã hóa CCITT Fax3 trong khi lưu kết quả dưới định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffCcittFax4: Đặc biệt cho mã hóa CCITT Fax4 trong khi lưu kết quả dưới định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffDeflateBW: Đặc biệt cho nén Deflate trong khi lưu kết quả dưới định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffDeflateRGB: Đặc biệt cho nén Deflate trong khi lưu kết quả dưới định dạng TIFF RGB (màu).
- TiffExpectedFormat.TiffJpegRGB: Đặc biệt cho nén JPEG trong khi lưu kết quả dưới định dạng TIFF RGB (màu).
- TiffExpectedFormat.TiffJpegYCBCR: Đặc biệt cho nén JPEG trong khi lưu kết quả dưới định dạng TIFF YCBCR (màu).
- TiffExpectedFormat.TiffLzwBW: Đặc biệt cho nén LZW trong khi lưu kết quả dưới định dạng TIFF 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffLzwRGB: Đặc biệt cho nén LZW trong khi lưu kết quả dưới định dạng TIFF RGB (màu).
- TiffExpectedFormat.TiffLzwRGBA: Đặc biệt cho nén LZW trong khi lưu kết quả dưới định dạng TIFF RGBA (màu với độ trong suốt).
- TiffExpectedFormat.TiffNoCompressionBW: Đặc biệt cho định dạng TIFF không nén trong khi lưu kết quả dưới định dạng 1 BitsPerPixel (đen trắng).
- TiffExpectedFormat.TiffNoCompressionRGB: Đặc biệt cho định dạng TIFF không nén trong khi lưu kết quả dưới định dạng RGB (màu).
- TiffExpectedFormat.TiffNoCompressionRGBA: Đặc biệt cho định dạng TIFF không nén trong khi lưu kết quả dưới định dạng RGBA (màu có độ trong suốt).

Đoạn mã sau giải thích cách sử dụng các trường TiffExpectedFormat khi tạo một thể hiện của lớp TiffOptions.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}

## **Hỗ trợ cho Nén và Nén Adobe Deflate**
Định dạng tệp TIFF (Tagged Image File Format) hỗ trợ nhiều loại nén trong đó loại nén được lưu trữ như một thẻ (một giá trị số nguyên) trong tệp. Một trong những phương pháp nén như vậy là Adobe Deflate (trước đây được biết đến là Deflate). Aspose.PSD cho .NET API hỗ trợ phương pháp nén này để xuất và tạo hình ảnh TIFF.

### **Lưu hình ảnh sang TIFF với Nén Deflate**
Chuyển hình ảnh đã tải thành TIFF với nén Deflate/Adobe Deflate rất dễ như sau.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}

### **Tạo TiffImage với Nén Adobe Deflate**
Mẫu dưới đây cho thấy cách sử dụng Aspose.PSD cho .NET API để tạo một hình ảnh từ đầu bằng cách sử dụng phương pháp nén Adobe Deflate.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}

### **Nén Hình Ảnh TIFF**
Aspose.PSD cho .NET API có thể được sử dụng để chuyển đổi hình ảnh PSD sang định dạng hình ảnh TIFF và thậm chí thay đổi nén của hình ảnh TIFF kết quả. API cũng có thể được sử dụng để lưu các hình ảnh khác nhau dưới dạng khung trong một hình ảnh TIFF cho mục đích lưu trữ trong khi nén các hình ảnh thành kích thước dữ liệu thấp nhất. Nén hình ảnh trong bất kỳ trường hợp nào cũng nên được thực hiện bằng cách giảm kích thước dữ liệu nguồn bất kể thuật toán nén sử dụng. Để đạt tỷ lệ nén tốt nhất, chúng ta có thể sử dụng không gian màu theo chỉ số. Đoạn mã dưới đây thực hiện việc nén tốt nhất bằng cách sử dụng 16 màu chỉ mục và thuật toán nén LZW tuy nhiên các màu nguồn đã được phân tán một chút.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}

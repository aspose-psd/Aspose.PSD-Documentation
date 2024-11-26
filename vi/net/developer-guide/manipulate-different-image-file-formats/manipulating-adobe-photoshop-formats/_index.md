---
title: Xử lý các định dạng Adobe Photoshop
type: docs
weight: 20
url: /vi/net/manipulating-adobe-photoshop-formats/
---

## **Gộp các lớp PSD vào các lớp khác**

## **Xuất hình ảnh sang PSD**
PSD, tài liệu PhotoShop, là định dạng tệp mặc định được sử dụng bởi Adobe Photoshop để làm việc với hình ảnh. Aspose.PSD cho phóp bạn tải, chỉnh sửa và lưu các tệp vào định dạng PSD để chúng có thể được mở và chỉnh sửa trong Photoshop. Bài viết này chỉ ra cách lưu một tệp vào định dạng PSD với Aspose.PSD, và nó cũng thảo luận về một số cài đặt có thể được sử dụng khi lưu sang định dạng này. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) là một lớp chuyên biệt trong không gian tên [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) được sử dụng để xuất hình ảnh sang PSD. Để xuất sang PSD, tạo một phiên bản của lớp Image, có thể được tải từ một tệp hình ảnh hiện có (ví dụ: hình thu nhỏ) hoặc tạo từ đầu. Bài viết này giải thích cách làm điều này. Trong các ví dụ dưới đây, một hình ảnh được tạo từ đầu. Ngay sau khi được tạo và dữ liệu điểm ảnh được đổ, lưu hình ảnh bằng cách sử dụng phương thức Save của lớp Image, và cung cấp một đối tượng PsdOptions như là đối số thứ hai. Một số thuộc tính của lớp PsdOptions có thể được thiết lập cho chuyển đổi nâng cao. Một số thuộc tính là ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) và Version. Aspose.PSD hỗ trợ các phương pháp nén sau thông qua việc liệt kê CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Các chế độ màu sau được hỗ trợ thông qua việc liệt kê [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


Các tài nguyên bổ sung có thể được thêm vào, chẳng hạn như tài nguyên hình xăm cho PSD v4.0, v5.0 và cao hơn, hoặc tài nguyên lưới và hướng dẫn cho PSD v4.0 và cao hơn. Mã dưới đây tạo một tệp Image từ đầu, đổ dữ liệu pixel và lưu chúng vào PSD với nén RLE và chế độ màu xám. Mã nguồn sau cho thấy cách xuất hình ảnh sang PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose-Sửa đổi- Và-Chuyển đổi-Hình ảnh-PSD-Xuất Hình ảnh Sang PSD-Xuất Hình ảnh Sang PSD.cs" >}}
## **Nhập hình ảnh vào lớp PSD**
Bài viết này demo việc sử dụng Aspose.PSD để thêm hoặc nhập hình ảnh vào một lớp PSD. Các API Aspose.PSD đã tiết lộ các phương thức hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD đã tiết lộ phương thức [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) của lớp Layer để thêm/nhập một hình ảnh vào một tệp PSD. Phương thức DrawImage cần vị trí và giá trị hình ảnh để thêm/nhập một hình ảnh vào một tệp PSD. Các bước để nhập một hình ảnh vào lớp PSD đơn giản như dưới đây:

- Tải một tệp PSD như hình ảnh bằng cách sử dụng phương thức nhà máy Load được tiết lộ bởi lớp Image.
- Tạo một phiên bản của lớp Layer từ luồng với tệp Png, Jpeg, Tiff, Gif, Bmp, Psd hoặc j2k
- Thêm Layer vào Psd sử dụng phương thức AddLayer
- Lưu kết quả.


Mã nguồn sau cho thấy cách nhập hình ảnh vào lớp PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose-Mở-Nạp Hình ảnh từ Dòng-Nạp Hình ảnh từ Dòng.cs" >}}
## **Thay thế màu trong các lớp PSD**
Bài viết này demo việc sử dụng Aspose.PSD để thêm hoặc nhập một hình ảnh vào một lớp PSD. Các API Aspose.PSD đã tiết lộ các phương thức hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD đã tiết lộ [phương thức](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) DrawImage của lớp Layer để thêm/nhập một hình ảnh vào một tệp PSD. Phương thức DrawImage cần vị trí và giá trị hình ảnh để thêm/nhập một hình ảnh vào một tệp PSD. Các bước để nhập hình ảnh vào lớp PSD đơn giản như dưới đây:

- Tải một tệp PSD như hình ảnh bằng cách sử dụng phương thức nhà máy Load được tiết lộ bởi lớp Image.
- Tạo một phiên bản của lớp Layer và gán lớp hình ảnh PSD cho nó.
- Tải hình ảnh cần được thêm hoặc tạo một hình ảnh từ đầu.
- Gọi phương thức Layer.DrawImage trong khi chỉ định vị trí và phiên bản hình ảnh.
- Lưu kết quả.


Mã nguồn sau cho thấy cách nhập hình ảnh vào lớp PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose- Sửa đổi-Và- Chuyển đổi- Hình ảnh-PSD-Thay Đổi Màu Trong PSD- Thay Đổi Màu Trong PSD.cs" >}}
## **Tạo hình thu nhỏ từ các tệp PSD**
PSD là định dạng tài liệu nguyên của ứng dụng Photoshop của Adobe. Adobe Photoshop (phiên bản 5.0 trở lên) lưu thông tin hình xăm để xem trước trong một khối tài nguyên hình ảnh bao gồm một tiêu đề 28 byte ban đầu, tiếp theo là một hình xăm JFIF theo trật tự RGB (đỏ, xanh lá, lam). Aspose.PSD API cung cấp một cơ chế dễ sử dụng để truy cập các tài nguyên của tệp PSD. Các tài nguyên này cũng bao gồm tài nguyên hình xăm mà lưu trữ thông tin hình xăm vi xử lý mà sau đó có thể được truy xuất và lưu vào đĩa theo nhu cầu của ứng dụng. Mã nguồn dưới đây cho thấy cách tạo hình thu nhỏ từ các tệp PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose-Sửa đổi-Và- Chuyển đổi-Hình ảnh-PSD-Tạo hình thu nhỏ từ các tệp PSD-Tạo hình thu nhỏ từ các tệp PSD.cs" >}}
## **Tạo tệp PSD có chứa chỉ mục**
Aspose.PSD cho .NET API có thể tạo tệp PSD có chứa chỉ mục từ đầu. Bài viết này chỉ ra cách sử dụng PsdOptions và [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) lớp để tạo một PSD có chứa chỉ mục trong khi vẽ một số hình dạng trên bề mặt mới tạo. Các bước đơn giản sau là cần thiết để tạo một tệp PSD có chứa chỉ mục.

- Tạo một phiên bản của PsdOptions và thiết lập nguồn của nó.
- Thiết lập thuộc tính ColorMode của PsdOptions thành ColorModes.Indexed.
- Tạo một bảng màu mới từ không gian màu RGB và đặt nó là Thuộc tính Palette của PsdOptions.
- Thiết lập thuộc tính CompressionMethod thành thuật toán nén yêu cầu.
- Tạo một hình ảnh PSD mới bằng cách gọi phương thức PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- Vẽ đồ họa hoặc thực hiện các hoạt động khác theo yêu cầu.
- Call phương thức PsdImage.Save để xác nhận tất cả các thay đổi.


Mã nguồn sau cho thấy cách tạo các tệp PSD có chứa chỉ mục.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose-Sửa đổi-Và- Chuyển đổi-Hình ảnh-PSD-Tạo Tệp PSD Chứa Chỉ mục-Tạo Tệp PSD Chứa Chỉ mục.cs" >}}
## **Xuất lớp PSD sang hình ảnh raster**
Aspose.PSD cho .NET cho phép bạn xuất các lớp trong tệp PSD thành hình ảnh raster. Vui lòng sử dụng phương thức [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) để xuất lớp sang hình ảnh. Mã mẫu dưới đây tải một tệp PSD và xuất mỗi lớp của nó thành một hình ảnh PNG bằng cách sử dụng Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Khi tất cả các lớp được xuất thành hình ảnh PNG, bạn có thể mở chúng bằng trình xem hình ảnh yêu thích của mình. Mã nguồn sau cho thấy cách xuất lớp PSD sang hình ảnh raster.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose-Sửa đổi-Và- Chuyển đổi-Hình ảnh-PSD-Xuất Lớp PSD Sang Hình ảnh Raster-Xuất Lớp PSD Sang Hình ảnh Raster.cs" >}}
## **Cập nhật Lớp Văn bản Trong Tệp PSD**
Aspose.PSD cho .NET cho phép bạn thao tác văn bản trong lớp văn bản của tệp PSD. Vui lòng sử dụng [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) lớp để cập nhật văn bản trong lớp PSD. Mã nguồn dưới đây tải một tệp PSD, truy cập lớp văn bản, cập nhật văn bản và lưu tệp PSD với một tên mới bằng cách sử dụng [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index) phương thức.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose-Sửa đổi-Và- Chuyển đổi-Hình ảnh-PSD-Cập Nhật Lớp Văn bản Trong Tệp PSD-Cập Nhật Lớp Văn bản Trong Tệp PSD.cs" >}}
## **Phát hiện PSD đã được phẳng**
Aspose.PSD cho .NET cho phép bạn xác định xem một tệp PSD cụ thể đã được phẳng hoặc chưa. Thuộc tính IsFlatten đã được giới thiệu trong lớp Aspose.PSD.FileFormats.Psd.PsdImage để thực hiện chức năng này. Mã nguồn dưới đây tải một tệp PSD và truy cập thuộc tính [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose-Sửa đổi-Và-Chuyển đổi-Hình ảnh-PSD-Phát Hiện PSD Đã Được Phẳng-Phát Hiện PSD Đã Được Phẳng.cs" >}}
## **Gộp các lớp PSD**
Bài viết này chỉ ra cách gộp các lớp trong tệp PSD trong quá trình chuyển đổi tệp PSD sang JPG với Aspose.PSD. Trong ví dụ dưới đây, một tệp PSD hiện có được tải bằng cách chuyển đường dẫn tệp vào phương thức tĩnh Load của lớp Image. Sau khi tải, chuyển đổi/đúc hình ảnh sang PsdImage. Tạo một phiên bản của lớp JpegOptions và thiết lập các thuộc tính khác nhau. Bây giờ gọi phương thức Save của thực thể PsdImage. Mã nguồn sau cho thấy cách gộp các lớp PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ví dụ-CSharp-Aspose-Sửa đổi-Và- Chuyển đổi-Hình ảnh-PSD-Gộp Các Lớp PSD-Gộp Các Lớp PSD.cs" >}}
## **Hỗ trợ Grayscale Với Alpha cho PSD**
Bài viết này chỉ ra cách hỗ trợ Grayscale với Alpha cho tệp PSD trong quá trình chuyển đổi tệp PSD sang PNG với Aspose.PSD. Trong ví
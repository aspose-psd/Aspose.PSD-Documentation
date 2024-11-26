---
title: Tạo, Mở và Lưu Tệp PSD
type: docs
weight: 10
url: /vi/tạo-mở-và-lưu-tệp-psd/
---

## **Xuất Ảnh Sang Định dạng PSD**
PSD, tài liệu PhotoShop, là định dạng tệp mặc định được sử dụng bởi Adobe PhotoShop để làm việc với hình ảnh. Aspose.PSD cho phép bạn tải, chỉnh sửa và lưu tệp vào PSD để có thể mở và chỉnh sửa trong PhotoShop. Bài viết này cho thấy cách lưu một tệp vào PSD với Aspose.PSD, và nó cũng thảo luận về một số thiết lập có thể được sử dụng khi lưu vào định dạng này. PsdOptions là một lớp chuyên biệt nằm trong không gian tên ImageOptions được sử dụng để xuất ảnh sang PSD. Để xuất sang PSD, tạo một thể hiện của lớp Image, enther được tải từ một tệp hình ảnh hiện có (ví dụ: hình ảnh thu nhỏ) hoặc được tạo mới từ đầu. Bài viết này giải thích cách làm điều đó. Trong các ví dụ bên dưới, một hình ảnh được tạo mới từ đầu. Khi nó được tạo và dữ liệu pixel được điền, lưu hình ảnh bằng phương thức Save của lớp Image và cung cấp một đối tượng PsdOptions như đối số thứ hai. Một số thuộc tính của lớp PsdOptions có thể được thiết lập cho phần chuyển đổi nâng cao. Một số thuộc tính là ColorMode, CompressionMethod và Version. Aspose.PSD hỗ trợ các phương pháp nén sau thông qua việc nén của CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Các chế độ màu sau được hỗ trợ thông qua việc màu của ColorModes enumeration:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Các tài nguyên bổ sung có thể được thêm vào, chẳng hạn như tài nguyên hình thu nhỏ cho PSD v4.0, v5.0 và cao hơn, hoặc lưới và hướng dẫn cho PSD v4.0 và cao hơn. Mã dưới đây tạo một tệp BMP từ đầu, điền vào các điểm ảnh và lưu vào PSD với nén RLE và chế độ màu xám. Đoạn mã dưới đây cho thấy cách xuất ảnh sang PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Nhập ảnh vào Lớp PSD**
Bài viết này demo phương pháp sử dụng Aspose.PSD để thêm hoặc nhập một hình ảnh vào một lớp PSD. Các API Aspose.PSD đã tiết lộ các phương thức hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD đã tiết lộ phương thức DrawImage của lớp Layer để thêm/nhập một hình ảnh vào tệp PSD. Phương thức DrawImage cần vị trí và giá trị hình ảnh để thêm/nhập một hình ảnh vào tệp PSD. Các bước để nhập hình ảnh vào lớp PSD rất đơn giản như dưới đây:

- Tải 1 tệp PSD như một hình ảnh bằng phương thức nhà máy Load được tiết lộ bởi lớp Image.
- Tạo một thể hiện của lớp Layer và gán lớp hình ảnh PSD cho nó.
- Tải hình ảnh cần được thêm vào hoặc tạo một từ đầu.
- Gọi phương thức Layer.DrawImage khi xác định vị trí và thể hiện hình ảnh.
- Lưu các kết quả.



Đoạn mã dưới đây cho thấy cách nhập ảnh vào lớp PSD.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Tạo Hình thu nhỏ từ Tệp PSD**
PSD là định dạng tài liệu tự nhiên của ứng dụng Photoshop của Adobe. Adobe Photoshop (phiên bản 5.0 và cao hơn) lưu thông tin hình thu nhỏ cho hiển thị xem trước trong một khối tài nguyên hình ảnh bao gồm một tiêu đề 28 byte ban đầu, tiếp theo là một hình thu nhỏ JFIF theo thứ tự RGB (đỏ, xanh lá cây, xanh dương). API Aspose.PSD cung cấp một cơ chế sử dụng dễ sử dụng để truy cập các tài nguyên của tệp PSD. Các tài nguyên này cũng bao gồm tài nguyên hình thu nhỏ mà có thể được truy xuất và lưu vào ổ đĩa theo nhu cầu của ứng dụng. Đoạn mã dưới đây cho thấy cách tạo hình thu nhỏ từ Tệp PSD.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Tạo Tệp PSD Chỉ mục**
Aspose.PSD cho Java API có thể tạo các tệp PSD Chỉ mục từ đầu. Bài viết này cho thấy việc sử dụng các lớp PsdOptions và PsdImage để tạo một tệp PSD Chỉ mục trong khi vẽ một số hình dạng trên bảng vẽ mới được tạo. Các bước đơn giản sau cần thiết để tạo một tệp PSD Chỉ mục.

- Tạo một thể hiện của PsdOptions và đặt nguồn.
- Đặt thuộc tính ColorMode của PsdOptions thành ColorModes.Indexed.
- Tạo một bảng màu mới từ không gian RGB và đặt nó là thuộc tính Palette của PsdOptions.
- Đặt thuộc tính CompressionMethod thành thuật toán nén cần thiết.
- Tạo một hình ảnh PSD mới bằng cách gọi phương thức PsdImage.Create.
- Vẽ đồ họa hoặc thực hiện các hoạt động khác theo yêu cầu.
- Gọi phương thức PsdImage.Save để xác nhận tất cả các thay đổi.

Đoạn mã dưới đây cho thấy cách tạo tệp PSD Chỉ mục.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}


## **Xuất lớp PSD Sang Ảnh Raster**
Aspose.PSD cho Java cho phép bạn xuất các lớp trong một tệp PSD thành hình ảnh raster. Vui lòng sử dụng phương thức Aspose.PSD.FileFormats.Psd.Layers.Layer.Save để xuất lớp sang hình ảnh. Đoạn mã mẫu sau tải một tệp PSD và xuất mỗi lớp của nó thành hình ảnh PNG bằng phương thức Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Khi tất cả các lớp được xuất thành hình ảnh PNG, bạn có thể mở chúng bằng trình xem hình ảnh yêu thích của bạn. Đoạn mã dưới đây cho thấy cách xuất lớp PSD sang hình ảnh raster.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Mẫu-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}

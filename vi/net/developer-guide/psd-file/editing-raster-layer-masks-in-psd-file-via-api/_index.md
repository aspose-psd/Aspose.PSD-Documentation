---
title: Chỉnh sửa các lớp mặt nạ raster trong tệp PSD thông qua API
type: docs
weight: 20
url: /vi/net/chinh-sua-cac-lop-mat-na-raster-trong-tep-psd-thong-qua-api/
---

## **Tổng quan**
**Để tự động hóa việc chỉnh sửa định dạng PSD và thay đổi tệp PSD mà không cần Adobe® Photoshop®, bạn có thể sử dụng API Aspose.PSD được cung cấp dưới đây. Có các đoạn mã C# và .NET có thể giúp bạn chỉnh sửa tệp PSD.**

Sử dụng các Mặt nạ Lớp và Vector trong PSD giúp chúng ta ẩn và hiện pixel lớp mà không xóa vĩnh viễn chúng. Các mặt nạ raster còn được gọi là mặt nạ lớp hoặc mặt nạ người dùng. Truy cập vào cả mặt nạ raster và vector trong Aspose.PSD được cung cấp thông qua thuộc tính lớp [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) mà có thể là một trường hợp của lớp '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' và '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' là các lớp con của lớp trừu tượng 'LayerMaskData'. Nếu một lớp có cả mặt nạ raster và vector thì sẽ cung cấp trường hợp của [LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull). Nếu một lớp chỉ có một mặt nạ raster hoặc một mặt nạ vector thì sẽ cung cấp trường hợp của [LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort). Nếu thuộc tính LayerMaskData là null thì lớp đó không có mặt nạ hoặc chỉ có một mặt nạ vector bị vô hiệu hóa.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Một mặt nạ raster và một mặt nạ vector đã vô hiệu hóa LayerMaskDataShort</p><p>Một mặt nạ raster đã vô hiệu hóa LayerMaskDataShort</p><p>Một mặt nạ raster và một mặt nạ vector LayerMaskDataFull</p><p>Một mặt nạ raster LayerMaskDataShort</p><p>Một mặt nạ vector LayerMaskDataShort</p><p>Một mặt nạ vector đã vô hiệu hóa null (Nhưng tài nguyên vector vẫn được cung cấp)</p>|
| :- | :- |
## **Làm thế nào để lấy một mặt nạ raster lớp trong tệp PSD?**
Đầu tiên, chúng ta cần tìm hiểu xem một lớp có cả mặt nạ vector và lớp không:

Mã mẫu dưới đây thể hiện cách lấy một mặt nạ raster lớp

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

Nếu không, loại của thuộc tính lớp LayerMaskData là LayerMaskDataShort. Trong trường hợp này, hãy kiểm tra xem lớp đã có chỉ mặt nạ raster bằng cách kiểm tra thuộc tính Flags. Nó không nên chứa [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData**, nếu không thì mặt nạ là một bộ nhớ đệm mặt nạ vector**.**

Thu thập đoạn mã mặt nạ:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Nếu bạn cần **trích xuất một mặt nạ raster** dưới dạng LayerMaskDataShort (để tiếp tục điều chỉnh) ngay cả khi cả hai mặt nạ hiện, LayerMaskDataFull nên được trích xuất và chuyển đổi thành LayerMaskDataShort. Mã sau có thể được sử dụng cho cả hai trường hợp:

Trích xuất một mặt nạ raster từ PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **Làm thế nào để kiểm tra xem một lớp trong tệp PSD có một mặt nạ raster không?**
Đoạn mã C# sau có thể giúp bạn kiểm tra xem một lớp có mặt nạ raster không:

Làm thế nào để biết xem mặt nạ raster được áp dụng vào [Lớp PSD](/psd/vi/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **Làm thế nào để xóa / thêm / cập nhật một mặt nạ raster lớp trong tệp PSD?**
Chỉ việc xóa / thêm / cập nhật LayerMaskData không đủ để lưu chính xác vì các kênh không được cập nhật; tuy nhiên có thể cung cấp hiển thị chính xác. Điều này không thay đổi các kênh mặt nạ:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Chúng ta nên sử dụng phương thức AddLayerMask của lớp để xóa / thêm / cập nhật.

Điều này thêm / cập nhật cả hai mặt nạ và kênh:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Điều này xóa cả hai mặt nạ và kênh:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **Xóa một mặt nạ raster lớp trong hình ảnh PSD**
Đầu tiên, chúng ta kiểm tra xem mặt nạ có ở định dạng ngắn không và nếu không phải mặt nạ vector chúng ta có thể gọi phương thức AddLayerMask với giá trị null để xóa mặt nạ raster. Nhưng nếu ở định dạng đầy đủ, chúng ta phải chuyển đổi nó thành định dạng ngắn để chỉ còn lại mặt nạ vector. Để xóa một mặt nạ lớp, đoạn mã C# .NET sau có thể được sử dụng:

Đoạn mã về cách xóa Mặt nạ Lớp khỏi Tệp PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **Cập nhật một mặt nạ raster lớp trong hình ảnh PSD**
Điều này rất đơn giản: nếu mặt nạ ở định dạng ngắn thì chúng ta phải thay đổi ImageData và MaskRectangle nếu cần, nếu không, UserMaskData và UserMaskRectangle nên được thay đổi. Đoạn mã C# .NET sau có thể được sử dụng để cập nhật một mặt nạ lớp:

Cập nhật Mặt nạ Lớp PSD với C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Dưới đây là một ví dụ về các hành động có thể thay đổi một mặt nạ raster. Ví dụ này đảo ngược một mặt nạ người dùng của lớp:

Cập nhật Mặt nạ Lớp PSD với C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **Cập nhật một mặt nạ vector trong tệp PSD khi còn mặt nạ raster lớp**
Điều này giả sử rằng người dùng đã thay đổi nguồn tài nguyên vector. Sau đó, có thể cập nhật mặt nạ vector bằng cách gọi phương thức [AddLayerMask](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask) của lớp:

Cập nhật [Mặt nạ Vector Lớp PSD](/psd/vi/net/layer-vector-mask/) với C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **Thêm một lớp mặt nạ raster vào tệp PSD**
Nếu một lớp không có mặt nạ, chúng ta có thể thêm mặt nạ raster cụ thể bằng cách gọi phương thức AddLayerMask của lớp.

Nếu mặt nạ không có [UserMaskFromRenderingOtherData**](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)flag thì đã có mặt nạ raster và chúng ta cần cập nhật như mô tả ở trên. Nếu không, nếu mặt nạ này ở định dạng ngắn chúng ta chuyển đổi thành định dạng đầy đủ. Nếu không chúng ta sử dụng như vậy. Sau đó cập nhật UserMaskData, UserMaskRectangle và các thuộc tính khác với các thuộc tính mặt nạ cung cấp. Đoạn mã C# .NET sau có thể được sử dụng để thêm (cập nhật) một mặt nạ lớp:

Thêm Mặt nạ Lớp mới vào PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Làm thế nào để kiểm tra xem một lớp có mặt nạ đã được bật hay chưa?**
Để biết trạng thái một lớp mặt nạ raster đã bật chúng ta có thể kiểm tra trạng thái cờ LayerMaskFlags.Disabled trong thuộc tính Flags cho LayerMaskDataShort hoặc trong RealFlags cho LayerMaskDataFull. Đoạn mã C# .NET sau có thể được sử dụng để lấy trạng thái một lớp mặt nạ đã bật:

Kiểm tra xem một mặt nạ đã bật:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}
## **Làm thế nào để kích hoạt hoặc vô hiệu hóa một mặt nạ raster lớp?**
Để kích hoạt hoặc vô hiệu hóa một mặt nạ raster lớp, chúng ta có thể thay đổi trạng thái cờ LayerMaskFlags.Disabled trong thuộc tính Flags cho LayerMaskDataShort hoặc trong RealFlags cho LayerMaskDataFull. Đoạn mã C# .NET sau có thể được sử dụng để thay đổi trạng thái một mặt nạ lớp đã bật:

Kích hoạt hoặc vô hiệu hóa Mặt nạ Lớp Raster:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}

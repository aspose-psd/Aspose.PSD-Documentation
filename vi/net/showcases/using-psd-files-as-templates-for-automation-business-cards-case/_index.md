---
title: Sử dụng tệp PSD như các mẫu cho tự động hóa - Trường hợp Thẻ danh thiếp
type: docs
weight: 10
url: /vi/net/su-dung-tep-psd-nhu-cac-mau-cho-tu-dong-hoa-truong-hop-the-danh-thiep/
---

### **Tổng quan**
Bài viết này mô tả các trường hợp thường được sử dụng khi bạn cần cập nhật một số lớp trong [Tệp PSD](https://wiki.fileformat.com/image/psd/) một cách tự động, trong đó tệp PSD/PSB có cấu trúc giống như một mẫu đã biết trước. Điều này có thể được sử dụng để tạo ra một lượng lớn Thẻ danh cho các người khác nhau (Trường hợp Thẻ danh). Hoặc bạn cần thực hiện việc dịch tệp PSD sang các ngôn ngữ khác với việc thay thế một số tài liệu đồ họa trong đó.

Sau khi đọc bài viết này, bạn sẽ biết cách thực hiện điều này:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
## **Trường hợp đơn giản**
Ví dụ, bạn có một Mẫu PSD với các Tên Lớp đã biết. Vì vậy, bạn cần thay đổi, cập nhật hoặc thay thế Lớp PSD thông qua C#. Đầu tiên, bạn cần mở tệp mẫu với Aspose.PSD.

Làm thế nào để mở Tệp PSD qua C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

Sau đó, chúng ta cần tìm một lớp mà chúng ta muốn thay thế theo tên của nó. Dưới đây là một cài đặt đơn giản cho điều này.

Làm thế nào để tìm lớp trong tệp PSD dựa trên tên của nó

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}



Khi tìm thấy lớp, chúng ta có thể cập nhật nó theo cách thông thường, sử dụng [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Làm thế nào để Vẽ trên Lớp PSD Diễn đồ họa

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

Trong trường hợp này, chúng ta vẽ một hình ảnh [PNG](https://wiki.fileformat.com/image/png/) mới được tải lên lớp PSD hiện có, vì vậy dữ liệu cũ sẽ bị mất trong tệp mới.

Nhưng nếu chúng ta cũng cần cập nhật văn bản? Quy trình sẽ tương tự. Tìm [Lớp Văn bản](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) theo tên của nó, sau đó chúng ta cập nhật một cách tự động [Lớp Văn bản của Tệp Photoshop](/psd/vi/net/render-text-with-different-colors-in-text-layer/) bằng C#.

Làm thế nào để cập nhật Lớp Văn bản trong Photoshop sử dụng C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



Cuối cùng, chúng ta cần lưu các thay đổi của chúng tôi:

Làm thế nào để lưu tệp PSD đã thay đổi bằng [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



Hình ảnh kết quả:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


## **Một trường hợp phức tạp với các tính năng bổ sung**
Ở trên, chúng tôi đã chỉ ra cách đơn giản nhất để thay thế hình ảnh trong một lớp của Tệp PSD.

Nhưng Aspose.PSD có thể cung cấp thêm các tính năng bổ sung phức tạp như thêm một lớp mới, loại bỏ các lớp cũ và cập nhật lớp văn bản bằng các kiểu khác nhau trong văn bản nhiều dòng.

Chúng tôi có thể tìm thấy [Lớp](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) mà chúng tôi muốn thay thế, sau đó chúng tôi tìm vị trí của nó trong Danh sách Lớp, loại bỏ nó và chèn một lớp mới sau khi tạo từ [Tệp Jpeg](https://wiki.fileformat.com/image/jpeg/) vào cùng một vị trí.

Tạo một lớp mới từ tệp và chèn nó vào Hình ảnh PSD bằng [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



Cuối cùng trong đoạn mã tệp này, chúng tôi sửa vị trí của lớp và lưu mảng Lớp mới vào Hình ảnh Psd.

Làm thế nào để sao chép thuộc tính Lớp của [Hình ảnh Psd](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



Và sau tất cả, chúng ta cần cập nhật các lớp văn bản trong hình ảnh PSD hiện có bằng C#. Aspose.PSD hỗ trợ [cập nhật của Lớp Văn bản theo Portion](/psd/vi/net/working-with-text-layers/). Mỗi [phần văn bản](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) có một kết hợp duy nhất của các thuộc tính Style và Paragraph.

Làm thế nào để sao chép thuộc tính Lớp của [Hình ảnh Psd](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



Kết quả, chúng ta đã thay đổi mẫu PSD thông qua mã với một lớp mới từ tệp Jpeg, Png, J2k, Bmp, Gif hoặc Tiff và văn bản nhiều dòng với các [kiểu khác nhau](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) trong mỗi hàng.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)

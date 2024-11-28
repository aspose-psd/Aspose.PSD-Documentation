---
title: Tiêu đề và Đề mục File PSD và PSB
type: tài liệu
weight: 40
url: /vi/net/tieu-de-va-de-muc-file-psd-va-psb/
---

## **Mô tả**
Tiêu đề File Adobe Photoshop chứa thông tin về phiên bản của File (1 cho PSD và 2 cho PSB), Số lượng Kênh, Chế độ Màu và Độ sâu Bit.

Bạn có thể tìm hiểu các Kết hợp của Chế độ Màu và Độ sâu Bit được hỗ trợ bởi Aspose.PSD từ bài viết liên quan.


Tiêu đề File chứa các thuộc tính cơ bản của hình ảnh.

|**Độ dài**|**Mô tả**|
| :- | :- |
|4|Chữ ký: luôn bằng *"8BPS"*|
|2|[Phiên bản PSD](https://reference.aspose.com/psd/vi/aspose.psd.fileformats.psd/fileformatversion): luôn bằng 1 cho Files PSD và 2 cho Files PSB. Aspose.PSD có thể phát hiện phiên bản của Định dạng File và đọc chính xác.| 
|6|Được dành: phải bằng không.| 
|2|Số lượng kênh trong hình ảnh, bao gồm bất kỳ kênh alpha nào. Phạm vi được hỗ trợ là từ 1 đến 56.| 
|4|Độ cao của hình ảnh trong pixel. Phạm vi được hỗ trợ là từ 1 đến 30.000. File PSB hỗ trợ chiều cao lên đến 300.000 pixel. File PSB cũng được hỗ trợ bởi Aspose.PSD.| 
|4|Chiều rộng của hình ảnh trong pixel. Phạm vi được hỗ trợ là từ 1 đến 30.000. File PSB hỗ trợ chiều rộng lên đến 300.000 pixel. Xử lý hàng loạt các file PSD/PSB lớn cũng được hỗ trợ bởi Aspose.PSD.| 
|2|Sâu: số lượng bit trên mỗi kênh. Các giá trị được hỗ trợ là 1, 8, 16 và 32. Nhưng không phải Chế độ Màu nào cũng hoạt động với mọi độ sâu.| 
|2|[Chế độ màu PSD](https://reference.aspose.com/psd/vi/com.aspose.psd.fileformats.psd/ColorModes) của file. Giá trị được hỗ trợ là: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multichannel = 7; Duotone = 8; Lab = 9.| 
Bạn có thể kiểm tra [Tham chiếu API PSD của chúng tôi](https://reference.aspose.com/psd) để biết thêm thông tin.

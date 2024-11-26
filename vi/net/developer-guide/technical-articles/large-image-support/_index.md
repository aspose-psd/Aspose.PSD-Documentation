---
title: Hỗ trợ Ảnh Lớn
type: docs
weight: 40
url: /vi/net/large-image-support/
---

## **Hỗ trợ Ảnh Lớn**
Vì thư viện .NET tiêu chuẩn có một số hạn chế về kích thước ảnh mà nó có thể xử lý, chúng tôi đã giới thiệu một cơ chế mới để hỗ trợ ảnh lớn. Phương pháp mới này vượt qua các hạn chế nhưng do hạn chế về kích thước dữ liệu nên kích thước tối đa được hỗ trợ cho việc tạo và tải là 2,147,483,647 x 2,147,483,647 pixel.
### **Làm việc với Ảnh Lớn**
Aspose.PSD đã cải thiện hiệu suất và hỗ trợ cho ảnh lớn. Việc làm việc với những ảnh có kích thước hàng trăm megabyte không còn là một vấn đề nữa, bạn có thể tạo, tải và vẽ trên những ảnh đó. Tuy nhiên, do xử lý một phần và xử lý các ngoại lệ OutOfMemoryException, hiệu suất có thể rất thấp trên những ảnh rất lớn. Điều này là do Aspose.PSD cố gắng phân phối lại một lượng dữ liệu nhỏ hơn để xử lý và mỗi bước phân phối lại là rất tốn kém. Những lợi ích của kiến trúc mới là rõ ràng:

- Không có hạn chế về kích thước ảnh.
- Bạn không bị giới hạn bởi bộ nhớ có sẵn trên máy tính của bạn.

Nếu bạn gặp vấn đề xử lý chậm, được khuyến nghị tăng tổng lượng RAM để vừa với tất cả các pixel vào bộ nhớ. Nếu không, việc xử lý vẫn có thể thực hiện nhưng chậm hơn. Phương pháp là như sau:

- Gọi phương thức [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) với hình chữ nhật mong muốn và delegate để nhận các pixel được chỉ định.

Aspose.PSD cố gắng tải toàn bộ hình chữ nhật.

- Nếu có đủ bộ nhớ để chứa tất cả các pixel, thì tất cả các pixel đơn giản được trả lại cho người gọi.
- Nếu không đủ bộ nhớ, người gọi nhận được một tập hợp của các pixel từ bên trong hình chữ nhật chỉ định. Khi các pixel đó đã được xử lý, người gọi nhận được hình chữ nhật tiếp theo. Việc xử lý kết thúc khi toàn bộ hình chữ nhật đã được xử lý.

Aspose.PSD cố gắng trích xuất càng nhiều dòng càng tốt. Nếu không đủ bộ nhớ để chứa một dòng duy nhất của pixel, thì một dòng sẽ được chia thành các phần phù hợp với các hình chữ nhật có chiều cao 1. Bạn cũng có thể vẽ trên các ảnh lớn. Quá trình vẽ cố gắng ảnh hưởng toàn bộ hình chữ nhật mong muốn. Nếu không đủ bộ nhớ, việc vẽ được thực hiện trên các hình chữ nhật một phần cho đến khi toàn bộ khu vực được vẽ. Ngoài ra, Aspose.PSD hỗ trợ lưu trữ và xuất ảnh lớn. Lưu ảnh nguồn lại vào ổ đĩa hoặc xuất nó sang một định dạng tệp khác. Quá trình lưu hoặc xuất được thực hiện bằng cách sử dụng các hình chữ nhật một phần nếu cần thiết. 
### **Định Dạng Ảnh Được Hỗ Trợ**
Các định dạng sau được hỗ trợ cho việc xử lý ảnh lớn:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Các định dạng trên có thể được xử lý an toàn thông qua việc tạo, sửa đổi, thực hiện các thao tác vẽ, lưu vào ổ đĩa hoặc xuất sang định dạng khác mà không cần quan tâm đến kích thước ảnh.

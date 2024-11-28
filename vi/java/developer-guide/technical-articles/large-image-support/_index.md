---
title: Hỗ Trợ Hình Ảnh Lớn
type: docs
weight: 60
url: /vi/java/large-image-support/
---

## **Hỗ Trợ Hình Ảnh Lớn**
Vì thư viện Java tiêu chuẩn có một số hạn chế về kích thước hình ảnh mà nó có thể xử lý, chúng tôi đã giới thiệu một cơ chế mới để hỗ trợ hình ảnh lớn. Phương pháp mới vượt qua các hạn chế nhưng do hạn chế về kích thước dữ liệu, kích thước tối đa được hỗ trợ cho việc tạo và tải là 2,147,483,647 x 2,147,483,647 điểm ảnh.
### **Làm Việc với Hình Ảnh Lớn**
Aspose.PSD đã cải thiện hiệu suất và hỗ trợ cho hình ảnh lớn. Ảnh có kích thước hàng trăm megabyte không còn là vấn đề nên bạn có thể tạo, tải và vẽ trên những hình ảnh đó. Tuy nhiên, do việc xử lý một phần và xử lý các ngoại lệ OutOfMemoryException, hiệu suất có thể rất thấp trên những hình ảnh rất lớn. Điều này là do Aspose.PSD cố gắng cấp phát lại một lượng dữ liệu nhỏ hơn cho việc xử lý và mỗi bước cấp phát lại rất tốn kém. Những lợi ích của kiến trúc mới là rõ ràng:

- Không giới hạn kích thước hình ảnh.
- Bạn không bị giới hạn bởi bộ nhớ có sẵn trên máy tính của bạn.

Nếu bạn gặp vấn đề về tốc độ xử lý, khuyến nghị là tăng tổng lượng RAM để phù hợp với tất cả các điểm ảnh của bạn vào bộ nhớ. Nếu không, việc xử lý vẫn có thể thực hiện nhưng chậm hơn. Phương pháp là như sau:

- Gọi phương thức LoadPartialPixels với hình chữ nhật mong muốn và ủy nhiệm nhận các điểm ảnh đã tải cụ thể.

Aspose.PSD cố gắng tải toàn bộ hình chữ nhật.

- Nếu có đủ bộ nhớ để chứa tất cả các điểm ảnh, thì tất cả các điểm ảnh được trả về đơn giản cho người gọi.
- Nếu không đủ bộ nhớ, người gọi nhận 1 tập hợp con của các điểm ảnh từ bên trong hình chữ nhật đã chỉ định. Khi các điểm ảnh đó được xử lý, người gọi nhận hình chữ nhật tiếp theo. Việc xử lý kết thúc khi toàn bộ hình chữ nhật được xử lý.

Aspose.PSD cố gắng trích xuất càng nhiều dòng càng tốt. Nếu không đủ bộ nhớ để chứa một dòng duy nhất của điểm ảnh, thì một dòng duy nhất sẽ được chia thành các phần tuân thủ với các hình chữ nhật có chiều cao là 1. Bạn cũng có thể vẽ trên hình ảnh lớn. Quá trình vẽ cố gắng ảnh hưởng toàn bộ hình chữ nhật mong muốn. Nếu không đủ bộ nhớ, việc vẽ được thực hiện trên các hình chữ nhật phần bổ cho đến khi toàn bộ diện tích được vẽ. Ngoài ra, Aspose.PSD hỗ trợ lưu và xuất hình ảnh lớn. Lưu hình ảnh nguồn vào đĩa hoặc xuất nó sang một định dạng tập tin khác. Quá trình lưu hoặc xuất được thực hiện bằng cách sử dụng hình chữ nhật phần bổ nếu cần thiết. 
### **Định Dạng Hình Ảnh Được Hỗ Trợ**
Các định dạng sau được hỗ trợ cho xử lý hình ảnh lớn:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Các định dạng trên có thể được xử lý một cách an toàn thông qua việc tạo mới, chỉnh sửa, áp dụng các thao tác vẽ, lưu vào đĩa hoặc xuất ra bất kỳ kích thước hình ảnh nào.

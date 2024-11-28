---
title: Xử Lý Dữ Liệu Gốc
type: docs
weight: 50
url: /vi/net/raw-data-processing/
---

## **Xử Lý Dữ Liệu Gốc**
Để cải thiện hiệu suất API Aspose.PSD, chúng tôi đã giới thiệu một phương thức xử lý dữ liệu gốc trong phiên bản 2.4.0. Việc xử lý dữ liệu gốc hiện đang được sử dụng bên trong và có một API bên ngoài để có thể sử dụng từ bên ngoài thư viện để cải thiện hiệu suất tổng thể. Đôi khi việc xử lý trở nên phức tạp và cần một số giải thích. Hiện tại, xử lý dữ liệu gốc chỉ có sẵn cho định dạng BMP.

Để giúp nhà phát triển đạt được hiệu suất tốt nhất, API Aspose.PSD cung cấp hệ thống xử lý dữ liệu gốc có một API bên ngoài cho tùy chỉnh. Nhà phát triển gọi các phương thức [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) và [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) để sử dụng xử lý dữ liệu gốc. Những phương thức này cũng yêu cầu định dạng dữ liệu gốc mong muốn được thiết lập bằng cách sử dụng lớp [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings). Lớp RawDataSettings cho phép nhà phát triển chỉ định bất kỳ định dạng dữ liệu gốc nào. Tuy nhiên, để đạt được hiệu suất tốt nhất, bạn cần sử dụng định dạng dữ liệu gốc mà dữ liệu đang được lưu trữ trong đó. RawDataSettings được xác định trong lớp [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) giúp xác định định dạng dữ liệu gốc của hình ảnh. Khi đưa ví dụ RawDataSettings vào phương thức LoadRawData, dữ liệu sẽ được trả về như vậy, mà không cần thực hiện bất kỳ chuyển đổi nào, và có thể cải thiện hiệu suất. Ngược lại, bạn cần chú ý đến tất cả các bố cục định dạng dữ liệu gốc có thể đôi khi hơi phức tạp.

Để đơn giản hóa quá trình xử lý, với một số chi phí về hiệu suất, bạn có thể chỉ định RawDataSettings mong muốn bằng cách khởi tạo lớp với các cài đặt dữ liệu gốc mong muốn. Có những trường hợp khi không thể trả về dữ liệu gốc ở định dạng đã chỉ định (ví dụ: chuyển đổi từ không gian màu CMYK thành RGB không khả dụng trong phiên bản 2.4.0). Hơn nữa, có thể xảy ra các tình huống khi xử lý dữ liệu gốc không khả dụng cho một định dạng hình ảnh nào đó. Để xác định có thể sử dụng phương thức LoadRawData và SaveRawData, bạn cần kiểm tra thuộc tính [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable).
### **Tri Thức**
Đối với định dạng [dữ liệu pixel](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) RGB, có các định dạng dữ liệu gốc dựa trên bảng màu và RGB. Các định dạng dữ liệu gốc dựa trên bảng màu chứa chỉ số mục nhập bảng màu trong phạm vi 0..(2^số bit - 1). Các định dạng dữ liệu gốc dựa trên bảng màu là 1, 2, 4 và 8 bit mỗi pixel. Các định dạng còn lại là dựa trên RGB. Khi tải dữ liệu gốc, cần chú ý rằng cần đủ byte để tải dữ liệu, nếu không sẽ có một ngoại lệ tương ứng sẽ được ném ra. Bạn có thể đơn giản ước lượng kích thước mảng byte bằng cách nhân kích thước dòng với số dòng yêu cầu. Kích thước dòng có thể thay đổi và phụ thuộc vào định dạng lưu trữ dữ liệu gốc.

Để đạt được hiệu suất tốt nhất, luôn sử dụng kích thước dòng dữ liệu gốc bằng giá trị thuộc tính [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize). Tuy nhiên, đôi khi bạn có thể cần thêm các byte lề cho các hàng dữ liệu gốc, hoặc giảm bớt nó, và khi đó một kích thước dòng khác có thể được sử dụng. Nếu cần một tập con của hình chữ nhật giới hạn ảnh, hãy xem xét các dịch bit có thể xảy ra đối với định dạng pixel RGB được chỉ mục. Ví dụ, hãy xem xét một hình ảnh có kích thước 100x100 pixel và định dạng dữ liệu gốc 1 bit mỗi pixel. Bạn muốn tải một hình chữ nhật dữ liệu gốc với vị trí (7,0) và (2,1) kích thước, hoặc nói cách khác, bạn cần 2 pixel bắt đầu từ x=7 và y=0. Trong trường hợp này, bạn nên nhận được bố cục dữ liệu sau:




![cần thực hiện: văn bản thay thế cho hình ảnh](raw-data-processing_1.png)

Điều này có nghĩa rằng bạn nhận được 2 byte trong đó byte đầu chứa 7 pixel không mong muốn, sau đó là 1 pixel mong muốn, và byte thứ hai chứa 1 pixel mong muốn và sau đó là 7 pixel không mong muốn. Bạn có thể hỏi tại sao chúng tôi không thực hiện dịch chuyển dữ liệu và đặt những 2 pixel đó vào một byte duy nhất? Câu trả lời rất đơn giản: để giữ cho hiệu suất cao. Tất cả các xử lý nội bộ thường được thực hiện với tất cả dữ liệu bắt đầu từ pixel đầu tiên và kết thúc với pixel cuối cùng có sẵn. Hiếm khi có tình huống mà một tập con pixel được yêu cầu. Ngoài ra, chúng tôi không biết cách những pixel đó sẽ được xử lý sau đó nên việc dịch chuyển sẽ làm giảm hiệu suất và làm cho mã không cần thiết phức tạp. Luôn ước lượng bit đúng (không cần phải xác định byte đúng vì dữ liệu luôn đi với byte đầu tiên được điền) nơi các pixel đòi hỏi sẽ bắt đầu. Để tính toán bit đúng, có thể sử dụng một công thức đơn giản: (rect.Left * số bits) % 8.
### **Chuyển Đổi Màu Indexed RGB**
Để đạt hiệu suất cao nhất có thể, luôn sử dụng cùng các cài đặt dữ liệu gốc nguồn và đích, định dạng pixel và kích thước dòng. Tuy nhiên, đôi khi bạn có thể cần thực hiện chuyển đổi dữ liệu. Ví dụ, bạn có thể tải một hình ảnh RGB 1 bit mỗi pixel và lưu nó với 2 bit mỗi pixel, hoặc tải một hình ảnh RGB 4 bit và giảm phạm vi màu của nó xuống còn 2 bit mỗi pixel. Trong cả hai trường hợp, một chuyển đổi màu nên được áp dụng. Chuyển đổi các hình ảnh RGB chỉ mục có thể đôi khi khó khăn và không thể thực hiện mà không có một số cài đặt áp dụng. Chúng ta cần xác định cách phạm vi màu nguồn được ánh xạ vào không gian màu đích. Để hoàn thành nhiệm vụ này, chúng ta có các [chế độ](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods) khác nhau:

- Ánh xạ bảng màu (DitheringMethods.PaletteConversion)
- Ánh xạ dữ liệu gốc (DitheringMethods.PaletteIgnore)
- Chuyển đổi tùy chỉnh (DitheringMethods.CustomConverter)

Khi sử dụng chế độ ánh xạ bảng màu, không gian màu nguồn cố gắng phù hợp với không gian màu đích càng gần càng tốt. Ví dụ, hãy giả sử chúng ta có một hình ảnh 4 bit với các màu sau:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

Hình ảnh nguồn trông như sau:



![cần thực hiện: văn bản thay thế cho hình ảnh](raw-data-processing_2.png)

Và chúng ta chuyển hình ảnh 4 bit sang hình ảnh 1 bit với các màu bảng màu sau được xác định:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Trong trường hợp chuyển đổi bảng màu, bộ chuyển đổi đọc màu nguồn và xác định chỉ mục mục tiêu bằng cách sử dụng phương thức [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) của bảng màu mục tiêu. Giá trị thuộc tính [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) được sử dụng trong trường hợp phương thức GetNearestColorIndex của bảng màu cung cấp một chỉ mục nằm ngoài phạm vi. Điều này chuyển đổi các màu nguồn thành các màu đích gần nhất về giá trị cường độ. Hình ảnh đích phù hợp nhất với hình ảnh nguồn càng gần càng tốt. Bạn có thể xem kết quả sau:



![cần thực hiện: văn bản thay thế cho hình ảnh](raw-data-processing_3.png)

Trong chế độ ánh xạ dữ liệu gốc, sử dụng một tình huống khác. Các bảng màu nguồn và đích đơn giản bị bỏ qua và các chỉ số nguồn được ánh xạ sang chỉ số đích. Khi tìm thấy một giá trị không thể ánh xạ vào phạm vi đích (khi giảm số bit), sau đó giá trị của RasterImage.RawFallbackIndex sẽ được sử dụng. Giá trị này mặc định là 0 và sẽ được ánh xạ vào màu đầu tiên trong bảng màu đích. Nếu giá trị thuộc tính này nằm ngoài phạm vi đích, một ngoại lệ tương ứng sẽ được ném ra. Điều này dẫn đến kết quả ít đoán trước hơn có thể được hiển thị trên hình ảnh sau:



![cần thực hiện: văn bản thay thế cho hình ảnh](raw-data-processing_4.png)

Chế độ ánh xạ bảng màu là giải pháp đúng đắn hơn cho vấn đề ánh xạ màu nhưng nó cũng mất một chút thời gian hơn để hoàn thành vì cần thực hiện tính toán để ước lượng ánh xạ bảng màu chính xác. (Thường thì không có sự khác biệt hiệu suất lớn giữa hai phương pháp.) Ngược lại, chế độ ánh xạ dữ liệu gốc thực hiện nhanh hơn một chút và có thể được sử dụng cho việc chuyển đổi màu cơ bản hơn khi việc ánh xạ màu chính xác không quá quan trọng. Ví dụ, có những trường hợp khi bảng màu màu nguồn đã được cắt giảm và có thể an toàn chuyển đổi sang số lượng bit ít hơn vì các bit phụ không bao giờ được sử dụng.

Để sử dụng bất kỳ trong các phương pháp này, sử dụng thuộc tính RawDitheringMethod của lớp RasterImage. Theo mặc định, nó được thiết lập cho phương pháp chuyển đổi bảng màu để đạt được kết quả tốt nhất về mặt thẩm mĩ. Bạn có thể thay đổi thuộc tính này trước bất kỳ việc chuyển đổi nào diễn ra (ví dụ, khi lưu hình ảnh
---
title: Xử lý Dữ liệu Thô
type: docs
weight: 70
url: /vi/java/xu-ly-du-lieu-tho/
---

## **Xử lý Dữ liệu Thô**
Để cải thiện hiệu suất của API Aspose.PSD, chúng tôi giới thiệu một phương pháp cho xử lý dữ liệu thô với phiên bản 2.4.0. Việc xử lý dữ liệu thô được sử dụng ở mức độ nội bộ và có một API bên ngoài để có thể sử dụng từ bên ngoài thư viện để tối ưu hiệu suất tổng thể. Đôi khi quá trình xử lý trở nên phức tạp và cần một số giải thích. Hiện tại, xử lý dữ liệu thô chỉ có sẵn cho định dạng BMP.

Để giúp các nhà phát triển đạt được hiệu suất tốt nhất, API Aspose.PSD cung cấp một hệ thống xử lý dữ liệu thô có API bên ngoài để tùy chỉnh. Các nhà phát triển gọi tới họ LoadRawData và SaveRawData các phương thức để sử dụng xử lý dữ liệu thô. Để đạt được hiệu suất tốt nhất, bạn cần sử dụng định dạng dữ liệu thô mà dữ liệu đã được lưu trữ trong đó. Lớp RawDataSettings cho phép các nhà phát triển chỉ định bất kỳ định dạng dữ liệu thô nào. Tuy nhiên, để đạt được hiệu suất tốt nhất, bạn cần sử dụng định dạng dữ liệu thô mà dữ liệu đã được lưu trữ trong đó. Các RawDataSettings được xác định trong lớp RasterImage giúp xác định định dạng dữ liệu thô của hình ảnh. Khi truyền thực thể RawDataSettings vào phương thức LoadRawData, dữ liệu sẽ được trả về dưới dạng nguyên sơ, mà không áp dụng bất kỳ chuyển đổi nào, và có thể cải thiện hiệu suất. Ngược lại, bạn cần chú ý đến tất cả các bố cục định dạng dữ liệu thô có thể đôi khi hơi phức tạp.

Để đơn giản hóa quá trình xử lý, với một số phạt hiệu suất nhất định, bạn có thể chỉ định RawDataSettings mong muốn bằng cách khởi tạo lớp với các thiết lập dữ liệu thô mong muốn. Có trường hợp không thể trả về dữ liệu thô ở định dạng được chỉ định (ví dụ: chuyển đổi từ không gian màu CMYK sang RGB không khả dụng trong phiên bản 2.4.0). Hơn nữa, có thể có các tình huống khi xử lý dữ liệu thô không khả dụng cho bất kỳ định dạng hình ảnh nào. Để xác định xem bạn có thể sử dụng các phương thức LoadRawData và SaveRawData hay không, bạn cần kiểm tra tính sẵn có của thuộc tính IsRawDataAvailable.
### **Thông số**
Đối với định dạng dữ liệu pixel RGB, có sẵn các định dạng dữ liệu thô dựa trên bảng màu và dựa trên RGB. Các định dạng dữ liệu thô dựa trên bảng màu chứa các chỉ số mục bảng màu trong phạm vi 0..(2^số bit - 1). Các định dạng dữ liệu thô dựa trên bảng màu là 1, 2, 4 và 8 bit mỗi pixel. Các định dạng còn lại là dựa trên RGB. Khi tải dữ liệu thô, cần chú ý rằng có đủ byte để tải dữ liệu, nếu không, một ngoại lệ phù hợp sẽ được kích hoạt. Bạn có thể ước lượng kích thước mảng byte đơn giản bằng cách nhân kích thước dòng với số dòng cần tải. Kích thước dòng có thể thay đổi và phụ thuộc vào định dạng lưu trữ dữ liệu thô.

Để đạt hiệu suất tốt nhất, luôn sử dụng kích thước dòng dữ liệu thô bằng giá trị thuộc tính RasterImage.RawLineSize. Tuy nhiên, đôi khi bạn có thể cần thêm dữ liệu đệm cho các hàng dữ liệu thô, hoặc giảm nó, và khi điều này xảy ra, có thể sử dụng một kích thước dòng khác. Nếu cần một tập hợp con của một hình chữ nhật hình ảnh, sau đó cân nhắc các dịch chuyển bit có thể xảy ra cho các định dạng dữ liệu pixel RGB được chỉ mục. Ví dụ, hãy xem xét một hình ảnh với kích thước 100x100 pixel và định dạng dữ liệu thô 1 bit mỗi pixel. Bạn muốn tải một hình chữ nhật dữ liệu nguyên thô với vị trí (7,0) và (2,1) kích thước, hoặc nói cách khác, bạn yêu cầu 2 pixel bắt đầu từ x=7 và y=0. Trong trường hợp này, bạn nên nhận bố cục dữ liệu sau đây:



![làm gì đó: văn bản thay thế của hình ảnh](raw-data-processing_1.png)

Điều này có nghĩa là bạn nhận được 2 byte trong đó byte đầu chứa 7 pixel không mong muốn, sau đó là 1 pixel mong muốn, và byte thứ hai chứa 1 pixel mong muốn và sau đó là 7 pixel không mong muốn. Bạn có thể hỏi tại sao chúng tôi không thực hiện việc dịch dữ liệu và đặt những 2 pixel đó vào một byte duy nhất? Câu trả lời đơn giản là để giữ cho hiệu suất cao. Tất cả quá trình xử lý nội bộ thường được thực hiện với tất cả dữ liệu bắt đầu từ pixel đầu tiên và kết thúc với pixel cuối cùng có sẵn. Hiếm khi có tình huống pixel con yêu cầu. Ngoài ra, chúng tôi không biết làm thế nào các pixel sẽ được xử lý sau đó, vì vậy việc dịch sẽ làm giảm hiệu suất và làm cho mã không cần thiết phức tạp. Luôn ước lượng bit đúng (không cần xác định byte đúng vì dữ liệu luôn được đi với byte đầu tiên đã được điền) nơi các pixel đòi hỏi sẽ bắt đầu. Để tính toán bit đúng có thể được sử dụng một công thức đơn giản: (rect.Left * bitsCount) % 8.
### **Chuyển Đổi Màu RGB Chỉ Mục**
Để đạt hiệu suất cao nhất có thể, luôn sử dụng các thiết lập dữ liệu thô nguồn và đích, định dạng pixel và kích thước dòng giống nhau. Tuy nhiên, đôi khi bạn có thể cần thực hiện chuyển đổi dữ liệu. Ví dụ, bạn có thể tải một hình ảnh RGB 1 bit mỗi pixel và lưu nó với 2 bit mỗi pixel, hoặc tải một hình ảnh RGB 4 bit và giảm phạm vi màu của nó xuống còn 2 bit mỗi pixel. Trong cả hai trường hợp, cần áp dụng một chuyển đổi màu. Chuyển đổi một hình ảnh chỉ mục RGB đôi khi rắc rối và không thể thực hiện mà không có một số thiết lập được áp dụng. Chúng ta cần xác định cách phạm vi màu nguồn được ánh xạ vào không gian màu đích. Để thực hiện công việc này, chúng ta có các chế độ khác nhau:

- Ánh xạ bảng màu (DitheringMethods.PaletteConversion)
- Ánh xạ dữ liệu thô (DitheringMethods.PaletteIgnore)
- Chuyển đổi tùy chỉnh (DitheringMethods.CustomConverter)

Khi sử dụng chế độ ánh xạ bảng màu, không gian màu nguồn cố gắng khớp với không gian màu đích càng gần càng tốt. Ví dụ hãy để chúng ta giả sử chúng ta có một hình ảnh 4 bit với các màu sau:
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



![làm gì đó: văn bản thay thế của hình ảnh](raw-data-processing_2.png)

Và chúng ta chuyển đổi hình ảnh 4 bit sang hình ảnh 1 bit với các màu bảng màu được xác định sau:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Trong chế độ ánh xạ bảng màu, bộ chuyển đổi đọc màu nguồn và xác định chỉ số đích bằng cách sử dụng phương thức GetNearestColorIndex của bảng màu đích. Giá trị thuộc tính RasterImage.RawFallbackIndex được sử dụng trong trường hợp phương thức GetNearestColorIndex của bảng màu trả về một chỉ số ngoài phạm vi. Điều này chuyển đổi các màu nguồn sang các màu đích gần nhất về giá trị cường độ. Hình ảnh đích khớp với hình ảnh nguồn càng gần càng tốt. Bạn có thể thấy kết quả sau:



![làm gì đó: văn bản thay thế của hình ảnh](raw-data-processing_3.png)

Trong chế độ ánh xạ dữ liệu thô, một kịch bản khác được sử dụng. Các bảng màu màu nguồn và màu đích đơn giản bị bỏ qua và các chỉ số nguồn được ánh xạ sang chỉ số đích. Khi tìm thấy một giá trị không thể ánh xạ vào phạm vi đích (khi giảm số bit), sau đó giá trị thuộc tính RasterImage.RawFallbackIndex được sử dụng. Giá trị này mặc định là 0 và sẽ được ánh xạ vào màu đầu tiên trong bảng màu đích. Nếu giá trị của thuộc tính này nằm ngoài phạm vi đích, một ngoại lệ phù hợp sẽ được kích hoạt. Điều này dẫn đến kết quả ít biết trước hơn có thể được hiển thị trên hình ảnh sau:



![làm gì đó: văn bản thay thế của hình ảnh](raw-data-processing_4.png)

Chế độ chuyển đổi bảng màu là một giải pháp chính xác hơn cho vấn đề ánh xạ màu nhưng nó cũng mất một chút thời gian hơn để hoàn thành vì cần thực hiện các phép toán để ước lượng ánh xạ bảng màu đúng. (Thường có một sự khác biệt hiệu suất rất nhỏ giữa hai phương pháp này.) Ngược lại, chế độ ánh xạ dữ liệu thô thực hiện một chút nhanh hơn và có thể được sử dụng cho chuyển đổi màu thô hơn khi ánh xạ màu chính xác không quan trọng. Ví dụ, có các trường hợp khi bảng màu màu nguồn bị cắt bớt và có thể an toàn chuyển đổi sang số bit ít hơn vì các bit thừa không được sử dụng.

Để sử dụng bất kỳ phương pháp nào, sử dụng thuộc tính RawDitheringMethod của lớp RasterImage. Theo mặc định, nó được thiết lập cho phương pháp chuyển đổi bảng màu để đạt được kết quả tốt nhất. Bạn có thể thay đổi thuộc tính này trước khi thực hiện bất kỳ chuyển đổi nào (ví dụ: khi lưu hình ảnh vào luồng). Xin lưu ý rằng các phương pháp bỏ qua bảng màu và chuyển đổi bảng màu sẽ không diễn ra nếu bạn đã tải một hình ảnh và ghi đè lên một số dữ liệu pixel ban đầu vì dữ liệu mới được lưu vào bộ đệm và bộ đệm lưu trữ dữ liệu theo định dạng tối đa có sẵn 32ARGB (tính đến 2.4.0, có thể thay đổi). Định dạng này được sử dụng để khắc phục vấn đề với các phạm vi màu khác nhau có thể xảy ra đối với hình ảnh đã tải và đã lưu. Hơn nữa, các
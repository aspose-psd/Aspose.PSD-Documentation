---
title: Điều chỉnh Lớp Cân bằng Màu
type: docs
weight: 30
url: /vi/java/layer-types/adjustment-layer/color-balance/
---

# Làm việc với lớp điều chỉnh cân bằng màu trong Photoshop bằng Java

Trong bài viết này, chúng ta sẽ **điều chỉnh cân bằng màu của hình ảnh** trong định dạng tệp PSD bằng Java. Chúng ta sẽ sử dụng một thư viện đặc biệt có tên Aspose.PSD cho Java, đây là một công cụ cho việc xử lý tài liệu Photoshop.

Vì thư viện làm việc với định dạng tệp PSD nên nó chứa hầu hết [tất cả các tính năng](https://docs.aspose.com/psd/java/features/) có sẵn trong trình chỉnh sửa Photoshopvà **lớp điều chỉnh cân bằng màu** , một tính năng rất phù hợp cho công việc này, không phải là một ngoại lệ.

Lớp điều chỉnh cân bằng màu cho phép thay đổi sự cân bằng giữa các màu chính (RGB) và các màu trừ (-CMY) cho bóng, điểm trung và đèn cao cấp một cách đơn giản và nhanh chóng.

## Điều chỉnh cân bằng màu

Như đã đề cập trước đó, lớp điều chỉnh cân bằng màu trong Aspose.PSD cho Java chính là **trình cân bằng giữa màu chính và màu trừ**. Điều này có nghĩa là có ba thang đo cho mỗi cặp màu (cyan/đỏ, magenta/xanh lá cây, vàng/xanh). Độ cường độ của màu cụ thể trong cặp màu sẽ tăng nếu giá trị di chuyển về phía nó và ngược lại. Hơn nữa, ba cặp màu này ứng với mỗi khu vực của dải tông sắc (bóng, điểm trung và đèn cao cấp) tăng tính linh hoạt của kiểu điều chỉnh này.

Vì vậy, hãy áp dụng kiến thức này vào thực hành. Ví dụ, chúng ta chọn một bức ảnh mặt của một phụ nữ có tông màu đỏ (b). Bức mặt có thể quá hồng và chúng ta sẽ sửa điều đó bằng cách **thêm lớp điều chỉnh cân bằng màu** để giảm đỏ và tăng cyan cơ bản (a) để có được bức mặt trông tự nhiên hơn (c). Một lần nữa, vẫn còn rất nhiều công việc phải làm với bức ảnh này nhưng trong bài viết này đó là tất cả chúng ta sẽ làm.

![Ví dụ lớp điều chỉnh cân bằng màu](color-balance-adjustment-layer-example-figure-1.png) API của lớp điều chỉnh cân bằng màu có thiết kế phẳng. Do đó, [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) là tất cả những gì bạn cần. Trước hết, bảo toàn độ sáng vì nó đã bị vô hiệu hóa mặc định. Sau đó, thêm một chút xanh và nhiều vàng cho bóng bằng các phương thức tương ứng (tên của họ bao gồm tên khu vực dải tông nhất định và tên màu trong cặp màu), sau đó thêm nhiều cyan và một chút xanh cho điểm trung và cuối cùng thêm nhiều cyan ngoài một chút magenta và xanh:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Giờ chúng ta có được bức ảnh mà chúng ta muốn! Điều này đơn giản quá, phải không?

Hãy chú ý rằng _giá trị của mỗi cặp màu phải nằm trong khoảng từ -100 đến 100_ với giá trị âm cho các màu trừ và dương cho màu chính tương ứng, giống như trong trình chỉnh sửa Photoshop.

Tham khảo tài liệu API của chúng tôi để biết thêm chi tiết kỹ thuật về [lớp điều chỉnh cân bằng màu](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Kết luận

Trong bài viết này, chúng ta đã xem xét cách điều chỉnh Cân bằng Màu của hình ảnh theo cách lập trình trong Java bằng thư viện Aspose.PSD cho Java. Thư viện chứa API đầy đủ tính năng để làm việc với các lớp điều chỉnh cân bằng màu trong tài liệu Photoshop.

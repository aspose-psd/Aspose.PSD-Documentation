---
title: Lớp Điều chỉnh Độ sáng Tương phản Sáng
type: docs
weight: 30
url: /vi/java/layer-types/adjustment-layer/brightness-contrast/
---

# Làm việc với lớp điều chỉnh Độ sáng/Tương phản trong Photoshop bằng Java

Trong bài viết này, chúng ta sẽ áp dụng điều chỉnh Độ sáng/Tương phản vào tài liệu Adobe® Photoshop® bằng thư viện Aspose.PSD cho Java®. Ngoài ra, chúng ta sẽ tìm hiểu thêm về các tính năng của thư viện liên quan đến loại điều chỉnh này trong quá trình tiếp theo.

Nhưng trước hết là một chút lý thuyết.

Lớp điều chỉnh Độ sáng/Tương phản thay đổi độ sáng và độ tương phản của hình ảnh. Nhưng chờ đã, điều này có nghĩa là gì? Tăng độ sáng làm sáng màu lên đến trắng và giảm độ sáng làm tối màu xuống đen. Tăng độ tương phản sẽ tăng sự khác biệt giữa các màu sáng và màu tối và giảm độ tương phản sẽ giảm sự khác biệt đó; điều này có nghĩa là màu sáng trở nên sáng hơn và màu tối trở nên tối hơn.

## Hỗ trợ chế độ màu

Thư viện cho phép thêm lớp điều chỉnh Độ sáng/Tương phản vào hình ảnh trong chế độ màu RGB, CMYK hoặc Lab.

## Hành vi hiện tại và cổ điển

Bản triển khai thư viện hiện tại (v20.6 khi viết bài) sử dụng thuật toán mặc định của Photoshop để bảo tồn toàn bộ dải tonal từ bóng đến điểm sáng, nhưng vẫn chưa hỗ trợ hành vi cổ điển. Điều này có nghĩa là thư viện hỗ trợ lớp điều chỉnh Độ sáng/Tương phản trong các tài liệu được tạo ra trong các phiên bản mới nhất của Photoshop (CS4 trở lên). Tuy nhiên, nếu cần, bạn có thể [yêu cầu triển khai cổ điển của lớp điều chỉnh Độ sáng/Tương phản](https://forum.aspose.com/c/psd) trên diễn đàn của chúng tôi.

## Điều chỉnh độ sáng và tương phản

Bây giờ chúng ta hãy mô tả cách làm việc của API cấp cao của lớp điều chỉnh Độ sáng/Tương phản (trước bước, API này rất đơn giản). Lớp PsdImage chứa một phương thức factory (addBrightnessContrastAdjustmentLayer) để khởi tạo lớp BrightnessContrastLayer là cổng vào điều chỉnh độ sáng và tương phản. Lớp BrightnessContrastLayer chỉ chứa một cặp getters và setters để truy cập các thuộc tính độ sáng và tương phản cũng như thay đổi giá trị của chúng.

![|Ví dụ Lớp Điều chỉnh Độ sáng/Tương phản trong PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

Vậy, hãy lấy một hình ảnh của một con chó (b), ví dụ, để điều chỉnh độ sáng1 và tương phản2 của nó (a), chỉ bằng cách sử dụng phương thức factory với các đối số tương ứng, để cuối cùng có được một hình ảnh (c) trông rõ ràng hơn:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Lưu ý:

1. Giá trị của độ sáng phải nằm trong khoảng từ -150 đến 150.
2. Giá trị của tương phản phải nằm trong khoảng từ -50 đến 100.

Tham khảo tài liệu của [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) để biết thêm chi tiết.

## Kết luận

Trong bài viết này, chúng ta đã có một cái nhìn nhanh chóng về lớp điều chỉnh Độ sáng/Tương phản và học cách điều chỉnh độ sáng và tương phản của hình ảnh bằng phương thức factory.

Tham khảo series bài viết về [API lớp điều chỉnh](/vi/java/layer-types/adjustment-layer/) của Aspose.PSD cho Java để biết thêm chi tiết.

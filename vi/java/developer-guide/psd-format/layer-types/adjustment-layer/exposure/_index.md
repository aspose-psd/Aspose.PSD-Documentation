---
title: Lớp Điều chỉnh Phơi sáng
type: tài liệu
weight: 30
url: /vi/java/layer-types/adjustment-layer/exposure/
---

# Làm việc với lớp điều chỉnh Phơi sáng trong Photoshop bằng Java

Trong bài viết này, chúng tôi sẽ thêm lớp điều chỉnh Phơi sáng vào tài liệu Adobe® Photoshop® bằng thư viện Aspose.PSD cho Java - thư viện thao tác định dạng tệp PSD. Thư viện hoạt động mà không cần cài đặt trình chỉnh sửa Photoshop vì nó sử dụng các thuật toán xử lý ảnh riêng. Chúng ta cũng đã tìm hiểu một số chi tiết liên quan đến API điều chỉnh phơi sáng của thư viện.

## Tổng quan API

Lớp điều chỉnh Phơi sáng được cấu hình thông qua lớp [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) chứa các thuộc tính sau để làm việc với điều chỉnh phơi sáng:

- Định nghĩa mức độ ánh sáng của ảnh bằng cách nén hoặc mở rộng toàn bộ biểu đồ tương phản so với màu đen. Do đó, điều này ảnh hưởng chủ yếu đến những điểm sáng.
- Ngược lại, độ lệch phơi sáng ảnh hưởng chủ yếu đến bóng.
- Sửa chữa gamma. Nó điều chỉnh sáng tạo hình ảnh.

## Điều chỉnh phơi sáng đúng

Việc sửa lỗi phơi sáng và các thuộc tính liên quan rất đơn giản như việc thay đổi một số thuộc tính của lớp. Hãy áp dụng một số điều chỉnh phơi sáng (a) cho một bức ảnh thiếu ánh sáng trong thư viện (b) để làm cho nó dễ nhìn với mắt người (c).

![Ví dụ lớp Điều chỉnh Phơi sáng](exposure-adjustment-layer-figure-1.png)

Toàn bộ điều chỉnh chủ yếu được thực hiện bằng cách sửa lỗi gamma. Tuy nhiên, phơi sáng và giá trị lệch cũng được điều chỉnh một chút. Tất cả những gì bạn cần làm là thiết lập các giá trị phù hợp cho các thuộc tính đã nói:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Chú ý rằng phơi sáng phải nằm trong khoảng từ -20.0 đến 20.0, giá trị lệch phải nằm trong khoảng từ -0.5 đến 0.5 và dải giá trị của sửa lỗi gamma phải nằm giữa 9.99 và 0.01.

Tham khảo [tài liệu API của lớp điều chỉnh phơi sáng](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) để biết thêm chi tiết.

## Kết luận

Trong bài viết này, chúng ta đã tìm hiểu cách thêm Lớp Điều chỉnh Phơi sáng vào tệp PSD để làm sáng ảnh cũng như xem xét một số chi tiết API.

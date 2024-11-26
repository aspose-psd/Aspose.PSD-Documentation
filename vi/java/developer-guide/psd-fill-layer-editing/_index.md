---
title: Cập Nhật Lớp Fill Layer trong PSD bằng Java
weight: 100
type: docs
description: Các ví dụ về việc sử dụng tất cả các loại lớp điều chỉnh bao gồm Color Fill, Gradient Fill và Pattern Fill
keywords: [lớp fill, Color Fill, Gradient Fill, Pattern Fill, psd api, java, mẫu code]
url: vi/java/psd-fill-layer-editing/
---

## **Tổng Quan**

Để tạo một lớp thông thường, bạn cần sử dụng hàm createRegularLayer, yêu cầu các tham số định nghĩa vị trí và kích thước của lớp. Hàm này tạo một lớp mới, đặt khung của nó và điền nó với một màu cụ thể.

Đối với lớp fill màu, bạn sử dụng phương thức FillLayer.createInstance với tham số FillType.Color. Khi lớp fill được tạo, truy cập cài đặt fill của nó thông qua thuộc tính fill_settings và đặt màu mong muốn bằng thuộc tính color của lớp ColorFillSettings. Ở đây, màu được đặt thành Color.getCoral(). Ngoài ra, thuộc tính clipping của lớp fill cũng được đặt thành 1, khiến cho nó hoạt động như một lớp cắt.

Các lớp fill gradient được tạo tương tự bằng cách sử dụng phương thức FillLayer.create_instance, nhưng với tham số FillType.Gradient. Giống như các lớp fill màu, bạn truy cập cài đặt fill qua fill_settings và đặt các điểm màu gradient và điểm độ trong suốt. Trong ví dụ này, các điểm màu gradient được xác định bằng lớp GradientColorPoint, và các điểm độ trong suốt bằng lớp GradientTransparencyPoint. Thuộc tính clipping của lớp fill cũng được đặt thành 1.

Các lớp fill họa tiết được tạo bằng FillLayer.createInstance với tham số FillType.Pattern. Một lần nữa, truy cập cài đặt fill thông qua fill_settings và đặt dữ liệu họa tiết và các thuộc tính khác. Trong đoạn mã này, dữ liệu họa tiết được xác định bằng lớp PatternFillSettings, và thuộc tính clipping được đặt thành 1.

Khi các lớp fill đã được tạo, thêm chúng vào hình ảnh PSD bằng cách sử dụng phương thức addLayer, chỉ định tên hiển thị và các thuộc tính khác cho mỗi lớp fill.

Cuối cùng, lưu hình ảnh PSD và hình ảnh PNG tương ứng với đoạn mã được cung cấp. Các tùy chọn PNG được cấu hình để sử dụng màu thật với alpha cho tính trong suốt.

Vui lòng tham khảo ví dụ đầy đủ để biết thêm chi tiết.

## **Ví Dụ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}

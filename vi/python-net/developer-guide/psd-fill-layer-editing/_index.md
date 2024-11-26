---
title: Cập nhật lớp Fill Layer PSD bằng Python
weight: 100
type: docs
description: Các ví dụ về việc sử dụng tất cả các loại lớp điều chỉnh bao gồm Color Fill, Gradient Fill và Pattern Fill
keywords: [fill layer, Color Fill, Gradient Fill, Pattern Fill, psd api, python, code sample]
url: vi/python-net/psd-fill-layer-editing/
---

## **Tổng quan**

Để tạo một lớp thông thường, bạn có thể sử dụng hàm create_regular_layer được cung cấp trong mã. Hàm này lấy các tham số left, top, width và height để xác định vị trí và kích thước của lớp. Nó tạo ra một lớp mới, đặt ranh giới của nó và điền nó với một màu cụ thể.

Để tạo một lớp fill màu, bạn có thể sử dụng phương thức FillLayer.create_instance với tham số FillType.COLOR. Sau khi tạo lớp fill, bạn có thể truy cập các cài đặt fill của nó bằng cách sử dụng thuộc tính fill_settings và đặt màu bằng cách sử dụng thuộc tính màu của lớp ColorFillSettings. Trong mã được cung cấp, màu được đặt thành Màu coral. Thuộc tính clipping của lớp fill được đặt thành 1, làm cho lớp hoạt động như mặt nạ cắt.

Để tạo một lớp fill gradient, bạn có thể sử dụng phương thức FillLayer.create_instance với tham số FillType.GRADIENT. Tương tự như lớp fill màu, bạn có thể truy cập các cài đặt fill bằng cách sử dụng thuộc tính fill_settings và đặt các điểm màu gradient và các điểm độ trong suốt. Trong mã được cung cấp, các điểm màu gradient được xác định bằng lớp GradientColorPoint và các điểm độ trong suốt được xác định bằng lớp GradientTransparencyPoint. Thuộc tính clipping của lớp fill cũng được đặt thành 1.

Để tạo một lớp fill pattern, bạn có thể sử dụng phương thức FillLayer.create_instance với tham số FillType.PATTERN. Một lần nữa, bạn có thể truy cập các cài đặt fill bằng cách sử dụng thuộc tính fill_settings và đặt dữ liệu mẫu và các thuộc tính khác. Trong mã được cung cấp, dữ liệu mẫu được xác định bằng lớp PatternFillSettings, và thuộc tính clipping được đặt thành 1.

Sau khi tạo các lớp fill, bạn có thể thêm chúng vào hình ảnh PSD bằng cách sử dụng phương thức add_layer. Bạn cũng có thể chỉ định tên hiển thị và các thuộc tính khác cho mỗi lớp fill.

Cuối cùng, bạn có thể lưu hình ảnh PSD và hình ảnh PNG tương ứng bằng cách sử dụng mã được cung cấp. Các tùy chọn PNG được đặt để sử dụng truecolor với alpha cho tính trong suốt.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-fill-layer-editing.py" >}}

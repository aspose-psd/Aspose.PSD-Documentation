---
title: Sử dụng Graphics API để chỉnh sửa Layers trong tệp PSD
weight: 100
type: docs
description: Ví dụ về việc sử dụng Graphics API trong Aspose.PSD cho Java
keywords: [cập nhật layer, vẽ hình tròn, vẽ elip, vẽ hình tròn đổ màu, đồ họa, psd api, java, mẫu mã code]
url: vi/java/graphics-api/
---

## **Tổng quan**
Để bắt đầu, tải tệp PSD bằng cách sử dụng phương thức Image.load() hoặc tạo một Psd Image từ đầu. Sử dụng biến inputFile để đại diện cho đường dẫn đến tệp PSD của bạn và xác định bất kỳ tùy chọn tải nào bằng loadOpt, nếu cần.

Tiếp theo, truy cập lớp đầu tiên của hình ảnh PSD bằng cú pháp psdImage.getLayers()[0] để nhận một tham chiếu đến đối tượng lớp để thao tác.

Để chỉnh sửa lớp, tạo một đối tượng Graphics bằng cách truyền lớp làm tham số. Đối tượng này cung cấp các phương thức khác nhau để vẽ các hình dạng và áp dụng cọ.

Đối tượng Pen được sử dụng để xác định màu sắc và độ dày của viền của các hình dạng. Tương tự, cọ như LinearGradientBrush được sử dụng để xác định màu sắc đổ.

Vẽ các hình dạng trên lớp bằng cách sử dụng các phương thức như graphics.drawEllipse() để đánh dấu các hình dạng và graphics.fillEllipse() để điền chúng.

Sau khi thay đổi mong muốn lên lớp, lưu hình ảnh PSD đã chỉnh sửa bằng cách sử dụng psdImage.save().

Ngoài ra, bạn có thể lưu hình ảnh đã chỉnh sửa dưới dạng định dạng khác như PNG bằng cách sử dụng các tùy chọn phù hợp.

Đó là tất cả! Bạn đã thành công sử dụng Graphics API của Aspose.PSD cho Java để chỉnh sửa layers trong tệp PSD. Khám phá thêm các tính năng và chức năng của thư viện Aspose.PSD để cải thiện khả năng chỉnh sửa hình ảnh của bạn.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}

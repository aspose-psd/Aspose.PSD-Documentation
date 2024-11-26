---
title: Ví dụ về việc sử dụng group layers trong Aspose.PSD cho Java
weight: 100
type: docs
description: Sử dụng Group Layer của tệp PSD thông qua Java
keywords: [layer group, group layer, add layer to group, psd api, java, code sample]
url: vi/java/psd-group-layer/
---

## **Tổng quan**

Sử dụng group layers trong Aspose.PSD cho Java nâng cao khả năng quản lý và tổ chức các lớp trong hình ảnh PSD một cách hiệu quả. Group layers, còn được gọi là folder layers, cho phép bạn kết hợp nhiều layers và áp dụng biến đổi hoặc hiệu ứng một cách tổng thể.

Để bắt đầu, tạo một hình ảnh PSD mới bằng cách sử dụng phương thức PsdImage.create(). Tiếp đó, khởi tạo một đối tượng LayerGroup mới thông qua phương thức addLayerGroup của đối tượng PsdImage. Cung cấp tên mong muốn cho group layer ("Folder"), chỉ định chỉ mục chèn (0), và đặt một cờ boolean để chỉ ra sự hiển thị của nó (Đúng).

Tiếp theo, tạo hai đối tượng Layer và đặt tên hiển thị của chúng bằng cách sử dụng phương thức setDisplayName. Thêm các layer này vào group layer bằng cách sử dụng phương thức addLayer.

Để truy cập các layers trong group, sử dụng thuộc tính layers của đối tượng LayerGroup. Xác nhận rằng tên hiển thị của lớp đầu tiên và thứ hai trong group lần lượt là "Layer 1" và "Layer 2".

Sau khi bạn đã thao tác với group layers, lưu hình ảnh PSD được chỉnh sửa bằng cách sử dụng phương thức save của đối tượng PsdImage.

Đây là một ví dụ cơ bản để giúp bạn làm quen với việc làm việc với group layers bằng cách sử dụng Aspose.PSD cho Java. Thư viện cung cấp rất nhiều tính năng tiên tiến cho việc manipulate và transform layers trong hình ảnh PSD. Để biết thêm chi tiết và ví dụ về việc tận dụng group layers và các chức năng khác của thư viện, hãy tham khảo tài liệu Aspose.PSD cho Java.

Để làm việc với group layers trong Aspose.PSD cho Java, sử dụng lớp LayerGroup. Dưới đây là một đoạn mã minh họa cách tạo một group layer, thêm layers và lưu hình ảnh PSD chỉnh sửa.

Hãy tham khảo ví dụ đầy đủ được cung cấp.

## **Ví dụ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}

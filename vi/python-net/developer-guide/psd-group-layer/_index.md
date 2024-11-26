---
title: Ví dụ về việc sử dụng các nhóm lớp trong Aspose.PSD cho Python
weight: 100
type: docs
description: Sử dụng Group Layer của tập tin PSD thông qua Python
keywords: [layer group, group layer, add layer to group, psd api, python, code sample]
url: vi/python-net/psd-group-layer/
---

## **Tổng quan**

Làm việc với các nhóm lớp trong Aspose.PSD cho Python là một tính năng mạnh mẽ cho phép bạn tổ chức và thao tác các lớp trong một hình ảnh PSD. Các nhóm lớp, cũng được gọi là lớp thư mục, cung cấp một cách để nhóm nhiều lớp với nhau và áp dụng biến đổi hoặc hiệu ứng cho toàn bộ nhóm.

Trong ví dụ này, chúng ta trước tiên tạo một hình ảnh PSD mới bằng cách sử dụng phương thức PsdImage.create. Sau đó, chúng ta tạo một đối tượng LayerGroup mới bằng cách sử dụng phương thức add_layer_group của đối tượng PsdImage. Chúng ta cung cấp tên của nhóm lớp ("Folder"), chỉ mục mà nó sẽ được chèn vào (0), và một cờ boolean cho biết liệu nhóm lớp có nên hiển thị hay không (True).

Tiếp theo, chúng ta tạo hai đối tượng Layer và đặt tên hiển thị của họ bằng cách sử dụng thuộc tính display_name. Chúng ta thêm các lớp này vào nhóm lớp bằng cách sử dụng phương thức add_layer.

Cuối cùng, chúng ta có thể truy cập các lớp trong nhóm bằng cách sử dụng thuộc tính layers của đối tượng LayerGroup. Trong ví dụ, chúng ta khẳng định rằng tên hiển thị của các lớp đầu tiên và thứ hai trong nhóm lần lượt là "Layer 1" và "Layer 2".

Sau khi thao tác với các nhóm lớp, chúng ta có thể lưu hình ảnh PSD đã sửa đổi bằng cách sử dụng phương thức save của đối tượng PsdImage.

Đây chỉ là một ví dụ cơ bản để giúp bạn bắt đầu với việc làm việc với các nhóm lớp bằng cách sử dụng Aspose.PSD cho Python. Thư viện cung cấp nhiều tính năng tiên tiến khác để thao tác và biến đổi lớp trong hình ảnh PSD. Bạn có thể tham khảo tài liệu Aspose.PSD cho Python để biết thêm chi tiết và ví dụ về làm việc với các nhóm lớp và các tính năng khác của thư viện.

Để làm việc với các nhóm lớp trong Aspose.PSD cho Python, bạn có thể sử dụng lớp LayerGroup. Dưới đây là một đoạn mã ví dụ mô tả cách tạo một nhóm lớp, thêm lớp vào đó, và lưu hình ảnh PSD đã sửa đổi.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}

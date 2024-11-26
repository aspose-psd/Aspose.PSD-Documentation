---
title: Sử dụng nhóm lớp trong Aspose.PSD cho C#
weight: 100
type: docs
description: Sử dụng Nhóm Lớp của Tập Tin PSD thông qua C#
keywords: [nhóm lớp, nhóm lớp, thêm lớp vào nhóm, giao diện lập trình ứng dụng PSD, C#, mã nguồn mẫu]
url: vi/net/psd-group-layer/
---

## Tổng quan

Nhóm lớp trong Aspose.PSD cho C# cho phép tổ chức và thao tác hiệu quả các lớp trong một tập tin PSD. Bằng cách sử dụng các lớp thư mục, bạn có thể nhóm nhiều lớp cùng nhau và áp dụng các biến đổi hoặc hiệu ứng cho toàn bộ nhóm.

Ví dụ này giới thiệu việc tạo hình ảnh PSD mới với `PsdImage.Create`. Sau đó, một đối tượng `LayerGroup` mới được tạo bằng cách sử dụng `AddLayerGroup` từ đối tượng `PsdImage`. Lớp nhóm được đặt tên là "Thư mục", chèn vào chỉ mục 0 và đặt là hiển thị.

Tiếp theo, hai đối tượng `Layer` được tạo với các thuộc tính `DisplayName` của họ được đặt. Những lớp này được thêm vào lớp nhóm bằng cách sử dụng `AddLayer`.

Các lớp bên trong nhóm có thể được truy cập thông qua thuộc tính `Layers` của đối tượng `LayerGroup`. Ví dụ khẳng định rằng tên hiển thị của lớp thứ nhất và thứ hai trong nhóm là "Lớp 1" và "Lớp 2".

Sau khi sửa đổi các lớp nhóm, hình ảnh PSD được cập nhật được lưu bằng phương thức `Save` của đối tượng `PsdImage`.

Ví dụ cơ bản này giới thiệu cách làm việc với nhóm lớp bằng Aspose.PSD cho C#. Thư viện này cung cấp các tính năng tiên tiến để thao tác và biến đổi các lớp trong các tập tin PSD. Tham khảo tài liệu Aspose.PSD cho C# để biết thêm ví dụ chi tiết và tính năng.

Dưới đây là một đoạn mã mẫu thể hiện việc sử dụng nhóm lớp trong Aspose.PSD cho C#:

## Ví dụ

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Để biết thông tin và ví dụ chi tiết hơn, vui lòng truy cập [Tài liệu Aspose.PSD cho C#](https://docs.aspose.com/psd/net/).


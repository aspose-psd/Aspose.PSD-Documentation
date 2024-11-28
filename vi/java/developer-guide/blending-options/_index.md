---
title: Psd Thao tác các tùy chọn trộn
weight: 100
type: docs
description: Aspose.PSD cho Java có thể hỗ trợ bạn trong việc điều chỉnh các tùy chọn trộn với một đoạn mã nguồn đơn giản.
keywords: [tùy chọn trộn, trộn, thêm hiệu ứng, thay đổi độ mờ, thay đổi màu của bóng, thêm bóng, psd api, java, mẫu mã nguồn]
url: vi/java/blending-options/
---

## **Tổng quan**
Với Aspose.PSD cho Java, bạn có khả năng thay đổi các tùy chọn trộn để cải thiện hình ảnh PSD của bạn. Dưới đây là một ví dụ mã nguồn Java mô tả các phương pháp khác nhau để sử dụng các tùy chọn trộn.

Ban đầu, mã nguồn tải một hình ảnh PSD và lưu nó dưới dạng tập tin PNG gốc. Tiếp theo, nó thay đổi độ mờ và chế độ trộn của các lớp cụ thể. Ví dụ, nó đặt độ mờ của lớp thứ hai là 100 và thay đổi chế độ trộn của lớp thứ năm thành Hue.

Hơn nữa, mã nguồn kết hợp các hiệu ứng trộn vào các lớp chỉ định. Sử dụng phương thức `addDropShadow()`, nó giới thiệu một hiệu ứng bóng đổ cho lớp thứ bảy, xác định một góc bóng đổ là 30 độ và một màu bóng đổ là RGB(255, 0, 0).

Bên cạnh đó, mã nguồn điều chỉnh chế độ trộn của lớp thứ chín thành Lighten. Thêm vào đó, nó áp dụng một hiệu ứng màu nền cho lớp thứ năm thông qua phương thức `addColorOverlay()`, thiết lập màu nền là RGB(30, 50, 0) với độ mờ là 150.

Cuối cùng, mã nguồn lưu hình ảnh đã chỉnh sửa dưới dạng tập tin PNG cập nhật.

Nói một cách đơn giản, Aspose.PSD cho Java cung cấp một loạt các tùy chọn trộn đa dạng để thao tác vẻ bên ngoài của các lớp trong hình ảnh PSD của bạn. Các tùy chọn này bao gồm việc thay đổi độ mờ, chế độ trộn và thực hiện các hiệu ứng trộn khác nhau như bóng đổ và màu nền.

## **Ví dụ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-blending-options.java" >}}

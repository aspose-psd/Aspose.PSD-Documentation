---
title: Cách Sử Dụng Warp trong Aspose.PSD
type: docs
weight: 40
url: /vi/net/cach-su-dung-warp-trong-aspose-psd/
---

## **Phần 1 – Hiển Thị Một Tập Tin PSD với Hiệu Ứng Warp**

Photoshop lưu hình ảnh được hiển thị sau khi áp dụng hiệu ứng Warp. Thư viện của chúng tôi có thể tái tạo hoặc hiển thị lại hình ảnh với hiệu ứng Warp. Để kích hoạt tính năng này, đơn giản chỉ cần thiết lập cờ AllowWarpRepaint trong cài đặt khi mở tập tin PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Tài liệu-Aspose-PSD-Warp-Rendering-1.cs" >}}

Kết quả:
![Aspose.PSD cho .NET Warp Kết Quả 1](warp1.png)

Ngoài việc hiển thị hiệu ứng Warp cho SmartLayers, thư viện của chúng tôi cũng hỗ trợ Warp cho TextLayers. Mã triển khai vẫn giữ nguyên không đổi, với sự khác biệt duy nhất là tên tập tin.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Tài liệu-Aspose-PSD-Warp-Rendering-2.cs" >}}

Kết quả:
![Aspose.PSD cho .NET Warp Kết Quả 2](warp2.png)

**! Lưu ý: ** Hiện tại, thư viện của chúng tôi hỗ trợ hiển thị cả hai loại Warp Tùy chỉnh (nơi người dùng điều chỉnh điểm lưới) và tất cả các loại Warp chuẩn.
* - Hiện tại, thư viện của chúng tôi hỗ trợ Warp Tùy chỉnh với lưới chuẩn, và chúng tôi đang tích cực làm việc để mở rộng hỗ trợ của mình để bao gồm tất cả các loại lưới trong tương lai gần.

## **Phần 2 – Sửa Đổi Hiệu Ứng Warp**

Thư viện của chúng tôi cho phép bạn không chỉ hiển thị mà còn sửa đổi (thêm) hiệu ứng Warp.
Những sửa đổi này được thực hiện thông qua các tính năng của lớp **WarpParams**.

| **Tính Năng** | **Mô Tả** |
|:-------------|:---------|
| Bounds       | Trả về ranh giới của hình ảnh đã bị uốn. |
| MeshPoints   | Một mảng điểm, với mỗi điểm đại diện cho một đỉnh của lưới uốn. |
| Value        | Giá trị của hiệu ứng warp cho các hiệu ứng warp không phải là Tùy chỉnh. |
| WarpRotates  | Một biến loại xác định hướng của các hiệu ứng warp không phải là Tùy chỉnh. |
| WarpStyles   | Một biến loại xác định loại hiệu ứng warp. |

Ví dụ mã dưới đây minh họa cách xác định loại hiệu ứng Warp cho một lớp thông minh và điều chỉnh loại và cường độ của méo mó cho hiệu ứng.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Tài liệu-Aspose-PSD-Warp-Rendering-3.cs" >}}

Kết quả:
![Aspose.PSD cho .NET Warp Kết Quả 3](warp3.png)

## **Phần 3 – Thêm Hiệu Ứng Warp**

Ví dụ mã dưới đây minh họa cách thêm một hiệu ứng Warp chuẩn vào một lớp thông minh.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Tài liệu-Aspose-PSD-Warp-Rendering-4.cs" >}}

Kết quả:
![Aspose.PSD cho .NET Warp Kết Quả 4](warp4.png)

Ví dụ mã dưới đây minh họa cách thêm một hiệu ứng Warp Tùy chỉnh vào một lớp thông minh.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Tài liệu-Aspose-PSD-Warp-Rendering-5.cs" >}}

Kết quả:
![Aspose.PSD cho .NET Warp Kết Quả 5](warp5.png)

Ví dụ mã dưới đây minh họa cách thêm một hiệu ứng Warp vào một lớp văn bản.
**! Lưu ý:** Theo tiêu chuẩn của Photoshop, hiệu ứng Warp cho các lớp văn bản thường giới hạn vào loại chuẩn. Tuy nhiên, thư viện của chúng tôi hỗ trợ việc sử dụng hai loại hiệu ứng Warp. Vui lòng lưu ý rằng các tập tin như vậy có thể không hoàn toàn tương thích với Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Tài liệu-Aspose-PSD-Warp-Rendering-5.cs" >}}

Kết quả:
![Aspose.PSD cho .NET Warp Kết Quả 6](warp6.png)

Chúng tôi liên tục hoàn thiện và mở rộng khả năng của hiệu ứng Warp của chúng tôi, tập trung vào việc cải thiện tốc độ, chất lượng và chức năng được hỗ trợ. Hãy cập nhật với các bản phát hành hàng tháng của chúng tôi để nhận thông tin về các phát triển mới nhất.
Nhóm của bạn Aspose.PSD

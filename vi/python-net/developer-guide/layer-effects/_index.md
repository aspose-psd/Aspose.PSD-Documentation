---
title: Sử dụng Hiệu Ứng Layer trong tệp PSD
weight: 100
type: docs
description: Ví dụ về việc sử dụng Hiệu Ứng Layer trong Aspose.PSD cho Python
keywords: [bóng đổ, phủ màu, ánh sáng nội, ánh sáng ngoại, psd api, python, mẫu mã code]
url: vi/python-net/layer-effects/
---

## **Tổng Quan**
Trong Aspose.PSD cho Python, bạn có thể tạo ra các hiệu ứng khác nhau trên các lớp để tăng cường vẻ bề ngoại hình ảnh của bạn. Điều này có thể được thực hiện bằng cách sử dụng lớp BlendingOptions, cung cấp các phương thức để thêm các loại hiệu ứng khác nhau như viền, bóng nội, bóng đổ, phủ màu, phủ mẫu, và ánh sáng ngoại.

Để minh họa việc tạo ra hiệu ứng trên các lớp, hãy xem xét đoạn mã ví dụ sau

Trong đoạn mã này, chúng tôi đầu tiên tải một hình ảnh PSD và lưu hình ảnh gốc dưới dạng PNG. Sau đó, chúng tôi tạo ra các hiệu ứng khác nhau trên các lớp khác nhau bằng cách sử dụng lớp BlendingOptions. Dưới đây là một giải thích ngắn gọn về mỗi hiệu ứng:

- Stroke: Chúng tôi thêm một viền gradient vào lớp 1, chỉ định kích thước viền, các điểm màu gradient và điểm độ mờ trong suốt.
- Inner Shadow: Chúng tôi thêm một bóng nội vào lớp 2, chỉ định góc và màu của bóng.
- Drop Shadow: Chúng tôi thêm một bóng đổ vào lớp 3, chỉ định góc và màu của bóng.
- Gradient Overlay: Chúng tôi thêm một gradient phủ lên lớp 4, chỉ định các điểm màu gradient và điểm độ mờ trong suốt.
- Color Overlay: Chúng tôi thêm một phủ màu vào lớp 5, chỉ định màu và độ mờ của phủ màu.
- Pattern Overlay: Chúng tôi thêm một phủ mẫu vào lớp 6, chỉ định dữ liệu mẫu, chiều rộng và chiều cao.
- Outer Glow: Chúng tôi thêm một ánh sáng ngoại vào lớp 7, chỉ định kích thước và màu đổ của ánh sáng.

Cuối cùng, chúng tôi lưu hình ảnh đã chỉnh sửa dưới dạng cả PNG và PSD.

Đây chỉ là một ví dụ cơ bản về cách bạn có thể tạo ra hiệu ứng trên các lớp sử dụng Aspose.PSD cho Python. Bạn có thể tinh chỉnh các hiệu ứng thêm bằng cách điều chỉnh các tham số và thuộc tính của từng hiệu ứng. Thư viện cung cấp các tùy chọn và cài đặt khác nhau để tạo ra các hiệu ứng phức tạp và hấp dẫn về mặt thị giác.

Hy vọng bài viết này giúp bạn hiểu cách tạo ra hiệu ứng trên các lớp trong Aspose.PSD cho Python. Hãy khám phá tài liệu thư viện để biết thêm chi tiết và ví dụ.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-layer-effects.py" >}}

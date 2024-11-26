---
title: Vấn Đề Đã Biết
type: docs
weight: 40
url: /vi/net/known-issues/
---

## **.NET Compact Framework**
- Đã quan sát thấy rằng trên một số phiên bản cụ thể của Windows như Windows Mobile 5.0-6.0, các tập hợp framework compact đã được ký bằng chứng chỉ (hoặc chứng chỉ được ký kép) không hoạt động như mong đợi và không thể tải đúng cách (sẽ ném ra một TypeLoadException). Để vượt qua vấn đề này, người dùng cần xóa bất kỳ chứng chỉ nào và sau đó sử dụng tập hợp đã được cập nhật. Xin lưu ý rằng bạn tự chịu rủi ro khi thực hiện điều này và chúng tôi không đảm bảo tính hợp lệ do sự thay đổi tập hợp như vậy. Cũng không chúng tôi cung cấp các tập hợp không có chữ ký vì đây là một mối đe dọa an ninh tiềm ẩn. Thay vào đó, khách hàng nên tránh sử dụng các hệ điều hành cũ như vậy, nếu có thể, và/hoặc nâng cấp hệ điều hành lên các phiên bản hoặc bản vá dịch vụ mới hơn giải quyết vấn đề ký chứng chỉ.

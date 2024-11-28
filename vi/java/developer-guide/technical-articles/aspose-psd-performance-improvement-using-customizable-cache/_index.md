---
title: Tối Ưu Hiệu Suất Aspose.PSD bằng Bộ Nhớ Cache Có Thể Tùy Biến
type: tài Liệu
weight: 30
url: /vi/java/tối-ưu-hiệu-sự-aspose-psd-bằng-bộ-nhớ-cache-có-thể-tùy-biến/
---

## **Nâng Cao Hiệu Suất với Bộ Nhớ Cache Có Thể Tùy Biến**
Aspose.PSD sử dụng bộ nhớ cache để lưu trữ dữ liệu tạm thời. Cơ chế này đơn giản để sử dụng, có thể tùy chỉnh và minh bạch. Nó đảm bảo không có vấn đề về hiệu suất trong quá trình xử lý hình ảnh. Bài viết này giải thích cách tùy chỉnh bộ nhớ cache với Aspose.PSD API cho Java.
### **Tùy Biến Bộ Nhớ Cache**
Khi một quá trình cần bộ nhớ lưu trữ dữ liệu tạm thời, bộ nhớ se được phân bổ trong cache. Cache có thể là không gian trong bộ nhớ hoặc trên ổ đĩa và được thiết lập bởi người dùng. Khi dữ liệu tạm thời không cần nữa, không gian sẽ được giải phóng. Thống kê về không gian đã được phân bổ có thể được kiểm tra bất kỳ lúc nào. Cách mà Aspose.PSD phân bổ và sử dụng caches có thể được tùy biến. Phần này mô tả các thiết lập khác nhau và các giá trị mặc định của chúng, và các đoạn mã dưới đây cho thấy cách chúng có thể được sử dụng.
### **Thiết Lập Nơi Phân Bổ Cache**
Để tùy chỉnh cách phân bổ không gian cache, hãy thiết lập thuộc tính CacheType. Mặc định, cache được phân bổ trong bộ nhớ và khi không còn không gian nữa trong bộ nhớ, nó được phân bổ sang ổ đĩa. Hành vi này được thu thập bởi chế độ Tự động. Chế độ Tự động là linh hoạt và tối ưu hiệu suất. Cũng có các chế độ khác:

- Chế độ CacheOnDiskOnly: phân bổ chỉ sang ổ đĩa.
- Chế độ CacheInMemoryOnly: phân bổ chỉ trong bộ nhớ.

Chọn chế độ CacheOnDiskOnly có thể dẫn đến hiệu suất kém.
### **Thiết Lập Kích Thước Của Bộ Nhớ Cache**
Đặt không gian tối đa (theo byte) mà có thể được phân bổ trên ổ đĩa hoặc trong bộ nhớ bằng cách thiết lập các thuộc tính MaxDiskSpaceForCache và MaxMemoryForCache tương ứng. Theo mặc định, cả hai giá trị đều được thiết lập là 0, có nghĩa không có giới hạn trên trên.
### **Điều Khiển Phân Bổ Lại Của Cache**
Nếu không có đủ không gian trong bộ nhớ (như được chỉ định bởi thuộc tính MaxMemoryForCache) khi một cache mới được phân bổ, cache được phân bổ sang ổ đĩa. Nếu không có đủ không gian trên ổ đĩa, một ngoại lệ được ném. Quá trình phân bổ cache di chuyển từ bộ nhớ sang ổ đĩa nhưng không ngược lại. Thuộc tính ExactReallocateOnly được sử dụng để kiểm soát phân bổ lại bộ nhớ. Phân bổ lại rất có thể xảy ra cho các cache đã được phân bổ trước. Nó có thể xảy ra khi hệ thống nhận ra rằng không gian đã được phân bổ sẽ không đủ. Nếu ExactReallocateOnly được thiết lập với giá trị mặc định là False, không gian sẽ được phân bổ lại sang cùng một phương tiện. Khi thiết lập là True, phân bổ lại không thể vượt quá không gian đã chỉ định tối đa. Trong trường hợp này, cache đã được phân bổ trong bộ nhớ (cần phân bổ lại) được giải phóng và không gian mở rộng được phân bổ trên ổ đĩa.
### **Mẫu Chương Trình**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}

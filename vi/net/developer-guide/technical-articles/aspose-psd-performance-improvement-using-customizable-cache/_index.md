---
title: Tối Ưu Hiệu Suất Aspose.PSD bằng Cache Có Thể Tùy Chỉnh
type: docs
weight: 20
url: /vi/net/tối-ưu-hiệu-suat-aspose-psd-bang-cache-co-the-tuy-chinh/
---

## **Cải Thiện Hiệu Suất với Cache Có Thể Tùy Chỉnh**
[Aspose.PSD](https://products.aspose.com/psd/family) sử dụng cache để lưu trữ dữ liệu tạm thời. Cơ chế này dễ sử dụng, có thể tùy chỉnh và minh bạch. Nó đảm bảo không có vấn đề hiệu suất nào xảy ra trong quá trình xử lý ảnh. Bài viết này giải thích cách tùy chỉnh cache với API Aspose.PSD cho .NET.
### **Tùy chỉnh Cache**
Khi một quy trình cần lưu trữ dữ liệu tạm thời, không gian này được cấp phát trong cache. Cache có thể là không gian trong bộ nhớ hoặc trên ổ đĩa và được thiết lập bởi người dùng. Khi dữ liệu tạm thời không còn cần thiết, không gian sẽ được giải phóng. Thống kê về không gian được cấp phát có thể được kiểm tra bất kỳ lúc nào. Cách Aspose.PSD cấp phát và sử dụng cache có thể được tùy chỉnh. Phần này mô tả các cài đặt khác nhau và giá trị mặc định của chúng, và các đoạn mã dưới đây thể hiện cách họ có thể được sử dụng.
### **Thiết lập Nơi Cache Được Cấp Phát**
Để tùy chỉnh cách không gian cache được cấp phát, hãy thiết lập thuộc tính [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Theo mặc định, cache được cấp phát trong bộ nhớ và khi không còn không gian nào khả dụng trong bộ nhớ, nó được cấp phát vào ổ đĩa. Hành vi này được ghi lại bởi Chế độ Tự động. Chế độ Tự động linh hoạt và tối ưu hiệu suất. Còn có các chế độ khác:

- Chế độ CacheOnDiskOnly: cấp phát chỉ vào ổ đĩa.
- Chế độ CacheInMemoryOnly: cấp phát chỉ vào bộ nhớ.

Chọn chế độ CacheOnDiskOnly có thể dẫn đến hiệu suất kém.
### **Thiết lập Kích Thước Cache**
Thiết lập không gian tối đa (theo byte) có thể được cấp phát trên ổ đĩa hoặc bộ nhớ bằng cách thiết lập các thuộc tính [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) và [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) tương ứng. Theo mặc định, cả hai giá trị đều được thiết lập là 0, tức là không có giới hạn tối đa.
### **Kiểm Soát Việc Cấp Phát Lại Cache**
Nếu không đủ không gian khả dụng trong bộ nhớ (như được chỉ rõ bởi thuộc tính MaxMemoryForCache) khi một cache mới được cấp phát, cache sẽ được cấp phát vào ổ đĩa. Nếu không đủ không gian trên ổ đĩa, một ngoại lệ sẽ được đưa ra. Quá trình cấp phát cache di chuyển từ bộ nhớ sang ổ đĩa nhưng không ngược lại. Thuộc tính [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) được sử dụng để kiểm soát việc cấp phát lại bộ nhớ. Việc cấp phát lại khả năng xảy ra nhất với các caches được cấp phát trước. Điều này có thể xảy ra khi hệ thống nhận ra rằng không gian đã cấp phát sẽ không đủ. Nếu ExactReallocateOnly được thiết lập với giá trị mặc định, False, không gian sẽ được cấp phát lại vào cùng một phương tiện. Khi thiết lập là True, việc cấp phát lại không thể vượt quá không gian tối đa đã chỉ định. Trong trường hợp này, bộ nhớ cache đã được cấp phát (đòi hỏi cấp phát lại) sẽ được giải phóng và mở rộng không gian sẽ được cấp phát vào ổ đĩa.
### **Mẫu Chương Trình**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}

---
title: Áp dụng Bộ lọc Trung vị và Wiener
type: docs
weight: 10
url: /vi/java/ap-dung-bo-loc-trung-vi-va-wiener/
---

## **Áp dụng Bộ lọc Trung vị và Wiener**
Bộ lọc trung vị là một kỹ thuật lọc kỹ thuật số phi tuyến được sử dụng thường xuyên để loại bỏ nhiễu. Việc giảm nhiễu như vậy thường là bước tiền xử lý điển hình để cải thiện kết quả của việc xử lý sau này. Bộ lọc Wiener là bộ lọc tuyến tính cố định MSE (mean squared error) tối ưu cho các hình ảnh bị biến dạng do nhiễu cộng và làm mờ. Bằng cách sử dụng Aspose.PSD cho API Java, nhà phát triển có thể áp dụng bộ lọc trung vị để giảm nhiễu cho hình ảnh và có thể áp dụng bộ lọc Gauss Wiener cho hình ảnh. Bài viết này demo cách áp dụng bộ lọc trung vị và bộ lọc Gauss Wiener cho hình ảnh.

### **Áp dụng Bộ lọc Trung vị**
Aspose.PSD cung cấp lớp MedianFilterOptions để áp dụng bộ lọc trên một RasterImage. Đoạn mã dưới đây mô tả cách áp dụng bộ lọc trung vị lên một hình ảnh raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}

### **Áp dụng Bộ lọc Gauss Wiener**
Aspose.PSD cung cấp lớp GaussWienerFilterOptions để áp dụng bộ lọc trên một RasterImage. Đoạn mã dưới đây mô tả cách áp dụng bộ lọc Gauss Wiener lên một hình ảnh raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}

### **Áp dụng Bộ lọc Gauss Wiener Cho Hình ảnh màu**
Aspose.PSD cung cấp lớp GaussWienerFilterOptions cho các hình ảnh màu. Đoạn mã dưới đây mô tả cách áp dụng bộ lọc Gauss Wiener lên một hình ảnh màu.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}

### **Áp dụng Bộ lọc Wiener Chuyển động**
Aspose.PSD cung cấp lớp MotionWienerFilterOptions để áp dụng bộ lọc trên một RasterImage. Đoạn mã dưới đây mô tả cách áp dụng bộ lọc Wiener chuyển động lên một hình ảnh raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}

## **Áp dụng Bộ lọc Sửa Chữa Trên Một Hình Ảnh**
Bài viết này demo việc sử dụng Aspose.PSD cho Java để thực hiện bộ lọc sửa chữa trên một hình ảnh. API Aspose.PSD đã tiết lộ các phương thức hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD cho Java đã tiết lộ các lớp BilateralSmoothingFilterOptions và SharpenFilterOptions để lọc. Lớp BilateralSmoothingFilterOptions cần một số nguyên làm kích thước. Các bước để thực hiện Thay đổi kích cỡ đơn giản như sau:

1. Tải một hình ảnh bằng phương thức Factory Load được tiết lộ bởi lớp Image.
2. Chuyển đổi hình ảnh thành RasterImage.
3. Tạo một instances của lớp BilateralSmoothingFilterOptions và lớp SharpenFilterOptions.
4. Gọi phương thức RasterImage.Filter trong khi chỉ định hình chữ nhật là biên giới hình ảnh và instance của lớp BilateralSmoothingFilterOptions.
5. Gọi phương thức RasterImage.Filter trong khi chỉ định hình chữ nhật là biên giới hình ảnh và instance của lớp SharpenFilterOptions.
6. Điều chỉnh độ tương phản
7. Đặt độ sáng
8. Lưu kết quả.

Đoạn mã dưới đây sẽ hướng dẫn bạn cách áp dụng bộ lọc sửa chữa.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}

## **Sử dụng thuật toán ngưỡng Bradley**
Ngưỡng hình ảnh được sử dụng trong các ứng dụng đồ họa. Mục tiêu của việc ngưỡng một hình ảnh là phân loại pixel là "tối" hoặc "sáng". Aspose.PSD API cho phép bạn sử dụng ngưỡng Bradley khi chuyển đổi hình ảnh. Đoạn mã dưới đây sẽ hướng dẫn bạn cách xác định giá trị ngưỡng và sau đó gọi thuật toán ngưỡng của Bradley.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}

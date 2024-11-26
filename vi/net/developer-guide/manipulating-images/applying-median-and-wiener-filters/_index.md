---
title: Áp dụng Bộ lọc Trung bình và Wiener
type: docs
weight: 10
url: /vi/ứng-dụng-bộ-lọc-trung-bình-và-wiener/
---

## **Áp dụng Bộ lọc Trung bình và Wiener**
Bộ lọc trung bình là một kỹ thuật lọc số không tuyến tính, thường được sử dụng để loại bỏ nhiễu. Việc giảm nhiễu như vậy là một bước tiền xử lý điển hình để cải thiện kết quả của thao tác xử lý sau này. Bộ lọc Wiener là bộ lọc tuyến tính tĩnh tối ưu MSE (lỗi bình phương trung bình) cho các hình ảnh bị biến dạng do nhiễu cộng và làm mờ. Sử dụng Aspose.PSD cho các nhà phát triển API .NET, bạn có thể áp dụng bộ lọc trung bình để làm sạch ảnh và có thể áp dụng bộ lọc wiener Gauss trên hình ảnh. Bài viết này minh họa cách áp dụng bộ lọc trung bình và bộ lọc wiener Gauss cho hình ảnh.
### **Áp dụng Bộ lọc Trung bình**
Aspose.PSD cung cấp class [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) để áp dụng bộ lọc trên một  [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Đoạn mã dưới đây minh họa cách áp dụng bộ lọc trung bình cho một hình ảnh raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Áp dụng Bộ lọc Wiener Gauss**
Aspose.PSD cung cấp class [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) để áp dụng bộ lọc trên một [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Đoạn mã dưới đây minh họa cách áp dụng bộ lọc wiener Gauss cho một hình ảnh raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Áp dụng Bộ lọc Wiener Gauss Cho Hình ảnh màu**
Aspose.PSD cung cấp [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)cho hình ảnh màu. Đoạn mã dưới đây minh họa cách áp dụng bộ lọc wiener Gauss cho một hình ảnh màu.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Áp dụng Bộ lọc Wiener Chuyển động**
Aspose.PSD cung cấp class [MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions)để áp dụng bộ lọc trên một [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Đoạn mã dưới đây minh họa cách áp dụng bộ lọc wiener chuyển động cho một hình ảnh raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Áp dụng Bộ lọc Sửa Đổi Trên Một Hình ảnh**
Bài viết này minh họa cách sử dụng Aspose.PSD cho .NET để thực hiện các bộ lọc sửa đổi trên một hình ảnh. API của Aspose.PSD đã tiếp cận các phương pháp hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD cho .NET đã tiết lộ các class [BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)và [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions)cho việc lọc. Class BilateralSmoothingFilterOptions cần một số nguyên làm kích thước. Các bước để thực hiện thay đổi đơn giản như sau:

1. Nạp một hình ảnh bằng phương thức tạo của lớp Hình ảnh.
1. Chuyển đổi hình ảnh thành RasterImage.
1. Tạo một thể hiện của các class BilateralSmoothingFilterOptions và SharpenFilterOptions.
1. Gọi phương thức [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) trong khi chỉ định hình chữ nhật là ranh giới hình ảnh và thể hiện class BilateralSmoothingFilterOptions.
1. Gọi phương thức [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) trong khi chỉ định hình chữ nhật là ranh giới hình ảnh và thể hiện class SharpenFilterOptions.
1. Điều chỉnh độ tương phản
1. Đặt độ sáng
1. Lưu kết quả.


## **Sử dụng thuật toán ngưỡng Bradley**
Việc ngưỡng hình ảnh được sử dụng trong các ứng dụng đồ họa. Mục tiêu của việc ngưỡng ảnh là phân loại các pixel thành "tối" hoặc "sáng". API của Aspose.PSD cho phép bạn sử dụng ngưỡng Bradley trong khi chuyển đổi ảnh. Đoạn mã dưới đây hiển thị cách xác định giá trị ngưỡng sau đó kích hoạt thuật toán ngưỡng của Bradley.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}

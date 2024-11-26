---
title: Hỗ trợ của Lớp Tầng Fill
type: docs
weight: 50
url: /vi/java/support-of-fill-layers/
---

## **Hỗ trợ của Lớp Tầng Fill Với Fill Màu**
Bài viết này mô tả cách điền lớp PSD với màu. Vui lòng sử dụng Aspose.PSD.FileFormats.Psd.Layers.FillLayer để thêm Màu vào lớp PSD. Đoạn mã dưới đây tải một tệp PSD, truy cập vào lớp Filllayer và thiết lập màu bằng cách sử dụng thuộc tính FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Hỗ trợ của Lớp Tầng Fill Với Fill Gradient**
Bài viết này mô tả cách sử dụng fill Gradient để điền lớp PSD. Các API của Aspose.PSD đã tiết lộ các phương thức hiệu quả và dễ sử dụng để đạt được mục tiêu này. Aspose.PSD đã tiết lộ các lớp GradientColorPoint và GradientTransparencyPoint để thêm hiệu ứng Gradient vào một lớp.

Các bước để điền lớp PSD bằng fill Gradient như sau:

- Tải tệp PSD dưới dạng ảnh bằng phương thức nhà máy Load được tiết lộ bởi lớp Image.
- Thiết lập các thuộc tính cài đặt của đối tượng FillLayer.
- Tạo danh sách ColorPoints với màu cần thiết và vị trí của màu.
- Tạo danh sách transparencyPoints với độ mờ cần thiết và vị trí của điểm độ trong suốt.
- Gọi phương thức FillLayer.Update
- Lưu kết quả.

Đoạn mã sau cho thấy cách thêm fill Gradient để điền lớp PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}

## **Hiệu Ứng Stroke Với Fill Màu**
Bài viết này mô tả cách tạo hiệu ứng đám đè bằng fill màu. Hiệu ứng Stroke được sử dụng để thêm đường kẻ và viền vào các lớp và hình dáng. Nó có thể được sử dụng để tạo ra các đường kẻ màu đơn, gradient sặc sỡ, cũng như viền mẫu.

Các bước để tạo hiệu ứng Stroke với Fill màu như sau:

- Thiết lập thuộc tính **LoadEffectsResource.**
- Tải tệp PSD dưới dạng ảnh bằng phương thức nhà máy Load được tiết lộ bởi lớp Image và xác định **PsdLoadOptions.**
- Thiết lập các thuộc tính cài đặt của **ColorFillSetting.**
- Lưu kết quả.

Đoạn mã sau cho thấy cách tạo hiệu ứng Stroke với Fill màu.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}

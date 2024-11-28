---
title: Lớp Điều chỉnh Đen Trắng
type: docs
weight: 30
url: /vi/java/layer-types/adjustment-layer/levels/
---

## Làm việc với lớp điều chỉnh Levels trong Photoshop sử dụng Java

Trong bài viết này, chúng ta sẽ tìm hiểu cách điều chỉnh phạm vi màu sắc và cân bằng màu của một bức ảnh trong định dạng tệp [PSD](/psd/vi/vi/psd-format/) theo cách lập trình bằng Java. Chúng ta không sử dụng trình chỉnh sửa ảnh Adobe® Photoshop® mà thay vào đó, chúng ta sử dụng thư viện Aspose.PSD cho Java hoạt động độc lập để thao tác với tài liệu Photoshop.

Mặc dù, Aspose.PSD cho Java hỗ trợ đủ [công cụ chỉnh sửa ảnh](/psd/vi/vi/manipulating-images/) theo ý muốn, chúng ta **sẽ làm việc với API lớp điều chỉnh Levels** vì đây là một trong những cách đơn giản và nhanh nhất để hoàn thành công việc.

## Tổng quan về API

Hiện tại, phiên bản thực thi (20.6 vào thời điểm viết bài này) của API lớp điều chỉnh Levels **hỗ trợ tất cả các tính năng cơ bản của Photoshop Levels**, tức là điều chỉnh các mức đầu vào và đầu ra cho kênh tổng hợp (RGB) cũng như cho mỗi kênh màu cơ bản (đỏ, xanh lá cây và xanh dương).

API của lớp điều chỉnh Levels rất dễ hiểu. Lớp [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) là điểm nhập vào cho việc điều chỉnh Levels. Nó chứa một vài phương thức để truy cập các kênh màu: getMasterChannel và getChannel(int). Cả hai phương thức trên trả về [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) có các thuộc tính tương ứng để thao tác với các mức đầu vào và đầu ra. Khác biệt giữa chúng là getMasterChannel dùng để chỉnh sửa kênh màu tổng hợp (RGB) trong khi getChannel truy cập vào một kênh màu cụ thể (đỏ, xanh lá cây hoặc xanh dương) thông qua chỉ số tương ứng.

## Tương thích với chế độ màu

Đáng chú ý rằng lớp điều chỉnh Levels **tương thích với phần lớn các chế độ màu** theo tính năng Levels của Photoshop. Do đó, hoàn toàn có thể điều chỉnh Levels cho hình ảnh trong chế độ màu Đen trắng (kênh màu xám), RGB (RGB, đỏ, xanh lá cây và xanh dương), CMYK (CMYK, xanh lam, đỏ, xanh lá cây và đen), Duotone (một kênh màu) và LAB (độ sáng, a và b channels).

## Điều chỉnh phạm vi màu sắc

Đơn giản, việc chỉnh sửa màu sắc áp dụng cho một bức ảnh để remap bóng đổ và đặc. Thông thường, **nó làm cho bức ảnh trở nên sắc nét hơn** , nếu thực hiện đúng cách. Ví dụ, hãy xem xét một bức ảnh của một con chó (b) và điều chỉnh phạm vi màu sắc của nó (a – ảnh chụp màn hình từ cửa sổ Levels trong Photoshop để rõ ràng) để làm cho bức ảnh trở nên sắc nét hơn (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Hình 1 Lớp Levels](levels-adjustment-figure-1.png)|

Để **điều chỉnh tổng quát phạm vi màu sắc** của một bức ảnh, mức đầu vào của kênh tổng màu cần được thiết lập:

```java
LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

LevelChannel masterChannel = levelsLayer.getMasterChannel();
masterChannel.setInputShadowLevel(( **short** )21);
masterChannel.setInputMidtoneLevel(( **float** )1.19);
masterChannel.setInputHighlightLevel(( **short** )229);
```

Cần lưu ý rằng các mức đầu vào phải nằm trong khoảng từ 0 đến 253 cho bóng đổ, từ 9.99 đến 0.01 cho vùng trung tính và từ 2 đến 255 cho điểm sáng. Dải mức đầu ra phải nằm trong khoảng từ 0 đến 255.

Cần thêm ví dụ hơn nữa? Bạn có thể tìm thấy chúng trên [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) và trong [cơ sở kiến thức](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Kết luận

Tóm lại, Aspose.PSD cho Java có API tiện dụng và đơn giản để thay đổi phạm vi màu sắc và cân bằng màu của một hình ảnh, tương thích với hầu hết chế độ màu. API lớp điều chỉnh Levels của thư viện giống với Photoshop Levels, do đó, rất dễ bắt đầu ngay cả khi bạn chưa từng làm việc với thư viện trước đây.

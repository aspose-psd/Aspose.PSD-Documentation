---
title: Điều chỉnh Layer Đảo Ngược
type: docs
weight: 30
url: /vi/java/layer-types/adjustment-layer/invert/
---

# Làm việc với layer điều chỉnh Đảo Ngược trong Photoshop bằng Java

Trong bài viết này, chúng tôi sẽ hướng dẫn cách chuyển ảnh trong tài liệu Photoshop thành ảnh âm một cách tự động trong Java. Vì mục đích này, chúng ta sẽ sử dụng thư viện cho việc tương tác với định dạng tập tin PSD gọi là Aspose.PSD cho Java.

API đảo ngược màu cho phép **thêm hiệu ứng âm vào ảnh**. Bạn có thể đã biết cách [đảo ngược màu ảnh bằng layer điều chỉnh Curves](/psd/vi/java/layer-types/adjustment-layer/curves/). Tuy nhiên, hôm nay chúng ta sẽ xem xét một cách nhanh hơn và dễ dàng hơn để thực hiện công việc với layer điều chỉnh Đảo Ngược.

## Tổng quan về API

**API layer điều chỉnh Đảo Ngược** bao gồm lớp layer chính là [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Lớp này không có các thành viên công cộng riêng, vì nó kế thừa tất cả các thành viên công cộng từ lớp cha ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). Sự thực này giúp đơn giản hóa việc sử dụng vì tất cả những gì bạn cần làm là thêm nó vào tập tin PSD và ảnh sẽ trở thành ảnh âm.

## Đảo ngược màu ảnh

Vậy, thậm chí nếu điều này có vẻ hiển nhiên nhưng hãy minh họa để làm rõ cách **áp dụng layer điều chỉnh Đảo Ngược vào ảnh** của một phi hành gia (a) để tạo hiệu ứng âm cho hình ảnh đó (b).

![Ví dụ Layer Điều chỉnh Đảo Ngược Trước và Sau](invert-adjustment-layer-figure-1.png)

Để **đảo ngược màu của ảnh**, chỉ cần thêm một layer điều chỉnh Đảo Ngược vào trong PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

Vậy là hoàn tất! Không có các thuộc tính cụ thể để cấu hình cho loại layer điều chỉnh này.

## Kết luận

Trong bài viết này, chúng ta đã tìm hiểu về API layer điều chỉnh Đảo Ngược của Aspose.PSD cho Java. Đó là một công cụ đơn giản để lấy ảnh âm vì API của layer điều chỉnh này không khai báo bất kỳ thành viên công cộng nào.

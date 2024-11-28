---
title: Điều chỉnh Lớp Điều chỉnh Bộ lọc Ảnh
type: docs
weight: 30
url: /vi/java/layer-types/adjustment-layer/photo-filter/
---

# Làm việc với lớp điều chỉnh Bộ lọc Ảnh trong Photoshop bằng Java

Hôm nay chúng ta sẽ thấy cách áp dụng lớp điều chỉnh Bộ lọc Ảnh vào tài liệu Photoshop hiện có bằng cách sử dụng Aspose.PSD cho Java, thư viện để thao tác định dạng tệp PSD.

**API lớp điều chỉnh Bộ lọc Ảnh** thay đổi cân bằng màu của hình ảnh bằng cách tô màu. Hình ảnh kết quả sẽ trông giống như sau khi sử dụng bộ lọc máy ảnh thực sự. Lưu ý rằng API lớp điều chỉnh Bộ lọc Ảnh của thư viện hơi khác so với Photoshop vì chưa có bộ lọc được xác định trước. Tuy nhiên, nó giống nhau ở tất cả các khía cạnh khác. Điều đó có nghĩa là bạn có thể đặt một màu của tô và thay đổi độ sáng (mật độ) của nó cũng như sử dụng tùy chọn Bảo toàn Độ Sáng.

## Tổng quan về API

API lớp điều chỉnh Bộ lọc Ảnh khá đơn giản để sử dụng. Có lớp chính [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) làm điểm nhập của lớp điều chỉnh này và chỉ chứa ba thuộc tính công cộng, đó là tô, mật độ và bảo toàn độ sáng mà qua đó điều chỉnh xảy ra.

## Điều chỉnh cân bằng màu 

Do không có nhiều điều để nói, hãy cùng xem xét **một ví dụ về việc điều chỉnh cân bằng màu** bằng cách sử dụng Bộ lọc Ảnh ngay lập tức. Chúng ta sẽ thêm một bộ lọc ấm (a) vào hình ảnh điêu khắc hươu (b) để có được hình ảnh trong những gam màu ấm (c) dễ nhìn hơn.

![Ví dụ Lớp Điều chỉnh Bộ lọc Ảnh](photo-filter-adjustment-layer-figure-1.png)

Đầu tiên hãy chú ý rằng [phương thức nhà máy](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) khác với những [lớp điều chỉnh khác](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers) vì không có phương thức mặc định (không có đối số). Do đó, để thêm một lớp điều chỉnh Bộ lọc Ảnh vào tài liệu Photoshop đã tải chỉ cần một đối số duy nhất đó là [màu](https://reference.aspose.com/psd/java/com.aspose.psd/Color). Vì vậy, để tái tạo hiệu ứng bộ lọc ấm chỉ cần chuyển màu cam như một đối số cho phương thức nhà máy, sau đó thiết lập mật độ bằng cách sử dụng các phương thức thiết lập tương ứng:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Nó đáng giá khi mức độ Mật độ có giá trị mặc định là 100 cũng như true là giá trị mặc định cho tính năng Bảo toàn Độ Sáng (đó là lý do tại sao chúng ta không kích hoạt lựa chọn này một cách rõ ràng).

## Kết luận

Trong bài viết này, chúng ta đã xem xét việc sử dụng API lớp điều chỉnh Bộ lọc Ảnh của Aspose.PSD cho Java. Công cụ này dễ sử dụng và cho phép thêm tô vào hình ảnh với mật độ biến thiên. Đó là một cách nhanh chóng để điều chỉnh cân bằng màu của toàn bộ hình ảnh.

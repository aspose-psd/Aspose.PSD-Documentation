---
title: Sử dụng Layer Điều chỉnh để Tăng cường PSD
weight: 100
type: docs
description: Ví dụ về việc sử dụng layer điều chỉnh thông qua Aspose.PSD cho Java
keywords: [layer điều chỉnh, tăng cường ảnh, điều chỉnh đường cong, tăng cường mức độ, đảo ngược, bộ lọc ảnh,  api psd, java, mẫu mã code]
url: vi/java/adjustment-layer-enhancement/
---

## **Tổng quan**

Bài viết này khám phá việc chỉnh sửa các lớp điều chỉnh trong Aspose.PSD cho Java. Các lớp điều chỉnh là một tính năng mạnh mẽ trong chỉnh sửa ảnh cho phép bạn thực hiện các thay đổi không phá hủy đối với ảnh của bạn. Aspose.PSD cung cấp một tập hợp toàn diện các lớp điều chỉnh mà bạn có thể sử dụng để sửa đổi các khía cạnh khác nhau của ảnh của bạn.

Để minh họa việc chỉnh sửa các lớp điều chỉnh, chúng tôi sẽ cung cấp một đoạn mã mẫu ở cuối trang mà nạp hình ảnh PSD và áp dụng các điều chỉnh khác nhau cho các lớp của nó.

Trong đoạn mã mẫu sau, chúng tôi bắt đầu bằng việc nạp hình ảnh PSD bằng cách sử dụng phương thức PsdImage.load(). Sau đó, chúng tôi thiết lập các tùy chọn để lưu các tệp PNG đầu ra. Lớp PngOptions cho phép chúng ta chỉ định loại màu cho hình ảnh đầu ra.

Tiếp theo, chúng tôi lặp qua từng lớp trong hình ảnh PSD và kiểm tra loại của nó bằng cách sử dụng phương thức isAssignable(). Nếu lớp là một loại cụ thể, chúng ta ép kiểu nó thành loại đó bằng cách sử dụng phương thức cast() và áp dụng điều chỉnh mong muốn. Ví dụ, chúng tôi điều chỉnh độ sáng và sự tương phản của một BrightnessContrastLayer, sửa đổi mức độ của một LevelsLayer, thêm một điểm đường cong vào một CurvesLayer, và còn nhiều nữa.

Bạn có thể thêm mã khác để áp dụng các điều chỉnh khác cho các lớp tương ứng của họ. Aspose.PSD cung cấp một loạt rộng lớp điều chỉnh, như [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), và nhiều lớp khác.

Cuối cùng, chúng tôi lưu hình ảnh đã sửa đổi bằng cách sử dụng phương thức save() của lớp PsdImage.

Điều này cung cấp một cái nhìn tổng quan cơ bản về cách chỉnh sửa các lớp điều chỉnh trong Aspose.PSD cho Java. Bạn có thể tùy chỉnh các điều chỉnh theo yêu cầu của mình và khám phá các tùy chọn khác nhau có sẵn trong tài liệu API.

Vui lòng kiểm tra ví dụ đầy đủ bên dưới.

## **Ví dụ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}

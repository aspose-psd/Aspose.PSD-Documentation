---
title: Sử dụng Adjustment Layer để Tăng cường PSD
weight: 100
type: docs
description: Ví dụ về việc sử dụng adjustment layer thông qua Aspose.PSD cho Python
keywords: [adjustment layer, tăng cường ảnh, cải thiện độ sáng, cải thiện mức độ, đảo ngược, bộ lọc ảnh, psd api, python, mã mẫu]
url: vi/python-net/adjustment-layer-enhancement/
---

## **Tổng quan**

Trong bài viết này, chúng ta sẽ khám phá việc chỉnh sửa các lớp điều chỉnh trong Aspose.PSD cho Python. Các lớp điều chỉnh là một tính năng mạnh mẽ trong việc chỉnh sửa ảnh cho phép bạn thực hiện các thay đổi không phá hủy đến ảnh của bạn. Aspose.PSD cung cấp một bộ lớp điều chỉnh toàn diện mà bạn có thể sử dụng để thay đổi các khía cạnh khác nhau của ảnh của bạn.

Để minh họa việc chỉnh sửa các lớp điều chỉnh, chúng ta sẽ sử dụng một đoạn mã mẫu ở cuối trang để tải một hình ảnh PSD và áp dụng các điều chỉnh khác nhau cho các lớp của nó.

Trong đoạn mã mẫu bên dưới, chúng ta bắt đầu bằng cách tải hình ảnh PSD bằng cách sử dụng phương thức PsdImage.load(). Sau đó, chúng ta thiết lập tùy chọn để lưu các tệp PNG đầu ra. Lớp PngOptions cho phép chúng ta xác định loại màu cho hình ảnh đầu ra.

Tiếp theo, chúng ta lặp lại qua mỗi lớp trong hình ảnh PSD và kiểm tra loại của nó bằng cách sử dụng phương thức is_assignable(). Nếu lớp đó là một loại cụ thể, chúng ta sẽ đúng hoá nó thành loại đó bằng phương thức cast() và áp dụng điều chỉnh mong muốn. Ví dụ, chúng ta điều chỉnh độ sáng và đối chọi của một BrightnessContrastLayer, sửa đổi mức của một LevelsLayer, thêm một điểm đường cong vào một CurvesLayer, và vân vân.

Bạn có thể thêm mã khác để áp dụng các điều chỉnh khác cho các lớp tương ứng của họ. Aspose.PSD cung cấp một loạt rộng các lớp điều chỉnh, như [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), và nhiều hơn nữa.

Cuối cùng, chúng ta lưu hình ảnh đã được sửa đổi bằng phương thức save() của lớp PsdImage.

Mã này cung cấp một tổng quan cơ bản về cách chỉnh sửa các lớp điều chỉnh trong Aspose.PSD cho Python. Bạn có thể tùy chỉnh các điều chỉnh theo yêu cầu của mình và khám phá các tùy chọn khác nhau có sẵn trong tài liệu API.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}

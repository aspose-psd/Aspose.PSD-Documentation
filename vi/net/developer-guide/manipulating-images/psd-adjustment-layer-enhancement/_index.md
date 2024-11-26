---
title: Sử dụng Layer Điều chỉnh cho Việc Tăng cường PSD
weight: 100
type: docs
description: Ví dụ về việc sử dụng các lớp điều chỉnh qua Aspose.PSD cho C#
keywords: [layer điều chỉnh, tăng cường ảnh, điều chỉnh đường cong, tăng cường mức độ, đảo ngược, bộ lọc ảnh, psd api, C#, csharp, mẫu mã code]
url: vi/net/adjustment-layer-enhancement/
---

## Tổng quan

Trong bài viết này, chúng ta sẽ khám phá việc chỉnh sửa các lớp điều chỉnh trong Aspose.PSD cho C#. Các lớp điều chỉnh là một tính năng mạnh mẽ trong chỉnh sửa ảnh cho phép bạn thực hiện các thay đổi không phá hoại đến ảnh của bạn. Aspose.PSD cung cấp một bộ lớp điều chỉnh toàn diện mà bạn có thể sử dụng để sửa đổi các khía cạnh khác nhau của ảnh của bạn.

Để minh họa việc chỉnh sửa các lớp điều chỉnh, chúng ta sẽ sử dụng một đoạn mã mẫu ở cuối trang sẽ tải một hình ảnh PSD và áp dụng các điều chỉnh khác nhau cho các lớp của nó.

Ở đoạn mã mẫu dưới đây, chúng ta bắt đầu bằng việc tải hình ảnh PSD bằng cách sử dụng phương thức `PsdImage.Load()`. Sau đó, chúng ta thiết lập các tùy chọn để lưu các tệp PNG đầu ra. Lớp `PngOptions` cho phép chúng ta chỉ định loại màu cho ảnh đầu ra.

Tiếp theo, chúng ta duyệt qua mỗi lớp trong hình ảnh PSD và kiểm tra loại của nó bằng cách sử dụng phương thức `IsAssignable()`. Nếu lớp đó là của một loại cụ thể, chúng ta đưa nó về loại đó bằng cách sử dụng phương thức `Cast()` và áp dụng điều chỉnh cần thiết. Ví dụ, chúng ta điều chỉnh độ sáng và độ tương phản của một `BrightnessContrastLayer`, sửa đổi các mức độ của một `LevelsLayer`, thêm một điểm Curve cho một `CurvesLayer`, và cứ tiếp tục.

Bạn có thể thêm mã code bổ sung để áp dụng các điều chỉnh khác cho các lớp tương ứng của họ. Aspose.PSD cung cấp một loạt rộng các lớp điều chỉnh, như [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), và nhiều hơn nữa.

Cuối cùng, chúng ta lưu hình ảnh đã sửa đổi bằng cách sử dụng phương thức `Save()` của lớp `PsdImage`.

Đoạn mã này cung cấp một cái nhìn tổng quan cơ bản về cách chỉnh sửa các lớp điều chỉnh trong Aspose.PSD cho C#. Bạn có thể tùy chỉnh các điều chỉnh theo yêu cầu của bạn và khám phá các tùy chọn khác nhau có sẵn trong tài liệu API.

## Ví dụ

Dưới đây là một đoạn mã mẫu biểu diễn cách sử dụng các lớp điều chỉnh bằng Aspose.PSD cho C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Để biết thêm thông tin chi tiết và ví dụ, vui lòng truy cập [tài liệu Aspose.PSD cho C#](https://docs.aspose.com/psd/net/).


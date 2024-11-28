---
title: Điều khiển Bộ lọc Thông minh trong Aspose.PSD cho C#
weight: 100
type: docs
description: Ví dụ về cách sử dụng Bộ lọc Thông minh trong Tệp PSD
keywords: [bộ lọc thông minh, thêm nhiễu, làm mờ gauss, làm sắc nét, bộ lọc, bộ lọc psd, api psd, C#, code mẫu]
url: vi/net/smart-filters/
---

## Tổng quan

Có ba cách để áp dụng bộ lọc thông minh trong Aspose.PSD cho C#.

### Áp Dụng Bộ lọc Trực Tiếp

Ví dụ này demo cách áp dụng trực tiếp bộ lọc thông minh trong Aspose.PSD cho C#.

Đầu tiên, chỉ định tệp PSD nguồn, tệp đầu ra cho hình ảnh gốc, và tệp đầu ra cho hình ảnh được cập nhật.

Tiếp theo, tải hình ảnh PSD bằng phương thức `Image.Load` và ép kiểu nó thành một đối tượng `PsdImage`.

Lưu hình ảnh gốc bằng phương thức `Save` với tên tệp đầu ra đã chỉ định.

Tạo một đối tượng `SharpenSmartFilter`, đại diện cho bộ lọc thông minh sẽ được áp dụng.

Truy xuất lớp thông thường từ hình ảnh PSD bằng cách sử dụng `psdImage.Layers[1]`.

Áp dụng `sharpenFilter` vào lớp thông thường ba lần trong một vòng lặp.

Cuối cùng, lưu hình ảnh được cập nhật bằng phương thức `Save` với tên tệp đầu ra đã chỉ định.

Mã này demo cách áp dụng trực tiếp bộ lọc thông minh trong Aspose.PSD cho C#. Bằng cách sử dụng các đối tượng bộ lọc thích hợp và áp dụng chúng vào các lớp mong muốn, bạn có thể đạt được những hiệu ứng mong muốn trên hình ảnh của bạn.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Điều khiển Bộ lọc Thông minh trong Đối tượng Thông minh

Ví dụ này thể hiện cách điều khiển bộ lọc thông minh trong các đối tượng thông minh.

Đầu tiên, chỉ định tệp PSD nguồn, tệp đầu ra cho hình ảnh gốc, và tệp đầu ra cho hình ảnh được cập nhật.

Tải hình ảnh PSD bằng phương thức `Image.Load` và ép kiểu nó thành một đối tượng `PsdImage`.

Lưu hình ảnh gốc bằng phương thức `Save` với tên tệp đầu ra đã chỉ định.

Ép kiểu lớp thứ hai của hình ảnh PSD thành một đối tượng `SmartObjectLayer`.

Chỉnh sửa bộ lọc thông minh. Ví dụ này thể hiện cách làm việc với `GaussianBlurSmartFilter` và `AddNoiseSmartFilter`.

Đối với `GaussianBlurSmartFilter`, cập nhật các giá trị bộ lọc bao gồm bán kính, chế độ hòa trộn, độ mờ và trạng thái đã được bật.

Đối với `AddNoiseSmartFilter`, đặt phân phối nhiễu thành `NoiseDistribution.UNIFORM`.

Thêm các mục bộ lọc mới vào lớp đối tượng thông minh: một `GaussianBlurSmartFilter` khác và `AddNoiseSmartFilter`.

Áp dụng các thay đổi bằng cách sử dụng phương thức `UpdateResourceValues`.

Áp dụng các bộ lọc trực tiếp vào lớp và vào mặt nạ của lớp bằng cách sử dụng các phương thức `Apply` và `ApplyToMask` một cách tương ứng.

Lưu hình ảnh được cập nhật bằng phương thức `Save` với tên tệp đầu ra đã chỉ định.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Áp Dụng Bộ lọc Thông minh vào Mặt nạ Lớp

Bộ lọc thông minh là một công cụ chỉnh sửa hình ảnh mạnh mẽ cho phép người dùng áp dụng nhiều bộ lọc và hiệu ứng khác nhau. Một kỹ thuật thú vị là áp dụng chúng vào các mặt nạ, giúp kiểm soát chính xác các khu vực bị ảnh hưởng bởi bộ lọc.

Một mặt nạ là một hình ảnh mức xám xác định sự trong suốt của một số khu vực hình ảnh, cho phép áp dụng bộ lọc, điều chỉnh hoặc hiệu ứng một cách chọn lọc.

Khi áp dụng bộ lọc thông minh vào mặt nạ, bộ lọc chỉ được áp dụng vào các khu vực được chỉ định bởi mặt nạ. Kiểm soát chính xác này cho phép điều chỉnh độ mạnh và mức độ của bộ lọc.

Để biết thông tin chi tiết và ví dụ, vui lòng tham khảo tài liệu của [Aspose.PSD cho C#](https://docs.aspose.com/psd/net/).


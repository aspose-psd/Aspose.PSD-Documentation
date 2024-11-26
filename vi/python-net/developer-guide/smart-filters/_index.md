---
title: Làm thế nào để thao tác Smart Filters thông minh trong Aspose.PSD cho Python
weight: 100
type: docs
description: Ví dụ về cách sử dụng Smart Filters trong tệp PSD
keywords: [smart filter, thêm noise, gauss blur, làm sắc nét, filter, psd filter, psd api, python, mẫu mã code]
url: vi/python-net/smart-filters/
---

## **Tổng quan**

Có 3 cách để áp dụng smart filters trong Aspose.PSD cho Python.

## **Ứng dụng bộ lọc trực tiếp**
Trong mẫu mã code này, chúng ta có thể thấy một ví dụ về cách áp dụng smart filters trực tiếp trong Aspose.PSD cho Python.

Trước hết, mã xác định tệp PSD nguồn, tệp đầu ra cho hình ảnh gốc và tệp đầu ra cho hình ảnh được cập nhật.

Tiếp theo, mã tải hình ảnh PSD bằng phương thức Image.load() và chuyển đổi nó thành một đối tượng PsdImage.

Hình ảnh gốc sau đó được lưu bằng phương thức save(), với tên tệp đầu ra được xác định.

Một đối tượng SharpenSmartFilter được tạo ra, đại diện cho smart filter cần áp dụng.

Sau đó, mã truy xuất lớp thông thường từ hình ảnh PSD bằng im.layers[1].

Một vòng lặp được sử dụng để áp dụng sharpenFilter vào lớp thường xuyên ba lần.

Cuối cùng, hình ảnh được cập nhật được lưu bằng phương thức save() và tên tệp đầu ra được xác định.

Mã này thể hiện cách áp dụng smart filters trực tiếp trong Aspose.PSD cho Python. Bằng cách sử dụng các đối tượng bộ lọc thích hợp và áp dụng chúng vào các lớp mong muốn, bạn có thể đạt được hiệu ứng mong muốn trên hình ảnh của mình.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Thao tác Smart Filters trên Đối tượng Thông Minh**

Trước hết, mã xác định tệp PSD nguồn, tệp đầu ra cho hình ảnh gốc và tệp đầu ra cho hình ảnh được cập nhật.

Hình ảnh PSD được tải bằng phương thức Image.load(), và sau đó được chuyển đổi thành đối tượng PsdImage.

Hình ảnh gốc sau đó được lưu bằng phương thức save(), với tên tệp đầu ra được xác định.

Mã sau đó chuyển đổi lớp thứ hai của hình ảnh PSD thành đối tượng SmartObjectLayer, đại diện cho lớp đối tượng thông minh.

Mã sau đó tiếp tục chỉnh sửa các smart filters. Trong ví dụ này, nó minh họa cách làm việc với hai loại smart filters: GaussianBlurSmartFilter và AddNoiseSmartFilter.

Đối với GaussianBlurSmartFilter, mã cập nhật các giá trị bộ lọc, bao gồm bán kính, chế độ pha trộn, độ mờ, và xem nó đã được kích hoạt hay chưa.

Đối với AddNoiseSmartFilter, mã đặt phân phối tiếng ồn thành NoiseDistribution.UNIFORM.

Tiếp theo, mã thêm hai mục bộ lọc mới vào lớp đối tượng thông minh: một GaussianBlurSmartFilter khác và một AddNoiseSmartFilter.

Sau khi thêm các bộ lọc mới, mã áp dụng các thay đổi bằng cách sử dụng phương thức update_resource_values().

Cuối cùng, mã thể hiện cách áp dụng trực tiếp các bộ lọc vào lớp và vào mặt nạ của lớp bằng cách sử dụng phương thức apply() và apply_to_mask() tương ứng.

Hình ảnh được cập nhật sau đó được lưu bằng phương thức save() và tên tệp đầu ra được xác định.

Bằng cách làm theo mẫu mã code này, bạn có thể học cách làm việc với smart filters trong Aspose.PSD cho Python. Thư viện cung cấp một loạt rộng bộ lọc thông minh, mỗi loại có tập hợp các thuộc tính và phương thức riêng biệt có thể tùy chỉnh để đạt được hiệu ứng mong muốn trên hình ảnh của bạn.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **Áp dụng Smart Filters cho Mặt nạ Lớp**

Áp dụng Smart Filters cho Mặt nạ: Một Kỹ Thuật Chỉnh Sửa Hình Ảnh Mạnh Mẽ

Smart filters là một tính năng phổ biến trong phần mềm chỉnh sửa hình ảnh cho phép người dùng áp dụng các bộ lọc và hiệu ứng khác nhau vào hình ảnh của họ. Một kỹ thuật thú vị có thể đạt được bằng cách sử dụng smart filters là áp dụng chúng vào các mặt nạ. Trong bài viết này, chúng ta sẽ khám phá cách áp dụng smart filters vào các mặt nạ và thảo luận về việc sử dụng chúng trong thế giới chỉnh sửa hình ảnh.

Mặt nạ là gì? Trước khi chúng ta tìm hiểu về cách áp dụng smart filters vào các mặt nạ, hãy hiểu trước mặt mặt nạ là gì. Trong chỉnh sửa hình ảnh, một mặt nạ là một hình ảnh xám xác định sự trong suốt của các khu vực cụ thể của một hình ảnh. Một mặt nạ có thể được sử dụng để áp dụng lọc, điều chỉnh hoặc hiệu ứng vào các phần cụ thể của một hình ảnh, trong khi để lại các khu vực khác không thay đổi.

Áp dụng Smart Filters vào các Mặt nạ: Khi áp dụng smart filters vào các mặt nạ, các bộ lọc chỉ được áp dụng vào các khu vực được chỉ định bởi mặt nạ. Điều này giúp kiểm soát chính xác vùng nào của hình ảnh bị ảnh hưởng bởi bộ lọc. Bằng cách điều chỉnh mặt nạ, bạn có thể xác định cường độ và phạm vi của hiệu ứng của bộ lọc.

Vui lòng kiểm tra ví dụ trước và phương thức: [API Tham Khảo Áp Dụng Smart Filter vào Mặt nạ](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

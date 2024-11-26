---
title: Xử lý Bộ lọc Thông minh trong Aspose.PSD cho Java
weight: 100
type: docs
description: Ví dụ về cách sử dụng Bộ lọc Thông minh trong Tệp PSD
keywords: [bộ lọc thông minh, thêm nhiễu, làm mờ gauss, làm nhọn, bộ lọc, bộ lọc psd,  api psd, java, mẫu mã code]
url: /vi/java/smart-filters/
---

## **Tổng quan**

Có 3 phương pháp để áp dụng bộ lọc thông minh trong Aspose.PSD cho Java.

## **Ứng dụng Bộ lọc Trực tiếp**

Đoạn mã này minh họa cách áp dụng trực tiếp bộ lọc thông minh trong Aspose.PSD cho Java.

Ban đầu, mã xác định tệp PSD nguồn, tệp đầu ra cho ảnh gốc, và tệp đầu ra cho ảnh đã được cập nhật.

Sau đó, mã tải hình ảnh PSD bằng phương thức Image.load() và ép kiểu thành đối tượng PsdImage.

Ảnh gốc được lưu bằng cách sử dụng phương thức save(), chỉ định tên tệp đầu ra.

Một đối tượng SharpenSmartFilter được tạo để đại diện cho bộ lọc thông minh mong muốn.

Tiếp theo, mã lấy lớp thông thường từ hình ảnh PSD bằng cách sử dụng psdImage.getLayers()[1].

Một vòng lặp được sử dụng để áp dụng bộ lọc sharpenFilter vào lớp thông thường ba lần.

Cuối cùng, ảnh đã được cập nhật được lưu bằng cách sử dụng phương thức save() với tên tệp đầu ra được cung cấp.

Đoạn mã này minh họa việc áp dụng trực tiếp bộ lọc thông minh trong Aspose.PSD cho Java. Bằng cách sử dụng các đối tượng bộ lọc thích hợp và áp dụng chúng vào các lớp mong muốn, có thể đạt được hiệu ứng mong muốn trên hình ảnh.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## **Xử lý Bộ lọc Thông minh trong Các Đối tượng Thông minh**

Đoạn mã này đề cập cách xử lý bộ lọc thông minh trong các đối tượng thông minh trong Aspose.PSD cho Java.

Ban đầu, mã xác định tệp PSD nguồn, tệp đầu ra cho ảnh gốc, và tệp đầu ra cho ảnh đã được cập nhật.

Hình ảnh PSD được tải bằng phương thức Image.load() và sau đó ép kiểu thành đối tượng PsdImage.

Ảnh gốc được lưu bằng cách sử dụng phương thức save(), chỉ định tên tệp đầu ra.

Sau đó, mã ép kiểu lớp thứ hai của hình ảnh PSD thành đối tượng SmartObjectLayer, đại diện cho lớp đối tượng thông minh.

Tiếp theo, mã minh họa việc chỉnh sửa bộ lọc thông minh, giới thiệu hai loại: GaussianBlurSmartFilter và AddNoiseSmartFilter.

Đối với GaussianBlurSmartFilter, mã cập nhật các giá trị bộ lọc như bán kính, chế độ hòa trộn, độ mờ và trạng thái kích hoạt.

Đối với AddNoiseSmartFilter, mã thiết lập phân phối tạp âm thành NoiseDistribution.Uniform.

Tiếp theo, mã thêm hai mục bộ lọc mới vào lớp đối tượng thông minh: một GaussianBlurSmartFilter khác và một AddNoiseSmartFilter.

Sau khi thêm các bộ lọc mới, mã áp dụng thay đổi bằng cách sử dụng phương thức updateResourceValues().

Cuối cùng, mã minh họa việc áp dụng trực tiếp bộ lọc vào lớp và mặt nạ của nó bằng cách sử dụng phương thức apply() và applyToMask() tương ứng.

Ảnh đã cập nhật sau đó được lưu bằng cách sử dụng phương thức save() với tên tệp đầu ra được cung cấp.

Bằng cách theo dõi mẫu mã code này, bạn có thể hiểu cách xử lý bộ lọc thông minh trong các đối tượng thông minh trong Aspose.PSD cho Java. Thư viện cung cấp một loạt các bộ lọc thông minh, mỗi cái với bộ thuộc tính và phương thức riêng biệt có thể được tùy chỉnh để đạt được hiệu ứng mong muốn trên hình ảnh.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## **Áp dụng Bộ lọc Thông minh vào Mặt nạ của Lớp**

Áp Dụng Bộ lọc Thông minh vào Mặt nạ: Một Kỹ Thuật Chỉnh Sửa Ảnh Mạnh Mẽ

Bộ lọc thông minh, phổ biến trong phần mềm chỉnh sửa hình ảnh, cho phép người dùng áp dụng nhiều bộ lọc và hiệu ứng đa dạng vào hình ảnh của họ. Một kỹ thuật hấp dẫn mà bộ lọc thông minh cho phép là áp dụng chúng vào các mặt nạ. Bài viết này khám phá việc áp dụng bộ lọc thông minh vào mặt nạ và thảo luận về tính hữu ích của chúng trong lĩnh vực chỉnh sửa hình ảnh.

Hiểu Mặt nạ: Trước khi đào sâu vào việc áp dụng bộ lọc thông minh vào mặt nạ, quan trọng phải hiểu khái niệm về một mặt nạ. Trong chỉnh sửa hình ảnh, một mặt nạ là một hình ảnh xám quy định độ trong suốt của các khu vực cụ thể trong hình ảnh. Mặt nạ cho phép áp dụng bộ lọc, điều chỉnh hoặc hiệu ứng lựa chọn vào một số phần cụ thể của hình ảnh trong khi để lại các phần khác không bị ảnh hưởng.

Áp Dụng Bộ lọc Thông minh vào Mặt nạ: Khi các bộ lọc thông minh được áp dụng vào mặt nạ, chúng chỉ ảnh hưởng đến các khu vực được chỉ định bởi mặt nạ, cung cấp sự kiểm soát chính xác đối với tác động của bộ lọc. Bằng cách điều chỉnh mặt nạ, người dùng có thể điều chỉnh cường độ và phạm vi của hiệu ứng của bộ lọc.

Vui lòng tham khảo ví dụ trước đó và phương thức: [Tham Khảo API Áp Dụng Bộ Lọc Thông minh vào Mặt nạ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

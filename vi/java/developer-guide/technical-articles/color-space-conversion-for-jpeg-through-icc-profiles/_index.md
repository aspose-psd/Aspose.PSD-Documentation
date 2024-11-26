---
title: Chuyển Đổi Không Gian Màu cho JPEG thông qua Các Hồ Sơ ICC
type: docs
weight: 50
url: /vi/java/chuyen-doi-khong-gian-mau-cho-jpeg-qua-cac-ho-so-icc/
---

## **Quản lý Màu Sắc cho Định Dạng JPEG**

Bài viết này thảo luận về việc sử dụng các hồ sơ ICC để thực hiện quản lý không gian màu khi xử lý định dạng JPEG với API của Aspose.PSD. Không gian màu nội bộ của JPEG là YCbCr tuy nhiên định dạng này cũng có thể chứa các không gian màu Grayscale, RGB, CMYK và YCCK để lưu trữ siêu dữ liệu của hình ảnh. API của Aspose.PSD chủ yếu hoạt động trong không gian màu RGB do đó API phải thực hiện chuyển đổi giữa các không gian màu để xử lý file JPEG một cách chính xác. Chuyển từ Grayscale sang RGB & YCbCr sang RGB có thể được thực hiện bằng cách biến đổi toán học nhưng không gian CMYK & YCCK không thể dễ dàng chuyển đổi sang không gian RGB.


API của Aspose.PSD phải thực hiện chuyển đổi màu trực tiếp từ RGB sang CMYK cho các hình ảnh JPEG có không gian màu CMYK. Ngược lại, các hình ảnh có không gian màu YCCK yêu cầu chuyển đổi màu từ RGB sang CMYK và từ CMYK sang YCCK, trong đó chuyển đổi từ CMYK sang YCCK sử dụng chuyển đổi ITU-R BT.601 áp dụng cho ba kênh đầu tiên, giữ kênh k không đổi. Tóm lại, API của Aspose.PSD phải thực hiện chuyển đổi qua lại giữa không gian màu RGB và CMYK cho cả ảnh CMYK & YCCK, và các chuyển đổi này được thực hiện với sự trợ giúp của các hồ sơ ICC mà cơ bản là các bảng tra cứu mô tả các thuộc tính của màu sắc và hỗ trợ trong chuyển đổi màu sắc.


## **Các Hồ Sơ ICC**
Cơ chế chuyển đổi ICC sử dụng "Hồ Sơ" mà ánh xạ không gian màu nguồn sang không gian màu CIELAB hoặc CIEXYZ không phụ thuộc vào thiết bị. Aspose.PSD có thể chuyển đổi dữ liệu vào không gian màu khi cần thiết trong khi sử dụng hai không gian màu này với các hồ sơ bổ sung. Do đó, để chuyển đổi ICC, người dùng cần cung cấp hai hồ sơ - một hồ sơ RGB để đến không gian màu CIE nội bộ và một hồ sơ CMYK để có được các đặc tính màu CMYK. Để thực hiện chuyển đổi từ CMYK sang RGB, người cần hoán đổi hồ sơ, nghĩa là; sử dụng hồ sơ CMYK làm hồ sơ nguồn và hồ sơ RGB làm hồ sơ đích.


## **Chuyển Đổi Màu cho JPEG Qua Các Hồ Sơ ICC**
API của Aspose.PSD che giấu chi tiết, cung cấp một cơ chế dễ sử dụng để chỉ định các hồ sơ ICC qua lớp JpegOptions. Hơn nữa, Aspose.PSD sử dụng các hồ sơ mẫu của SWOP CMYK và sRGB được nhúng vào lõi của nó do đó trong hầu hết các trường hợp sử dụng thông thường, người dùng không cần phải tìm kiếm các hồ sơ cụ thể nào. Hạn chế của những sự điều chỉnh như vậy là; các chuyển đổi không gian màu như vậy là không thể đảo ngược vì chúng ta không thể mong đợi được cùng một màu sắc sau chuyển đổi từ RGB sang CMYK và sau đó từ CMYK quay trở lại RGB do không tương thích giữa các không gian màu và các hồ sơ màu khác nhau. Đoạn mã sau thể hiện cách sử dụng Aspose.PSD cho API Java để chỉ định hồ sơ màu RGB và CMYK cho ảnh JPEG YCCK. Trong ví dụ dưới đây, hồ sơ màu RGB và CMYK đã được thay đổi và ảnh được lưu trong không gian màu YCCK. Lưu ý rằng các thuộc tính RgbColorProfile và CmykColorProfile sẽ hoạt động để thay đổi dữ liệu pixel cho không gian màu YCCK. Tất cả các không gian màu khác không cần phải lấy các hồ sơ màu để cập nhật dữ liệu màu sắc.


Nếu không có hồ sơ nào được thiết lập thì API Aspose.PSD cho Java sẽ sử dụng các hồ sơ mặc định. Ví dụ dưới đây sử dụng các thuộc tính hồ sơ đích để thay đổi không gian màu đích cho hầu hết các JpegImage.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}

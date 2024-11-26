---
title: Chuyển đổi không gian màu cho JPEG thông qua Hồ sơ ICC
type: docs
weight: 60
url: /vi/net/chuyen-doi-khong-gian-mau-cho-jpeg-thong-qua-ho-so-icc/
---

## **Quản lý màu sắc cho định dạng JPEG**

Bài viết này bàn về việc sử dụng các hồ sơ ICC để thực hiện quản lý không gian màu khi xử lý định dạng JPEG với API Aspose.PSD. Không gian màu nội của JPEG là YCbCr tuy nhiên [định dạng](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) này cũng có thể chứa các không gian màu Grayscale, RGB, CMYK và YCCK để lưu trữ siêu dữ liệu của hình ảnh. API Aspose.PSD chủ yếu hoạt động trong không gian màu RGB do đó API phải thực hiện việc chuyển đổi giữa các không gian màu để xử lý đúng các tập tin JPEG. Chuyển đổi từ Grayscale sang RGB & YCbCr sang RGB có thể được thực hiện qua các biến đổi toán học nhưng không gian CMYK & YCCK không thể dễ dàng chuyển đổi sang không gian màu RGB.

API Aspose.PSD phải thực hiện chuyển đổi màu trực tiếp từ RGB sang CMYK cho các hình ảnh JPEG có không gian màu CMYK. Ngược lại, các hình ảnh có không gian màu YCCK yêu cầu chuyển đổi màu từ RGB sang CMYK và từ CMYK sang YCCK, trong đó chuyển đổi từ CMYK sang YCCK sử dụng quá trình [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) áp dụng cho ba kênh đầu tiên, để lại kênh k không động đến. Tóm lại, các API Aspose.PSD phải thực hiện việc chuyển đổi qua lại giữa không gian màu RGB và CMYK cho cả hình ảnh CMYK & YCCK, các biến đổi như vậy được thực hiện với sự trợ giúp của các hồ sơ ICC, đó là các bảng tra cứu mô tả thuộc tính của một màu và giúp trong việc chuyển đổi màu sắc.

## **Hồ sơ ICC**
Cơ chế chuyển đổi ICC sử dụng "Hồ sơ" mà ánh xạ không gian màu nguồn sang không gian màu CIELAB hoặc CIEXYZ không phụ thuộc vào thiết bị. Aspose.PSD có thể chuyển đổi dữ liệu vào không gian màu khi sử dụng hai không gian màu này với các hồ sơ bổ sung. Do đó, để chuyển đổi ICC, người dùng cần cung cấp hai hồ sơ - một hồ sơ RGB để đến được không gian màu CIE nội và một hồ sơ CMYK để đến được các đặc tính màu CMYK. Để thực hiện chuyển đổi từ CMYK sang RGB, người dùng cần phải hoán đổi hồ sơ, tức là; sử dụng hồ sơ CMYK làm hồ sơ nguồn và hồ sơ RGB làm hồ sơ đích.

## **Chuyển đổi màu cho JPEG thông qua Hồ sơ ICC**
API Aspose.PSD che giấu các chi tiết, cung cấp cơ chế dễ sử dụng để chỉ định hồ sơ ICC thông qua lớp [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). Hơn nữa, Aspose.PSD sử dụng các hồ sơ mẫu của SWOP, CMYK và sRGB được nhúng vào lõi nên trong hầu hết các trường hợp sử dụng phổ biến, người dùng không cần phải tìm kiếm các hồ sơ cụ thể. Tuy nhiên có một hạn chế của việc sửa đổi như vậy, đó là; chuyển đổi không gian màu như vậy không thể đảo ngược vì chúng ta không thể mong đợi cùng một màu sau chuyển đổi từ RGB sang CMYK và rồi lại từ CMYK sang RGB do không tương thích giữa các không gian màu và các hồ sơ màu khác nhau. Đoạn mã dưới đây thể hiện cách sử dụng Aspose.PSD cho API .NET để chỉ định hồ sơ màu RGB và CMYK cho hình ảnh JPEG YCCK. Trong ví dụ dưới đây, hồ sơ màu RGB và CMYK được thay đổi và hình ảnh được lưu trữ vào không gian màu YCCK. Lưu ý rằng những thuộc tính [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) và [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) này sẽ hoạt động để thay đổi dữ liệu điểm ảnh cho không gian màu YCCK. Tất cả các không gian màu khác không lấy các hồ sơ màu để cập nhật dữ liệu màu.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

Nếu không có hồ sơ được thiết lập thì API Aspose.PSD cho .NET sẽ sử dụng các hồ sơ mặc định. Ví dụ dưới đây sử dụng các thuộc tính hồ sơ đích để thay đổi không gian màu đích cho hầu hết các Hình ảnh JPEG.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}


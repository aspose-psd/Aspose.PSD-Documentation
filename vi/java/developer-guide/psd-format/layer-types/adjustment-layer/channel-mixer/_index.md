---
title: Lớp Điều chỉnh Mixer Kênh
type: docs
weight: 30
url: /vi/java/layer-types/adjustment-layer/channel-mixer/
---

# Làm việc với lớp điều chỉnh Mixer Kênh trong Photoshop bằng Java

Hôm nay, chúng ta sẽ tìm hiểu cách pha trộn màu kênh trong tài liệu Photoshop một cách chuyên nghiệp bằng Java. Vì trình chỉnh sửa Photoshop không hỗ trợ việc tạo kịch bản Java, chúng ta sẽ sử dụng thư viện Aspose.PSD dành cho Java để thao tác với định dạng tệp PSD một cách đặc biệt.

Thư viện chứa **API chuyên làm việc với các kênh màu**. Có một số cách để pha trộn màu nhưng, trong bài viết này, chúng ta sẽ tập trung vào lớp điều chỉnh Mixer Kênh.

API lớp điều chỉnh Mixer Kênh **cho phép thao tác với các kênh màu** để tạo ra ảnh tô sắc hoặc tạo ra các hiệu ứng màu sáng tạo khác nhau hoặc thậm chí chuyển đổi hình ảnh thành hình ảnh đen và trắng. Tiếp theo, chúng ta sẽ xem xét cách áp dụng lớp điều chỉnh Mixer Kênh vào tài liệu Photoshop hiện có bằng Aspose.PSD cho Java nhưng trước hết chúng ta cần thảo luận về các tính năng API tổng quan.

## Tổng quan về API

Không có gì đặc biệt trong việc tạo lớp điều chỉnh Mixer Kênh. Nó có thể được thêm vào thông qua [phương thức nhà máy mặc định](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) mà trả về một phiên bản của lớp ChannelMixerLayer. Lớp này chứa chức năng chung như tùy chọn Màu Đơn sắc và một phương thức để có được một kênh đầu ra. Một kênh đầu ra cụ thể có thể là một trong hai loại: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) hoặc [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Loại [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) phụ thuộc vào [chế độ màu](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) của hình ảnh.

## Biến ảnh thành đen trắng

Bây giờ, chúng ta hãy xem xét và ví dụ về việc áp dụng lớp điều chỉnh Mixer Kênh vào một tài liệu Photoshop hiện có. Vì loại lớp điều chỉnh này không hỗ trợ cài đặt trước, chúng ta sẽ **tái tạo cài đặt trước Đen và Trắng Hồng ngoại (RGB) của Photoshop** (a). Cài đặt trước sẽ được áp dụng vào ảnh của một cây đang nói (b). Kết quả, chúng ta muốn đạt được hiệu ứng ảnh hồng ngoại (c).

![Ví dụ về Lớp Điều chỉnh Mixer Kênh](channel-mixer-adjustment-psd-layer-figure-1.png) Đầu tiên, để tái tạo cài đặt trước Đen và Trắng Hồng ngoại (RGB) của Photoshop, cần phải bật cờ màu đơn sắc và thiết lập các giá trị thô phù hợp cho mỗi màu (đỏ, xanh lá cây và xanh dương) cho kênh đầu ra Màu Xám:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

Hình ảnh phải ở chế độ màu RGB để mã hoạt động (do ép kiểu sang lớp RgbMixerChannel). Chế độ màu CMYK cũng được hỗ trợ nhưng chỉ dành cho hình ảnh với chế độ màu tương ứng.

Hãy nhớ rằng giá trị của mỗi màu cũng như thuộc tính Constant phải nằm trong khoảng từ -200 đến 200.

## Kết luận

Trong bài viết này, chúng ta đã xem xét cách làm việc với API Điều chỉnh Mixer Kênh của Aspose.PSD cho Java để điều chỉnh màu sắc trong các kênh màu cũng như chuyển đổi hình ảnh thành hình ảnh đen và trắng.

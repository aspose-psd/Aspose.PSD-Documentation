---
title: Mở tệp PSD, PSB và AI và xuất chúng sang PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Ví dụ về xuất tệp PSD, PSB và AI sang các định dạng khác
keywords: [mở psd, mở ai, mở psb, xuất sang png, xuất sang pdf, xuất sang jpeg, xuất sang tiff, psd api, java, mẫu mã code]
url: vi/java/mo-xuat-psd-psb-ai-sang-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Tổng quan**
Để chuyển đổi các file PSD, PSB và AI sang các định dạng khác bằng Java, bạn có thể sử dụng thư viện Aspose.PSD. Dưới đây là một cái nhìn tổng quan về các bước cần thực hiện:

- Nhập các lớp và mô-đun cần thiết từ thư viện Aspose.PSD.

- Xác định các tùy chọn khác nhau cho các định dạng như PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB và PSD.

- Tạo một từ điển ánh xạ các phần mở rộng tệp với tùy chọn lưu tương ứng.

- Tải tệp PSD bằng cách sử dụng PsdImage.load() và lặp qua từ điển các định dạng để lưu hình ảnh vào từng định dạng mong muốn.

- Tương tự, tải tệp AI bằng cách sử dụng AiImage.load() và lặp qua từ điển các định dạng để lưu hình ảnh vào từng định dạng mong muốn.

Hãy đảm bảo cung cấp các đường dẫn tệp đúng cho tệp PSD và AI nguồn.
Đó là quy trình chung để chuyển đổi các tệp PSD, PSB và AI sang các định dạng khác bằng Aspose.PSD cho Java.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.java" >}}

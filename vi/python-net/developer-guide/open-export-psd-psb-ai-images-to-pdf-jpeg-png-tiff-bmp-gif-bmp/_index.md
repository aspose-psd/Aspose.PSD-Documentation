---
title: Mở tệp PSD, PSB, và AI và xuất chúng sang PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Ví dụ xuất tệp PSD, PSB, và AI sang các định dạng khác
keywords: [mở psd, mở ai, mở psb, xuất sang png, xuất sang pdf, xuất sang jpeg, xuất sang tiff, psd api, python, mã mẫu]
url: /zh/python-net/mo-xuat-psd-psb-ai-sang-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Tổng quan**
Để chuyển đổi các tệp PSD, PSB, và AI sang các định dạng khác, bạn có thể sử dụng thư viện Aspose.PSD trong Python. Thư viện này cung cấp các tùy chọn và cài đặt khác nhau để tùy chỉnh quá trình chuyển đổi.

Trước hết, bạn cần import các lớp và modules cần thiết từ thư viện Aspose.PSD. Đảm bảo bạn đã cài đặt thư viện trước khi chạy mã.

Trong mã này, chúng ta xác định các tùy chọn cho các định dạng khác nhau như PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB, và PSD. Các tùy chọn này cho phép bạn tùy chỉnh tệp đầu ra theo yêu cầu của bạn.

Tiếp theo, chúng ta xác định một từ điển "formats" ánh xạ các phần mở rộng tệp tới tùy chọn lưu tương ứng.

Để chuyển đổi một tệp PSD sang các định dạng khác, bạn cần tải tệp PSD bằng cách sử dụng PsdImage.load() và sau đó lặp qua từ điển formats. Đối với mỗi định dạng, chỉ định tên tệp đầu ra và lưu hình ảnh bằng cách sử dụng phương thức image.save().

Tương tự, để chuyển đổi một tệp AI sang các định dạng khác, tải tệp AI bằng cách sử dụng AiImage.load() và lặp qua từ điển formats. Chỉ định tên tệp đầu ra và lưu hình ảnh bằng cách sử dụng phương thức image.save().

Đảm bảo cung cấp đúng đường dẫn tệp nguồn cho tệp PSD và AI.

Đó là tất cả! Bây giờ bạn có thể sử dụng mã này để chuyển đổi các tệp PSD, PSB, và AI sang các định dạng khác bằng Aspose.PSD cho Python.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}

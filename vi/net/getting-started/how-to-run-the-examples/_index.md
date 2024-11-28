---
title: Cách Chạy Ví dụ
type: docs
weight: 90
url: /vi/net/cach-chay-vi-du/
description: Tìm hiểu cách chạy các ví dụ liên quan đến thư viện định dạng tệp PSD được lưu trữ trên GitHub.
---

## **Yêu Cầu Phần Mềm**
Vui lòng đảm bảo rằng bạn đáp ứng các yêu cầu sau trước khi tải xuống và chạy các ví dụ.

1. Visual Studio 2010 hoặc cao hơn.
1. Quản lý Gói NuGet được cài đặt trong Visual Studio. Hãy chắc chắn rằng phiên bản API NuGet mới nhất được cài đặt trong Visual Studio. Để biết thông tin chi tiết về cách cài đặt quản lý gói NuGet, vui lòng kiểm tra [http://docs.nuget.org/ndocs/guides/install-nuget](http://docs.nuget.org/ndocs/guides/install-nuget)
1. Đi đến Tools->Options->NuGet Package Manager->Package Sources và đảm bảo rằng tùy chọn **nuget.org** được chọn.
1. Dự án các ví dụ sử dụng tính năng Khôi Phục Gói Tự Động của NuGet vì vậy bạn cần phải có kết nối internet hoạt động. Nếu bạn không có kết nối internet hoạt động trên máy nơi các ví dụ sẽ được thực thi, vui lòng kiểm tra [Cài Đặt](/psd/vi/net/installation/) để thêm tham chiếu đến Aspose.Imaging.dll trong dự án ví dụ.

## **Tải từ GitHub**
Tất cả các ví dụ của Aspose.PSD cho .NET được lưu trữ trên [GitHub](https://github.com/aspose-psd/Aspose.PSD-for-.NET).

- Bạn có thể clone kho lưu trữ bằng cách sử dụng ứng dụng GitHub yêu thích hoặc tải xuống tệp ZIP từ [đây](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip).
- Giải nén nội dung của tệp ZIP vào bất kỳ thư mục nào trên máy tính của bạn. Tất cả các ví dụ được đặt trong thư mục **Examples**.
- Có một tệp giải pháp Visual Studio cho C#.
- Các dự án được tạo trong Visual Studio 2013, nhưng các tệp giải pháp tương thích với Visual Studio 2010 SP1 và cao hơn.
- Mở tệp giải pháp trong Visual Studio và xây dựng dự án.
- Khi chạy lần đầu, các phụ thuộc sẽ tự động được tải xuống qua NuGet.
- Thư mục **Data** tại thư mục gốc của **Examples** chứa các tệp đầu vào mà các ví dụ C# sử dụng. Điều quan trọng là bạn phải tải xuống thư mục **Data** cùng với dự án ví dụ.
- Mở tệp RunExamples.cs, tất cả các ví dụ được gọi từ đây.
- Gỡ bỏ dấu chú thích của các ví dụ mà bạn muốn chạy từ bên trong dự án.

Đừng ngần ngại liên hệ với chúng tôi qua Diễn Đàn nếu bạn gặp bất kỳ vấn đề nào khi cài đặt hoặc chạy các ví dụ.

## **Đóng Góp**
Nếu bạn muốn thêm hoặc cải thiện một ví dụ, chúng tôi khuyến khích bạn đóng góp vào dự án. Tất cả các ví dụ và dự án trình bày trong kho lưu trữ này là mã nguồn mở và có thể được sử dụng tự do trong ứng dụng của bạn.

Để đóng góp, bạn có thể nhánh kho lưu trữ, chỉnh sửa mã nguồn và tạo yêu cầu kéo (pull request). Chúng tôi sẽ xem xét các thay đổi và bao gồm chúng vào kho lưu trữ nếu được xem là hữu ích.

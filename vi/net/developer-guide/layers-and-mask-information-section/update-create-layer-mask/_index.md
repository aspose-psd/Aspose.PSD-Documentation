---
title: Làm việc với mặt nạ trong Aspose.PSD cho С#
weight: 100
type: docs
description: Các ví dụ về cách làm việc với Mặt nạ Cắt, Rộng và Vector trong Tệp PSD
keywords: [masks, layer mask, vector mask, clipping mask, psd, psd api, C#, csharp, code sample]
url: vi/net/update-create-layer-mask/
---

## Tổng quan

Có ba loại mặt nạ trong các tệp PSD:
1. Mặt Nạ Cắt
2. Mặt Nạ Raster
3. Mặt Nạ Vector

Bài viết này bao gồm cả ba loại.

### Mặt Nạ Cắt

Mặt nạ cắt là một tính năng mạnh mẽ trong thiết kế đồ họa và phần mềm chỉnh sửa hình ảnh cho phép bạn kiểm soát sự hiển thị của một lớp dựa trên hình dạng và nội dung của một lớp khác. Đơn giản, một mặt nạ cắt hạn chế sự hiển thị của một lớp thành hình dạng được xác định bởi một lớp khác phía dưới.

Để tạo một mặt nạ cắt, bạn cần hai lớp: lớp cơ sở và lớp cắt. Lớp cơ sở xác định hình dạng hoặc khu vực sẽ được hiển thị, trong khi lớp cắt chứa nội dung sẽ bị giới hạn vào hình dạng của lớp cơ sở.

Khi bạn áp dụng một mặt nạ cắt, nội dung của lớp cắt chỉ hiển thị trong ranh giới của lớp cơ sở. Bất kỳ nội dung ngoài các ranh giới của lớp cơ sở đều bị ẩn hoặc bị cắt đi.

Mặt nạ cắt đặc biệt hữu ích để áp dụng hiệu ứng, chẳng hạn như họa tiết hoặc mẫu, vào các khu vực cụ thể của một hình ảnh hoặc tác phẩm nghệ thuật. Bằng cách sử dụng mặt nạ cắt, bạn có thể đảm bảo rằng hiệu ứng được giới hạn trong khu vực mong muốn mà không ảnh hưởng đến phần còn lại của hình ảnh.

### Mặt Nạ Raster

Mặt nạ raster trong các tệp PSD là không thể thiếu để kiểm soát sự hiển thị của các khu vực cụ thể trong một lớp. Khác với mặt nạ vector, mà sử dụng các hình dạng toán học để xác định khu vực được mặt nạ, mặt nạ raster sử dụng thông tin dựa trên pixel để xác định phần nào của một lớp là hiển thị hoặc ẩn.

Một mặt nạ raster bao gồm một hình ảnh xám được áp dụng vào một lớp. Các khu vực màu trắng của mặt nạ đại diện cho các phần hiển thị, trong khi các khu vực màu đen đại diện cho các phần bị ẩn. Các mức xám ở giữa tạo ra tính trong suốt hoặc các khu vực semi-hiển thị.

Sử dụng mặt nạ raster, bạn có thể đạt được các hiệu ứng mặt nạ phức tạp, cho phép kiểm soát chính xác về khả năng hiển thị lớp dựa trên chi tiết cấp độ pixel. Tính năng này đặc biệt hữu ích cho các công việc yêu cầu chỉnh sửa chi tiết và kết hợp trong một hình ảnh.

### Mặt Nạ Vector

Mặt nạ vector trong các tệp PSD là một công cụ linh hoạt được sử dụng để xác định sự hiển thị của các khu vực cụ thể trong một lớp dựa trên hình dạng toán học. Khác với mặt nạ raster, mà sử dụng thông tin dựa trên pixel, mặt nạ vector sử dụng đường dẫn và đường cong để tạo ra các khu vực mặt nạ mượt mà và có khả năng co dãn.

Một mặt nạ vector về cơ bản là một đường dẫn được áp dụng vào một lớp. Hình dạng của đường dẫn xác định phần của lớp nào là hiển thị và phần nào là ẩn. Bằng cách điều chỉnh các điểm điều khiển và đường cong của đường dẫn, bạn có thể tạo ra các khu vực mặt nạ chính xác và phức tạp.

Mặt nạ vector đặc biệt hữu ích để tạo ra các mặt nạ sạch, co dãn có thể được điều chỉnh dễ dàng mà không mất chất lượng. Tính năng này lý tưởng cho các công việc yêu cầu tính chính xác cao và linh hoạt trong việc xác định các khu vực hiển thị trong một lớp.

Để biết thêm thông tin về cách thêm mặt nạ vector, vui lòng truy cập [Trang Mặt Nạ Vector](psd/vi/net/layer-vector-mask/).

## Ví dụ
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

Để biết thông tin chi tiết và ví dụ, vui lòng truy cập [Tài liệu Aspose.PSD cho C#](https://docs.aspose.com/psd/net/).

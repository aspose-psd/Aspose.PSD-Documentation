---
title: Làm việc với mặt nạ trong Aspose.PSD cho Python
weight: 100
type: docs
description: Các ví dụ về cách làm việc với Mặt nạ Cắt, Raster và Vector trong Tệp PSD
keywords: [mặt nạ, mặt nạ lớp, mặt nạ vector, mặt nạ cắt, psd, psd api, python, mẫu mã code]
url: vi/python-net/update-create-layer-mask/
---

## **Tổng quan**

**Tổng quan**

	Có 3 loại mặt nạ trong tệp PSD:
	1. Mặt nạ Cắt
	2. Mặt nạ Raster
	3. Mặt nạ Vector
	
	Bài viết này bao gồm tất cả 3 loại mặt nạ.

**Mặt nạ Cắt**

Mặt nạ cắt là một tính năng mạnh mẽ trong thiết kế đồ hoạ và phần mềm chỉnh sửa hình ảnh. Chúng cho phép bạn kiểm soát sự hiển thị của một lớp dựa trên hình dạng và nội dung của một lớp khác. Nói cách khác, một mặt nạ cắt hạn chế việc nhìn thấy của một lớp theo hình dạng của một lớp khác ở dưới.

Để tạo một mặt nạ cắt, bạn cần hai lớp: lớp cơ sở và lớp bạn muốn cắt. Lớp cơ sở xác định hình dạng hoặc khu vực sẽ được nhìn thấy, trong khi lớp bạn muốn cắt chứa nội dung sẽ bị cắt theo hình dạng của lớp cơ sở.

Khi bạn áp dụng một mặt nạ cắt, nội dung của lớp được cắt chỉ hiện thị bên trong ranh giới của lớp cơ sở. Bất kỳ nội dung nào bên ngoài ranh giới của lớp cơ sở sẽ bị ẩn hoặc bị cắt.

Mặt nạ cắt rất hữu ích khi bạn muốn áp dụng một hiệu ứng, chẳng hạn như một cấu trúc hoặc mẫu, vào một khu vực cụ thể trong một hình ảnh hoặc tác phẩm nghệ thuật. Bằng cách sử dụng một mặt nạ cắt, bạn có thể hạn chế hiệu ứng vào khu vực mong muốn mà không ảnh hưởng đến phần còn lại của hình ảnh.

Vui lòng xem ví dụ ở cuối trang

**Mặt nạ Raster**

Mặt nạ raster trong tệp PSD được sử dụng để kiểm soát sự hiển thị của các khu vực cụ thể trong một lớp. Không giống như mặt nạ vector, mà sử dụng các hình dạng toán học để xác định các khu vực bị mặt nạ, mặt nạ raster sử dụng thông tin dựa trên pixel để xác định phần nào của một lớp là nhìn thấy hoặc ẩn.

Một mặt nạ raster bao gồm một hình ảnh xám được áp dụng cho một lớp. Các khu vực màu trắng của mặt nạ đại diện cho các phần nhìn thấy, trong khi các khu vực màu đen đại diện cho các phần ẩn. Các cặp màu xám ở giữa có thể được sử dụng để tạo ra độ trong suốt một phần hoặc khu vực mờ.

Vui lòng xem ví dụ ở cuối trang

**Mặt nạ Vector**

Mặt nạ vector trong tệp PSD là một công cụ linh hoạt được sử dụng để xác định sự hiển thị của các khu vực cụ thể trong một lớp dựa trên các hình dạng toán học. Không giống như mặt nạ raster, mà sử dụng thông tin dựa trên pixel, mặt nạ vector sử dụng các đường đường cong để tạo ra các khu vực mặt nạ mềm mại và có thể thu phóng.

Một mặt nạ vector về cơ bản là một đường đường cong được áp dụng cho một lớp. Hình dạng của đường đường cong xác định phần nào của lớp là nhìn thấy và phần nào bị ẩn. Bằng cách điều khiển các điểm kiểm soát và đường cong của đường đường cong, bạn có thể tạo ra các khu vực mặt nạ chính xác và phức tạp.

Vui lòng xem [trang Mặt nạ Vector](psd/vi/net/layer-vector-mask/) để biết thông tin về việc thêm mặt nạ vector bằng cách sử dụng nguồn tài nguyên.

## **Ví dụ**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Tài liệu-Python-Aspose-psd-update-create-layer-mask.py" >}}

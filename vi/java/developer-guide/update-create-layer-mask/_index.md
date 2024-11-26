---
title: Làm việc với mặt nạ trong Aspose.PSD cho Java
weight: 100
type: docs
description: Ví dụ về cách làm việc với Mặt nạ Cắt, Mặt nạ Đa hình và Mặt nạ Vector trong Tệp PSD
keywords: [mặt nạ, mặt nạ lớp, mặt nạ vector, mặt nạ cắt, psd, api psd, java, mẫu mã code]
url: vi/java/update-create-layer-mask/
---

## **Tổng quan**

**Tổng quan**
	
	Có 3 loại mặt nạ trong các tệp PSD:
	1. Mặt nạ Cắt
	2. Mặt nạ Raster
	3. Mặt nạ Vector
	
	Bài viết này bao gồm tất cả 3 loại mặt nạ.


** Mặt nạ Cắt **

Mặt nạ cắt là một tính năng mạnh mẽ trong phần mềm thiết kế đồ họa và chỉnh sửa hình ảnh, đặc biệt là trong Java. Chúng cho phép kiểm soát chính xác việc hiển thị của một lớp dựa trên hình dạng và nội dung của một lớp khác. Về cơ bản, một mặt nạ cắt hạn chế việc hiển thị của một lớp theo hình dạng của một lớp khác nằm bên dưới nó.

Để thực hiện một mặt nạ cắt trong Java, bạn sẽ cần hai lớp: lớp cơ sở và lớp mà bạn dự định cắt. Lớp cơ sở xác định hình dạng hoặc khu vực sẽ được hiển thị, trong khi lớp được cắt chứa nội dung sẽ tuân thủ theo hình dạng của lớp cơ sở.

Khi một mặt nạ cắt được áp dụng trong Java, nội dung của lớp đã được cắt chỉ hiển thị bên trong ranh giới của lớp cơ sở. Bất kỳ nội dung nằm bên ngoài các ranh giới này sẽ được ẩn hoặc cắt bỏ.

Mặt nạ cắt chứng minh giá trị đặc biệt khi áp dụng hiệu ứng, như texture hoặc họa tiết, vào các khu vực cụ thể của một hình ảnh hoặc tác phẩm nghệ thuật. Bằng cách sử dụng một mặt nạ cắt, bạn có thể hạn chế hiệu ứng vào khu vực mong muốn mà không ảnh hưởng đến phần còn lại của hình ảnh.

Vui lòng tham khảo ví dụ ở cuối trang để hiểu rõ hơn.

** Mặt nạ Raster **

Mặt nạ raster trong các tệp Java được sử dụng để quản lý việc hiển thị của các khu vực cụ thể trong một lớp. Khác với mặt nạ vector, sử dụng các hình dạng toán học để xác định các khu vực bị che khuất, mặt nạ raster dựa vào thông tin dựa trên pixel để xác định các khu vực hiển thị hoặc ẩn.

Một mặt nạ raster bao gồm một bức ảnh xám được áp dụng vào một lớp. Các khu vực trắng trong mặt nạ biểu thị việc hiển thị, trong khi các khu vực đen đại diện cho phần bị ẩn. Các tone xám ở giữa có thể tạo ra tính trong suốt một phần hoặc các khu vực mờ.

Vui lòng tham khảo ví dụ ở cuối trang để hiểu rõ hơn.

** Mặt nạ Vector **

Mặt nạ vector trong các tệp Java là công cụ linh hoạt được sử dụng để xác định sự hiển thị của các khu vực cụ thể trong một lớp dựa trên các hình dạng toán học. Khác với mặt nạ raster, phụ thuộc vào dữ liệu dựa trên pixel, mặt nạ vector sử dụng các đường path và đường cong để tạo ra các khu vực bị che khuất mượt mà và có thể co giãn.

Mặt nạ vector về cơ bản bao gồm một đường path được áp dụng vào một lớp. Hình dạng của đường path này quyết định phần nào của lớp được hiển thị và phần nào bị ẩn. Bằng cách điều khiển các điểm kiểm soát và đường cong của đường path, bạn có thể tạo ra các khu vực bị che khuất chính xác và phức tạp.

Vui lòng tham khảo [trang Mặt nạ Vector](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) để biết thông tin về thêm mặt nạ vector bằng tài nguyên.

## **Ví dụ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-update-create-layer-mask.java" >}}

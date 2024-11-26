---
title: Chuyển đổi AI sang PNG bằng Java
weight: 100
type: docs
description: Kiểm tra cách Aspose.PSD cho Java có thể chuyển đổi Tệp AI thành PNG.
keywords: [ai sang png, định dạng ai, tệp illustrator, chuyển đổi illustrator, png, psd api, java, mẫu mã code]
url: vi/java/convert/ai-to-png
---

## **Tổng quan**
Để chuyển đổi các tệp AI sang định dạng PNG bằng Aspose.PSD cho Java, bạn có thể thực hiện các bước sau:

- Cài đặt Aspose.PSD cho Java: Bắt đầu bằng cách tải về và cài đặt thư viện Aspose.PSD cho Java. Bạn có thể bao gồm nó như một phụ thuộc trong dự án của mình bằng cách thêm nó vào cấu hình Maven hoặc Gradle của mình hoặc bằng cách bao gồm tệp JAR vào thủ công.

- Nhập các module cần thiết: Sau khi đã thêm thư viện Aspose.PSD vào dự án của bạn, hãy nhập các lớp cần thiết vào mã Java của bạn. Các lớp này bao gồm các lớp cần thiết để tải và thao tác với các tệp AI, cũng như xuất chúng sang định dạng PNG.

- Tải và Thao tác với Tệp AI: Sử dụng các lớp do Aspose.PSD cung cấp để tải các tệp AI của bạn vào ứng dụng Java của bạn. Bạn có thể sử dụng lớp Image để tải tệp AI và thao tác với nội dung của nó theo nhu cầu.

- Xuất AI sang PNG: Sau khi tải tệp AI, tạo một phiên bản của lớp PsdOptions để chỉ định các cài đặt cho việc xuất PNG. Điều này bao gồm các tham số như chất lượng hình ảnh, cấp độ nén và nhiều hơn nữa. Cấu hình các tùy chọn này theo yêu cầu của bạn.

- Lưu và Sử dụng PNG: Sau khi bạn đã cấu hình các tùy chọn xuất, sử dụng phương thức Image.Save để lưu tệp AI dưới dạng PNG. Chỉ định đường dẫn tệp mong muốn nơi bạn muốn lưu tệp PNG kết quả.

- Sử Dụng Tệp PNG: Sau khi lưu tệp PNG, bạn có thể sử dụng nó cho các mục đích khác nhau, chẳng hạn như chia sẻ, hiển thị trên một trang web, hoặc xử lý tiếp theo. Tệp PNG kết quả sẽ chứa toàn bộ nội dung từ tệp AI gốc, được chuyển đổi sang định dạng PNG.

## **Tóm tắt**
Tóm lại, bằng cách sử dụng Aspose.PSD cho Java, bạn có thể dễ dàng chuyển đổi các tệp AI sang định dạng PNG, cho phép tương thích với các ứng dụng và thiết bị khác nhau hỗ trợ PNG. Quá trình chuyển đổi bao gồm tải tệp AI, cấu hình tùy chọn xuất sử dụng [PngOptions](https://reference.aspose.com/psd/java/com.aspose.psd.imageoptions/pngoptions/) và lưu đầu ra dưới dạng tệp PNG bằng phương thức PsdImage.save. Với Aspose.PSD cho Java, bạn có thể đạt được các chuyển đổi chính xác và đáng tin cậy từ AI sang PNG một cách dễ dàng.

## **Ví dụ**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-Convert-Ai-To-Png.java" >}}

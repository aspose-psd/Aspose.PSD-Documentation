---
title: Ghi chú phiên bản Aspose.PSD CLI NLP Editor cho .NET 24.6
type: docs
weight: 90
url: /vi/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD CLI NLP Editor cho .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Khóa**    | **Tóm tắt**                                                                                  | **Danh mục**  |
|:------------|:--------------------------------------------------------------------------------------------|:--------------|
| PSDNET-2110 | Phát hành Ban đầu của các ứng dụng Aspose.PSD CLI: Aspose.PSD.CLI.Xuất và Aspose.PSD.CLI.NLP.Editor |  Cải tiến |


## **Ví dụ về việc sử dụng:**

**PSDNET-2110. Phát hành ban đầu của Ứng dụng Aspose.PSD CLI NLP Editor**

## **Sử dụng từ dòng lệnh:**

{{% alert color="primary" %}}
Trước tiên, cài đặt công cụ dotnet này:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Chúng tôi khuyên bạn nên chạy lệnh sau trước khi sử dụng lần đầu tiên:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Sau lệnh này, bạn sẽ có thể chạy ứng dụng này với tên ngắn nlp.cli thay vì Aspose.PSD.CLI.NLP.Editor. Bạn có thể chỉ định tên ngắn của riêng bạn.
{{% /alert %}}

**Các ví dụ về việc sử dụng**

1. Lệnh này sẽ chuyển đổi tệp đầu tiên được tìm thấy (Có thể mở bằng aspose.psd) từ thư mục hiện tại và lưu nó dưới định dạng png với độ trong suốt. Ngoài ra, giấy phép sẽ được thiết lập. Bạn chỉ cần chỉ định giấy phép một lần. Các lần chạy sau giấy phép sẽ được sử dụng từ đường dẫn đã chỉ định. Lệnh này sẽ hiển thị log chi tiết về xử lý NLP nếu có sẵn.
{{< highlight bash >}}nlp.cli Chuyển đổi tệp từ thư mục này sang định dạng png với độ trong suốt --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. Lệnh này tìm tệp có tên giống nhất với "smth.psd". Sau đó sẽ điều chỉnh độ tương phản và lưu thành tệp jpeg với chất lượng tốt nhất. Tên tệp xuất sẽ được in. Nó sẽ là smth.jpg.
{{< highlight bash >}}Điều chỉnh tương phản trên layer số 10 có tên ellipse trong tệp smth.psd và lưu thành output.jpg với chất lượng tốt nhất{{< /highlight >}}

3. Lệnh này sẽ xoay tệp ở đường dẫn chỉ định và giảm kích thước của nó xuống 25%. Tệp xuất sẽ được in. Nó sẽ được lưu trong thư mục hiện tại của dòng lệnh.
{{< highlight bash >}}Thay đổi kích thước tệp C:\Users\someuser\Desktop\input.psd xuống 25%{{< /highlight >}}

4. Lệnh này sẽ tìm tệp input.psd trong C:\Users\someuser\Desktop\. Sau đó, sẽ tìm layer có chỉ số 3 và điều chỉnh kích thước lên 50px chiều rộng và 100px chiều cao. Sau đó layer này sẽ được lưu dưới dạng PDF trong C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Điều chỉnh kích thước layer có chỉ số 3 của C:\Users\someuser\Desktop\input.psd thành chiều rộng 50 và chiều cao 100 và lưu vào C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. Lệnh này sẽ mở smth.psd trong thư mục hiện tại, nhưng tất cả các hiệu ứng sẽ bị vô hiệu hóa. Sau đó tệp này sẽ được chuyển đổi thành định dạng BMP và xuất ra output.bmp trong thư mục hiện tại.
{{< highlight bash >}}Mở smth.psd mà không có hiệu ứng và lưu vào output.bmp{{< /highlight >}}

**Miễn trừ trách nhiệm**

Đây là một ứng dụng thử nghiệm. Vui lòng thử nghiệm và để lại phản hồi. Mọi phản hồi sẽ được đánh giá cao. Chúng tôi muốn đưa ứng dụng Không mã vào một cấp độ mới. Mục tiêu của chúng tôi là tích hợp dễ dàng vào bất kỳ đường ống xây dựng hoặc quy trình kinh doanh nào.


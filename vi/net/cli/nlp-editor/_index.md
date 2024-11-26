---
title: Ứng Dụng Chỉnh Sửa NLP Aspose.PSD CLI cho .NET
type: tài liệu
weight: 10
url: /vi/net/cli/nlp-editor/
is_root: false
keywords: CLI, Công cụ Photoshop, NLP, Xử lý Ngôn Ngữ Tự Nhiên, PSD, Console, Thư Viện C#, API PSD
description: Ứng dụng chỉnh sửa CLI NLP dựa trên Aspose.PSD cho định dạng tệp PSD, PSB và AI. Tự động hóa CI/CD không cần mã. Hỗ trợ xử lý ngôn ngữ tự nhiên để chỉnh sửa tệp PSD. Chỉ cần viết yêu cầu của bạn bằng ngôn ngữ tự nhiên để thực hiện các hoạt động như chuyển đổi, điều chỉnh, thay đổi kích thước và nhiều hơn nữa. Không cần phải cài đặt Adobe Photoshop hoặc Adobe Illustrator và có thể chạy từ console mà không cần mã bổ sung.
---

**![Logo Sản Phẩm Aspose.PSD cho .NET](home_1.png)**

**Chào mừng đến với Ứng Dụng Chỉnh Sửa NLP Aspose.PSD CLI cho .NET**

Ứng dụng Chỉnh Sửa NLP CLI Aspose.PSD là một tiện ích console nhẹ dành cho việc chỉnh sửa các tệp PSD bằng các lệnh ngôn ngữ tự nhiên. Dễ dàng tích hợp vào các quy trình CI/CD.

**Thông báo**

Đây là một ứng dụng thử nghiệm. Vui lòng thử nghiệm và để lại phản hồi. Mọi phản hồi đều được đánh giá cao. Chúng tôi muốn đưa ứng dụng NO-Code lên một tầm cao mới. Mục tiêu của chúng tôi là dễ dàng tích hợp vào bất kỳ pipeline xây dựng hoặc quy trình kinh doanh nào.

**Chức năng chính của Ứng Dụng Chỉnh Sửa NLP Aspose.PSD CLI cho .NET**

1. Thực hiện các hoạt động trên các tệp PSD, PSB, AI bằng lệnh ngôn ngữ tự nhiên.
2. Hỗ trợ nhiều hoạt động như chuyển đổi, điều chỉnh, thay đổi kích thước và nhiều hơn nữa.
3. Tự động hóa CI/CD không cần mã.
4. Hỗ trợ viết yêu cầu bằng ngôn ngữ tự nhiên để chỉnh sửa tệp PSD.

## **Sử dụng từ dòng lệnh:**

{{% alert color="primary" %}}
Đầu tiên cài đặt công cụ dotnet này:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Chúng tôi khuyến nghị trước khi sử dụng lần đầu tiên chạy lệnh sau:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Sau lệnh này, bạn sẽ có thể chạy ứng dụng này với tên ngắn nlp.cli thay vì Aspose.PSD.CLI.NLP.Editor. Bạn có thể chỉ định tên ngắn của riêng bạn.
{{% /alert %}}

**Các tham số có sẵn cho Ứng Dụng Cắt  Aspose.PSD.CLI**

| **Đối số**     | **Mô Tả**                                   |
|:-------------|:----------------------------------------|
| bất kỳ văn bản    | Bắt buộc. Lệnh của bạn bằng ngôn ngữ tự nhiên để cập nhật Tệp PSD hoặc PSB      |
| bản quyền      | Đường dẫn đến bản quyền.                   |
| chi tiết      | Hiển thị thông tin thêm về một lệnh cụ thể. |
| setup        | Tạo tệp bat trong thư mục công cụ để gọi nhanh từ console. Ví dụ: --setup psd.nlp. Sau đó, bạn có thể gọi công cụ với lệnh psd.nlp |


**Ví dụ về cách sử dụng**

1. Lệnh này sẽ chuyển đổi tệp đầu tiên được tìm thấy (có thể mở bằng aspose.psd) từ thư mục hiện tại và sẽ lưu nó dưới định dạng png với độ trong suốt. Ngoài ra, bản quyền sẽ được thiết lập. Bạn cần chỉ định bản quyền chỉ một lần. Các lần chạy sau sẽ sử dụng bản quyền từ đường dẫn đã chỉ định. Lệnh này sẽ hiển thị thông tin chi tiết về việc xử lý NLP nếu có sẵn. 
{{< highlight bash >}}
  nlp.cli Chuyển đổi tệp từ thư mục này sang định dạng png với alpha --license "C:\Aspose\TệpGiấyPhép.lic --verbose "
{{< /highlight >}}

2. Lệnh này sẽ tìm tệp có tên gần nhất với "smth.psd". Sau đó, nó sẽ điều chỉnh độ tương phản và lưu nó thành jpeg với chất lượng tốt nhất. Tên tệp đầu ra sẽ được in ra. Nó sẽ là smth.jpg
{{< highlight bash >}}
Điều chỉnh độ tương phản trên 10 của lớp với tên elip trong tệp smth.psd và lưu nó thành output.jpg với chất lượng tốt nhất
{{< /highlight >}}

3. Lệnh này sẽ xoay tệp trên định dạng đã chỉ định và giảm kích thước của nó xuống 25%. Tệp đầu ra sẽ được in ra. Nó sẽ được lưu trong thư mục hiện tại của console.
{{< highlight bash >}}
Giảm kích thước tệp C:\Users\someuser\Desktop\input.psd xuống 25%
{{< /highlight >}}

4. Lệnh này sẽ tìm tệp input.psd trong C:\Users\someuser\Desktop\. Sau đó, nó sẽ tìm lớp có chỉ số 3 và thay đổi kích thước của nó thành chiều rộng 50px và chiều cao 100px. Sau đó, lớp này sẽ được lưu dưới dạng PDF trong C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
Thay đổi kích thước lớp có chỉ số 3 của tệp C:\Users\someuser\Desktop\input.psd thành chiều rộng 50 và chiều cao 100 và lưu nó trong C:\Users\someuser\Desktop\output.pdf
{{< /highlight >}}

5. Lệnh này sẽ mở smth.psd trong thư mục hiện tại, nhưng tất cả các hiệu ứng sẽ bị vô hiệu hóa. Sau đó, tệp này sẽ được chuyển đổi thành định dạng BMP và lưu dưới dạng output.bmp trong thư mục hiện tại.
{{< highlight bash >}}
Mở smth.psd mà không có hiệu ứng và lưu nó dưới dạng output.bmp
{{< /highlight >}}


**Vui lòng kiểm tra các [Ứng Dụng CLI Aspose.PSD](https://docs.aspose.com/psd/net/cli) cho .NET nếu bạn cần thêm hỗ trợ cho các Định dạng PSD, PSB và AI cho quy trình làm việc của bạn**

1. [Aspose.PSD CLI Chuyển đổi](/psd/vi/net/cli/convert)
2. [Aspose.PSD CLI Cắt](/psd/vi/net/cli/crop)
3. [Aspose.PSD CLI Thay đổi kích thước](/psd/vi/net/cli/resize)
4. [Aspose.PSD CLI Xuất](/psd/vi/net/cli/export)
5. [Aspose.PSD CLI Chỉnh Sửa NLP](/psd/vi/net/cli/nlp-editor)

**Vui lòng kiểm tra Aspose.PSD cho .NET hoặc [các nền tảng khác]**

Ứng dụng CLI Aspose.PSD là một giải pháp sẵn sàng cho các hoạt động phổ biến. Nếu bạn cần một giải pháp linh hoạt, vui lòng kiểm tra phiên bản đầy đủ của Aspose.PSD

1. [Aspose.PSD cho .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD cho Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD cho Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Tài Nguyên Aspose.PSD cho .NET**

Dưới đây là các liên kết đến một số tài nguyên hữu ích mà bạn có thể cần để hoàn thành các nhiệm vụ của mình.

- [Tài Liệu Trực Tuyến về Ứng Dụng CLI Aspose.PSD cho .NET](/psd/vi/net/cli/conversion)
- [Ghi Chú Phát Hành về Ứng Dụng CLI Aspose.PSD cho .NET](/psd/vi/net/cli/conversion/release-notes/)
- [Trang Sản Phẩm Ứng Dụng CLI Aspose.PSD cho .NET](https://products.aspose.com/psd/net/cli)
- [Hướng Dẫn Tham Khảo API Aspose.PSD cho .NET](https://reference.aspose.com/net/psd)
- [Tải Ví Dụ Tại Thư viện GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Diễn Đàn Hỗ Trợ Miễn Phí Aspose.PSD cho .NET](https://forum.aspose.com/c/psd)
- [Trung Tâm Trợ Giúp Hỗ Trợ Trả Phí Aspose.PSD cho .NET](https://helpdesk.aspose.com/)

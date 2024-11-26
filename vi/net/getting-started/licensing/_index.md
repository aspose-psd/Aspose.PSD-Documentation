---
title: Bản quyền
type: docs
weight: 70
url: /vi/net/licensing/
description: Đánh giá thư viện PSD Photoshop C# từ NuGet và áp dụng giấy phép bằng tập tin hoặc luồng để loại bỏ bất kỳ hạn chế nào từ bản đánh giá đã cài đặt.
---

## **Hạn chế phiên bản Đánh giá**
Bạn có thể tải phiên bản đánh giá của Aspose.PSD cho .NET từ [NuGet](https://www.nuget.org/packages/Aspose.psd/). Phiên bản đánh giá cung cấp các tính năng giống như phiên bản có bản quyền đầy đủ của thành phần với một số hạn chế. Khi bạn mua Aspose.PSD, việc áp dụng giấy phép sẽ loại bỏ bất kỳ hạn chế nào từ bản đánh giá đã cài đặt. Phiên bản đánh giá Aspose.PSD cho .NET cung cấp đầy đủ chức năng sản phẩm, chỉ có hai hạn chế:

- **Một dấu nước trên mỗi hình ảnh**: Bất kỳ hình ảnh bạn lưu, chỉnh sửa hoặc xuất có một dấu nước đọc "Chỉ Đánh Giá. Được tạo với Aspose.PSD. Bản quyền 2010-2018 Aspose Pty Ltd.". Hình ảnh nhỏ, mà không phù hợp với dấu nước đầy đủ, có hai đường chéo trên hình ảnh thay vì.
- **Không hỗ trợ chức năng vẽ cốt lõi**: Trong chế độ đánh giá, các pixel hình ảnh không thể được tải hoặc lưu vào hình ảnh. Để vẽ hình ảnh, hãy sử dụng chức năng vẽ tiên tiến thay vì. Hạn chế này ảnh hưởng đến chức năng phụ thuộc vào chức năng vẽ cốt lõi. Aspose.PSD cho .NET cho phép bạn đăng ký định dạng tệp của riêng bạn. Tuy nhiên, tính năng này phụ thuộc vào chức năng vẽ cốt lõi nên không có ý nghĩa sử dụng nó trong chế độ đánh giá vì bạn không thể thay đổi nội dung của những tệp đó.

Nếu bạn muốn kiểm tra Aspose.PSD cho .NET mà không gặp các hạn chế đánh giá, yêu cầu một giấy phép tạm thời 30 ngày. Vui lòng tham khảo [Cách nhận Giấy phép Tạm thời?](https://purchase.aspose.com/temporary-license) để biết thêm thông tin.
## **Về Tập Tin Giấy Phép**
Sau khi bạn hài lòng với đánh giá của Aspose.PSD, bạn có thể mua giấy phép trên [trang web của Aspose](https://purchase.aspose.com/default.aspx). Làm quen với các loại đăng ký khác nhau được cung cấp. Nếu bạn có bất kỳ câu hỏi nào, đừng ngần ngại liên hệ với [đội ngũ bán hàng của Aspose](https://company.aspose.com/contact). Mỗi giấy phép Aspose đi kèm với một đăng ký một năm cho các cập nhật phần mềm. Sau năm đầu tiên, hãy gia hạn đăng ký của bạn để tiếp tục nhận những tính năng và sửa lỗi mới nhất. Hỗ trợ kỹ thuật là miễn phí và không giới hạn và được cung cấp cho cả người dùng đã mua và đánh giá thông qua [Diễn đàn Hỗ trợ](https://forum.aspose.com/). Giấy phép là một tập tin XML chứa các thông tin như tên sản phẩm, số lượng nhà phát triển được cấp phép, ngày hết hạn đăng ký và một số thông tin khác. Tập tin được ký số, vì vậy đừng chỉnh sửa nó: thậm chí thêm một dòng ngắt hàng thừa cũng làm cho tập tin trở nên không hợp lệ. Sau khi mua Aspose.PSD, bạn cần áp dụng giấy phép trước khi tạo, chỉnh sửa hoặc xử lý hình ảnh. Nếu bạn quên áp dụng giấy phép, bất kỳ hình ảnh đầu ra nào sẽ có dấu nước đánh giá. Bạn chỉ cần cài đặt giấy phép một lần cho mỗi ứng dụng hoặc quy trình mà bạn phát triển.
## **Nơi Áp Dụng Giấy Phép trong Ứng Dụng của Bạn**
Nơi bạn áp dụng giấy phép phụ thuộc vào loại ứng dụng bạn đang phát triển. Hãy tuân thủ những quy tắc đơn giản sau:

- Chỉ áp dụng giấy phép một lần cho mỗi miền ứng dụng. Gọi License.SetLicense nhiều lần không gây hại nhưng lãng phí thời gian xử lý.
- Áp dụng giấy phép trước khi gọi bất kỳ lớp nào Aspose.PSD cho .NET.
- **Ứng dụng Windows Forms hoặc Console**: gọi License.SetLicense trong mã khởi động, trước khi sử dụng bất kỳ lớp Aspose.PSD cho .NET nào.
- **Ứng dụng ASP.NET**: gọi License.SetLicense từ tệp Global.asax.cs (Global.asax.vb), trong phương thức bảo vệ Application_Start. Điều này sẽ gọi một lần khi ứng dụng bắt đầu. Đừng gọi License.SetLicense từ trong phương thức Page_Load hoặc giấy phép sẽ được tải mỗi khi một trang web được tải.
- **Ứng dụng Silverlight**: gọi License.SetLicense từ sự kiện Application_Startup trong tập tin App.xaml.cs (App.xaml.vb).
- **Thư viện lớp**: gọi License.SetLicense từ một bản sao tĩnh của lớp sử dụng Aspose.PSD. Hàm tạo tĩnh thực thi trước khi một phiên bản của lớp của bạn được tạo, đảm bảo rằng giấy phép Aspose.PSD được thiết lập đúng cách.
## **Áp Dụng Giấy Phép**
Bạn có thể dễ dàng tải phiên bản đánh giá của Aspose.PSD từ trang tải về của NuGet [trang tải về](https://www.nuget.org/packages/Aspose.psd/). Phiên bản đánh giá cung cấp hoàn toàn các khả năng giống như phiên bản đủ giấy phép của Aspose.PSD. Hơn nữa, phiên bản đánh giá đơn giản trở thành có bản quyền khi bạn mua một giấy phép và thêm vài dòng mã để áp dụng giấy phép.
### **Sử dụng Tập Tin hoặc Luồng**
Nếu bạn muốn tránh làm việc với hạn chế đánh giá, bạn cần thiết lập một giấy phép trước khi sử dụng Aspose.PSD. Bạn chỉ cần thiết lập giấy phép một lần cho mỗi ứng dụng (hoặc quy trình).
### **Áp dụng giấy phép từ tập tin**
Cách dễ nhất để áp dụng giấy phép là đặt tệp giấy phép trong cùng một thư mục như Aspose.PSD.dll. Sau đó, bạn có thể chỉ định tên tệp trong mã thay vì đường dẫn đầy đủ.



{{< highlight java >}}

// Tạo một phiên laricense và áp dụng giấy phép bằng một đường dẫn đầy đủ

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Khi bạn gọi phương thức SetLicense, tên giấy phép phải giống với tên tệp giấy phép của bạn. Ví dụ, nếu bạn đổi tên tệp giấy phép thành "Aspose.PSD.lic.xml" bạn nên sử dụng tên giấy phép này cho phương thức SetLicense.
### **Áp dụng giấy phép sử dụng một luồng**
Cũng có thể tải một giấy phép từ một luồng như dưới đây.



{{< highlight java >}}



// Tạo một phiên laricense và áp dụng giấy phép bằng một luồng

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);



{{< /highlight >}}
### **Kiểm tra trạng thái giấy phép**
Lớp Aspose.PSD.License có thuộc tính IsLicensed sẽ trả về true nếu giấy phép đã được thiết lập đúng cách.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Đã thiết lập Giấy phép!");

}

{{< /highlight >}}
### **Sử dụng Một Tài Nguyên Nhúng**
Một cách thực tế để đóng gói giấy phép với ứng dụng của bạn và đảm bảo nó không bị mất là bao gồm nó như một tài nguyên nhúng vào một trong các tập hợp gọi Aspose.PSD. Để bao gồm tệp giấy phép như một tài nguyên nhúng:

1. Trong Visual Studio .NET, nhấn vào **Tệp** và chọn **Thêm Mục Tồn Tại**.
1. Bao gồm tệp giấy phép (phần mở rộng .lic) vào dự án.
1. Chọn tệp trong Trình Duyệt Giải Pháp.
1. Trong cửa sổ Thuộc tính, đặt **Hành động Xây dựng** thành **Tài nguyên Nhúng**.

Không cần thiết phải gọi GetExecutingAssembly hoặc GetManifestResourceStream của hệ thống.Reflection. Lớp.Assembly trong Microsoft .NET Framework để truy cập giấy phép nhúng. Thay vào đó, nhúng tệp như một tài nguyên trong dự án và sau đó chuyển tên tệp giấy phép cho phương thức SetLicense. Lớp License tự động tìm tệp giấy phép trong tài nguyên nhúng. Ví dụ dưới đây cho thấy cách bao gồm giấy phép như một tài nguyên nhúng và áp dụng nó vào ứng dụng của bạn.



{{< highlight java >}}

// Tạo một lớp Giấy phép

Aspose.PSD.License license = new Aspose.PSD.License();



// Chuyển tên của tệp giấy phép nhúng

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Kiểm tra trạng thái giấy phép**
Lớp Aspose.PSD.License có thuộc tính IsLicensed sẽ trả về true nếu giấy phép đã được thiết lập đúng cách.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Đã thiết lập Giấy phép!");

}

{{< /highlight >}}

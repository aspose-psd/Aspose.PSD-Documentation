---
title: Giấy phép đo lường
type: tài liệu
weight: 80
url: /vi/net/metered-licensing/
description: Thư viện C# Photoshop PSD cho phép các nhà phát triển áp dụng khóa đo lường là cơ chế cấp phép mới và sẽ được sử dụng cùng với phương pháp cấp phép hiện có.
---

{{% alert color="primary" %}}

Aspose.PSD cho phép các nhà phát triển áp dụng khóa đo lường. Đó là một cơ chế cấp phép mới. Cơ chế cấp phép mới sẽ được sử dụng cùng với phương pháp cấp phép hiện có. Những khách hàng muốn được tính phí dựa trên việc sử dụng các tính năng của API có thể sử dụng giấy phép đo lường. Để biết thêm chi tiết, vui lòng tham khảo phần [Câu hỏi thường gặp về Giấy phép Đo lường](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}
## **Giấy phép đo lường**
Dưới đây là các bước đơn giản để sử dụng lớp Metered.

1. Tạo một phiên bản của lớp Metered.
1. Truyền khóa công khai và khóa riêng tư vào phương thức setMeteredKey.
1. Thực hiện xử lý (thực hiện nhiệm vụ).
1. Gọi phương thức getConsumptionQuantity của lớp Metered.
1. Nó sẽ trả về lượng/yêu cầu API mà bạn đã tiêu thụ cho đến nay.

Dưới đây là đoạn mã mẫu minh họa cách thiết lập khóa công khai và khóa riêng tư.

{{< highlight java >}}

// Tạo một phiên bản của lớp PSD Metered

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Truy cập thuộc tính setMeteredKey và truyền khóa công khai và khóa riêng tư làm tham số

metered.SetMeteredKey("*****", "*****");



// Lấy lượng dữ liệu đo lường trước khi gọi API

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// Hiển thị thông tin

Console.WriteLine("Số lượng Tiêu Thụ Trước: " + amountbefore.ToString());

// Lấy lượng dữ liệu đo lường sau khi gọi API

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// Hiển thị thông tin

Console.WriteLine("Số lượng Tiêu Thụ Sau: " + amountafter.ToString());

{{< /highlight >}}

---
title: Làm việc với Layer
type: tài liệu
weight: 150
url: /vi/net/working-with-layers/
---

## **Tạo một Nhóm Layer**
Một nhóm layer bao gồm một hoặc nhiều layer và giúp tổ chức các layer tương tự hoặc liên quan. Sử dụng Aspose.PSD cho .NET bạn có thể tạo một nhóm layer. Để thực hiện điều này, một phương thức mới [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) đã được thêm vào trong class **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** để thêm nhóm layer.

Các bước để tạo nhóm layer đơn giản như sau:

- Tạo một phiên bản hình ảnh bằng cách sử dụng class PsdImage với chiều rộng, chiều cao và tùy chọn hình ảnh cụ thể.
- Tạo một [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) với tên nhóm và chỉ mục cụ thể.
- Tạo một phiên bản của class Layer và gán hình ảnh PSD cho nó.
- Thêm layer đã tạo vào nhóm layer bằng cách sử dụng phương thức AddLayer được tiết lộ bởi class LayerGroup.
- Lưu kết quả.

Đoạn mã sau cho bạn biết cách tạo một nhóm layer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}

## **Đổi tên Layer**
Bạn có thể sử dụng bất kỳ tên nào bạn muốn, nhưng thực hành thông thường là sử dụng một mô tả chung về đối tượng hoặc phần tử đang ở trên layer đó. Bài viết này thể hiện cách bạn có thể đổi tên của một layer bằng cách sử dụng Aspose.PSD cho .NET. Để thực hiện điều này, một thuộc tính mới [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) đã được thêm vào trong class Layer để hiển thị tên layer đúng cách. Đã được quan sát rằng khi Photoshop lưu một tên layer bằng cách sử dụng thuộc tính [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), thì các ký tự Hàn Quốc được lưu trữ dưới dạng byte 63'?' trong ASCII. Vì vậy, nếu bạn muốn hiển thị tên layer đúng cách thì hãy sử dụng thuộc tính **DisplayName** vì thuộc tính **Name** không hỗ trợ các ký tự Hàn.

Đoạn mã mẫu sau cho thấy cách bạn có thể đổi tên của một layer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **Hỗ trợ của Linked Layers**
Liên kết các layer tương tự như việc nhóm các layer. Nếu bạn liên kết hai hoặc nhiều layer thì nó sẽ cho phép bạn thực hiện một số thay đổi cho tất cả các layer được liên kết. Ví dụ, nếu bạn áp dụng các biến đổi cho một layer thì nó sẽ được áp dụng cho tất cả các layer khác được liên kết. Bài viết này thể hiện cách bạn có thể lấy và hủy liên kết giữa các layer bằng cách sử dụng [Aspose.PSD](https://products.aspose.com/psd).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}


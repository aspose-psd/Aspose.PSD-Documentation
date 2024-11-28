---
title: Mặt nạ Vector Layer
type: docs
weight: 10
url: /vi/net/layer-vector-mask/
---

## **Tổng quan về Mặt nạ Vector Layer**
Một mặt nạ vector là một đường dẫn không phụ thuộc vào độ phân giải cắt ra nội dung của lớp. Mặt nạ vector thường chính xác hơn so với mặt nạ được tạo bằng các công cụ dựa trên pixel. Bạn tạo mặt nạ vector bằng cách sử dụng công cụ bút hoặc hình dạng.

Aspose.PSD hỗ trợ hiển thị và áp dụng mặt nạ vector. Bạn có thể chỉnh sửa mặt nạ vector thông qua việc chỉnh sửa của Vector Paths.
## **Đường vector trong Aspose.PSD**
Truy cập vào các đường vector trong Aspose.PSD được cung cấp thông qua [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) và [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) resources là các lớp con của [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:image_alt_text](layer-vector-mask_0.png)

## **Làm thế nào để chỉnh sửa một đường vector?**
### **Cấu trúc đường vector**
Cấu trúc cơ bản để chỉnh sửa đường là [VectorPathRecord.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord) Nhưng với sự tiện lợi của bạn, giải pháp sau được đề xuất.

Để dễ dàng chỉnh sửa các đường vector, bạn nên sử dụng lớp [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), chứa các phương thức để chỉnh sửa dữ liệu vector một cách thoải mái trong tài nguyên được kế thừa từ VectorPathDataResource

Bắt đầu với việc tạo một đối tượng kiểu VectorPath.

Để thuận tiện, bạn có thể sử dụng phương thức tĩnh [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), nó sẽ tìm một tài nguyên vector trong lớp đầu vào và tạo một đối tượng VectorPath dựa trên nó.

Sau tất cả các chỉnh sửa, bạn có thể áp dụng đối tượng VectorPath với các thay đổi trở lại lớp bằng cách sử dụng phương thức tĩnh [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

Kiểu VectorPath chứa một danh sách các phần tử [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) và mô tả một hình ảnh vector hoàn chỉnh có thể bao gồm một hoặc nhiều hình dạng.

![todo:image_alt_text](layer-vector-mask_1.png)



Mỗi PathShape là một hình vẽ vector bao gồm một bộ các nút bezier (điểm) riêng lẻ.

Nút là đối tượng kiểu [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) thực chất là các điểm từ đó hình dạng được xây dựng.

![todo:image_alt_text](layer-vector-mask_2.png)

Ví dụ mã sau cho thấy cách truy cập vào một hình và các điểm.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **Làm thế nào để tạo một hình dạng?**
Để chỉnh sửa một hình dạng, bạn cần lấy một hình dạng hiện có từ danh sách [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), hoặc thêm một hình dạng mới bằng cách tạo một thể hiện [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) và thêm nó vào danh sách [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **Làm thế nào để thêm nút (điểm)?**
Bạn có thể điều chỉnh các điểm của hình dạng như các phần tử của một danh sách thông thường sử dụng thuộc tính PathShape.Points, ví dụ, bạn có thể thêm các điểm hình dạng:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}



BezierKnot chứa Điểm gốc và hai Điểm điều khiển.

![todo:image_alt_text](layer-vector-mask_3.png)

Nếu điểm gốc và các điểm điều khiển có cùng giá trị, thì nút đó sẽ có một góc nhọn.

Để thay đổi vị trí điểm gốc cùng với các điểm điều khiển (tương tự như cách diễn ra trong Photoshop), BezierKnot có một phương thức Shift.

Ví dụ mã sau minh họa cách di chuyển toàn bộ nút bezier dọc lên theo tọa độ Y:

Bạn có thể điều chỉnh các điểm của hình dạng như các phần tử của một danh sách thông thường sử dụng thuộc tính PathShape.Points, ví dụ, bạn có thể thêm các điểm hình dạng:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}


## **Thuộc tính PathShape**
Chỉnh sửa PathShape không chỉ giới hạn ở việc chỉnh sửa nút, kiểu này cũng có các thuộc tính khác.
### **PathOperations (Các phép toán Boolean)**
Thuộc tính [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) là một phép toán boolean, việc thay đổi giá trị của nó xác định cách các hình dạng nhiều đã được kết hợp.

Có các giá trị có thể có sau:

- 0 = ExcludeOverlappingShapes (Phép XOR).
- 1 = CombineShapes (Phép OR).
- 2 = SubtractFrontShape (Phép NOT).
- 3 = IntersectShapeAreas (Phép AND).

![todo:image_alt_text](layer-vector-mask_4.png)
### **Thuộc tính IsClosed**
Ngoài ra, bằng cách sử dụng thuộc tính PathShape.IsClosed, chúng ta có thể xác định xem nút đầu tiên và cuối cùng của một hình dạng có được kết nối hay không.

|**Hình dạng Đóng**|**Hình dạng Mở**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **Thuộc tính FillColor**
Không có hình dạng nào có màu sắc riêng, vì vậy bạn có thể thay đổi màu sắc của toàn bộ đường vector với thuộc tính VectorPath.FillColor.

Bạn có thể điều chỉnh các điểm của hình dạng như các phần tử của một danh sách thông thường sử dụng thuộc tính PathShape.Points, ví dụ, bạn có thể thêm các điểm hình dạng:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}


## **Tại đây bạn sẽ tìm thấy mã nguồn của VectorDataProvider và các lớp liên quan:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}

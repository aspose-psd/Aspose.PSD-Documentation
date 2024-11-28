---
title: Cách tạo máy tạo hình thu nhỏ YouTube tự động bằng Java
type: docs
weight: 10
url: /vi/java/cach-tao-may-tao-hinh-thu-nho-youtube-tu-dong-bang-java/
---

## **Giới thiệu**
Mục đích của tài liệu này là để thể hiện cách sử dụng API của một số công cụ phức hợp của [Aspose.PSD cho Java](https://products.aspose.com/psd/java) trên một ví dụ thực tế. Trong bài viết này, **một chương trình Java đơn giản tạo ra hình thu nhỏ của YouTube** cho kênh [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q) sẽ được viết và giải thích. Kênh này được chọn từ thế giới thực vì hình thu nhỏ của nó khá tiêu chuẩn và chúng minh họa cách sử dụng một số công cụ phức hợp phổ biến của Aspose.PSD cho Java (ví dụ như hiệu ứng bóng đổ, điền gradient theo hình tròn, vẽ văn bản và hình dạng):

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **Cách hoạt động một cách đơn giản**
Một chương trình Java đơn giản nhận vào hai đối số: một chú thích và một hình ảnh. Một **tài liệu Photoshop (PSD) tạm thời được tạo ra** từ đầu vào bằng Aspose.PSD cho Java. Sau đó, chương trình **chuyển tài liệu từ PSD sang định dạng tệp PNG** để có được hình thu nhỏ YouTube với kích thước 1280x720 pixel. Hình ảnh đầu ra có vẻ giống như sau:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **Yêu cầu kỹ thuật**
Các công nghệ sau đây cần thiết để thành công khi chạy mã của bài viết này:

- Java 6+
- [Aspose.PSD cho Java](/psd/vi/java/installation/) (mới nhất)

## **Bắt đầu**
Như đã được đề cập, chương trình sử dụng PSD tạm thời để tạo ra hình thu nhỏ. Vì vậy, hãy **tạo một tài liệu PSD**, để bắt đầu:

PsdImage psdImage = new PsdImage(1280, 720);

Nếu bạn nhìn kỹ hơn vào hình thu nhỏ của YouTube ở trên, bạn có thể nhận thấy rằng **nó bao gồm một số thành phần**:

1. một hình ảnh nền (được in mask)
2. một gradient radial psd (nhấn mạnh khu vực ở góc trên bên phải)
3. một logo với hiệu ứng bóng đổ
4. một chú thích và một hình vẽ đơn giản (hình chữ nhật màu xanh)

Hãy thâm nhập sâu hơn để xem cách triển khai từng thành phần này bằng Aspose.PSD cho Java trong các phần tiếp theo.

## **1. Thêm hình ảnh nền**
Thứ tự của các lớp là quan trọng. Do đó, hình ảnh nền phải được thêm trước để không chồng lấp các lớp khác. Hãy chú ý rằng chỉ [các định dạng tệp raster được hỗ trợ](/psd/vi/java/supported-file-formats/) vào thời điểm hiện tại.
### **1.1. Thêm hình ảnh nền vào một lớp Photoshop**
Để **thêm một hình ảnh raster vào PSD**, một luồng đầu vào phải được truyền làm đối số trong quá trình xây dựng lớp (xem thêm [ví dụ về việc tải hình ảnh raster](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):

```java
// Mã ví dụ
```

1.2. Điều chỉnh hình ảnh nền phù hợp với bảng

Hai hành động sau đây (thay đổi kích thước, vị trí) hữu ích cho những trường hợp khi **kích thước hình ảnh khác với kích thước bảng**, mặc dù hình ảnh trong bài viết này có cùng kích thước với bảng (cho rằng thường không phải lúc nào cũng như vậy).

Đảm bảo hình ảnh đã tải **thích hợp** với **kích thước bảng** (xem thêm [ví dụ về việc thay đổi kích thước](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

```java
// Mã ví dụ
```

Sau khi thay đổi kích thước, vị trí của hình ảnh thay đổi. Do đó, để **đặt lại vị trí của hình ảnh**, di chuyển hình ảnh đã thay đổi kích thước đến góc trên bên trái:

```java
// Mã ví dụ
```

## **2. Thêm gradient theo hình tròn**
Có **hai cách thêm gradient theo hình tròn**, sử dụng:

- một [hiệu ứng lớp lớp gradient overlay](/psd/vi/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) trên một lớp hiện có (hiệu ứng gradient kết nối với lớp hiện tại và áp dụng cho nội dung của nó)
- một lớp [gradient fill layer mới](/psd/vi/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) (một lớp riêng biệt giữ cấu hình độ dốc độc lập của gradient)

Đủ để sử dụng hiệu ứng lớp gradient overlay cho ví dụ này. Tuy nhiên, để làm cho bài viết này thú vị và hữu ích hơn **lớp gradient fill layer được sử dụng** vì tất cả các hiệu ứng lớp áp dụng theo cách tương tự và một hiệu ứng lớp khác sẽ được sử dụng trong phần tiếp theo.
### **2.1. Thêm lớp gradient fill layer theo hình tròn**
Quá trình thêm một lớp gradient fill layer mới bao gồm 2 bước sau:

\1. Cần **khai báo cài đặt gradient fill** vì không có cài đặt mặc định. Cấu hình tối thiểu cần thiết có vẻ như sau (nghĩa là loại gradient, tỷ lệ, điểm màu sắc và độ trong suốt là các thuộc tính bắt buộc):

```java
// Mã ví dụ
```

Cấu hình trên định nghĩa một gradient theo hình tròn trong suốt ở các rìa và màu xanh đậm ở trung tâm. Vị trí gradient ở giữa bảng mặc định.

Để đảo ngược gradient fill và dịch nó hơi đến góc trên bên phải sử dụng các thuộc tính tùy chọn tương ứng:

```java
// Mã ví dụ
```

\2. Khi cài đặt đã hoàn thành, thêm một lớp gradient fill cùng với cài đặt của nó vào trong PSD:

```java
// Mã ví dụ
```

## **Thêm logo với bóng đổ**
**Bóng đổ** là một hiệu ứng cho phép thêm bóng đổ tùy chỉnh theo đường viền của đối tượng (hình ảnh, văn bản v.v.).
### **3.1. Thêm một logo vào lớp Photoshop**
Cách tiếp cận giống như ở phần 1.1. có thể được sử dụng để **thêm một logo vào PSD**:

```java
// Mã ví dụ
```

### **3.2. Đặt vị trí của logo**
Hình ảnh đã tải gần như dính vào góc trên bên trái mặc định. Tuy nhiên, một số **viền cần được thêm** để giống với hình thu nhỏ YouTube ban đầu trên kênh. Vì vậy, vị trí hình ảnh cần được dời ra xa khỏi các rìa của lớp:

```java
// Mã ví dụ
```

### **3.3. Thêm hiệu ứng bóng đổ vào logo**
Logo có thể trở nên mờ nếu sử dụng một hình ảnh nền sáng. Do đó, nên **thêm hiệu ứng bóng đổ** vào logo thông qua thuộc tính tùy chọn blending options (xem thêm [ví dụ về tạo bóng đổ](/psd/vi/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)):

```java
// Mã ví dụ
```

Hiệu ứng bóng đổ không có các thuộc tính cần thiết vì cấu hình mặc định (nó giống như của Photoshop). Tuy nhiên, bóng đổ trên đã được chỉnh sửa để trở thành một viền trong suốt bị mờ vào các rìa.

## **4. Thêm văn bản và hình dạng vẽ**
### **3.1. Tạo một lớp đồ họa**
Vẽ không được hỗ trợ trực tiếp bởi một lớp thông thường. Do đó, bộ máy đồ họa được sử dụng cạnh lớp để **cung cấp một API cho việc vẽ** (xem thêm [ví dụ về việc vẽ](/psd/vi/java/drawing-images-using-graphics/)):

```java
Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
```

### **3.2. Vẽ văn bản nhiều dòng**
Một độc giả sành sỏi có thể hỏi: tại sao không sử dụng một lớp văn bản để thêm văn bản? Có một vài lý do: chỉnh sửa văn bản không yêu cầu trong trường hợp này vì PSD được tạo ra lại từ đầu mỗi lần; tùy chỉnh phông chữ chưa được hỗ trợ bởi [API văn bản](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) (v20.6 tại thời điểm viết). 

Dễ dàng **vẽ một số văn bản với font tùy chỉnh** chỉ cần khởi tạo một font mong muốn và gọi phương thức tương ứng từ bộ máy đồ họa. Tuy nhiên, để tạo ra một hình chữ nhật (xem chi tiết trong phần tiếp theo) thay đổi chiều cao tự động dựa vào số dòng văn bản là khó. Chiều cao chính xác của tất cả dòng cần được tính toán trước:

```java
// Mã ví dụ
```

Số 1,15 là độ cao dòng, 3 là lề văn bản.

### **3.3. Vẽ một hình chữ nhật**
Một hình chữ nhật cũng dễ vẽ thậm chí với một cọ gradient (chỉ cần đặt một khu vực để vẽ và một dải màu). Khi chiều cao của văn bản đã biết thì kích cỡ và vị trí của hình chữ nhật được tính toán. Để **vẽ một hình chữ nhật được tô màu** **trong psd** (không chỉ một khung) gọi phương thức tương ứng từ bộ máy đồ họa với tất cả những thứ đó:

```java
// Mã ví dụ
```

` `Where 40, 15, 25 là khoảng cách.

## **Kết quả**
Vậy, việc tạo hình thu nhỏ đã hoàn tất. Vì vậy, đến lúc **xuất hình thu nhỏ sang định dạng tệp raster** (ví dụ, PNG) để phân phối tiếp theo:

```java
// Mã ví dụ
```

## **Kết luận**
Trong bài viết này, chúng ta đã tạo ra một máy tạo hình thu nhỏ YouTube cho kênh DW Documentary và giải thích cách sử dụng một số công cụ phức hợp phổ biến như hiệu ứng bóng đổ, điền gradient theo hình tròn, vẽ văn bản và hình dạng.

## **Ví dụ đầy đủ**
Bạn có thể [tải xuống Aspose.PSD SDK](https://products.aspose.com/psd/net)

```java
// Mã ví dụ
```

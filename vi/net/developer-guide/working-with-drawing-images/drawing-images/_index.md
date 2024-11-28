---
title: Vẽ Hình Ảnh
type: docs
weight: 10
url: /vi/net/drawing-images/
---

## **Vẽ Đường Thẳng**
Ví dụ này sử dụng lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) để vẽ các hình dạng đường thẳng trên bề mặt Ảnh. Để minh họa hoạt động, ví dụ tạo một Ảnh mới và vẽ các đường thẳng trên bề mặt Ảnh bằng phương thức [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) được công bố bởi lớp Graphics. Đầu tiên, chúng ta sẽ tạo một PsdImage chỉ định độ cao và độ rộng.

Khi ảnh đã được tạo, chúng ta sẽ sử dụng phương thức Clear được công bố bởi lớp Graphics để thiết lập màu nền của nó. Phương thức [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) của lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) được sử dụng để vẽ một đường thẳng trên một ảnh kết nối hai cấu trúc điểm. Phương thức này có một số phiên bản chấp nhận thể hiện của lớp Pen và cặp tọa độ điểm hoặc cấu trúc Point/PointF làm đối số. Lớp Pen định nghĩa một đối tượng được sử dụng để vẽ đường thẳng, đường cong và hình. Lớp Pen có một số hàm tạo nạp quá tải để vẽ đường thẳng với màu, độ rộng và bút được chỉ định. Lớp SolidBrush được sử dụng để vẽ liên tục với màu cụ thể. Cuối cùng, ảnh được xuất sang định dạng tập tin bmp. Đoạn mã sau cho bạn thấy cách vẽ các hình dạng đường thẳng trên bề mặt Ảnh.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}
## **Vẽ Hình Elip**
Ví dụ vẽ hình elip là bài viết thứ hai trong loạt các hình dạng vẽ. Chúng ta sẽ sử dụng lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) để vẽ hình elip trên bề mặt Ảnh. Để minh họa hoạt động, ví dụ tạo một Ảnh mới và vẽ hình dạng elip trên bề mặt Ảnh bằng phương thức DrawEllipse được công bố bởi lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Đầu tiên, chúng ta sẽ tạo một PsdImage chỉ định độ cao và độ rộng.

Sau khi tạo ảnh, chúng ta sẽ tạo và khởi tạo đối tượng lớp Graphics và thiết lập màu nền ảnh bằng cách sử dụng phương thức Clear của lớp Graphics. Phương thức DrawEllipse của lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) được sử dụng để vẽ hình dạng elip trên bề mặt ảnh được chỉ định bởi cấu trúc hình chữ nhật giới hạn. Phương thức này có một số phiên bản chấp nhận các thể hiện của lớp Pen và Rectangle/RectangleF hoặc một cặp tọa độ, chiều cao và chiều rộng làm đối số. Lớp Pen định nghĩa một đối tượng được sử dụng để vẽ đường thẳng, đường cong và hình dạng. Lớp Pen có một số hàm tạo nạp quá tải để vẽ đường thẳng với màu, độ rộng & bút được chỉ định. Lớp Rectangle lưu trữ một tập hợp bốn số nguyên đại diện cho vị trí và kích thước của một hình chữ nhật. Lớp Rectangle có một số hàm tạo nạp quá tải để vẽ cấu trúc hình chữ nhật với kích thước và vị trí được chỉ định. Lớp SolidBrush được sử dụng để vẽ liên tục với màu cụ thể. Cuối cùng, ảnh được xuất sang định dạng tập tin bmp. Đoạn mã sau cho bạn thấy cách vẽ hình dạng elip trên bề mặt Ảnh.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}
## **Vẽ Hình Chữ Nhật**
Trong ví dụ này, chúng ta sẽ vẽ hình dạng hình chữ nhật trên bề mặt Ảnh. Để minh họa hoạt động, ví dụ tạo một Ảnh mới và vẽ hình dạng hình chữ nhật trên bề mặt Ảnh bằng phương thức DrawRectangle được công bố bởi lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Đầu tiên, chúng ta sẽ tạo một PsdImage chỉ định độ cao và độ rộng. Sau đó, chúng ta sẽ thiết lập màu nền của Ảnh bằng cách sử dụng phương thức Clear của lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).

Phương thức DrawRectangle của lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) được sử dụng để vẽ hình dạng hình chữ nhật trên bề mặt ảnh được chỉ định bởi cấu trúc hình chữ nhật. Phương thức này có một số phiên bản chấp nhận các thể hiện của lớp Pen và Rectangle/RectangleF hoặc cặp tọa độ, một chiều rộng và chiều cao làm đối số. Lớp Rectangle lưu trữ một tập hợp bốn số nguyên đại diện cho vị trí và kích thước của một hình chữ nhật. Lớp Rectangle có một số hàm tạo nạp quá tải để vẽ cấu trúc hình chữ nhật với kích thước và vị trí được chỉ định. Cuối cùng, ảnh được xuất sang định dạng tập tin bmp. Đoạn mã sau cho bạn thấy cách vẽ hình dạng hình chữ nhật trên bề mặt Ảnh.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}
## **Vẽ Hình Cung**
Trong phần này của loạt các hình dạng vẽ, chúng ta sẽ vẽ hình dạng Cung trên bề mặt Ảnh. Chúng ta sẽ sử dụng phương thức DrawArc của [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) để minh họa hoạt động trên một hình ảnh BMP. Đầu tiên, chúng ta sẽ tạo một PsdImage chỉ định độ cao và độ rộng. Sau khi ảnh đã được tạo, chúng ta sẽ sử dụng phương thức Clear được công bố bởi lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) để thiết lập màu nền.

Phương thức DrawArc của lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) được sử dụng để vẽ hình dạng Cung trên bề mặt ảnh. DrawArc đại diện cho một phần của một elip được chỉ định bởi cấu trúc hình chữ nhật hoặc cặp tọa độ. Phương thức này có một số phiên bản chấp nhận các thể hiện của lớp Pen và cấu trúc Rectangle/RectangleF hoặc cặp tọa độ, một chiều rộng và chiều cao làm đối số. Cuối cùng, ảnh được xuất sang định dạng tập tin bmp. Đoạn mã sau cho bạn thấy cách vẽ hình dạng Cung trên bề mặt Ảnh.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
## **Vẽ Bezier**
Ví dụ này sử dụng lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) để vẽ hình dạng Bezier trên bề mặt Ảnh. Để minh họa hoạt động, ví dụ tạo một Ảnh mới và vẽ hình dạng Bezier trên bề mặt Ảnh bằng phương thức DrawBezier được công bố bởi lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Đầu tiên, chúng ta sẽ tạo một PsdImage chỉ định độ cao và độ rộng. Sau khi ảnh đã được tạo, chúng ta sẽ sử dụng phương thức Clear được công bố bởi lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) để thiết lập màu nền của nó.

Phương thức DrawBezier của lớp [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) được sử dụng để vẽ hình dạng đường cong Bezier trên bề mặt ảnh được xác định bởi bốn cấu trúc Point. Phương thức này có một số phiên bản chấp nhận các thể hiện của lớp Pen và bốn cặp tọa độ được sắp xếp hoặc bốn cấu trúc Point/PointF hoặc mảng cấu trúc Point/PointF. Lớp Pen định nghĩa một đối tượng được sử dụng để vẽ đường thẳng, đường cong và hình dạng. Lớp Pen có một số hàm tạo nạp quá tải để vẽ đường thẳng với màu, độ rộng & bút được chỉ định. Cuối cùng, ảnh được xuất sang định dạng tập tin bmp. Đoạn mã sau cho bạn thấy cách vẽ hình dạng Bezier trên bề mặt Ảnh.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}
## **Vẽ Hình Ảnh bằng Chức Năng Cốt Lõi**
Aspose.PSD là một thư viện cung cấp nhiều tính năng giá trị bao gồm tạo hình ảnh từ đầu. Vẽ sử dụng chức năng cốt lõi như thao tác thông tin bitmap của một ảnh, hoặc sử dụng các tính năng tiên tiến như [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) và [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) để vẽ hình dạng trên bề mặt ảnh với sự trợ giúp của các bút và bàn chải khác nhau. Sử dụng lớp RasterImage của Aspose.PSD, bạn có thể lấy thông tin pixel của một khu vực ảnh và thao tác nó. Lớp RasterImage chứa toàn bộ chức năng vẽ cốt lõi, như lấy và đặt pixel và các phương pháp khác để thao tác hình ảnh. Tạo một ảnh mới bằng cách sử dụng bất kỳ phương thức nào được mô tả trong Việc Tạo Tập Tin và gán nó cho một thể hiện lớp RasterImage. Sử dụng phương thức LoadPixels của lớp RasterImage để lấy thông tin pixel của một phần của ảnh. Sau khi có một mảng các pixel, bạn có thể thao tác nó bằng cách, ví dụ, thay đổi màu của từng pixel. Sau khi thao tác thông tin pixel, đặt lại vào khu vực mong muốn trong ảnh sử dụng phương thức SavePixels của lớp RasterImage. Đoạn mã sau cho bạn thấy cách vẽ hình ảnh bằng chức năng cốt lõi.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}


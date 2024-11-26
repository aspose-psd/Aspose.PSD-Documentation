---
title: Vẽ Hình Ảnh
type: docs
weight: 10
url: /vi/java/ve-hinh-anh/
---

## **Vẽ Đường Thẳng**
Ví dụ này sử dụng lớp Graphics để vẽ các hình dạng đường thẳng trên bề mặt Hình ảnh. Để minh họa hoạt động, ví dụ tạo một Hình ảnh mới và vẽ đường thẳng trên bề mặt Hình ảnh bằng cách sử dụng phương thức DrawLine mà lớp Graphics cung cấp. Đầu tiên, chúng ta sẽ tạo một PsdImage xác định chiều cao và chiều rộng của nó.

Sau khi Hình ảnh đã được tạo, chúng ta sẽ sử dụng phương thức Clear mà lớp Graphics cung cấp để đặt màu nền cho nó. Phương thức DrawLine của lớp Graphics được sử dụng để vẽ một đường thẳng trên một hình ảnh kết nối hai cặp điểm hoặc cấu trúc Point/PointF. Lớp Pen định nghĩa một đối tượng được sử dụng để vẽ đường thẳng, đường cong và hình dạng. Lớp Pen có một số constructor nạp chồng để vẽ đường thẳng với màu, độ rộng và bút cụ thể. Lớp SolidBrush được sử dụng để vẽ liên tục với màu cụ thể. Cuối cùng, hình ảnh được xuất ra định dạng tập tin BMP. Đoạn mã sau cho thấy cách vẽ các hình dạng đường thẳng trên bề mặt Hình ảnh.

## **Vẽ Hình Ellipse**
Ví dụ vẽ ellipse là bài viết thứ hai trong loạt các hình dạng vẽ. Chúng ta sẽ sử dụng lớp Graphics để vẽ hình dạng ellipse trên bề mặt Hình ảnh. Để minh họa hoạt động, ví dụ tạo một Hình ảnh mới và vẽ hình dạng ellipse trên bề mặt Hình ảnh bằng cách sử dụng phương thức DrawEllipse mà lớp Graphics cung cấp. Đầu tiên, chúng ta sẽ tạo một PsdImage xác định chiều cao và chiều rộng của nó.

Sau khi tạo hình ảnh, chúng ta sẽ tạo và khởi tạo đối tượng lớp Graphics và đặt màu nền cho hình ảnh bằng cách sử dụng phương thức Clear của lớp Graphics. Phương thức DrawEllipse của lớp Graphics được sử dụng để vẽ hình dạng ellipse trên một bề mặt hình ảnh được xác định bởi cấu trúc hình chữ nhật định. Phương thức này có một số nạp chồng chấp nhận các instance của lớp Pen và Rectangle/RectangleF hoặc một cặp tọa độ, chiều cao và chiều rộng làm đối số. Lớp Pen định nghĩa một đối tượng được sử dụng để vẽ đường thẳng, đường cong và hình dạng. Lớp Pen có một số constructor nạp chồng để vẽ đường thẳng với màu, độ rộng và bút cụ thể. Lớp Rectangle lưu trữ một bộ bốn số nguyên đại diện cho vị trí và kích thước của một hình chữ nhật. Lớp Rectangle có một số constructor nạp chồng để vẽ cấu trúc hình chữ nhật với kích thước và vị trí xác định. Lớp SolidBrush được sử dụng để vẽ liên tục với màu cụ thể. Cuối cùng, hình ảnh được xuất ra định dạng tập tin BMP. Đoạn mã sau cho thấy cách vẽ hình dạng ellipse trên bề mặt Hình ảnh.

## **Vẽ Hình Chữ Nhật**
Trong ví dụ này, chúng ta sẽ vẽ hình dạng hình chữ nhật trên bề mặt Hình ảnh. Để minh họa hoạt động, ví dụ tạo một Hình ảnh mới và vẽ hình dạng hình chữ nhật trên bề mặt Hình ảnh bằng cách sử dụng phương thức DrawRectangle mà lớp Graphics cung cấp. Đầu tiên, chúng ta sẽ tạo một PsdImage xác định chiều cao và chiều rộng của nó. Sau đó, chúng ta sẽ đặt màu nền của Hình ảnh bằng cách sử dụng phương thức Clear của lớp Graphics.

Phương thức DrawRectangle của lớp Graphics được sử dụng để vẽ hình dạng hình chữ nhật trên một bề mặt hình ảnh được xác định bởi cấu trúc hình chữ nhật. Phương thức này có một số nạp chồng chấp nhận các instance của lớp Pen và Rectangle/RectangleF hoặc cặp tọa độ, một chiều rộng và một chiều cao làm đối số. Lớp Rectangle lưu trữ một bộ bốn số nguyên đại diện cho vị trí và kích thước của một hình chữ nhật. Lớp Rectangle có một số constructor nạp chồng để vẽ cấu trúc hình chữ nhật với kích thước và vị trí xác định. Cuối cùng, hình ảnh được xuất ra định dạng tập tin BMP. Đoạn mã sau cho thấy cách vẽ hình dạng hình chữ nhật trên bề mặt Hình ảnh.

## **Vẽ Hình Cung**
Trong phần này của loạt bài vẽ hình dạng, chúng ta sẽ vẽ hình dạng Cung trên bề mặt Hình ảnh. Chúng ta sử dụng phương thức DrawArc của lớp Graphics để minh họa hoạt động trên một hình ảnh BMP. Đầu tiên, chúng ta sẽ tạo một PsdImage xác định chiều cao và chiều rộng của nó. Sau khi hình ảnh đã được tạo, chúng ta sẽ sử dụng phương thức Clear mà lớp Graphics cung cấp để đặt màu nền cho nó.

Phương thức DrawArc của lớp Graphics được sử dụng để vẽ hình dạng Cung trên một bề mặt hình ảnh. DrawArc đại diện cho một phần của một hình elip được xác định bởi cấu trúc hình chữ nhật hoặc cặp tọa độ. Phương thức này có một số nạp chồng chấp nhận các instance của lớp Pen và cấu trúc Rectangle/RectangleF hoặc cặp tọa độ, chiều rộng và chiều cao làm đối số. Cuối cùng, hình ảnh được xuất ra định dạng tập tin BMP. Đoạn mã sau cho thấy cách vẽ hình dạng Cung trên bề mặt Hình ảnh.

## **Vẽ Bezier**
Ví dụ này sử dụng lớp Graphics để vẽ hình dạng Bezier trên bề mặt Hình ảnh. Để minh họa hoạt động, ví dụ tạo một Hình ảnh mới và vẽ hình dạng Bezier trên bề mặt Hình ảnh bằng cách sử dụng phương thức DrawBezier mà lớp Graphics cung cấp. Đầu tiên, chúng ta sẽ tạo một PsdImage xác định chiều cao và chiều rộng của nó. Sau khi hình ảnh đã được tạo, chúng ta sẽ sử dụng phương thức Clear mà lớp Graphics cung cấp để đặt màu nền cho nó.

Phương thức DrawBezier của lớp Graphics được sử dụng để vẽ hình dạng Bezier spline trên một bề mặt hình ảnh xác định bởi bốn cấu trúc Điểm. Phương thức này có một số nạp chồng chấp nhận các instance của lớp Pen và bốn cặp tọa độ được sắp xếp hoặc bốn cấu trúc Point/PointF hoặc mảng các cấu trúc Point/PointF. Lớp Pen định nghĩa một đối tượng được sử dụng để vẽ đường thẳng, đường cong và hình dạng. Lớp Pen có nhiều constructor nạp chồng để vẽ đường thẳng với màu, chiều rộng và bút cụ thể. Cuối cùng, hình ảnh được xuất ra định dạng tập tin BMP. Đoạn mã sau cho thấy cách vẽ hình dạng Bezier trên bề mặt Hình ảnh.

## **Vẽ Hình Ảnh bằng Chức Năng Nhân Bản Cốt Lõi**
Aspose.PSD là một thư viện cung cấp nhiều tính năng quý giá bao gồm việc tạo hình ảnh từ đầu. Vẽ sử dụng chức năng cốt lõi như thao tác thông tin bitmap của một hình ảnh hoặc sử dụng các tính năng tiên tiến như Graphics và GraphicsPath để vẽ hình dạng trên bề mặt hình ảnh với sự trợ giúp của các bút và màu khác nhau. Sử dụng lớp RasterImage của Aspose.PSD, bạn có thể truy xuất thông tin pixel của một khu vực hình ảnh và thao tác nó. Lớp RasterImage chứa toàn bộ chức năng vẽ cốt lõi, như lấy và thiết lập pixel và các phương thức khác để thao tác hình ảnh. Tạo một hình ảnh mới bằng bất kỳ phương pháp nào mô tả trong Tạo Tệp và gán nó cho một thể hiện của lớp RasterImage. Sử dụng phương thức LoadPixels của lớp RasterImage để truy xuất thông tin pixel của một phần của hình ảnh. Sau khi có một mảng các pixel, bạn có thể thao tác nó bằng cách, ví dụ, thay đổi màu sắc của mỗi pixel. Sau khi thao tác thông tin pixel, hãy đặt nó lại vào khu vực mong muốn trong hình ảnh bằng cách sử dụng phương thức SavePixels của lớp RasterImage. Đoạn mã sau cho thấy cách vẽ hình ảnh bằng chức năng cốt lõi.

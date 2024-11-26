---
title: Sử dụng Graphics API để chỉnh sửa Layers trong tệp PSD
weight: 100
type: docs
description: Ví dụ về việc sử dụng Graphics API trong Aspose.PSD cho Python
keywords: [cập nhật layer, vẽ hình tròn, vẽ hình ellipse, vẽ hình tròn đổ màu, đồ họa, psd api, python, mẫu code]
url: vi/python-net/graphics-api/
---

## **Tổng quan**
Đầu tiên, bạn cần tải tệp PSD bằng cách sử dụng phương thức Image.load() hoặc tạo một hình ảnh Psd từ đầu. Trong ví dụ, biến inputFile đại diện cho đường dẫn đến tệp PSD của bạn, và loadOpt đại diện cho các tùy chọn tải (nếu có).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Tiếp theo, bạn có thể truy cập vào lớp đầu tiên của hình ảnh PSD bằng cú pháp psdImage.layers[0]. Điều này cung cấp cho bạn một tham chiếu đến đối tượng lớp mà bạn có thể thao tác.

```python 
layer = psdImage.layers[0]
```
Để chỉnh sửa lớp, bạn cần tạo một đối tượng Graphics bằng cách truyền lớp làm tham số. Đối tượng này cung cấp các phương thức khác nhau để vẽ hình dạng và áp dụng bút.

```python 
graphics = Graphics(layer)
```
Trong ví dụ code, một đối tượng Pen được tạo ra để xác định màu sắc và độ dày của đường viền của hình ellipse. Hằng Color.alice_blue đại diện cho màu sắc, và bạn có thể điều chỉnh độ dày theo nhu cầu.

```python 
pen = Pen(Color.alice_blue)
```
Tương tự, một đối tượng LinearGradientBrush được tạo ra để xác định màu nền của hình ellipse. Rectangle(250, 250, 150, 100) đại diện cho vị trí và kích thước của hình ellipse, và Color.red và Color.aquamarine đại diện cho màu bắt đầu và kết thúc của gradient.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Để vẽ hình ellipse trên lớp, bạn có thể sử dụng phương thức graphics.draw_ellipse(). Rectangle(100, 100, 200, 200) đại diện cho vị trí và kích thước của hình ellipse.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Để đổ màu hình ellipse bằng bút gradient, bạn có thể sử dụng phương thức graphics.fill_ellipse(). Rectangle(250, 250, 150, 100) đại diện cho vị trí và kích thước của hình ellipse.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Sau khi thực hiện các thay đổi mong muốn vào lớp, bạn có thể lưu hình ảnh PSD đã chỉnh sửa bằng cách sử dụng phương thức psdImage.save(). Trong ví dụ, biến psdName đại diện cho đường dẫn để lưu tệp PSD đã chỉnh sửa.

```python 
psdImage.save(psdName)
```
Ngoài ra, bạn cũng có thể lưu hình ảnh đã chỉnh sửa dưới dạng khác, như PNG, bằng cách sử dụng lớp PngOptions. Biến pngName đại diện cho đường dẫn để lưu tệp PNG.

```python 
psdImage.save(pngName, PngOptions())
```
Đó là tất cả! Bạn đã thành công sử dụng Graphics API của Aspose.PSD cho Python để chỉnh sửa layers trong một tệp PSD. Hãy thoải mái khám phá thêm các tính năng và chức năng của thư viện Aspose.PSD để nâng cao khả năng chỉnh sửa hình ảnh của bạn.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}

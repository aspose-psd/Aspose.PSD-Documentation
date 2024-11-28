---
title: Tạo Ảnh PSD hoặc PSB Từ Đầu bằng Python
weight: 100
type: docs
description: Ví dụ về cách Aspose.PSD cho Python có thể tạo Ảnh Psd từ đầu
keywords: [tạo psd, tạo psb, tạo mới, tạo layer, tạo layer văn bản, psd api, python, mã mẫu]
url: vi/python-net/create-psd-psb-images-from-scratch/
---

## **Tổng quan**
Để tạo một tệp PSD hoặc PSB từ đầu bằng Aspose.PSD cho Python, bạn có thể làm theo các bước sau:

Nhập các mô-đun và lớp cần thiết từ thư viện Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Chỉ định tên và đường dẫn tệp đầu ra:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

Tạo một ảnh PSD với kích thước mong muốn:

```python 
with PsdImage(500, 500) as img:
```

Thêm một lớp PSD thông thường và cập nhật nó bằng cách sử dụng API đồ họa:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Tạo một lớp văn bản:
```python 
textLayer = img.add_text_layer("Văn bản Ví dụ", Rectangle(200, 200, 100, 100))
```

Thêm hiệu ứng bóng đổ vào lớp văn bản:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Lưu tệp PSD:
```python 
img.save(outputFile)
```

Đoạn mã này tạo một ảnh PSD với kích thước là 500x500 pixel. Nó thêm một lớp thông thường và vẽ một hình elip lên đó bằng một cây bút và một bàn chải. Sau đó, nó thêm một lớp văn bản với văn bản "Văn bản Ví dụ" và áp dụng hiệu ứng bóng đổ cho nó. Cuối cùng, nó lưu tệp PSD với tên tệp đầu ra cụ thể.

Vui lòng lưu ý rằng bạn cần phải cài đặt và thiết lập thư viện Aspose.PSD đúng cách trong môi trường Python của mình để mã này hoạt động. Bạn có thể tham khảo tài liệu chính thức của Aspose.PSD để biết thêm thông tin về cách cài đặt và sử dụng thư viện.

Vui lòng kiểm tra ví dụ đầy đủ.

## **Ví dụ**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}

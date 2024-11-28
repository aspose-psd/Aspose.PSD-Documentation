---
title: Buat Gambar PSD atau PSB dari Awal menggunakan Python
weight: 100
type: docs
description: Contoh bagaimana Aspose.PSD untuk Python dapat membuat Gambar Psd dari awal
keywords: [buat psd, buat psb, buat baru, buat lapisan, buat lapisan teks, api psd, python, contoh kode]
url: id/python-net/create-psd-psb-images-from-scratch/
---

## **Ikhtisar**
Untuk membuat file PSD atau PSB dari awal menggunakan Aspose.PSD untuk Python, Anda dapat mengikuti langkah-langkah berikut:

Impor modul dan kelas yang diperlukan dari pustaka Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Tentukan nama file output dan jalurnya:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

Buat gambar PSD dengan dimensi yang diinginkan:

```python 
with PsdImage(500, 500) as img:
```

Tambahkan lapisan PSD biasa dan perbarui menggunakan API grafis:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Buat lapisan teks:
```python 
textLayer = img.add_text_layer("Teks Contoh", Rectangle(200, 200, 100, 100))
```

Tambahkan efek bayangan jatuh ke lapisan teks:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Simpan file PSD:
```python 
img.save(outputFile)
```

Kode ini menciptakan gambar PSD dengan dimensi 500x500 piksel. Ini menambahkan lapisan biasa dan menggambar sebuah elips di atasnya menggunakan pena dan kuas. Kemudian ditambahkan lapisan teks dengan teks "Teks Contoh" dan diterapkan efek bayangan jatuh ke dalamnya. Terakhir, file PSD disimpan dengan nama file output yang ditentukan.

Harap diperhatikan bahwa Anda harus memiliki pustaka Aspose.PSD terinstal dan diatur dengan benar di lingkungan Python Anda agar kode ini dapat berfungsi. Anda dapat merujuk ke dokumentasi resmi Aspose.PSD untuk informasi lebih lanjut tentang cara menginstal dan menggunakan pustaka tersebut.

Harap periksa contoh lengkap.

## **Contoh**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentasi-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}

---
title: Menggunakan API Grafis untuk mengedit Lapisan dalam file PSD
weight: 100
type: docs
description: Contoh penggunaan API Grafis dalam Aspose.PSD untuk Python
keywords: [perbarui lapisan, menggambar lingkaran, menggambar elips, menggambar lingkaran isian, grafis, api psd, python, contoh kode]
url: id/python-net/graphics-api/
---

## **Ikhtisar**
Pertama, Anda perlu memuat file PSD menggunakan metode Image.load() atau membuat Gambar Psd dari awal. Dalam contoh ini, variabel inputFile mewakili jalur file PSD Anda, dan loadOpt mewakili opsi pengisian (jika ada).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Selanjutnya, Anda dapat mengakses lapisan pertama dari gambar PSD menggunakan sintaks psdImage.layers[0]. Ini memberikan referensi ke objek lapisan yang dapat Anda manipulasi.

```python 
layer = psdImage.layers[0]
```
Untuk mengedit lapisan, Anda perlu membuat objek Grafis dengan melewati lapisan sebagai parameter. Objek ini menyediakan berbagai metode untuk menggambar bentuk dan menerapkan kuas.

```python 
graphics = Graphics(layer)
```
Dalam contoh kode, objek Pen dibuat untuk mendefinisikan warna dan ketebalan garis luar bentuk elips. Konstan Color.alice_blue mewakili warna, dan Anda dapat menyesuaikan ketebalan sesuai kebutuhan.

```python 
pen = Pen(Color.alice_blue)
```
Demikian pula, objek LinearGradientBrush dibuat untuk mendefinisikan warna isian bentuk elips. Rectangle(250, 250, 150, 100) mewakili posisi dan ukuran bentuk elips, dan Color.red dan Color.aquamarine mewakili warna awal dan akhir gradien.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
Untuk menggambar bentuk elips di lapisan, Anda dapat menggunakan metode graphics.draw_ellipse(). Rectangle(100, 100, 200, 200) mewakili posisi dan ukuran bentuk elips.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
Untuk mengisi bentuk elips dengan kuas gradien, Anda dapat menggunakan metode graphics.fill_ellipse(). Rectangle(250, 250, 150, 100) mewakili posisi dan ukuran bentuk elips.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
Setelah melakukan perubahan yang diinginkan pada lapisan, Anda dapat menyimpan gambar PSD yang sudah dimodifikasi menggunakan metode psdImage.save(). Dalam contoh ini, variabel psdName mewakili jalur untuk menyimpan file PSD yang sudah dimodifikasi.

```python 
psdImage.save(psdName)
```
Selain itu, Anda juga dapat menyimpan gambar yang sudah dimodifikasi dalam format lain, seperti PNG, dengan menggunakan kelas PngOptions. Variabel pngName mewakili jalur untuk menyimpan file PNG.

```python 
psdImage.save(pngName, PngOptions())
```
Itu dia! Anda telah berhasil menggunakan API Grafis dari Aspose.PSD untuk Python untuk mengedit lapisan dalam file PSD. Jangan ragu untuk menjelajahi fitur-fitur dan fungsionalitas lebih lanjut dari perpustakaan Aspose.PSD untuk meningkatkan kemampuan pengeditan gambar Anda.

Silakan periksa contoh lengkapnya.

## **Contoh**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentasi-Python-Aspose-Psd-API-Grafis.py" >}}

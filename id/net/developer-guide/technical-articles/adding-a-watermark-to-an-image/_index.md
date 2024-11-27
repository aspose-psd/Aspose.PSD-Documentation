---
title: Menambahkan Watermark ke Gambar
type: docs
weight: 30
url: /id/net/menambahkan-watermark-ke-gambar/
---

## **Menambahkan Watermark ke Gambar**
Dokumen ini menjelaskan cara menambahkan watermark ke gambar menggunakan Aspose.PSD. Menambahkan watermark ke gambar adalah kebutuhan umum untuk aplikasi pengolahan gambar. Contoh ini menggunakan kelas Graphics untuk menggambar string pada permukaan gambar.

### **Menambahkan Watermark**
Untuk menunjukkan operasi ini, kami akan memuat gambar BMP dari disk dan menggambar string sebagai watermark di permukaan gambar menggunakan metode DrawString kelas Graphics. Kami akan menyimpan gambar ke format PNG menggunakan kelas PngOptions. Berikut ini adalah contoh kode yang menunjukkan cara menambahkan watermark ke gambar. Kode contoh telah dibagi menjadi bagian-bagian untuk memudahkan pemahaman langkah demi langkah.

1. [Muat](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) sebuah gambar.
1. Buat dan inisialisasi objek [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. Buat dan inisialisasi objek Font dan [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. Gambar string sebagai watermark menggunakan metode [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) kelas Graphics.
1. Simpan gambar ke format PNG.

Potongan kode berikut ini menunjukkan cara menambahkan watermark pada gambar.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}

### **Menambahkan Watermark Diagonal**
Menambahkan watermark diagonal ke gambar mirip dengan menambahkan watermark horizontal seperti yang dibahas sebelumnya, dengan sedikit perbedaan. Untuk menunjukkan operasi ini, kami akan memuat gambar JPG dari disk, menambahkan transformasi menggunakan objek kelas [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) dan menggambar string sebagai watermark pada permukaan gambar menggunakan metode DrawString kelas Graphics. Berikut ini adalah contoh kode yang menunjukkan cara menambahkan watermark diagonal ke gambar. Kode contoh telah dibagi menjadi bagian-bagian untuk memudahkan pemahaman langkah demi langkah.

1. Muat gambar.
1. Buat dan inisialisasi objek Graphics.
1. Buat dan inisialisasi objek [Font](https://reference.aspose.com/psd/net/aspose.psd/font) dan SolidBrush.
1. Dapatkan ukuran gambar dalam objek [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. Buat sebuah instansi kelas Matrix dan lakukan transformasi komposit.
1. Tetapkan transformasi ke objek Graphics.
1. Buat dan inisialisasi objek [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. Gambar string sebagai watermark menggunakan metode DrawString kelas Graphics.
1. Simpan gambar hasil.

Potongan kode berikut ini menunjukkan cara menambahkan watermark diagonal.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}} 

---
title: Menambahkan Watermark ke Gambar
type: docs
weight: 20
url: /id/java/menambahkan-watermark-ke-gambar/
---

## **Menambahkan Watermark ke Gambar**
Dokumen ini menjelaskan cara menambahkan watermark ke gambar menggunakan Aspose.PSD. Menambahkan watermark ke gambar adalah kebutuhan umum untuk aplikasi pengolahan gambar. Contoh ini menggunakan kelas Graphics untuk menggambar string pada permukaan gambar.
### **Menambahkan Watermark**
Untuk mendemonstrasikan operasi ini, kita akan memuat gambar BMP dari disk dan menggambar sebuah string sebagai watermark di permukaan gambar menggunakan metode DrawString dari kelas Graphics. Kita akan menyimpan gambar dalam format PNG menggunakan kelas PngOptions. Berikut ini adalah contoh kode yang menunjukkan bagaimana menambahkan watermark ke gambar. Kode sumber contoh telah dibagi menjadi bagian-bagian untuk memudahkan pemahaman. Langkah demi langkah, contoh tersebut menunjukkan cara untuk:

1. Memuat sebuah gambar.
1. Membuat dan menginisialisasi objek Graphics.
1. Membuat dan menginisialisasi objek Font dan SolidBrush.
1. Menggambar sebuah string sebagai watermark menggunakan metode DrawString dari kelas Graphics.
1. Menyimpan gambar dalam format PNG.

Potongan kode berikut menunjukkan bagaimana cara menambahkan watermark ke gambar.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Menambahkan Watermark Diagonal**
Menambahkan watermark diagonal ke gambar mirip dengan menambahkan watermark horizontal seperti yang dibahas sebelumnya, dengan beberapa perbedaan. Untuk mendemonstrasikan operasi, kita akan memuat gambar JPG dari disk, menambahkan transformasi menggunakan objek kelas Matrix, dan menggambar sebuah string sebagai watermark di permukaan gambar menggunakan metode DrawString dari kelas Graphics. Berikut ini adalah contoh kode yang menunjukkan bagaimana menambahkan watermark diagonal ke gambar. Kode sumber contoh telah dibagi menjadi bagian-bagian untuk memudahkan pemahaman. Langkah demi langkah, contoh tersebut menunjukkan cara untuk:

1. Memuat sebuah gambar.
1. Membuat dan menginisialisasi objek Graphics.
1. Membuat dan menginisialisasi objek Font dan SolidBrush.
1. Mendapatkan ukuran gambar dalam objek SizeF.
1. Membuat sebuah instance dari kelas Matrix dan melakukan transformasi komposit.
1. Menetapkan transformasi ke objek Graphics.
1. Membuat dan menginisialisasi objek StringFormat.
1. Menggambar sebuah string sebagai watermark menggunakan metode DrawString dari kelas Graphics.
1. Menyimpan gambar hasilnya.

Potongan kode berikut menunjukkan bagaimana cara menambahkan watermark diagonal.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}

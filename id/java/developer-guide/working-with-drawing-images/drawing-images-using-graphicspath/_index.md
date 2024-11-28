---
title: Menggambar Gambar menggunakan GraphicsPath
type: docs
weight: 30
url: /id/menggambar-gambar-menggunakan-graphicspath/
---

## **Menggambar Gambar menggunakan GraphicsPath**
Kelas GraphicsPath bertanggung jawab untuk membuat dan mempertahankan jalur grafis. GraphicsPath tidak memiliki referensi ke gambar dan tidak mengubah gambar itu sendiri, namun, dapat dianggap sebagai objek yang berisi metadata yang menggambarkan jalur-jalur yang dapat digambar oleh kelas grafis. Kelas GraphicsPath menggunakan figur; setiap figur terdiri dari serangkaian garis dan kurva yang terhubung atau bentuk geometris primitif. Setiap bentuk dapat dibagi menjadi segmen bentuk. Anda dapat menambahkan, menghapus, dan mengubah berbagai figur atau bentuk dalam objek GraphicsPath. Ketika GraphicsPath sudah sepenuhnya dijelaskan, gunakan metode kelas Graphics yang sesuai (GambarPath Gambar dan Isi Jalur) untuk menggambar atau mengisi jalur. Kelas Grafik mengambil setiap segmen bentuk dan menggambarkannya untuk menghasilkan gambar akhir.

### **Menggambar menggunakan Kelas GraphicsPath**
Berikut adalah contoh yang menunjukkan penggunaan kelas GraphicsPath. Kode sumber contoh telah dibagi menjadi beberapa bagian untuk menjadikannya sederhana dan mudah diikuti. Langkah demi langkah, contoh-contoh ini menunjukkan kepada Anda bagaimana:

- Membuat gambar.
- Menginisialisasi objek Grafis.
- Menghapus permukaan.
- Membuat instans dari GraphicsPath.
- Membuat sebuah figur.
- Menambahkan bentuk ke figur.
- Membuat array Figur.
- Menggambar jalur.
- Mengisi jalur.

### **Menggambar Gambar menggunakan GraphicsPath: Sampel Pemrograman**
#### **GraphicsPath: Membuat Gambar**
Mulailah dengan membuat gambar menggunakan salah satu metode yang dijelaskan dalam Membuat Berkas.
#### **GraphicsPath: Menginisialisasi Objek Grafis**
Membuat dan menginisialisasi objek Grafis dengan melewatkan objek Gambar ke konstruktor objek tersebut.
#### **GraphicsPath: Menghapus Permukaan**
Hapus permukaan Grafis dengan memanggil metode Clear kelas Grafis dan melewati Warna sebagai parameter. Metode ini mengisi permukaan Grafis dengan warna yang dilewatkan sebagai argumen.
#### **GraphicsPath: Membuat Instans dari GraphicsPath**
Membuat sebuah instans dari GraphicsPath dengan GraphicsPath disetel ke Alternate secara default. Mode ini menentukan bagaimana mengisi interior suatu bentuk tertutup. Nilai GraphicsPath lainnya yang mungkin adalah Winding.
#### **GraphicsPath: Membuat Sebuah Figur**
Membuat sebuah instans dari kelas Figure. Seperti yang dibahas sebelumnya, Figure dapat berisi Shapes dan shapes berada di namespace Aspose.PSD.Shapes.
#### **GraphicsPath: Menambahkan Bentuk ke Figur**
Metode Add Shapes yang diungkapkan oleh kelas Figure memungkinkan Anda menambahkan bentuk ke figur. Pada contoh kode di bawah, beberapa bentuk ditambahkan ke objek Figure.
#### **GraphicsPath: Menambahkan Figur ke dalam Array**
Beberapa figur dapat ditambahkan ke objek GraphicsPath menggunakan metode AddFigures yang diungkapkan oleh kelas GraphicsPath. Metode ini menerima array figur sebagai parameter.
#### **GraphicsPath: Menggambar Jalur**
Gambar GraphicsPath menggunakan metode DrawPath yang diungkapkan oleh kelas Grafis. Metode ini menerima dua parameter. Parameter pertama adalah objek kelas Pen, yang menentukan warna, lebar, dan gaya jalur. Parameter kedua adalah objek kelas GraphicsPath, yang mewakili jalur itu sendiri.
#### **GraphicsPath: Mengisi Jalur**
Anda dapat mengisi jalur dengan melewati objek GraphicsPath ke metode Fill Paths yang diungkapkan oleh kelas Grafis. Metode Fill Paths mengisi jalur sesuai dengan mode pengisian (alternate atau winding) yang saat ini diatur untuk jalur tersebut. Jika jalur memiliki beberapa figur terbuka, jalur diisi seolah-olah figur tersebut tertutup.

Metode Fill Paths menerima dua parameter. Parameter pertama adalah objek dari kelas sikat apa pun dari namespace Aspose.PSD.Brushes. Parameter kedua adalah jalur itu sendiri. Untuk keperluan contoh ini, gunakan HatchBrush yang merupakan sikat persegi dengan gaya garis miring, warna depan, dan warna belakang. Sebelum melewatkan objek HatchBrush ke metode Fill Paths, atur propertinya.
### **GraphicsPath: Sumber Lengkap**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



Semua kelas yang mengimplementasikan IDisposable diinstansiasi dalam pernyataan Menggunakan untuk memastikan bahwa mereka dibuang dengan benar.

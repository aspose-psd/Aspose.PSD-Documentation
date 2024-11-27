---
title: Menggambar Gambar menggunakan GraphicsPath
type: docs
weight: 30
url: /id/net/menggambar-gambar-menggunakan-graphicspath/
---

## **Menggambar Gambar menggunakan GraphicsPath**
Kelas [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) bertanggung jawab untuk membuat dan memelihara jalur grafis. GraphicsPath tidak memiliki referensi ke gambar dan tidak mengubah gambar itu sendiri, sebaliknya, itu dapat dianggap sebagai objek yang berisi metadata yang menjelaskan jalur-jalur yang dapat digambar oleh kelas Graphics. Kelas GraphicsPath menggunakan gambar; setiap gambar terdiri dari urutan garis dan kurva yang terhubung atau bentuk geometris primitif. Setiap bentuk dapat dibagi menjadi segmen bentuk. Anda dapat menambahkan, menghapus, dan mengubah berbagai gambar atau bentuk dalam objek GraphicsPath. Ketika GraphicsPath telah sepenuhnya dijelaskan, gunakan metode kelas Graphics yang sesuai (GambarPath dan Isi Jalur) untuk menggambar atau mengisi jalur-jalur tersebut. Kelas Graphics mengambil setiap segmen bentuk dan menggambar untuk menghasilkan gambar akhir.
### **Menggambar menggunakan Kelas GraphicsPath**
Berikut adalah contoh yang menunjukkan penggunaan [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) kelas. Kode sumber contoh telah dibagi menjadi beberapa bagian agar lebih sederhana dan mudah diikuti. Langkah demi langkah, contoh-contoh tersebut menunjukkan cara:

- Membuat gambar.
- Menginisialisasi objek Grafis.
- Bersihkan permukaan.
- Buat instance [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Buat sebuah gambar.
- Tambahkan bentuk ke gambar.
- Buat array Figures.
- Menggambar jalur.
- Mengisi jalur.


### **Menggambar Gambar menggunakan GraphicsPath: Contoh Programming**
#### **GraphicsPath : Membuat Gambar**
Mulailah dengan membuat gambar menggunakan salah satu metode yang dijelaskan dalam Membuat File.
#### **GraphicsPath : Menginisialisasi Objek Grafis**
Buat dan inisialisasi objek Grafis dengan melewatkan objek Gambar ke konstrukturnya.
#### **GraphicsPath : Bersihkan Permukaan**
Bersihkan permukaan Grafis dengan memanggil metode Bersihkan kelas Grafis dan lewatkan Warna sebagai parameter. Metode ini mengisi permukaan Grafis dengan warna yang dilewatkan sebagai argumen.
#### **GraphicsPath : Membuat Instance dari GraphicsPath**
Buat instance GraphicsPath dengan GraphicsPath diatur ke Alternate secara default. Mode ini menentukan bagaimana mengisi interior sebuah gambar tertutup. Nilai GraphicsPath lain yang mungkin adalah Winding.
#### **GraphicsPath : Membuat Gambar**
Buat instance dari kelas Gambar. Seperti yang dibahas sebelumnya, Gambar dapat berisi Bentuk dan bentuk berada dalam namespace Aspose.PSD.Shapes.
#### **GraphicsPath : Tambahkan Bentuk ke Gambar**
Metode Tambah Bentuk yang terpapar oleh kelas Gambar memungkinkan Anda menambah bentuk ke gambar. Dalam contoh kode di bawah, beberapa bentuk ditambahkan ke objek Gambar.
#### **GraphicsPath : Tambahkan Gambar ke dalam Array**
Beberapa gambar dapat ditambahkan ke objek GraphicsPath menggunakan metode TambahGambar yang terpapar oleh kelas GraphicsPath. Metode ini menerima array gambar sebagai parameter.
#### **GraphicsPath : Gambar Jalur-Jalur**
Gambar GraphicsPath menggunakan metode Gambar Jalur yang terpapar oleh kelas Grafis. Metode ini menerima dua parameter. Parameter pertama adalah objek kelas Pen, yang menentukan warna, lebar, dan gaya jalur. Parameter kedua adalah objek kelas GraphicsPath, yang mewakili jalur itu sendiri.
#### **GraphicsPath : Isi Jalur**
Anda dapat mengisi jalur dengan melewatkan objek GraphicsPath ke metode Isi Jalur yang terpapar oleh kelas Grafis. Metode Isi Jalur mengisi jalur sesuai dengan mode pengisian (alternate atau winding) yang saat ini diatur untuk jalur tersebut. Jika jalur memiliki gambar terbuka, jalur diisi seolah-olah gambar tersebut ditutup.

Metode Isi Jalur menerima dua parameter. Parameter pertama adalah objek dari kelas kuas apa pun dari namespace Aspose.PSD.Brushes. Parameter kedua adalah jalurnya sendiri. Untuk contoh ini, gunakan HatchBrush yang merupakan kuas berbentuk persegi panjang dengan gaya hantaran, warna latar depan, dan warna latar belakang. Sebelum melewati objek HatchBrush ke metode Isi Jalur, atur propertinya.
### **GraphicsPath : Kode Sumber Lengkap**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Semua kelas yang mengimplementasikan IDisposable diinstansiasi dalam pernyataan Using untuk memastikan bahwa mereka dibuang dengan benar.

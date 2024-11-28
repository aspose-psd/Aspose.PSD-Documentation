---
title: Menggambar Gambar Menggunakan Grafik
type: docs
weight: 20
url: /id/java/menggambar-gambar-menggunakan-grafik/
---

## **Menggambar Gambar Menggunakan Grafik**


Dengan pustaka Aspose.PSD, Anda dapat menggambar bentuk sederhana seperti garis, persegi panjang, dan lingkaran, serta bentuk kompleks seperti poligon, kurva, lengkung, dan bentuk Bezier. Pustaka Aspose.PSD membuat bentuk-bentuk tersebut menggunakan kelas Grafik yang berada di dalam namespace Aspose.PSD. Objek Grafik bertanggung jawab untuk melakukan berbagai operasi menggambar pada gambar, sehingga mengubah permukaan gambar tersebut. Kelas Grafik menggunakan berbagai objek pembantu untuk meningkatkan bentuk-bentuk tersebut:

- Pens, untuk menggambar garis, menjelaskan bentuk, atau merender representasi geometris lainnya.
- Brushes, untuk mendefinisikan bagaimana area diisi.
- Fonts, untuk mendefinisikan bentuk karakter teks.
### **Menggambar dengan Kelas Grafik**
Berikut adalah contoh kode yang menunjukkan penggunaan kelas Grafik. Kode sumber contoh telah dibagi menjadi beberapa bagian untuk menjadikannya sederhana dan mudah diikuti. Langkah demi langkah, contoh-contoh tersebut menunjukkan cara untuk:

1. Membuat sebuah gambar.
1. Membuat dan menginisialisasi objek Grafik.
1. Menghapus permukaan.
1. Menggambar sebuah elips.
1. Menggambar sebuah poligon yang diisi dan menyimpan gambar.
### **Contoh Pengkodean**
#### **Membuat Sebuah Gambar**
Mulailah dengan membuat sebuah gambar menggunakan salah satu metode yang dijelaskan dalam Membuat File.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Membuat dan Menginisialisasi Objek Grafik**
Selanjutnya, buat dan inisialisasi objek Grafik dengan meneruskan objek Gambar ke konstrukturnya.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **Menghapus Permukaan**
Hapus permukaan Grafik dengan memanggil metode Clear dari kelas Grafik dan meneruskan warna sebagai parameter. Metode ini mengisi permukaan Grafik dengan warna yang diteruskan sebagai argumen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **Menggambar Sebuah Elips**
Anda mungkin melihat bahwa kelas Grafik telah mengekspos banyak metode untuk menggambar dan mengisi bentuk. Anda akan menemukan daftar lengkap metode-metode tersebut di Referensi API Aspose.PSD untuk Java. Terdapat beberapa versi overloaded dari metode DrawEllipse yang diekspos oleh kelas Grafik. Semua metode ini menerima objek Pen sebagai argumen pertamanya. Parameter-parameter berikutnya diteruskan untuk mendefinisikan persegi panjang pembatas sekitar elips. Untuk contoh ini, gunakan versi yang menerima objek Rectangle sebagai parameter kedua untuk menggambar elips menggunakan objek Pen dalam warna yang diinginkan.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **Menggambar Sebuah Poligon yang Diisi**
Selanjutnya, gambar sebuah poligon menggunakan LinearGradientBrush dan sebuah larik titik. Kelas Grafik telah mengekspos beberapa versi overloaded dari metode FillPolygon. Semua ini menerima objek Brush sebagai argumen pertamanya, yang mendefinisikan karakteristik pengisian. Parameter kedua adalah sebuah larik titik. Harap dicatat bahwa setiap dua titik berurutan dalam larik tersebut menentukan sisi poligon.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **Menggambar Gambar Menggunakan Grafik : Sumber Lengkap**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}



Semua kelas yang mengimplementasikan IDisposable dan mengakses sumber daya tak terkelola diinstansiasi dalam sebuah pernyataan Using untuk memastikan bahwa mereka dibuang dengan benar.


---
title: Menggambar Gambar dengan Grafik
type: docs
weight: 20
url: /id/net/drawing-images-using-graphics/
---

## **Menggambar Gambar dengan Grafik**
Dengan perpustakaan Aspose.PSD Anda dapat menggambar bentuk-bentuk sederhana seperti garis, persegi panjang, dan lingkaran, serta bentuk-bentuk kompleks seperti poligon, kurva, busur, dan bentuk Bezier. Perpustakaan Aspose.PSD menciptakan bentuk-bentuk tersebut menggunakan kelas [Grafik](https://reference.aspose.com/psd/net/aspose.psd/graphics) yang berada di dalam ruang nama Aspose.PSD. Objek Grafik bertanggung jawab untuk melakukan berbagai operasi menggambar pada gambar, sehingga mengubah permukaan gambar. Kelas [Grafik](https://reference.aspose.com/psd/net/aspose.psd/graphics) menggunakan berbagai objek pembantu untuk meningkatkan bentuk-bentuk tersebut:

- Pens, untuk menggambar garis, menggambar garis luar bentuk, atau merender representasi geometris lainnya.
- Kuas, untuk mendefinisikan bagaimana area diisi.
- Font, untuk mendefinisikan bentuk karakter teks.
### **Menggambar dengan Kelas Grafik**
Berikut adalah contoh kode yang menunjukkan penggunaan kelas [Grafik](https://reference.aspose.com/psd/net/aspose.psd/graphics). Kode sumber contoh telah dibagi menjadi beberapa bagian agar tetap sederhana dan mudah diikuti. Langkah demi langkah, contoh-contoh menunjukkan cara untuk:

1. Membuat sebuah gambar.
2. Membuat dan menginisialisasi objek Grafik.
3. Menghapus permukaan.
4. Menggambar sebuah elips.
5. Menggambar sebuah poligon berisi dan menyimpan gambar.
### **Contoh Program**
#### **Membuat Gambar**
Mulai dengan membuat gambar menggunakan salah satu metode yang dijelaskan dalam Menciptakan Berkas.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Membuat dan Menginisialisasi Objek Grafik**
Kemudian membuat dan menginisialisasi objek Grafik dengan meneruskan objek Gambar ke konstruktornya.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Menghapus Permukaan**
Menghapus permukaan Grafik dengan memanggil metode Bersih [Grafik](https://reference.aspose.com/psd/net/aspose.psd/graphics) dan meneruskan warna sebagai parameter. Metode ini mengisi permukaan Grafik dengan warna yang dilewatkan sebagai argumen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Menggambar Elips**
Anda mungkin melihat bahwa kelas [Grafik](https://reference.aspose.com/psd/net/aspose.psd/graphics) telah mengekspos banyak metode untuk menggambar dan mengisi bentuk. Anda akan menemukan daftar lengkap metode dalam Referensi API Aspose.PSD untuk .NET. Ada beberapa versi metode DrawEllipse yang diekspos oleh kelas Grafik. Semua metode ini menerima objek Pens sebagai argumen pertamanya. Parameter-parameter berikutnya diteruskan untuk mendefinisikan persegi panjang pembatas sekitar elips. Untuk contoh ini, gunakan versi yang menerima objek Rectangle sebagai parameter kedua untuk menggambar sebuah elips menggunakan objek Pens dalam warna yang diinginkan.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Menggambar Poligon Berisi**
Selanjutnya, gambar poligon menggunakan LinearGradientBrush dan sebuah array titik. Kelas Grafik telah mengekspos beberapa versi metode FillPolygon(). Semua ini menerima objek Brush sebagai argumen pertamanya, yang mendefinisikan karakteristik pengisian. Parameter kedua adalah sebuah array titik. Harap dicatat bahwa setiap dua titik berurutan dalam array menentukan sisi poligon.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Menggambar Gambar dengan Grafik: Sumber Lengkap**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Semua kelas yang mengimplementasikan IDisposable dan mengakses sumber daya yang tidak dikelola diinisiasikan dalam pernyataan Using untuk memastikan bahwa mereka dibuang dengan benar.

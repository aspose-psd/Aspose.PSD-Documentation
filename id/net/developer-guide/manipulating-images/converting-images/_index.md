---
title: Mengonversi Gambar
type: docs
weight: 20
url: /id/mengonversi-gambar/
---

## **Mengonversi Gambar Menjadi Hitam Putih dan Skala Abu-abu**
Terkadang Anda mungkin perlu mengonversi gambar berwarna menjadi hitam putih atau skala abu-abu untuk mencetak atau menyimpan arsip. Artikel ini menunjukkan penggunaan Aspose.PSD untuk API .NET guna mencapai hal ini dengan menggunakan dua metode seperti dijelaskan di bawah ini.

- Binarisasi
- Skala Abu-abu

### **Binarisasi**
Untuk memahami konsep Binarisasi, penting untuk mendefinisikan sebuah Gambar Biner; yaitu gambar digital yang hanya dapat memiliki dua nilai mungkin untuk setiap piksel. Biasanya, dua warna yang digunakan untuk gambar biner adalah hitam dan putih meskipun dapat digunakan dua warna apa pun. Binarisasi adalah proses mengonversi gambar menjadi bi-level yang berarti setiap piksel disimpan sebagai satu bit (0 atau 1) di mana 0 menunjukkan ketiadaan warna dan 1 berarti kehadiran warna. API Aspose.PSD untuk .NET saat ini mendukung dua metode Binarisasi.
#### **Binarisasi dengan Ambang Batas Tetap**
Potongan kode berikut menunjukkan bagaimana menggunakan binarisasi ambang tetap yang dapat diterapkan pada gambar.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarisasi dengan Ambang Otsu**
Potongan kode berikut menunjukkan bagaimana menggunakan binarisasi ambang Otsu yang dapat diterapkan pada gambar.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Skala Abu-abu**
Skala abu-abu adalah proses mengonversi gambar tone kontinu menjadi gambar dengan nuansa abu-abu yang terputus. Potongan kode berikut menunjukkan cara menggunakan Skala Abu-abu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **Mengonversi Lapisan Gambar GIF Menjadi Gambar TIFF**
Terkadang diperlukan untuk mengekstrak dan mengonversi lapisan Gambar PSD ke format gambar raster lain untuk memenuhi kebutuhan aplikasi. API Aspose.PSD mendukung fitur mengekstrak dan mengonversi lapisan Gambar PSD ke format gambar raster lain. Pertama, kita akan membuat sebuah instance gambar dan memuat gambar PSD dari disk lokal, kemudian kita akan mengulang setiap lapisan pada properti Layer. Selanjutnya kita akan mengonversi blok ke gambar TIFF. Potongan kode berikut menunjukkan bagaimana mengonversi lapisan gambar PSD menjadi gambar TIFF.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}

## **Mengonversi PSD CMYK ke TIFF CMYK**
Menggunakan Aspose.PSD untuk .NET, pengembang dapat mengonversi file PSD CMYK ke format tiff CMYK. Artikel ini menunjukkan bagaimana cara mengekspor/mengonversi file PSD CMYK ke format tiff CMYK dengan Aspose.PSD. Menggunakan Aspose.PSD untuk .NET, Anda dapat memuat gambar PSD dan kemudian Anda dapat mengatur berbagai properti menggunakan [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) class dan menyimpan atau mengekspor gambar. Potongan kode berikut menunjukkan cara mencapai fitur ini.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}

## **Mengekspor Gambar**
Selain kumpulan rutinitas pemrosesan gambar, Aspose.PSD menyediakan kelas-kelas khusus untuk mengonversi format file PSD ke format lain. Dengan menggunakan perpustakaan ini, konversi gambar PSD sangat sederhana dan intuitif. Di bawah ini adalah beberapa kelas khusus untuk tujuan ini dalam [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Mengekspor gambar PSD dengan Aspose.PSD untuk API .NET sangat mudah. Yang Anda butuhkan hanyalah objek kelas yang sesuai dari [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace. Dengan menggunakan kelas-kelas ini, Anda dapat dengan mudah mengekspor gambar apa pun yang dibuat, diedit, atau hanya dimuat dengan Aspose.PSD untuk .NET ke format yang didukung.
## **Menggabungkan Gambar**
Contoh ini menggunakan kelas Graphics dan menunjukkan bagaimana menggabungkan dua atau lebih gambar menjadi satu gambar lengkap. Untuk mendemonstrasikan operasi, contoh ini membuat sebuah PsdImage baru dan menggambar gambar-gambar di permukaan kanvas menggunakan metode Draw Image yang terbuka oleh kelas Graphics. Dengan menggunakan kelas Grafis, dua atau lebih gambar dapat digabungkan sedemikian rupa sehingga gambar yang dihasilkan akan terlihat sebagai gambar lengkap tanpa adanya ruang di antara bagian gambar dan tidak ada halaman. Ukuran kanvas harus sama dengan ukuran gambar hasilnya. Berikut adalah contoh kode yang menunjukkan cara menggunakan [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) metode kelas [Grafis](https://reference.aspose.com/psd/net/aspose.psd/graphics) untuk menggabungkan gambar dalam satu gambar.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **Memperluas dan Mencrop Gambar**
API Aspose.PSD memungkinkan Anda memperluas atau mencrop gambar selama proses konversi gambar. Pengembang perlu membuat persegi panjang dengan koordinat X dan Y dan menetapkan lebar dan tinggi dari kotak persegi panjang. X, Y dan Lebar, Tinggi dari persegi panjang akan menggambarkan perluasan atau pemotongan gambar yang dimuat. Jika diperlukan memperluas atau mencrop gambar selama konversi gambar, lakukan langkah-langkah berikut:

1. Buat instance kelas [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) dan muat gambar yang ada.
1. Buat Instance kelas ImageOption.
1. Buat instance kelas [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) dan inisialisasi X, Y dan Lebar, Tinggi persegi panjang
1. Panggil metode [Simpan](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) dari kelas RasterImage sambil melewati nama file output, opsi gambar, dan objek persegi panjang sebagai parameter.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **Membaca dan Menulis Data XMP ke Gambar**
XMP (Ekstensible Metadata Platform) adalah standar ISO. XMP mensandardisasi model data, format serialisasi, dan properti inti untuk definisi dan pemrosesan metadata yang dapat diperluas. Ini juga memberikan panduan untuk menyematkan informasi XMP ke dalam gambar populer seperti JPEG, tanpa merusak daya baca mereka oleh aplikasi yang tidak mendukung XMP. Dengan menggunakan API Aspose.PSD untuk .NET, pengembang dapat membaca atau menulis metadata XMP ke gambar. Artikel ini menunjukkan bagaimana metadata XMP dapat dibaca dari sebuah gambar dan menulis metadata XMP ke gambar.
### **Buat Metadata XMP, Tulis Itu dan Baca Dari File**
Dengan bantuan ruang nama Xmp, pengembang dapat membuat objek metadata XMP dan menuliskannya ke dalam gambar. Potongan kode berikut menunjukkan cara menggunakan paket-paket XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage dan DublinCorePackage yang terdapat dalam ruang nama [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **Mengekspor Gambar dalam Lingkungan Multithread**
Aspose.PSD untuk .NET sekarang mendukung mengonversi gambar dalam lingkungan multi-threaded. Aspose.PSD untuk .NET memastikan kinerja yang dioptimalkan dari operasi selama eksekusi kode dalam lingkungan multi-threaded. Semua kelas opsi gambar (misalnya BmpOptions, TiffOptions, JpegOptions, dll.) dalam Aspose.PSD untuk .NET mengimplementasikan antarmuka IDisposable. Oleh karena itu, penting bagi pengembang untuk membuang objek kelas opsi gambar dengan benar jika properti Sumber diatur. Potongan kode berikut mendemonstrasikan fungsionalitas tersebut.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD sekarang mendukung properti SyncRoot saat bekerja dalam lingkungan multi-threaded. Pengembang dapat menggunakan properti ini untuk menyinkronkan akses ke aliran sumber. Potongan kode berikut menunjukkan bagaimana properti SyncRoot dapat digunakan.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}

---
title: Mengkonversi Gambar
type: docs
weight: 20
url: /id/java/mengkonversi-gambar/
---

## **Mengkonversi Gambar ke Hitam Putih dan Grayscale**
Terkadang Anda mungkin perlu mengonversi gambar berwarna ke Hitam Putih atau Grayscale untuk tujuan mencetak atau pengarsipan. Artikel ini menunjukkan penggunaan Aspose.PSD untuk Java API untuk mencapai hal ini menggunakan dua metode sebagai berikut.

- Binarisasi
- Grayscaling
### **Binarisasi**
Untuk memahami konsep Binarisasi, penting untuk mendefinisikan Gambar Biner; yaitu gambar digital yang hanya dapat memiliki dua nilai yang mungkin untuk setiap pixel. Biasanya, dua warna yang digunakan untuk gambar biner adalah hitam dan putih meskipun dua warna apa pun dapat digunakan. Binarisasi adalah proses mengonversi gambar ke tingkat dua yang berarti setiap pixel disimpan sebagai satu bit (0 atau 1) di mana 0 mengindikasikan ketiadaan warna dan 1 berarti keberadaan warna. Aspose.PSD untuk Java API saat ini mendukung dua metode Binarisasi.
#### **Binarisasi dengan Ambang Tetap**
Potongan kode berikut menunjukkan bagaimana binarisasi ambang tetap dapat diterapkan pada gambar.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Binarisasi dengan Ambang Otsu**
Potongan kode berikut menunjukkan bagaimana binarisasi ambang Otsu dapat diterapkan pada gambar.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Grayscaling**
Grayscale adalah proses mengonversi gambar dengan nada yang kontinu menjadi gambar dengan nada abu-abu yang terputus-putus. Potongan kode berikut menunjukkan cara menggunakan Grayscale.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Mengkonversi Layer Gambar GIF ke Gambar TIFF**
Terkadang diperlukan untuk mengekstrak dan mengonversi lapisan dari Gambar PSD ke format gambar raster lain untuk memenuhi kebutuhan aplikasi. API Aspose.PSD mendukung fitur mengekstrak dan mengonversi lapisan dari Gambar PSD ke format gambar raster lain. Pertama, kita akan membuat instansi gambar dan memuat gambar PSD dari disk lokal, kemudian kita akan mengulangi setiap lapisan dalam properti Layer. Kemudian kami akan mengonversi blok ke gambar TIFF. Potongan kode berikut menunjukkan cara mengonversi lapisan gambar PSD ke gambar TIFF.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **Mengkonversi CMYK PSD ke CMYK TIFF**
Menggunakan Aspose.PSD untuk Java, pengembang dapat mengonversi file CMYK PSD ke format tiff CMYK. Artikel ini menunjukkan bagaimana cara mengekspor / mengonversi file CMYK PSD ke format tiff CMYK dengan Aspose.PSD. Menggunakan Aspose.PSD untuk Java Anda dapat memuat gambar PSD dan kemudian Anda dapat mengatur berbagai properti menggunakan kelas TiffOptions dan menyimpan atau mengekspor gambar. Potongan kode berikut menunjukkan cara mencapai fitur ini.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Mengekspor Gambar**
Selain serangkaian rutinitas pemrosesan gambar yang kaya, Aspose.PSD menyediakan kelas-kelas khusus untuk mengonversi format file PSD ke format lain. Dengan menggunakan pustaka ini, konversi gambar PSD sangat sederhana dan intuitif. Berikut adalah beberapa kelas khusus untuk tujuan ini dalam ruang nama ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Mudah untuk mengekspor gambar PSD dengan Aspose.PSD untuk Java API. Yang Anda butuhkan hanyalah objek dari kelas yang sesuai dari ruang nama ImageOptions. Dengan menggunakan kelas-kelas ini, Anda dapat dengan mudah mengekspor gambar apa pun yang dibuat, diedit, atau hanya dimuat dengan Aspose.PSD untuk Java ke format yang didukung.
## **Menggabungkan Gambar**
Contoh ini menggunakan kelas Grafik dan menunjukkan cara menggabungkan dua atau lebih gambar menjadi gambar tunggal lengkap. Untuk mendemonstrasikan operasi, contoh membuat gambar PsdImage baru dan menggambar gambar pada permukaan kanvas menggunakan metode Draw Image yang terekspos oleh kelas Grafik. Dengan menggunakan kelas Grafik, dua atau lebih gambar dapat digabungkan dengan cara sedemikian rupa sehingga gambar hasilnya akan terlihat sebagai gambar lengkap tanpa ruang antara bagian gambar dan tanpa halaman. Ukuran kanvas harus sama dengan ukuran gambar hasil. Berikut adalah demontrasi kode yang menunjukkan cara menggunakan metode Draw Image dari kelas Grafik untuk menggabungkan gambar menjadi gambar tunggal.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Memperluas dan Mencrop Gambar**
API Aspose.PSD memungkinkan Anda untuk memperluas atau mencrop gambar selama proses konversi gambar. Pengembang perlu membuat persegi panjang dengan koordinat X dan Y dan menentukan lebar dan tinggi kotak persegi panjang. Koordinat X,Y dan Lebar, Tinggi dari persegi panjang akan menggambarkan perluasan atau pencrop-an dari gambar yang dimuat. Jika diperlukan memperluas atau mencrop gambar selama konversi gambar, lakukan langkah-langkah berikut:

1. Buat instansi kelas RasterImage dan muat gambar yang ada.
1. Buat Instance kelas ImageOption.
1. Buat instansi kelas Rectangle dan inisialisasi X,Y dan Lebar, Tinggi dari persegi panjang
1. Panggil metode Save dari kelas RasterImage sambil melewati nama file output, opsi gambar, dan objek persegi panjang sebagai parameter.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Membaca dan Menulis Data XMP ke Gambar**
XMP (Extensible Metadata Platform) adalah standar ISO. XMP memstandarisasi model data, format serialisasi, dan properti inti untuk definisi dan pemrosesan metadata yang dapat diperluas. Ini juga memberikan panduan untuk menyematkan informasi XMP ke gambar populer seperti JPEG, tanpa merusak keberbacaan mereka oleh aplikasi yang tidak mendukung XMP. Menggunakan Aspose.PSD untuk Java API, pengembang dapat membaca atau menulis metadata XMP ke gambar. Artikel ini menunjukkan bagaimana metadata XMP dapat dibaca dari gambar dan menulis metadata XMP ke gambar.
### **Buat Metadata XMP, Tulis dan Baca Dari File**
Dengan bantuan ruang nama XMP, pengembang dapat membuat objek metadata XMP dan menulisnya ke gambar. Potongan kode berikut menunjukkan cara menggunakan paket-paket XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage, dan DublinCorePackage yang terkandung dalam ruang nama XMP.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Mengekspor Gambar dalam Lingkungan Berulang**
Aspose.PSD untuk Java sekarang mendukung mengonversi gambar dalam lingkungan berulang. Aspose.PSD untuk Java memastikan kinerja yang dioptimalkan dari operasi selama eksekusi kode dalam lingkungan multi-threaded. Semua kelas opsi gambar (mis. BmpOptions, TiffOptions, JpegOptions, dll.) dalam Aspose.PSD untuk Java mengimplementasikan antarmuka IDisposable. Oleh karena itu penting bagi pengembang untuk membuang objek kelas opsi gambar dengan benar jika properti Source diatur. Potongan kode berikut menunjukkan fungsionalitas yang disebutkan.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}

Aspose.PSD sekarang mendukung properti SyncRoot saat bekerja di lingkungan multi-threaded. Pengembang dapat menggunakan properti ini untuk menyinkronkan akses ke aliran sumber. Potongan kode berikut menunjukkan bagaimana properti SyncRoot dapat digunakan.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

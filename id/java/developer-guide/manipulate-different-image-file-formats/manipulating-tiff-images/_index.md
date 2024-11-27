---
title: Memanipulasi Gambar TIFF
type: docs
weight: 40
url: /id/java/memanipulasi-gambar-tiff/
---

## **Menambahkan Bingkai dengan Pengaturan Berbeda**
TIFF adalah format yang sangat fleksibel dan memungkinkan penambahan bingkai yang berbeda, dengan dimensi, kompresi, dan pengaturan lainnya. API Aspose.PSD memungkinkan Anda untuk menambahkan bingkai TIFF apa pun dengan ukuran apa pun yang membantu dalam membuat dokumen kompleks. Jika ada kebutuhan untuk menyesuaikan bingkai selama proses penambahan untuk membuat semuanya sama, lakukan langkah-langkah berikut:

- Buat bingkai kosong baru dengan opsi yang diinginkan atau salin bingkai sumber dengan opsi keluaran yang ditentukan menggunakan metode CreateFrameFrom.
- Ubah ukuran bingkai/gambar sumber ke dimensi yang diinginkan menggunakan metode Resize.
- Tambahkan piksel bingkai/gambar sumber ke bingkai baru.
- Tambahkan bingkai baru ke gambar TIFF keluaran.

## **Ekspor Lapisan Gambar PSD ke Format File TIFF dengan Banyak Halaman**
Terkadang Anda perlu mengekspor lapisan gambar PSD ke format file TIFF dengan banyak halaman. Artikel ini akan menunjukkan bagaimana kita dapat melakukan tugas ini menggunakan API Aspose.PSD untuk Java. Pertama, kami akan memuat gambar PSD dari disk. Kemudian kami akan mengulangi lapisan gambar PSD dan membuat TiffFrame dari lapisan yang sesuai. Akhirnya kami akan menyimpan gambar TIFF hasilnya ke dalam satu file di disk.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **Konfigurasi TiffOptions**


Pengembang dapat menyesuaikan properti berbeda dari kelas Tiffoptions untuk mendapatkan hasil yang diinginkan. Di dokumen ini, kami akan fokus pada 4 properti utama yang mengontrol atribut gambar hasil.

Properti ini terdaftar di bawah ini.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Setiap kali kami menginisialisasi struktur Tiffoptions kosong, setiap opsi diatur ke nilai defaultnya, misalnya kompresi diatur ke Tidak Ada, BitsPerSample diatur sebagai 1, dan Photometric sebagai MinIsWhite. Menyimpan ke dalam format ini akan membuat gambar akhir hitam dan putih dan ini adalah perilaku yang diharapkan untuk kombinasi opsi tersebut. Untuk mendapatkan hasil berwarna Anda harus mengatur semua properti yang disebutkan di atas ke nilai-nilai yang sesuai dengan ruang warna yang diinginkan atau Anda dapat menginisialisasi struktur Tiffoptions dengan pengaturan yang telah dibahas lebih lanjut dalam artikel ini. Berikut ini adalah tabel yang menggambarkan nilai parameter yang diharapkan yang dapat Anda atur untuk mencapai hasil yang diinginkan. Harap dicatat, Anda harus mengatur keempat kolom ini melalui Tiffoptions untuk menyimpan gambar apa pun yang dimuat/dibuat ke format file TIFF.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palet|LZW/Tidak Terkompresi|1/4/8/16 (palet, mode warna) saluran tunggal|None|
|MinIsWhite/MinIsBlack|LZW/Tidak Terkompresi|1/4/8/16 (mode grayskala) saluran tunggal|None|
|Palet|LZW/Tidak Terkompresi|8 (palet, mode warna) saluran tunggal|Horizontal (kompresi lebih banyak dicapai untuk LZW pola yang sama)|
|MinIsWhite/MinIsBlack|LZW/Tidak Terkompresi|8 (mode grayskala) saluran tunggal|Horizontal (kompresi lebih banyak dicapai untuk LZW pola yang sama)|
|RGB|LZW/Tidak Terkompresi|[8,8,8] (3 saluran RGB)|None/Horizontal|
|RGB|LZW/Tidak Terkompresi|[8,8,8,8] (3 saluran RGB dan saluran alpha tambahan mungkin diatur melalui TiffOptions.AlphaStorage) Sebenarnya, jumlah saluran tambahan apa pun didukung tetapi setiap saluran harus memiliki ukuran bit 8 seperti [8,8,8,8,8,8]|None/Horizontal|
Keempat properti harus diatur melalui TiffOptions untuk menyimpan gambar format apa pun ke format Tiff. Ketika menggunakan kombinasi yang berbeda, beberapa penampil (termasuk Penampil Foto Windows) mungkin menolak merender gambar hasil karena dukungan terbatas yang mereka tawarkan. Dalam kasus tersebut, harap pilih penampil yang berbeda untuk pengujian Anda.
### **Pengaturan Pratentuan untuk Kelas TiffOptions**
Untuk memudahkan pengguna dan menghindari kesalahan konfigurasi dari instance Tiffoptions, API Aspose.PSD untuk Java memiliki konstruktor lain yang menerima parameter bertipe TiffExpectedFormat. Berdasarkan nilai yang dipilih dari enumerasi TiffExpectedFormat, API secara otomatis mengonfigurasi semua properti wajib untuk instance Tiffoptions agar menghasilkan hasil yang diinginkan. Sebelum kita beralih ke kode sampel, berikut ini adalah daftar bidang TiffExpectedFormat dan rincian mereka untuk pemahaman yang lebih baik dari penggunaan.



- TiffExpectedFormat.Default: Mengatur bidang ini ke Default bertindak mirip dengan konstruktor default dari kelas Tiffoptions tanpa kompresi yang diatur dan BitsPerPixel diatur sebagai 1 untuk menghasilkan hasil hitam dan putih. Disarankan untuk menggunakan bidang ini ketika properti spesifik format lainnya harus diatur secara manual sesuai dengan hasil yang diinginkan.
- TiffExpectedFormat.TiffCcitRle: Khusus untuk encoding RLE saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam dan putih).
- TiffExpectedFormat.TiffCcittFax3: Khusus untuk encoding CCITT Fax3 saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam dan putih).
- TiffExpectedFormat.TiffCcittFax4: Khusus untuk encoding CCITT Fax4 saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam dan putih).
- TiffExpectedFormat.TiffDeflateBW: Khusus untuk kompresi Deflate saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam dan putih).
- TiffExpectedFormat.TiffDeflateRGB: Khusus untuk kompresi Deflate saat menyimpan hasil dalam format TIFF RGB (warna).
- TiffExpectedFormat.TiffJpegRGB: Khusus untuk kompresi Jpeg saat menyimpan hasil dalam format TIFF RGB (warna).
- TiffExpectedFormat.TiffJpegYCBCR: Khusus untuk kompresi Deflate saat menyimpan hasil dalam format TIFF YCBCR (warna).
- TiffExpectedFormat.TiffLzwBW: Khusus untuk kompresi LZW saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam dan putih).
- TiffExpectedFormat.TiffLzwRGB: Khusus untuk kompresi LZW saat menyimpan hasil dalam format TIFF RGB (warna).
- TiffExpectedFormat.TiffLzwRGBA: Khusus untuk kompresi LZW saat menyimpan hasil dalam format TIFF RGBA (warna dengan transparansi).
- TiffExpectedFormat.TiffNoCompressionBW: Khusus untuk format TIFF tanpa kompresi saat menyimpan hasil dalam 1 BitsPerPixel (hitam dan putih).
- TiffExpectedFormat.TiffNoCompressionRGB: Khusus untuk format TIFF tanpa kompresi saat menyimpan hasil dalam RGB (warna).
- TiffExpectedFormat.TiffNoCompressionRGBA: Khusus untuk format TIFF tanpa kompresi saat menyimpan hasil dalam RGBA (warna dengan transparansi).



Kode berikut menjelaskan penggunaan bidang TiffExpectedFormat saat membuat sebuah instance dari kelas Tiffoptions.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **Dukungan untuk Kompresi Deflate dan Adobe Deflate**
Format file TIFF (Tagged Image File Format) mendukung berbagai jenis kompresi sedangkan tipe kompresi disimpan sebagai tag (nilai integer) dalam file tersebut. Salah satu metode kompresi tersebut adalah Adobe Deflate (sebelumnya dikenal sebagai Deflate). API Aspose.PSD untuk Java mendukung metode kompresi ini untuk mengekspor & membuat gambar TIFF.
### **Menyimpan Gambar ke dalam TIFF dengan Kompresi Deflate**
Mengonversi gambar yang dimuat ke dalam TIFF dengan kompresi Deflate/Adobe Deflate mudah sebagai berikut.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Membuat TiffImage dengan Kompresi Adobe Deflate**
Contoh di bawah ini menunjukkan penggunaan API Aspose.PSD untuk Java untuk membuat gambar dari awal menggunakan metode kompresi Adobe Deflate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **Mengompresi Gambar TIFF**
API Aspose.PSD untuk Java dapat digunakan untuk mengonversi gambar PSD ke format gambar TIFF dan bahkan mengubah kompresi gambar TIFF hasil. API juga dapat digunakan untuk menyimpan gambar yang berbeda sebagai bingkai dalam gambar TIFF untuk tujuan arsip sambil memampatkan gambar ke ukuran data terendah. Kompresi gambar dalam semua kasus harus dilakukan dengan mengurangi ukuran data sumber terlepas dari algoritma kompresi yang digunakan. Untuk mencapai rasio kompresi terbaik, kita dapat menggunakan ruang warna indeks. Potongan kode berikut memberikan kompresi terbaik menggunakan 16 warna indeks dan algoritma kompresi LZW namun warna sumber sedikit bermuatan.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}

---
title: Memanipulasi Gambar TIFF
type: docs
weight: 50
url: /id/net/memanipulasi-gambar-tiff/
---

## **Menambahkan Bingkai dengan Pengaturan yang Berbeda**
TIFF adalah format yang sangat fleksibel dan memungkinkan penambahan bingkai yang berbeda, dengan dimensi, kompresi, dan pengaturan lainnya yang berbeda. API Aspose.PSD memungkinkan Anda untuk menambahkan bingkai TIFF apa pun dengan ukuran apa pun yang membantu dalam membuat dokumen yang kompleks. Jika ada kebutuhan untuk menyesuaikan bingkai selama proses penambahan untuk membuat mereka semua sama, lakukan langkah-langkah berikut:

- Buat bingkai kosong baru dengan opsi yang diinginkan atau salin bingkai sumber dengan opsi output yang ditentukan menggunakan metode CreateFrameFrom.
- Ubah ukuran bingkai/gambar sumber menjadi dimensi yang diinginkan menggunakan metode Resize.
- Tambahkan piksel bingkai/gambar sumber ke bingkai baru.
- Tambahkan bingkai baru ke gambar TIFF output.

## **Ekspor layer dari gambar PSD ke format file Tiff Multi Page**
Terkadang Anda perlu mengeskpor layer gambar PSD ke format file Tiff multi-halaman. Artikel ini akan menjelaskan bagaimana kita dapat melakukan tugas ini menggunakan Aspose.PSD untuk API .NET. Pertama, kami akan memuat gambar PSD dari disk. Kemudian kami akan mengulangi layer gambar PSD dan membuat TiffFrame dari layer yang sesuai. Akhirnya kami akan menyimpan gambar Tiff hasil ke file tunggal di disk.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **Konfigurasi TiffOptions**
Pengembang dapat menyesuaikan berbagai properti dari kelas [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) untuk mendapatkan hasil yang diinginkan. Dalam dokumen ini, kami akan fokus pada 4 properti utama yang mengontrol atribut gambar hasil.

Properti ini terdaftar di bawah ini.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Ketika kami menginisialisasi sebuah struktur TiffOptions kosong, setiap opsi diatur ke nilai defaultnya, misalnya kompresi diatur ke Tidak Ada, BitsPerSample diatur sebagai 1 dan Photometric sebagai MinIsWhite. Menyimpan ke format ini akan membuat gambar akhir hitam dan putih dan ini adalah perilaku yang diharapkan untuk kombinasi opsi tersebut. Untuk mendapatkan hasil berwarna, Anda harus mengatur semua properti yang disebutkan di atas ke nilai yang sesuai dengan ruang warna yang diinginkan atau Anda dapat menginisialisasi struktur TiffOptions dengan pengaturan tertentu seperti yang dibahas lebih lanjut dalam artikel ini. Berikut adalah tabel yang menggambarkan nilai parameter yang diharapkan yang bisa Anda set untuk mencapai hasil yang diinginkan. Harap dicatat, Anda harus mengatur semua 4 kolom melalui TiffOptions untuk menyimpan gambar yang dimuat/dibuat ke format file TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Tidak Terkompresi|1/4/8/16 (palet, mode warna) hanya satu saluran|Tidak Ada|
|MinIsWhite/MinIsBlack|LZW/Tidak Terkompresi|1/4/8/16 (mode skala abu-abu) hanya satu saluran|Tidak Ada|
|Palette|LZW/Tidak Terkompresi|8 (palet, mode warna) hanya satu saluran|Horizontal (kompresi lebih baik dicapai untuk LZW pola yang sama)|
|MinIsWhite/MinIsBlack|LZW/Tidak Terkompresi|8 (mode skala abu-abu) hanya satu saluran|Horizontal (kompresi lebih baik dicapai untuk LZW pola yang sama)|
|RGB|LZW/Tidak Terkompresi|[8,8,8] (3 saluran RGB)|Tidak Ada/Horizontal|
|RGB|LZW/Tidak Terkompresi|[8,8,8,8] (3 saluran RGB dan saluran alpha tambahan dapat diatur melalui TiffOptions.AlphaStorage) Sebenarnya, jumlah saluran tambahan apa pun didukung tetapi setiap saluran harus memiliki ukuran bit 8 seperti [8,8,8,8,8,8]|Tidak Ada/Horizontal|
Semua 4 properti harus diatur melalui TiffOptions untuk menyimpan format gambar apa pun ke format Tiff. Saat menggunakan kombinasi yang berbeda, beberapa penampil (termasuk Windows Photo Viewer) mungkin menolak merender gambar akhir karena dukungan terbatas yang mereka tawarkan. Dalam kasus seperti itu, pilih penampil yang berbeda untuk pengujian Anda.

### **Pengaturan Pra-Tentu untuk Kelas TiffOptions**
Untuk memudahkan pengguna dan menghindari salah konfigurasi dari contoh TiffOptions, API Aspose.PSD untuk .NET telah mengekspos konstruktor lain yang menerima parameter dari jenis [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Berdasarkan nilai yang dipilih dari enumerasi TiffExpectedFormat, API secara otomatis mengkonfigurasi semua properti wajib untuk contoh TiffOptions agar menghasilkan hasil yang diinginkan. Sebelum kita beralih ke kode contoh, berikut adalah daftar bidang TiffExpectedFormat dan detailnya untuk pemahaman yang lebih baik.

- TiffExpectedFormat.Default: Mengatur bidang ke Nilai Default bertindak serupa dengan konstruktor default dari kelas TiffOptions tanpa kompresi yang diatur dan BitsPerPixel diatur ke 1 untuk menghasilkan gambar hitam dan putih. Disarankan untuk menggunakan bidang ini ketika properti spesifik format lainnya harus diatur manual sesuai dengan hasil yang diinginkan.
- TiffExpectedFormat.TiffCcitRle: Khusus untuk enkoding RLE saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam putih).
- TiffExpectedFormat.TiffCcittFax3: Khusus untuk enkoding CCITT Fax3 saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam putih).
- TiffExpectedFormat.TiffCcittFax4: Khusus untuk enkoding CCITT Fax4 saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam putih).
- TiffExpectedFormat.TiffDeflateBW: Khusus untuk kompresi Deflate saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam putih).
- TiffExpectedFormat.TiffDeflateRGB: Khusus untuk kompresi Deflate saat menyimpan hasil dalam format TIFF RGB (warna).
- TiffExpectedFormat.TiffJpegRGB: Khusus untuk kompresi Jpeg saat menyimpan hasil dalam format TIFF RGB (warna).
- TiffExpectedFormat.TiffJpegYCBCR: Khusus untuk kompresi Deflate saat menyimpan hasil dalam format TIFF YCBCR (warna).
- TiffExpectedFormat.TiffLzwBW: Khusus untuk kompresi LZW saat menyimpan hasil dalam format TIFF 1 BitsPerPixel (hitam putih).
- TiffExpectedFormat.TiffLzwRGB: Khusus untuk kompresi LZW saat menyimpan hasil dalam format TIFF RGB (warna).
- TiffExpectedFormat.TiffLzwRGBA: Khusus untuk kompresi LZW saat menyimpan hasil dalam format TIFF RGBA (warna dengan transparansi).
- TiffExpectedFormat.TiffNoCompressionBW: Khusus untuk format TIFF tidak terkompresi saat menyimpan hasil dalam 1 BitsPerPixel (hitam putih).
- TiffExpectedFormat.TiffNoCompressionRGB: Khusus untuk format TIFF tidak terkompresi saat menyimpan hasil dalam format RGB (warna).
- TiffExpectedFormat.TiffNoCompressionRGBA: Khusus untuk format TIFF tidak terkompresi saat menyimpan hasil dalam format RGBA (warna dengan transparansi).



Potongan kode berikut menjelaskan penggunaan bidang TiffExpectedFormat saat membuat contoh kelas TiffOptions.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **Dukungan untuk Kompresi Deflate dan Adobe Deflate**
Format file TIFF (Tagged Image File Format) mendukung berbagai jenis kompresi sedangkan jenis kompresi disimpan sebagai tag (nilai integer) dalam file. Salah satu metode kompresi tersebut adalah Adobe Deflate (sebelumnya dikenal sebagai Deflate). API Aspose.PSD untuk .NET mendukung metode kompresi ini untuk mengekspor & membuat gambar TIFF.
### **Menyimpan Gambar ke TIFF dengan Kompresi Deflate**
Mengonversi gambar yang dimuat ke TIFF dengan kompresi Deflate/Adobe Deflate mudah seperti berikut.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Membuat TiffImage dengan Kompresi Adobe Deflate**
Contoh di bawah ini menunjukkan penggunaan API Aspose.PSD untuk .NET untuk membuat gambar dari awal menggunakan metode kompresi Adobe Deflate.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **Mengompresi Gambar TIFF**
API Aspose.PSD untuk .NET dapat digunakan untuk mengonversi gambar PSD ke format gambar TIFF dan bahkan mengubah kompresi dari gambar TIFF yang dihasilkan. API juga dapat digunakan untuk menyimpan berbagai gambar sebagai bingkai dalam gambar TIFF untuk tujuan arsip sambil mengompresi gambar ke ukuran data terendah. Kompresi gambar dalam setiap kasus harus dilakukan dengan mengurangi ukuran data sumber terlepas dari algoritma kompresi yang digunakan. Untuk mencapai rasio kompresi terbaik kita dapat menggunakan ruang warna pada indeks. Potongan kode berikut memberikan kompresi terbaik menggunakan 16 warna indeks saja dan algoritma kompresi LZW, namun warna sumber sedikit diterapkan pola.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}

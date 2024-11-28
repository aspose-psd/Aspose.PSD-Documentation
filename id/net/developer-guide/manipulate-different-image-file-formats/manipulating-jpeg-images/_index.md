---
title: Memanipulasi Gambar JPEG
type: docs
weight: 30
url: /id/memanipulasi-gambar-jpeg/
---

## **Menggunakan Kelas ExifData untuk Membaca dan Mengubah Tag EXIF Jpeg**
Hampir semua kamera digital (termasuk ponsel pintar), pemindai, dan sistem lain yang menangani gambar menyimpan gambar dengan informasi EXIF (Exchangeable Image File). Pengaturan kamera dan informasi seputar adegan direkam oleh kamera ke dalam file gambar. Data EXIF juga mencakup kecepatan shutter, tanggal dan waktu pengambilan foto, panjang fokus, kompensasi paparan, pola metering, dan apakah flash digunakan. API Aspose.Imaging telah memungkinkan untuk mengekstrak informasi EXIF dari gambar yang diberikan dengan cara yang sangat mudah dan sederhana. Pengembang juga dapat menulis data EXIF ke gambar atau mengubah informasi yang ada sesuai kebutuhan mereka. Aspose.PSD telah menyediakan [Kelas ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) untuk membaca, menulis, dan mengubah data EXIF, sementara namespace [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) berisi enumerasi yang relevan yang digunakan dalam proses tersebut.
### **Membaca Data EXIF**
API Aspose.PSD menyediakan cara untuk membaca data EXIF dari gambar yang diberikan. Langkah-langkah yang diberikan di bawah ini menggambarkan penggunaan kelas ExifData untuk membaca informasi EXIF dari sebuah gambar.

- Muat Gambar PSD menggunakan metode pabrik Load.
- Temukan gambar mini Jpeg di antara sumber daya PSD.
- Ekstrak sebuah instansi kelas ExifData.

Ambil informasi yang diperlukan dan tulis ke konsol.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}

Alternatifnya, pengembang juga dapat mendapatkan informasi spesifik menggunakan potongan kode berikut.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Menulis & Mengubah Data EXIF**
Dengan menggunakan API Aspose.PSD, pengembang dapat menulis informasi EXIF baru dan mengubah data EXIF yang ada dari sebuah gambar. Kedua proses (Menulis & Mengubah) memerlukan muatan gambar dan mendapatkan data EXIF ke dalam sebuah instansi kelas ExifData. Kemudian, pengguna dapat mengakses properti-properti yang terbuka oleh kelas ExifData untuk mengatur properti tersebut. Harap dicatat bahwa gambar-gambar untuk dimanipulasi harus berupa gambar Jpeg atau Tiff yang biasanya adalah miniatur PSD. Kode contoh untuk menunjukkan penggunaannya adalah sebagai berikut:




{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Mengekstrak miniatur dari sumber daya PSD**
Miniatur adalah versi berukuran lebih kecil dari gambar, yang digunakan untuk menampilkan bagian penting dari gambar bukan seluruh bingkainya. Beberapa file gambar (terutama yang diambil dengan kamera digital) memiliki gambar miniatur yang disematkan dalam file. API Aspose.PSD memungkinkan kamu untuk mengekstrak miniatur sumber daya PSD dan menyimpannya secara terpisah di disk. Sumber daya miniatur mengandung properti [Miniatur](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) ExifData yang dapat mengambil data miniatur. Potongan kode berikut ini menunjukkan bagaimana cara menggunakannya.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Gunakan pendekatan yang telah dibahas di atas untuk menyimpan miniatur ke format file lain yang didukung. Jika kamu ingin mengekspor data miniatur ke format gambar lain seperti BMP & PNG, silakan gunakan opsi ekspor gambar lainnya.


### **Mengekstrak miniatur dari segmen JFIF**
Juga memungkinkan untuk mengekstrak miniatur dari segmen ExifData atau JFIF dari sumber daya miniatur PSD. Potongan kode berikut menunjukkan bagaimana melakukan ekstraksi data miniatur dari segmen JFIF atau ExifData:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Gunakan pendekatan yang telah dibahas di atas untuk menyimpan miniatur ke format file lain yang didukung. Jika kamu ingin mengekspor data miniatur ke format gambar lain seperti BMP & PNG, silakan gunakan opsi ekspor gambar lainnya.
### **Menambahkan Miniatur ke Segmen JFIF**
Potongan kode di bawah ini menunjukkan bagaimana menggunakan properti JFIF. Miniatur untuk menambahkan gambar miniatur ke segmen JFIF dari gambar PSD yang dimuat.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Gambar miniatur dengan data segmen lainnya tidak boleh lebih dari 65.545 byte karena spesifikasi format JPEG. Dalam kasus di mana gambar besar akan diatur sebagai miniatur, pengecualian dapat muncul.


### **Menambahkan Miniatur ke Segmen EXIF**
Potongan kode di bawah ini menunjukkan cara menggunakan properti ExifData.Miniatur untuk menambahkan gambar miniatur ke segmen EXIF dari gambar PSD yang dimuat.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


Dalam hal ini, API Aspose.PSD tidak dapat memperkirakan ukuran gambar miniatur, tetapi dapat memeriksa ukuran seluruh segmen data EXIF. Ini tidak boleh lebih besar dari 65.535 byte.
## **Menggunakan Kelas JpegExifData untuk Membaca dan Mengubah Tag EXIF Jpeg**
API Aspose.PSD menyediakan kelas [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) yang secara eksklusif untuk format gambar Jpeg untuk mengambil & memperbarui informasi EXIF. Artikel ini menunjukkan penggunaan kelas JpegExifData untuk mencapai hal yang sama. Kelas Aspose.PSD.Exif.JpegExifData berfungsi sebagai wadah data EXIF untuk gambar Jpeg, dan memberikan cara untuk mendapatkan tag EXIF Jpeg standar sebagaimana ditunjukkan di bawah ini:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Daftar Lengkap Tag EXIF**
Potongan kode di atas membaca beberapa Tag EXIF menggunakan properti yang ditawarkan oleh kelas Aspose.PSD.Exif.JpegExifData. Daftar lengkap dari properti-properti ini tersedia di sini. Kode berikut akan membaca semua tag EXIF menggunakan [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) class.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Otomatis Koreksi Orientasi Gambar JPEG**


Foto dapat diambil dengan kamera yang diputar 90°, 180°, 270°, atau tidak ada (orientasi normal). Sebagian besar kamera digital menyimpan informasi orientasi bersama dengan data gambar sebagai tag EXIF dari gambar JEPG. Informasi ini dapat digunakan untuk melakukan rotasi otomatis pada gambar untuk mengoreksi orientasi. API Aspose.PSD menyediakan metode AutoRotate untuk kelas JpegImage untuk secara otomatis mengoreksi orientasi gambar JPEG. Berikut adalah cara menggunakan metode AutoRotate dengan API Aspose.PSD untuk .NET.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Dukungan untuk JPEG-LS dengan CMYK dan YCCK**


API Aspose.PSD untuk .NET menyediakan dukungan untuk model warna CMYK dan YCCK dengan JPEG-LS. Potongan kode di bawah ini menggambarkan cara menggunakan dukungan untuk JPEG-LS tersebut.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Dukungan untuk 2-7 bit per sampel dalam gambar JPEG-LS**


API Aspose.PSD untuk .NET menyediakan dukungan untuk gambar JPEG-LS dengan 2-7 bit per sampel. Potongan kode di bawah ini menggambarkan cara menggunakan dukungan tersebut untuk JPEG-LS.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Mengatur Jenis Warna dan Jenis Kompresi untuk gambar JPEG**


API Aspose.PSD untuk .NET menyediakan dukungan untuk Jenis Warna dan Jenis Kompresi serta mengaturnya sebagai skala abu-abu dan progresif untuk gambar JPEG. Potongan kode di bawah ini menggambarkan cara menggunakan dukungan tersebut.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}




Potongan kode di bawah ini menunjukkan bagaimana menggunakan properti ExifData.Miniatur untuk menambahkan gambar miniatur ke segmen EXIF dari gambar PSD yang dimuat.



{{< gist "aspose-com-gists" "8a4d34eep5a8c679246ce9c7oce9" "Examples-CSharT-Apsoe-ModiyingAnConvetingIng-SPEG-ddThumbnailToEXIfSegent-ddThumbnailToEXIfSeent.cs" >}}




Mencapai ini, API Aspose.PSD tidak dapat memperkirakan ukuran gambar miniatur, namun dapat memeriksa ukuran seluruh segmen data EXIF. Ukurannya tidak dapat lebih besar dari 65.535 byte.

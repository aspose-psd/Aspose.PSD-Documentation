---
title: Memanipulasi Gambar JPEG
type: docs
weight: 20
url: /id/java/memanipulasi-gambar-jpeg/
---

## **Menggunakan Kelas ExifData untuk Membaca dan Memodifikasi Tag EXIF JPEG**


Hampir semua kamera digital (termasuk ponsel pintar), pemindai, dan sistem lain yang menangani gambar menyimpan gambar dengan informasi EXIF (Exchangeable Image File). Pengaturan kamera dan informasi adegan direkam oleh kamera ke dalam file gambar. Data EXIF juga mencakup kecepatan rana, tanggal dan waktu pengambilan foto, panjang fokus, kompensasi paparan, pola pengukuran, dan apakah flash digunakan. API Aspose.Imaging telah memungkinkan untuk mengekstrak informasi EXIF dari gambar yang diberikan dengan cara yang sangat mudah dan sederhana. Pengembang juga dapat menulis data EXIF ke gambar atau memodifikasi informasi yang ada sesuai dengan kebutuhan mereka. Aspose.Imaging telah menyediakan kelas ExifData untuk membaca, menulis, dan memodifikasi data EXIF, di mana namespace Aspose.PSD.Exif.Enums berisi enumerasi yang relevan yang digunakan dalam proses.
### **Membaca Data EXIF**
API Aspose.PSD menyediakan cara untuk membaca data EXIF dari gambar yang diberikan. Langkah-langkah yang disediakan di bawah ini mengilustrasikan penggunaan kelas ExifData untuk membaca informasi EXIF dari sebuah gambar.

- Memuat Gambar PSD menggunakan metode pabrik Load.
- Temukan gambar miniatur JPEG di antara sumber daya PSD.
- Ekstrak sebuah instansi kelas ExifData.

Dapatkan informasi yang diperlukan dan tulis ke konsol.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



Alternatifnya, pengembang juga dapat mengambil informasi khusus menggunakan potongan kode berikut.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Menulis dan Memodifikasi Data EXIF**
Dengan menggunakan API Aspose.PSD, pengembang dapat menulis informasi EXIF baru dan memodifikasi data EXIF yang ada dari sebuah gambar. Kedua proses (Menulis & Memodifikasi) memerlukan memuat gambar dan mendapatkan data EXIF ke dalam sebuah instansi kelas ExifData. Kemudian, seseorang dapat mengakses properti yang diekspos oleh kelas ExifData untuk mengaturnya secara sesuai. Harap dicatat bahwa gambar untuk dimanipulasi harus berupa gambar JPEG atau TIFF yang biasanya adalah miniatur PSD. Kode sampel untuk mendemonstrasikan penggunaan adalah sebagai berikut:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Mengekstrak Thumbnail dari Sumber Daya PSD**
Thumbnail adalah versi berukuran lebih kecil dari gambar, digunakan untuk menampilkan bagian penting dari gambar daripada bingkai penuh. Beberapa file gambar (terutama yang diambil dengan kamera digital) memiliki gambar miniatur tertanam di dalam file. API Aspose.PSD memungkinkan Anda untuk mengekstrak miniatur sumber daya PSD dan menyimpannya terpisah di disk. Sumber daya thumbnail berisi properti ExifData.Thumbnail yang dapat mengambil data thumbnail. Potongan kode di bawah ini mendemonstrasikan cara menggunakannya.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Gunakan pendekatan yang dibahas di atas untuk menyimpan thumbnail ke format file lain yang didukung. Jika Anda ingin mengekspor data thumbnail ke format gambar lain seperti BMP & PNG, harap gunakan opsi ekspor gambar lain.
### **Mengekstrak Thumbnail dari Segmen JFIF**
Juga memungkinkan untuk mengekstrak thumbnail dari segmen ExifData atau JFIF dari sumber daya thumbnail PSD. Kode berikut menunjukkan bagaimana melakukan ekstraksi data thumbnail dari segmen JFIF atau ExifData:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Gunakan pendekatan yang dibahas di atas untuk menyimpan thumbnail ke format file lain yang didukung. Jika Anda ingin mengekspor data thumbnail ke format gambar lain seperti BMP & PNG, harap gunakan opsi ekspor gambar lain.
### **Menambahkan Thumbnail ke Segmen JFIF**
Potongan kode di bawah ini mendemonstrasikan cara menggunakan properti JFIF.Thumbnail untuk menambahkan gambar thumbnail ke segmen JFIF dari gambar PSD yang dimuat.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Gambar thumbnail dengan data segmen lain tidak dapat mencapai lebih dari 65.545 byte karena spesifikasi format JPEG. Dalam kasus di mana gambar besar akan diatur sebagai thumbnail, mungkin timbul pengecualian.


### **Menambahkan Thumbnail ke Segmen EXIF**
Potongan kode di bawah ini menunjukkan cara menggunakan properti ExifData.Thumbnail untuk menambahkan gambar thumbnail ke segmen EXIF dari gambar PSD yang dimuat.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

Dalam hal ini, API Aspose.PSD tidak dapat memperkirakan ukuran gambar thumbnail, tetapi dapat memeriksa ukuran seluruh segmen data EXIF. Ini tidak boleh lebih besar dari 65.535 byte.
## **Menggunakan Kelas JpegExifData untuk Membaca dan Memodifikasi Tag EXIF JPEG**
API Aspose.PSD menyediakan kelas JpegExifData yang eksklusif untuk format gambar JPEG untuk mengambil & memperbarui informasi EXIF. Artikel ini mendemonstrasikan penggunaan kelas JpegExifData untuk mencapai hal yang sama. Kelas Aspose.PSD.Exif.JpegExifData berfungsi sebagai wadah data EXIF untuk gambar JPEG, dan menyediakan cara untuk mengambil tag EXIF JPEG standar seperti yang ditunjukkan di bawah ini:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Daftar Lengkap Tag EXIF**
Potongan kode di atas membaca beberapa Tag EXIF menggunakan properti yang ditawarkan oleh kelas Aspose.PSD.Exif.JpegExifData. Daftar lengkap dari properti ini tersedia di sini. Kode berikut akan membaca semua tag EXIF menggunakan kelas System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Mengoreksi Otomatis Orientasi Gambar JPEG**
Foto dapat diambil dengan kamera yang diputar 90°, 180°, 270°, atau tidak sama sekali (orientasi normal). Kebanyakan kamera digital menyimpan informasi orientasi bersama dengan data gambar sebagai tag EXIF pada gambar JPEG. Informasi ini dapat digunakan untuk melakukan rotasi otomatis pada gambar untuk mengoreksi orientasi. API Aspose.PSD menyediakan metode AutoRotate untuk kelas JpegImage untuk mengoreksi otomatis orientasi gambar JPEG. Berikut cara menggunakannya dengan metode AutoRotate dengan Aspose.PSD untuk API Java.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Dukungan untuk JPEG-LS dengan CMYK dan YCCK**


API Aspose.PSD untuk Java menyediakan dukungan untuk model warna CMYK dan YCCK dengan JPEG-LS. Potongan kode di bawah ini menunjukkan cara menggunakan dukungan tersebut untuk JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Dukungan untuk 2-7 bit per sampel dalam gambar JPEG-LS**


API Aspose.PSD untuk Java menyediakan dukungan untuk gambar JPEG-LS dengan 2-7 bit per sampel. Potongan kode di bawah ini menunjukkan cara menggunakan dukungan tersebut untuk JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Mengatur Jenis Warna dan Jenis Kompresi untuk gambar JPEG**




API Aspose.PSD untuk Java menyediakan dukungan untuk Tipe Warna dan Tipe Kompresi dan mengatur mereka sebagai skala abu-abu dan progresif untuk gambar JPEG. Potongan kode di bawah ini menunjukkan cara menggunakan dukungan tersebut.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}



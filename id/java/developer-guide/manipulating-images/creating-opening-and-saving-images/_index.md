---
title: Membuat, Membuka, dan Menyimpan Gambar
type: docs
weight: 30
url: /id/java/membuat-membuka-dan-menyimpan-gambar/
---

## **Membuat File Gambar**
Aspose.PSD untuk Java memungkinkan pengembang membuat gambar mereka sendiri. Gunakan metode Create statis yang diungkapkan oleh kelas Image untuk membuat gambar baru. Yang perlu Anda lakukan hanyalah menyediakan objek yang sesuai dari salah satu kelas dari namespace ImageOptions untuk format gambar output yang diinginkan. Untuk membuat file gambar, pertama-tama buat instansi dari salah satu kelas dari namespace ImageOptions. Kelas-kelas ini menentukan format gambar output. Berikut adalah beberapa kelas dari namespace ImageOptions (perhatikan bahwa saat ini hanya keluarga format file PSD yang didukung untuk pembuatan):

PsdOptions menetapkan opsi untuk membuat file PSD. File gambar dapat dibuat dengan menetapkan path output atau dengan menetapkan stream.
### **Membuat dengan Mengatur Path**
Buat PsdOptions dari namespace ImageOptions dan atur berbagai properti. Properti yang paling penting untuk diatur adalah properti Source. Properti ini menentukan di mana data gambar berada (di file atau stream). Dalam contoh di bawah, sumbernya adalah file. Setelah mengatur properti, lewatkan objek ke salah satu metode Create statis bersama dengan parameter lebar dan tinggi. Lebar dan tinggi didefinisikan dalam piksel.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Membuat Menggunakan Stream**
Proses untuk membuat gambar menggunakan stream sama seperti menggunakan path. Satu-satunya perbedaannya adalah Anda perlu membuat instansi StreamSource dengan melewatkan objek Stream ke konstruktor dan menetapkannya ke properti Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Membuka File Gambar**
Pengembang dapat menggunakan API Aspose.PSD untuk Java untuk membuka file gambar PSD yang ada untuk berbagai tujuan, seperti menambahkan efek ke gambar atau mengonversi file yang ada ke format lain. Apapun tujuannya, Aspose.PSD menyediakan dua cara standar untuk membuka file yang ada: dari file atau dari sebuah stream.
### **Membuka dari Disk**
Buka file gambar dengan melewatkan path dan nama file sebagai parameter ke metode statis Load yang diungkapkan oleh kelas Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Membuka Menggunakan Stream**
Terkadang gambar yang perlu kita buka disimpan sebagai stream. Dalam kasus seperti itu, gunakan versi yang di-overload dari metode Load. Ini menerima objek Stream sebagai argumen untuk membuka gambar.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Muat Gambar sebagai Layer**
Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk memuat gambar sebagai layer. API Aspose.PSD telah mengungkapkan metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD telah mengungkapkan metode AddLayer dari kelas PsdImage untuk menambahkan gambar ke dalam file PSD sebagai layer.

Langkah-langkah untuk memuat gambar ke dalam PSD sebagai layer adalah sebagai berikut:

- Buat instansi gambar menggunakan kelas PsdImage dengan lebar dan tinggi yang ditentukan.
- Muat file PSD sebagai gambar menggunakan metode fakultas Load yang diungkapkan oleh kelas Image.
- Buat instansi kelas Layer dan berikan layer gambar PSD ke dalamnya.
- Tambahkan layer yang dibuat menggunakan metode AddLayer yang diungkapkan oleh kelas PsdImage
- Simpan hasilnya.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Menyimpan File Gambar**
Aspose.PSD memungkinkan Anda membuat file gambar dari awal. Ini juga menyediakan cara untuk mengedit file gambar yang ada. Setelah gambar dibuat atau diubah, file biasanya disimpan ke disk. Aspose.PSD menyediakan metode untuk menyimpan gambar ke disk dengan menentukan path atau menggunakan objek Stream.
### **Menyimpan ke Disk**
Kelas Image mewakili objek gambar, sehingga kelas ini menyediakan semua alat yang diperlukan untuk membuat, memuat, dan menyimpan file gambar. Gunakan metode Save kelas Image untuk menyimpan gambar. Satu versi yang di-overload dari metode Save menerima lokasi file sebagai string.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Menyimpan ke Stream**
Versi lain yang di-overload dari metode Save menerima objek Stream sebagai argumen dan menyimpan file gambar ke stream.

Jika gambar dibuat dengan menentukan salah satu CreateOptions dalam konstruktor Image, gambar secara otomatis disimpan ke path atau stream yang disediakan selama inisialisasi kelas Image dengan memanggil metode Save yang tidak menerima parameter apa pun.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Pengaturan untuk Mengganti Font yang Hilang**
Pengembang dapat menggunakan API Aspose.PSD untuk Java untuk memuat file gambar PSD yang ada untuk berbagai tujuan, misalnya untuk menetapkan nama font default saat menyimpan dokumen PSD sebagai gambar raster (ke format PNG, JPG, dan BMP). Font default ini harus digunakan sebagai pengganti untuk semua font yang hilang (font yang tidak ditemukan dalam Sistem Operasi saat ini). Setelah gambar dimodifikasi, file akan disimpan ke disk.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}



---
title: Membuat, Membuka, dan Menyimpan Gambar
type: docs
weight: 30
url: /id/net/membuat-membuka-dan-menyimpan-gambar/
---

## **Membuat Berkas Gambar**
Aspose.PSD untuk .NET memungkinkan pengembang untuk membuat gambar mereka sendiri. Gunakan metode Create statis yang terpapar oleh kelas Gambar untuk membuat gambar baru. Yang perlu Anda lakukan hanyalah menyediakan objek yang sesuai dari salah satu kelas dari namespace ImageOptions untuk format gambar output yang diinginkan. Untuk membuat sebuah berkas gambar, pertama-tama buat instansi dari salah satu kelas dari namespace ImageOptions. Kelas-kelas ini menentukan format gambar output. Berikut adalah beberapa kelas dari namespace ImageOptions (perlu diingat bahwa saat ini hanya keluarga format file PSD yang didukung untuk pembuatan):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) menetapkan opsi untuk membuat berkas PSD. Berkas gambar dapat dibuat dengan menetapkan jalur output atau dengan menetapkan aliran.
### **Membuat dengan Menetapkan Jalur**
Buat PsdOptions dari namespace [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) dan tentukan berbagai properti. Properti yang paling penting untuk ditetapkan adalah properti Source. Properti ini menentukan di mana data gambar berada (di dalam berkas atau aliran). Pada contoh di bawah, sumbernya adalah berkas. Setelah menetapkan properti, lewatkan objek tersebut ke salah satu metode statis [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) bersama dengan parameter lebar dan tinggi. Lebar dan tinggi didefinisikan dalam piksel.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Membuat dengan Menggunakan Aliran**
Proses untuk membuat gambar menggunakan aliran sama dengan menggunakan jalur. Satu-satunya perbedaan adalah Anda perlu membuat instansi [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) dengan melewatkan objek Aliran ke konstrukturnya dan menetapkannya ke properti Sumber.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Membuka Berkas Gambar**
Pengembang dapat menggunakan API Aspose.PSD untuk .NET untuk membuka berkas gambar PSD yang ada untuk berbagai tujuan, seperti menambahkan efek ke gambar atau mengonversi berkas yang ada ke format lain. Apapun tujuannya, Aspose.PSD menyediakan dua cara standar untuk membuka berkas yang ada: dari berkas atau dari aliran.
### **Membuka dari Disk**
Buka berkas gambar dengan melewatkan jalur dan nama berkas sebagai parameter ke metode statis Load yang terpapar oleh kelas Gambar.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Membuka dengan Menggunakan Aliran**
Terkadang gambar yang perlu kita buka disimpan sebagai aliran. Dalam kasus seperti itu, gunakan versi overload dari metode Load. Ini menerima objek Aliran sebagai argumen untuk membuka gambar.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Muat Gambar sebagai Layer**
Artikel ini menunjukkan penggunaan Aspose.PSD untuk memuat gambar sebagai lapisan. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD telah mengekspos metode AddLayer dari kelas PsdImage untuk menambahkan gambar ke berkas PSD sebagai lapisan.

Langkah-langkah untuk memuat gambar ke dalam PSD sebagai lapisan adalah sebagai berikut:

- Buat instansi gambar menggunakan kelas PsdImage dengan lebar dan tinggi tertentu.
- Muat berkas PSD sebagai gambar menggunakan metode fabrik Load yang terpapar oleh kelas Gambar.
- Buat instansi kelas Layer dan berikan lapisan gambar PSD kepadanya.
- Tambahkan lapisan yang dibuat menggunakan metode AddLayer yang terpapar oleh kelas PsdImage.
- Simpan hasilnya.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Muat Gambar Sebagai Lapisan dari Sebuah Aliran**
Artikel ini menunjukkan penggunaan Aspose.PSD untuk memuat gambar sebagai lapisan dari sebuah aliran. Untuk memuat gambar dari sebuah aliran, cukup lewatkan objek aliran yang berisi gambar ke konstruktor kelas Layer. Tambahkan lapisan yang dibuat menggunakan AddLayer yang terpapar oleh kelas PsdImage dan simpan hasilnya.


Berikut adalah contoh kode.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Menyimpan Berkas Gambar**
Aspose.PSD memungkinkan Anda membuat berkas gambar dari awal. Ini juga memberikan cara untuk mengedit berkas gambar yang sudah ada. Setelah gambar dibuat atau diubah, biasanya berkas tersebut disimpan ke disk. Aspose.PSD menyediakan Anda dengan metode untuk menyimpan gambar ke disk dengan menentukan sebuah jalur atau menggunakan objek Aliran.
### **Menyimpan ke Disk**
Kelas Gambar mewakili objek gambar, jadi kelas ini menyediakan semua alat yang diperlukan untuk membuat, memuat, dan menyimpan berkas gambar. Gunakan metode Simpan kelas Gambar untuk menyimpan gambar. Salah satu versi overload dari metode Simpan menerima lokasi berkas sebagai string.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Menyimpan ke Sebuah Aliran**
Versi overload lain dari metode Simpan menerima objek Aliran sebagai argumen dan menyimpan berkas gambar ke dalam aliran.

Jika gambar dibuat dengan menentukan salah satu CreateOptions dalam konstruktor Gambar, gambar tersebut secara otomatis disimpan ke jalur atau aliran yang disediakan selama inisialisasi kelas Gambar dengan memanggil metode Simpan yang tidak menerima parameter apapun.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Pengaturan untuk Mengganti Font yang Hilang**
Pengembang dapat menggunakan API Aspose.PSD untuk .NET untuk memuat berkas gambar PSD yang ada untuk berbagai tujuan, misalnya, untuk menetapkan nama font default saat menyimpan dokumen PSD sebagai gambar raster (ke dalam format PNG, JPG, dan BMP). Font default ini harus digunakan sebagai pengganti semua font yang hilang (font yang tidak ditemukan dalam Sistem Operasi saat ini). Setelah gambar dimodifikasi, berkas akan disimpan ke disk.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}

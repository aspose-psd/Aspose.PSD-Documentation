---
title: Cara Menggunakan Warp di Aspose.PSD
type: docs
weight: 40
url: /id/net/cara-menggunakan-warp-di-aspose-psd/
---

## **Bagian 1 – Merender Berkas PSD dengan Efek Warp**

Photoshop menyimpan gambar yang dirender setelah menerapkan efek Warp. Perpustakaan kami dapat mereproduksi atau merender kembali gambar dengan efek Warp. Untuk mengaktifkan fitur ini, cukup atur flag AllowWarpRepaint di pengaturan saat membuka berkas PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentasi-Aspose-PSD-Warp-Merender-1.cs" >}}

Hasil:
![Hasil Warp Aspose.PSD untuk .NET 1](warp1.png)

Selain merender efek Warp untuk SmartLayers, perpustakaan kami juga mendukung Warp untuk TextLayers. Kode implementasinya tetap sama, satu-satunya perbedaannya adalah dalam nama berkas.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentasi-Aspose-PSD-Warp-Merender-2.cs" >}}

Hasil:
![Haspose.PSD untuk .NET Warp Result 2](warp2.png)

**! Catatan: ** Saat ini, perpustakaan kami mendukung merender Custom Warp (dimana pengguna memanipulasi titik mesh) dan semua jenis Warp standar.
* - Saat ini, perpustakaan kami mendukung Custom Warp dengan mesh standar, dan kami sedang aktif bekerja untuk memperluas dukungan kami untuk memasukkan semua jenis mesh di masa mendatang.


## **Bagian 2 – Memodifikasi Efek Warp**

Perpustakaan kami memungkinkan Anda tidak hanya merender tetapi juga memodifikasi (menambahkan) efek Warp.
Modifikasi ini difasilitasi melalui fitur kelas **WarpParams**.

| **Fitur**   | **Deskripsi**                                                         | 
|:-----------:|:---------------------------------------------------------------------|
| Batas       | Mengembalikan batas gambar yang distorsi.                            |
| TitikMesh   | Sebuah array titik, dengan setiap titik mewakili sebuah titik sudut mesh distorsi.  |
| Nilai       | Nilai efek Warp untuk efek Warp non-Custom.                          |
| PutarWarp   | Sebuah enumerasi yang mendefinisikan arah efek Warp non-Custom.      |
| GayaWarp    | Sebuah enumerasi yang mendefinisikan jenis efek Warp.                |

Contoh kode di bawah ini menunjukkan bagaimana menentukan jenis efek Warp untuk Lapisan Pintar dan menyesuaikan jenis dan intensitas distorsi untuk efek tersebut.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentasi-Aspose-PSD-Warp-Merender-3.cs" >}}

Hasil:
![Hasil Warp Aspose.PSD untuk .NET 3](warp3.png)

## **Bagian 3 – Menambahkan Efek Warp**

Contoh kode di bawah ini menunjukkan cara menambahkan efek Warp standar ke Lapisan Pintar.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentasi-Aspose-PSD-Warp-Merender-4.cs" >}}

Hasil:
![Hasil Warp Aspose.PSD untuk .NET 4](warp4.png)

Contoh kode di bawah ini menunjukkan cara menambahkan efek Warp Custom ke Lapisan Pintar.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentasi-Aspose-PSD-Warp-Merender-5.cs" >}}

Hasil:
![Hasil Warp Aspose.PSD untuk .NET 5](warp5.png)

Contoh kode di bawah ini menunjukkan cara menambahkan efek Warp ke Lapisan Teks. 
**! Catatan:** Menurut standar Photoshop, efek Warp untuk Lapisan Teks biasanya terbatas pada tipe standar. Namun, perpustakaan kami mendukung penggunaan dua jenis efek Warp. Harap perhatikan bahwa berkas seperti ini mungkin tidak sepenuhnya kompatibel dengan Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentasi-Aspose-PSD-Warp-Merender-6.cs" >}}

Hasil:
![Hasil Warp Aspose.PSD untuk .NET 6](warp6.png)

Kami terus melakukan penyempurnaan dan perluasan kemampuan efek Warp kami, dengan fokus pada meningkatkan kecepatan, kualitas, dan fungsionalitas yang didukung. Tetap up-to-date dengan rilis bulanan kami untuk perkembangan terbaru.
Tim Aspose.PSD Anda

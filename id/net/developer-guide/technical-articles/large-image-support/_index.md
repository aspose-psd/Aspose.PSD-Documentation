---
title: Dukungan Gambar Besar
type: docs
weight: 40
url: /id/net/dukungan-gambar-besar/
---

## **Dukungan Gambar Besar**
Karena perpustakaan standar .NET memiliki beberapa keterbatasan terkait ukuran gambar yang dapat diproses, kami memperkenalkan mekanisme baru untuk mendukung gambar besar. Pendekatan baru ini mengatasi batasan namun karena batasan ukuran data, dimensi maksimum yang didukung untuk pembuatan dan pengambilan adalah 2.147.483.647 x 2.147.483.647 piksel.
### **Bekerja dengan Gambar Besar**
Aspose.PSD telah meningkatkan kinerja dan dukungan untuk gambar besar. Gambar yang berukuran ratusan megabita tidak lagi menjadi masalah sehingga Anda dapat membuat, memuat, dan menggambar di atas gambar tersebut. Namun, karena pemrosesan parsial dan penanganan pengecualian OutOfMemoryException, kinerja mungkin sangat rendah pada gambar yang sangat besar. Hal ini disebabkan oleh fakta bahwa Aspose.PSD mencoba untuk mengalokasikan kembali jumlah data yang lebih kecil untuk diproses dan setiap langkah pengalokasian ulang menjadi sangat mahal. Manfaat dari arsitektur baru ini jelas:

- Tidak ada batasan ukuran gambar.
- Anda tidak terbatas pada memori yang tersedia di PC Anda.

Jika Anda mengalami pemrosesan yang lambat, disarankan untuk meningkatkan total jumlah RAM agar semua piksel muat ke dalam memori. Jika tidak, pemrosesan tetap mungkin tetapi lebih lambat. Pendekatannya adalah sebagai berikut:

- Panggil metode [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) dengan persegi panjang yang diinginkan dan delegasi untuk menerima piksel yang dimuat yang ditentukan.

Aspose.PSD mencoba untuk memuat seluruh persegi panjang.

- Jika ada cukup memori untuk muat semua piksel, maka semua piksel akan dikembalikan kepada pemanggil.
- Jika tidak cukup memori, pemanggil menerima subset piksel dari dalam persegi yang ditentukan. Ketika piksel-piksel tersebut telah diproses, pemanggil menerima persegi berikutnya. Pemrosesan berakhir ketika seluruh persegi telah diproses.

Aspose.PSD mencoba untuk mengekstrak sebanyak mungkin baris. Jika tidak cukup memori untuk muat satu baris piksel, maka satu baris akan dibagi menjadi bagian-bagian sesuai dengan persegi yang memiliki tinggi 1. Anda juga dapat menggambar di atas gambar besar. Proses penggambaran mencoba mempengaruhi seluruh persegi yang diinginkan. Jika tidak ada cukup memori, penggambaran dilakukan pada persegi parsial hingga seluruh area digambar. Selain itu, Aspose.PSD mendukung penyimpanan dan ekspor gambar besar. Simpan gambar sumber ke disk atau ekspor ke format file lain. Proses penyimpanan atau ekspor dilakukan dengan menggunakan persegi parsial jika diperlukan. 
### **Format Gambar yang Didukung**
Format-format berikut didukung untuk pemrosesan gambar besar:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Format-format di atas dapat diproses dengan aman melalui pembuatan, modifikasi, mengaplikasikan operasi penggambaran, menyimpan ke disk atau mengekspor ke dalam tanpa memperhatikan ukuran gambar.

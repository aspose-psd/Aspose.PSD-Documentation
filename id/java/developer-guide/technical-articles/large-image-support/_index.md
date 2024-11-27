---
title: Dukungan Gambar Besar
type: docs
weight: 60
url: /id/java/dukungan-gambar-besar/
---

## **Dukungan Gambar Besar**
Karena pustaka Java standar memiliki beberapa batasan terkait ukuran gambar yang dapat diproses, kami memperkenalkan mekanisme baru untuk mendukung gambar besar. Pendekatan baru ini mengatasi batasan namun karena batasan ukuran data, dimensi maksimum yang didukung untuk pembuatan dan pemuatan adalah 2.147.483.647 x 2.147.483.647 piksel.
### **Bekerja dengan Gambar Besar**
Aspose.PSD telah meningkatkan kinerja dan dukungan untuk gambar besar. Gambar berukuran ratusan megabita sudah bukan lagi masalah sehingga Anda dapat membuat, memuat, dan menggambar di atas gambar-gambar tersebut. Namun, karena pemrosesan sebagian dan penanganan pengecualian OutOfMemoryException, kinerja mungkin sangat rendah pada gambar-gambar yang sangat besar. Hal ini disebabkan oleh fakta bahwa Aspose.PSD mencoba untuk mengalokasikan kembali jumlah data yang lebih kecil untuk pemrosesan dan setiap langkah pengalokasian ulang sangat mahal. Manfaat dari arsitektur baru ini adalah jelas:

- Tidak ada batasan ukuran gambar.
- Anda tidak terbatas pada memori yang tersedia di PC Anda.

Jika Anda mengalami pemrosesan lambat, disarankan untuk meningkatkan jumlah RAM total agar semua piksel Anda muat ke dalam memori. Jika tidak, pemrosesan tetap memungkinkan namun lebih lambat. Pendekatan ini adalah sebagai berikut:

- Panggil metode LoadPartialPixels dengan persegi panjang yang diinginkan dan delegasi untuk menerima piksel yang dimuat yang ditentukan.

Aspose.PSD mencoba memuat seluruh persegi panjang.

- Jika ada cukup memori untuk muat semua piksel, maka semua piksel dikembalikan secara sederhana kepada pemanggil.
- Jika tidak ada cukup memori, pemanggil menerima subset piksel dari dalam persegi panjang yang ditentukan. Ketika piksel-piksel tersebut telah diproses, pemanggil menerima persegi panjang berikutnya. Pemrosesan berakhir ketika seluruh persegi panjang telah diproses.

Aspose.PSD mencoba mengekstrak sebanyak mungkin baris. Jika tidak cukup memori untuk muat satu baris piksel, maka satu baris dibagi menjadi bagian-bagian sesuai dengan persegi panjang yang memiliki tinggi 1. Anda juga dapat menggambar pada gambar-gambar besar. Proses penggambaran mencoba mempengaruhi seluruh persegi panjang yang diinginkan. Jika tidak ada cukup memori, penggambaran dilakukan pada persegi panjang parsial sampai seluruh area digambar. Selain itu, Aspose.PSD mendukung penyimpanan dan ekspor gambar besar. Simpan gambar sumber ke disk atau ekspor ke format file lain. Proses penyimpanan atau ekspor dilakukan dengan menggunakan persegi panjang parsial jika diperlukan.
### **Format Gambar yang Didukung**
Format-format berikut didukung untuk pemrosesan gambar besar:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Format-format di atas dapat diproses secara aman melalui pembuatan, modifikasi, penerapan operasi penggambaran, penyimpanan ke disk, atau ekspor tanpa memandang ukuran gambar.

---
title: Menambahkan Tanda Tangan ke Gambar
type: docs
weight: 70
url: /id/net/adding-a-signature-to-an-image/
---

## **Menambahkan Tanda Tangan**


Menambahkan tanda tangan ke gambar kadang-kadang diperlukan untuk menandatangani gambar secara digital untuk menghindari pemalsuan. Pikiran lainnya mungkin adalah untuk memperlakukan gambar seperti sedang ditampilkan di galeri. Apapun alasan yang ada, API Aspose.PSD menyediakan fitur untuk menambahkan tanda tangan pada gambar menggunakan mekanisme termudah seperti yang dijelaskan di bawah ini. Harap dicatat, contoh ini menggunakan kelas [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) untuk menggambar gambar lain dengan tanda tangan ke permukaan gambar asli. Untuk mendemonstrasikan operasi ini, kita akan memuat gambar PSD dari disk dan menggambar gambar lain sebagai tanda tangan ke permukaan gambar asli menggunakan metode [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) dari kelas Graphics. Kita akan menyimpan gambar hasilnya dalam format PNG menggunakan kelas [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions). Berikut adalah contoh kode yang menunjukkan bagaimana menambahkan tanda tangan ke gambar. Kode contoh ini telah dibagi menjadi beberapa bagian untuk memudahkan pemahaman. Langkah demi langkah, contoh tersebut menunjukkan cara:

- Memuat gambar primer dan sekunder (tanda tangan).
- Membuat dan menginisialisasi objek Grafis.
- Menggambar gambar menggunakan metode DrawImage dari kelas Graphics.
- Menyimpan hasilnya dalam format PNG.
### **Contoh Program**
#### **Memuat Gambar**
Pertama, buat instansi kelas Image untuk memuat gambar contoh dari disk.
#### **Membuat dan Menginisialisasi Objek Grafis**
Setelah memuat gambar, buat dan inisialisasi objek kelas Graphics saat menggunakan objek gambar primer.
#### **Menggambar Gambar Sekunder ke Gambar Primer**
Kemudian menggunakan metode DrawImage dari kelas Graphics, tambahkan gambar sekunder ke gambar primer. Ada beberapa overload dari metode DrawImage yang menerima objek Image sebagai parameter pertama sedangkan semua parameter lainnya berkorespondensi dengan lokasi di mana gambar harus digambar. Untuk keperluan demonstrasi, kode berikut menggunakan versi overload dari DrawImage yang menerima objek Point sebagai parameter kedua dan mencoba untuk menggambar tanda tangan di sudut kanan bawah gambar primer.
#### **Menyimpan Gambar**
Terakhir, simpan gambar kembali ke disk lokal sebagai file PNG menggunakan kelas PngOptions.
#### **Sumber Lengkap**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}

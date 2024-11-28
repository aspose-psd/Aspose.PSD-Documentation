---
title: Menambahkan Tanda Tangan ke Gambar
type: docs
weight: 10
url: /id/java/menambahkan-tanda-tangan-ke-gambar/
---

## **Menambahkan Tanda Tangan**


Menambahkan tanda tangan ke gambar kadang-kadang diperlukan untuk menandatangani digital gambar untuk menghindari pemalsuan. Mungkin juga untuk membuat tampilan gambar seperti sedang dipamerkan di galeri. Alasan apapun itu, API Aspose.PSD menyediakan fitur untuk menambahkan tanda tangan pada gambar menggunakan mekanisme yang paling sederhana seperti yang dijelaskan di bawah ini. Harap diperhatikan, contoh ini menggunakan kelas Graphics untuk menggambar gambar lain dengan tanda tangan ke permukaan gambar asli. Untuk mendemonstrasikan operasi, kami akan memuat gambar PSD dari disk dan menggambar gambar lain sebagai tanda tangan ke permukaan gambar asli menggunakan metode DrawImage kelas Graphics. Kami akan menyimpan gambar hasilnya dalam format PNG menggunakan kelas PngOptions. Berikut adalah contoh kode yang menunjukkan bagaimana menambahkan tanda tangan ke gambar. Kode contoh telah dibagi menjadi bagian-bagian agar mudah dipahami. Langkah demi langkah, contoh tersebut menunjukkan cara:

- Memuat gambar primer dan sekunder (tanda tangan).
- Membuat dan menginisialisasi objek Grafis.
- Menggambar gambar menggunakan metode DrawImage kelas Grafis.
- Menyimpan hasil dalam format PNG.
### **Contoh Program**
#### **Memuat Gambar**
Pertama, buat instansi kelas Image untuk memuat gambar contoh dari disk.
#### **Membuat dan Menginisialisasi Objek Grafis**
Setelah memuat gambar, buat dan inisialisasi objek kelas Grafis sambil menggunakan objek gambar primer.
#### **Menggambar Gambar Sekunder ke Gambar Primer**
Kemudian menggunakan metode DrawImage kelas Grafis, tambahkan gambar sekunder ke gambar primer. Ada beberapa overloading dari metode DrawImage yang menerima objek Image sebagai parameter pertama sedangkan semua parameter lainnya berkaitan dengan lokasi di mana gambar harus digambar. Untuk keperluan demonstrasi, kode berikut menggunakan versi overloading dari DrawImage yang menerima objek Point sebagai parameter kedua dan mencoba menggambar tanda tangan di sudut kanan bawah gambar primer.
#### **Menyimpan Gambar**
Terakhir, simpan gambar kembali ke disk lokal sebagai file PNG menggunakan kelas PngOptions.
#### **Kode Sumber Lengkap**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}

---
title: Menggunakan API Grafik untuk mengedit Lapisan dalam file PSD
weight: 100
type: docs
description: Contoh penggunaan API Grafik di Aspose.PSD untuk Java
keywords: [perbarui lapisan, gambar lingkaran, gambar elips, gambar isi lingkaran, grafik, api psd, java, contoh kode]
url: id/java/graphics-api/
---

## **Ikhtisar**
Untuk memulai, muat file PSD menggunakan metode Image.load() atau buat Gambar Psd dari awal. Gunakan variabel inputFile untuk menggambarkan jalur ke file PSD Anda, dan tentukan opsi pengisian dengan loadOpt, jika diperlukan.

Selanjutnya, akses lapisan pertama dari gambar PSD dengan menggunakan sintaks psdImage.getLayers()[0] untuk mendapatkan referensi ke objek lapisan untuk dimanipulasi.

Untuk mengedit lapisan, buat objek Grafik dengan melewati lapisan sebagai parameter. Objek ini menyediakan berbagai metode untuk menggambar bentuk dan menerapkan kuas.

Objek Pen digunakan untuk mendefinisikan warna dan ketebalan garis luar dari bentuk. Begitu pula, kuas seperti LinearGradientBrush digunakan untuk mendefinisikan warna pengisian.

Gambar bentuk pada lapisan menggunakan metode seperti graphics.drawEllipse() untuk menggambar garis luar bentuk dan graphics.fillEllipse() untuk mengisinya.

Setelah melakukan perubahan yang diinginkan pada lapisan, simpan gambar PSD yang sudah dimodifikasi menggunakan psdImage.save().

Selain itu, Anda dapat menyimpan gambar yang sudah dimodifikasi dalam format lain seperti PNG dengan menggunakan opsi yang sesuai.

Itu dia! Anda telah berhasil menggunakan API Grafik Aspose.PSD untuk Java untuk mengedit lapisan dalam file PSD. Telusuri lebih banyak fitur dan fungsionalitas dari pustaka Aspose.PSD untuk meningkatkan kemampuan pengeditan gambar Anda.

Silakan lihat contoh lengkap.

## **Contoh**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentasi-Java-Aspose-Psd-graphics-api.java" >}}

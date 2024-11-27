---
title: Contoh penggunaan kelompok lapisan di Aspose.PSD untuk Java
weight: 100
type: docs
description: Menggunakan Layer Grup dari Berkas PSD melalui Java
keywords: [kelompok lapisan, lapisan grup, menambahkan lapisan ke grup, psd api, java, contoh kode]
url: id/java/psd-kelompok-layer/
---

## **Ikhtisar**

Pemanfaatan kelompok lapisan di Aspose.PSD untuk Java meningkatkan kemampuan Anda dalam mengelola dan mengorganisir lapisan-lapisan dalam gambar PSD dengan efektif. Kelompok lapisan, juga disebut sebagai folder lapisan, memungkinkan Anda menggabungkan beberapa lapisan dan menerapkan transformasi atau efek secara kolektif.

Untuk memulai, buat gambar PSD baru menggunakan metode PsdImage.create(). Kemudian, inisialisasi objek LayerGroup baru melalui metode addLayerGroup dari objek PsdImage. Berikan nama yang diinginkan untuk lapisan grup ("Folder"), tentukan indeks penyisipan (0), dan atur tanda boolean yang menunjukkan ketersediaannya (Benar).

Selanjutnya, buat dua objek Layer dan atur nama tampilan mereka menggunakan metode setDisplayName. Tambahkan lapisan-lapisan ini ke dalam lapisan grup menggunakan metode addLayer.

Untuk mengakses lapisan-lapisan dalam grup, gunakan properti layers dari objek LayerGroup. Pastikan bahwa nama tampilan lapisan pertama dan kedua dalam grup adalah "Layer 1" dan "Layer 2" secara berturut-turut.

Setelah Anda memanipulasi kelompok lapisan tersebut, simpan gambar PSD yang telah dimodifikasi dengan menggunakan metode save dari objek PsdImage.

Ini merupakan contoh fundamental yang membantu Anda mengenal penggunaan kelompok lapisan dengan Aspose.PSD untuk Java. Perpustakaan ini menawarkan beragam fitur canggih untuk manipulasi lapisan dan transformasi dalam gambar PSD. Untuk detail lebih lanjut dan contoh-contoh tentang penggunaan kelompok lapisan dan fungsionalitas lain dari perpustakaan ini, lihat dokumentasi Aspose.PSD untuk Java.

Untuk bekerja dengan kelompok lapisan di Aspose.PSD untuk Java, gunakan kelas LayerGroup. Berikut ini adalah potongan kode yang mengilustrasikan bagaimana membuat kelompok lapisan, menambahkan lapisan-lapisan ke dalamnya, dan menyimpan gambar PSD yang telah dimodifikasi.

Silakan merujuk pada contoh lengkap yang disediakan.

## **Contoh**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentasi-Java-Aspose-psd-kelompok-layer.java" >}}

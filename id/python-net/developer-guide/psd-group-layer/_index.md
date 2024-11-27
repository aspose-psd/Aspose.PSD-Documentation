---
title: Contoh penggunaan lapisan grup di Aspose.PSD untuk Python
weight: 100
type: docs
description: Penggunaan Lapisan Grup pada Berkas PSD melalui Python
keywords: [kelompok lapisan, lapisan grup, menambahkan lapisan ke grup, psd api, python, contoh kode]
url: id/python-net/psd-group-layer/
---

## **Ikhtisar**

Bekerja dengan lapisan grup di Aspose.PSD untuk Python adalah fitur yang sangat berguna yang memungkinkan Anda mengatur dan memanipulasi lapisan dalam gambar PSD. Lapisan grup, juga dikenal sebagai lapisan folder, memberikan cara untuk mengelompokkan beberapa lapisan bersama dan menerapkan transformasi atau efek ke seluruh grup.

Pada contoh ini, pertama kita membuat gambar PSD baru menggunakan metode PsdImage.create. Lalu, kita membuat objek LayerGroup baru menggunakan metode add_layer_group dari objek PsdImage. Kami memberikan nama lapisan grup ("Folder"), indeks tempat harus dimasukkan (0), dan tanda boolean yang menunjukkan apakah lapisan grup seharusnya terlihat (True).

Selanjutnya, kami membuat dua objek Layer dan mengatur nama tampilan mereka menggunakan properti display_name. Kami menambahkan lapisan-lapisan ini ke lapisan grup menggunakan metode add_layer.

Terakhir, kami dapat mengakses lapisan-lapisan dalam grup menggunakan properti layers dari objek LayerGroup. Dalam contoh ini, kami memastikan bahwa nama tampilan dari lapisan pertama dan kedua dalam grup adalah "Layer 1" dan "Layer 2" masing-masing.

Setelah memanipulasi lapisan grup, kita dapat menyimpan gambar PSD yang dimodifikasi menggunakan metode save dari objek PsdImage.

Ini hanyalah contoh dasar untuk memulai bekerja dengan lapisan grup menggunakan Aspose.PSD untuk Python. Perpustakaan ini menyediakan banyak fitur lanjutan untuk memanipulasi dan mentransformasi lapisan dalam gambar PSD. Anda dapat merujuk ke dokumentasi Aspose.PSD untuk Python untuk detail lebih lanjut dan contoh-contoh dalam bekerja dengan lapisan grup dan fitur-fitur lain dari perpustakaan ini.

Untuk bekerja dengan lapisan grup di Aspose.PSD untuk Python, Anda dapat menggunakan kelas LayerGroup. Berikut adalah contoh potongan kode yang menunjukkan bagaimana membuat lapisan grup, menambahkan lapisan ke dalamnya, dan menyimpan gambar PSD yang dimodifikasi.

Silakan periksa contoh lengkap.

## **Contoh**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}

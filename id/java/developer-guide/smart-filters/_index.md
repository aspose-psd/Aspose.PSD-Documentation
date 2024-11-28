---
title: Manipulasi Filter Cerdas di Aspose.PSD untuk Java
weight: 100
type: docs
description: Contoh penggunaan Filter Cerdas dalam Berkas PSD
keywords: [filter cerdas, tambahkan noise, gauss blur, tajamkan, filter, filter psd, psd api, java, contoh kode]
url: id/java/smart-filters/
---

## **Gambaran**

Terdapat 3 metode untuk menerapkan filter cerdas di Aspose.PSD untuk Java.

## **Penerapan Filter Langsung**
Contoh kode ini menunjukkan cara menerapkan filter cerdas secara langsung di Aspose.PSD untuk Java.

Pertama, kode mendefinisikan berkas PSD sumber, berkas keluaran untuk gambar asli, dan berkas keluaran untuk gambar yang diperbarui.

Kemudian, kode memuat gambar PSD menggunakan metode Image.load() dan mengubahnya menjadi objek PsdImage.

Gambar asli disimpan menggunakan metode save(), dengan menentukan nama berkas keluaran.

Objek SharpenSmartFilter diinisialisasi untuk mewakili filter cerdas yang diinginkan.

Selanjutnya, kode mengambil lapisan reguler dari gambar PSD menggunakan psdImage.getLayers()[1].

Sebuah loop digunakan untuk menerapkan sharpenFilter ke lapisan reguler sebanyak tiga kali.

Terakhir, gambar yang diperbarui disimpan menggunakan metode save() dengan menyediakan nama berkas keluaran.

Kode ini menjelaskan penerapan langsung filter cerdas di Aspose.PSD untuk Java. Dengan menggunakan objek filter yang sesuai dan menerapkannya ke lapisan yang diinginkan, efek yang diinginkan dapat dicapai pada gambar.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentasi-Java-Aspose-psd-smart-filter-penerapan-langung.java" >}}

## **Manipulasi Filter Cerdas di Objek Cerdas**

Potongan kode ini menjelaskan bagaimana memanipulasi filter cerdas dalam objek cerdas di Aspose.PSD untuk Java.

Pertama, kode mendefinisikan berkas PSD sumber, berkas keluaran untuk gambar asli, dan berkas keluaran untuk gambar yang diperbarui.

Gambar PSD dimuat menggunakan metode Image.load() dan kemudian diubah menjadi objek PsdImage.

Gambar asli disimpan menggunakan metode save(), dengan menentukan nama berkas keluaran.

Kemudian, kode mengubah lapisan kedua dari gambar PSD menjadi objek SmartObjectLayer, yang mewakili lapisan objek cerdas.

Selanjutnya, kode menunjukkan pengeditan filter cerdas, dengan menampilkan dua jenis: GaussianBlurSmartFilter dan AddNoiseSmartFilter.

Untuk GaussianBlurSmartFilter, kode memperbarui nilai filter seperti radius, mode pencampuran, opasitas, dan status aktivasi.

Untuk AddNoiseSmartFilter, kode mengatur distribusi noise menjadi NoiseDistribution.Uniform.

Selanjutnya, kode menambahkan dua item filter baru ke lapisan objek cerdas: GaussianBlurSmartFilter lainnya dan AddNoiseSmartFilter.

Setelah penambahan filter baru, kode menerapkan perubahan menggunakan metode updateResourceValues().

Terakhir, kode menunjukkan penerapan langsung filter ke lapisan dan maskernya menggunakan metode apply() dan applyToMask() secara berturut-turut.

Gambar yang diperbarui kemudian disimpan menggunakan metode save() dengan menyediakan nama berkas keluaran.

Dengan mengikuti contoh kode ini, Anda dapat memahami cara memanipulasi filter cerdas dalam objek cerdas di Aspose.PSD untuk Java. Perpustakaan ini menawarkan berbagai macam filter cerdas, masing-masing dengan seperangkat properti dan metode sendiri yang dapat disesuaikan untuk mencapai efek yang diinginkan pada gambar.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentasi-Java-Aspose-psd-smart-filter-fitur.java" >}}

## **Menerapkan Filter Cerdas ke Masker Lapisan**

Menerapkan Filter Cerdas ke Masker: Teknik Pengeditan Gambar Yang Memberi Kuasa

Filter cerdas, umum dalam perangkat lunak pengeditan gambar, memungkinkan pengguna untuk menerapkan berbagai filter dan efek pada gambar mereka. Salah satu teknik menarik yang dimungkinkan oleh filter cerdas adalah penerapannya ke masker. Artikel ini mengeksplorasi penerapan filter cerdas ke masker dan membahas kegunaannya dalam ranah pengeditan gambar.

Memahami Masker: Sebelum terjun ke penerapan filter cerdas ke masker, penting untuk memahami konsep masker. Dalam pengeditan gambar, masker adalah gambar grayscale yang mengatur transparansi area tertentu dalam gambar. Masker memungkinkan penerapan selektif filter, penyesuaian, atau efek ke bagian-bagian tertentu dari gambar sambil meninggalkan yang lain tidak terpengaruh.

Menerapkan Filter Cerdas ke Masker: Ketika filter cerdas diterapkan ke masker, mereka hanya memengaruhi daerah yang ditentukan oleh masker, menawarkan kontrol yang tepat atas dampak filter. Dengan memanipulasi masker, pengguna dapat mengatur intensitas dan luas efek filter.

Silakan mengacu pada contoh sebelumnya dan metodenya: [Referensi API Menerapkan Filter Cerdas ke Masker](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

---
title: Manipulasi Filter Cerdas di Aspose.PSD untuk Python
weight: 100
type: docs
description: Contoh bagaimana menggunakan Filter Cerdas dalam Berkas PSD
keywords: [filter cerdas, tambahkan noise, gauss blur, sharpen, filter, filter psd, api psd, python, contoh kode]
url: id/python-net/smart-filters/
---

## **Ikhtisar**

Ada 3 cara untuk menerapkan filter cerdas di Aspose.PSD untuk Python.

## **Penerapan Filter Langsung**
Pada contoh kode ini, kita bisa melihat contoh bagaimana menerapkan langsung filter cerdas di Aspose.PSD untuk Python.

Pertama, kode menentukan berkas PSD sumber, berkas keluaran untuk gambar asli, dan berkas keluaran untuk gambar yang diperbarui.

Selanjutnya, kode memuat gambar PSD menggunakan metode Image.load() dan mengonversinya menjadi objek PsdImage.

Gambar asli kemudian disimpan menggunakan metode save(), dengan nama berkas keluaran yang ditentukan.

Objek SharpenSmartFilter dibuat, yang mewakili filter cerdas yang akan diterapkan.

Kode kemudian mengambil lapisan biasa dari gambar PSD menggunakan im.layers[1].

Lalu, sebuah perulangan digunakan untuk menerapkan sharpenFilter ke lapisan biasa tiga kali.

Terakhir, gambar yang diperbarui disimpan menggunakan metode save() dan nama berkas keluaran yang ditentukan.

Kode ini menunjukkan bagaimana menggunakan langsung filter cerdas di Aspose.PSD untuk Python. Dengan menggunakan objek filter yang sesuai dan menerapkannya pada lapisan yang diinginkan, Anda dapat mencapai efek yang diinginkan pada gambar-gambar Anda.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Manipulasi Filter Cerdas dalam Objek Cerdas**

Pertama, kode menentukan berkas PSD sumber, berkas keluaran untuk gambar asli, dan berkas keluaran untuk gambar yang diperbarui.

Gambar PSD dimuat menggunakan metode Image.load(), dan kemudian dikonversi menjadi objek PsdImage.

Gambar asli disimpan menggunakan metode save(), dengan nama berkas keluaran yang ditentukan.

Kode kemudian mengonversi lapisan kedua gambar PSD menjadi objek SmartObjectLayer, yang mewakili lapisan objek cerdas.

Kode kemudian melanjutkan untuk mengedit filter cerdas. Pada contoh ini, itu menunjukkan bagaimana bekerja dengan dua jenis filter cerdas: GaussianBlurSmartFilter dan AddNoiseSmartFilter.

Untuk GaussianBlurSmartFilter, kode memperbarui nilai filter, termasuk radius, mode campur, opasitas, dan apakah itu diaktifkan atau tidak.

Untuk AddNoiseSmartFilter, kode mengatur distribusi noise menjadi NoiseDistribution.UNIFORM.

Selanjutnya, kode menambahkan dua item filter baru ke lapisan objek cerdas: GaussianBlurSmartFilter lainnya dan AddNoiseSmartFilter.

Setelah menambahkan filter baru, kode menerapkan perubahan menggunakan metode update_resource_values().

Terakhir, kode menunjukkan bagaimana menerapkan langsung filter ke lapisan dan ke masker lapisan menggunakan metode apply() dan apply_to_mask(), masing-masing.

Gambar yang diperbarui kemudian disimpan menggunakan metode save() dan nama berkas keluaran yang ditentukan.

Dengan mengikuti contoh kode ini, Anda dapat belajar bagaimana bekerja dengan filter cerdas di Aspose.PSD untuk Python. Perpustakaan ini menyediakan berbagai filter cerdas, masing-masing dengan seperangkat properti dan metode yang dapat disesuaikan untuk mencapai efek yang diinginkan pada gambar-gambar Anda.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **Menerapkan Filter Cerdas ke Masker Lapisan**

Menerapkan Filter Cerdas ke Masker: Teknik Pengeditan Gambar yang Kuat

Filter cerdas adalah fitur populer dalam perangkat lunak pengeditan gambar yang memungkinkan pengguna menerapkan berbagai filter dan efek pada gambar mereka. Salah satu teknik menarik yang dapat dicapai dengan menggunakan filter cerdas adalah menerapkannya ke masker. Dalam artikel ini, kita akan menjelajahi bagaimana menerapkan filter cerdas ke masker dan mendiskusikan penggunaannya dalam dunia pengeditan gambar.

Apa Itu Masker? Sebelum kita mempelajari cara menerapkan filter cerdas ke masker, mari kita terlebih dahulu memahami apa itu masker. Dalam pengeditan gambar, masker adalah gambar skala abu-abu yang menentukan transparansi area tertentu dari sebuah gambar. Masker dapat digunakan untuk secara selektif menerapkan filter, penyesuaian, atau efek ke bagian-bagian tertentu dari sebuah gambar, sementara meninggalkan area lain tidak berubah.

Menerapkan Filter Cerdas ke Masker: Saat menerapkan filter cerdas ke masker, filter hanya diterapkan ke area yang ditentukan oleh masker. Hal ini memungkinkan kontrol yang presisi atas bagian-bagian mana dari gambar yang terkena filter. Dengan memanipulasi masker, Anda dapat menentukan intensitas dan sejauh mana efek filter tersebut.

Silakan periksa contoh sebelumnya dan metodenya: [Referensi API Menerapkan Filter Cerdas ke Masker](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

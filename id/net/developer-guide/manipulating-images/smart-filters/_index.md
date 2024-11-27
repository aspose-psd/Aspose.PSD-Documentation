---
title: Manipulasi Filter Cerdas di Aspose.PSD untuk C#
weight: 100
type: docs
description: Contoh cara menggunakan Filter Cerdas dalam Berkas PSD
keywords: [filter cerdas, tambahkan noise, blur gauss, runcing, filter, filter psd, api psd, C#, csharp, contoh kode]
url: id/net/smart-filters/
---

## Ikhtisar

Ada tiga cara untuk menerapkan filter cerdas di Aspose.PSD untuk C#.

### Penerapan Filter Langsung

Contoh ini menunjukkan bagaimana cara langsung menerapkan filter cerdas di Aspose.PSD untuk C#.

Pertama, tentukan berkas PSD sumber, berkas output untuk gambar asli, dan berkas output untuk gambar yang diperbarui.

Selanjutnya, muat gambar PSD menggunakan metode `Image.Load` dan konversikan ke objek `PsdImage`.

Simpan gambar asli menggunakan metode `Save` dengan nama berkas output yang ditentukan.

Buat objek `SharpenSmartFilter`, yang mewakili filter cerdas yang akan diterapkan.

Dapatkan layer reguler dari gambar PSD menggunakan `psdImage.Layers[1]`.

Terapkan `sharpenFilter` ke layer reguler sebanyak tiga kali dalam loop.

Terakhir, simpan gambar yang diperbarui menggunakan metode `Save` dengan nama berkas output yang ditentukan.

Kode ini menunjukkan bagaimana cara langsung menerapkan filter cerdas di Aspose.PSD untuk C#. Dengan menggunakan objek filter yang sesuai dan menerapkannya ke layer yang diinginkan, Anda dapat mencapai efek yang diinginkan pada gambar Anda.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Memanipulasi Filter Cerdas dalam Objek Cerdas

Contoh ini menunjukkan bagaimana memanipulasi filter cerdas dalam objek cerdas.

Pertama, tentukan berkas PSD sumber, berkas output untuk gambar asli, dan berkas output untuk gambar yang diperbarui.

Muat gambar PSD menggunakan metode `Image.Load` dan konversikan ke objek `PsdImage`.

Simpan gambar asli menggunakan metode `Save` dengan nama berkas output yang ditentukan.

Konversikan layer kedua dari gambar PSD ke objek `SmartObjectLayer`.

Edit filter cerdas. Contoh ini menunjukkan cara bekerja dengan `GaussianBlurSmartFilter` dan `AddNoiseSmartFilter`.

Untuk `GaussianBlurSmartFilter`, perbarui nilai filter termasuk radius, mode campuran, opacity, dan status diaktifkan.

Untuk `AddNoiseSmartFilter`, atur distribusi noise ke `NoiseDistribution.UNIFORM`.

Tambahkan item filter baru ke layer objek cerdas: `GaussianBlurSmartFilter` lainnya dan `AddNoiseSmartFilter`.

Terapkan perubahan menggunakan metode `UpdateResourceValues`.

Terapkan filter langsung ke layer dan ke masker layer menggunakan metode `Apply` dan `ApplyToMask` masing-masing.

Simpan gambar yang diperbarui menggunakan metode `Save` dengan nama berkas output yang ditentukan.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Menerapkan Filter Cerdas ke Masker Layer

Filter cerdas adalah alat pengeditan gambar yang kuat yang memungkinkan pengguna menerapkan berbagai filter dan efek. Salah satu teknik menarik adalah menerapkannya ke masker, yang memungkinkan pengendalian yang tepat terhadap area yang terkena filter.

Sebuah masker adalah gambar skala abu-abu yang menentukan transparansi area gambar tertentu, secara selektif menerapkan filter, penyesuaian, atau efek.

Ketika menerapkan filter cerdas ke masker, filter hanya diterapkan ke area yang ditentukan oleh masker. Pengendalian yang presisi ini memungkinkan untuk memanipulasi intensitas dan luas filter.

Untuk informasi lebih detail dan contoh, lihat [dokumentasi Aspose.PSD untuk C#](https://docs.aspose.com/psd/net/).


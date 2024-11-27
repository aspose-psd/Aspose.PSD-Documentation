---
title: Bekerja dengan masker di Aspose.PSD untuk С#
weight: 100
type: docs
description: Contoh tentang bagaimana cara kerja dengan Clipping, Raster, dan Vector Masks dalam Berkas PSD
keywords: [masker, layer mask, vector mask, clipping mask, psd, psd api, C#, csharp, contoh kode]
url: id/net/update-create-layer-mask/
---

## Gambaran

Ada tiga jenis masker dalam berkas PSD:
1. Clipping Masks
2. Raster Masks
3. Vector Masks

Artikel ini mencakup ketiga jenis tersebut.

### Clipping Masks

Clipping masks adalah fitur yang kuat dalam desain grafis dan perangkat lunak pengeditan gambar yang memungkinkan Anda mengontrol keterlihatan satu lapisan berdasarkan bentuk dan konten lapisan lain. Secara esensial, masker clipping membatasi keterlihatan lapisan menjadi bentuk yang ditentukan oleh lapisan di bawahnya.

Untuk membuat masker clipping, Anda memerlukan dua lapisan: lapisan dasar dan lapisan clipping. Lapisan dasar menentukan bentuk atau area yang akan terlihat, sementara lapisan clipping berisi konten yang akan terbatas pada bentuk lapisan dasar.

Ketika Anda menerapkan masker clipping, konten lapisan clipping hanya terlihat di dalam batas lapisan dasar. Konten di luar batas lapisan dasar tersembunyi atau terpotong.

Masker clipping sangat berguna untuk menerapkan efek, seperti tekstur atau pola, ke area spesifik dari gambar atau karya seni. Dengan menggunakan masker clipping, Anda dapat memastikan efek terbatas pada area yang diinginkan tanpa memengaruhi bagian lain dari gambar.

### Raster Masks

Masker raster dalam berkas PSD penting untuk mengontrol keterlihatan area-area tertentu dalam lapisan. Tidak seperti masker vektor, yang menggunakan bentuk matematika untuk menentukan area yang di-masker, masker raster menggunakan informasi berbasis piksel untuk menentukan bagian mana dari lapisan yang terlihat atau tersembunyi.

Sebuah masker raster terdiri dari gambar grayscale yang diterapkan pada suatu lapisan. Area putih pada masker mewakili bagian-bagian yang terlihat, sementara area hitam mewakili bagian yang tersembunyi. Nuansa abu-abu di antaranya menciptakan transparansi parsial atau area semi-terlihat.

Dengan menggunakan masker raster, Anda dapat mencapai efek masking yang rumit, memungkinkan kontrol yang tepat terhadap keterlihatan lapisan berdasarkan detail tingkat piksel. Fitur ini sangat berguna untuk tugas-tugas yang memerlukan pengeditan dan pencampuran detail dalam gambar.

### Vector Masks

Masker vektor dalam berkas PSD adalah alat serbaguna yang digunakan untuk menentukan keterlihatan area-area tertentu dalam lapisan berdasarkan bentuk matematika. Tidak seperti masker raster, yang menggunakan informasi berbasis piksel, masker vektor menggunakan jalur dan kurva untuk membuat area ter-masker halus dan dapat diperbesar.

Masker vektor pada dasarnya adalah jalur yang diterapkan pada lapisan. Bentuk jalur menentukan bagian-bagian lapisan yang terlihat dan yang tersembunyi. Dengan memanipulasi titik kontrol dan kurva jalur, Anda dapat membuat area ter-masker yang tepat dan rumit.

Masker vektor sangat berguna untuk membuat masker bersih dan dapat diperbesar yang dapat dengan mudah disesuaikan tanpa kehilangan kualitas. Fitur ini ideal untuk tugas-tugas yang membutuhkan presisi tinggi dan fleksibilitas dalam mendefinisikan area terlihat dalam suatu lapisan.

Untuk informasi lebih lanjut tentang menambahkan masker vektor, silakan kunjungi halaman [Masker Vector](psd/id/id/net/layer-vector-mask/).

## Contoh
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

Untuk informasi lebih detail dan contoh-contoh, silakan kunjungi [Dokumentasi Aspose.PSD untuk C#](https://docs.aspose.com/psd/net/).

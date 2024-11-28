---
title: Bekerja dengan masker di Aspose.PSD untuk Python
weight: 100
type: docs
description: Contoh cara kerja dengan Clipping, Raster, dan Masker Vektor dalam Berkas PSD
keywords: [masker, masker lapisan, masker vektor, masker clipping, psd, psd api, python, contoh kode]
url: id/python-net/update-create-layer-mask/
---

## **Ikhtisar**

**Ikhtisar**
	
	Terdapat 3 jenis masker dalam berkas PSD:
	1. Masker Clipping
	2. Masker Raster
	3. Masker Vektor
	
	Artikel ini mencakup semua 3 jenis.

** Masker Clipping **

Masker clipping adalah fitur yang kuat dalam perangkat desain grafis dan perangkat lunak pengeditan gambar. Mereka memungkinkan Anda mengontrol visibilitas satu lapisan berdasarkan bentuk dan konten lapisan lain. Dengan kata lain, masker clipping membatasi visibilitas lapisan sesuai dengan bentuk lapisan lain di bawahnya.

Untuk membuat masker clipping, pertama-tama Anda memerlukan dua lapisan: lapisan dasar dan lapisan yang ingin Anda potong. Lapisan dasar menentukan bentuk atau area yang akan terlihat, sedangkan lapisan yang ingin Anda potong berisi konten yang akan dipotong ke bentuk lapisan dasar.

Saat Anda menerapkan masker clipping, konten lapisan yang dipotong hanya terlihat dalam batas lapisan dasar. Setiap konten di luar batas lapisan dasar akan disembunyikan atau dipotong.

Masker clipping sangat berguna saat Anda ingin menerapkan efek, seperti tekstur atau pola, pada area tertentu dari gambar atau karya seni. Dengan menggunakan masker clipping, Anda dapat membatasi efek pada area yang diinginkan tanpa memengaruhi sisa gambar.

Silakan lihat contohnya di akhir halaman

** Masker Raster ** 

Masker raster dalam berkas PSD digunakan untuk mengontrol visibilitas area tertentu dalam satu lapisan. Berbeda dengan masker vektor, yang menggunakan bentuk matematis untuk menentukan area yang di-mask, masker raster menggunakan informasi berbasis piksel untuk menentukan bagian mana dari lapisan yang terlihat atau tersembunyi.

Masker raster terdiri dari gambar skala abu-abu yang diterapkan pada lapisan. Area putih dari masker mewakili bagian yang terlihat, sedangkan area hitam mewakili bagian yang tersembunyi. Nuansa abu-abu di antaranya bisa digunakan untuk membuat transparansi parsial atau area semi-terlihat.

Silakan lihat contohnya di akhir halaman

** Masker Vektor **

Masker vektor dalam berkas PSD adalah alat serbaguna yang digunakan untuk menentukan visibilitas area tertentu dalam satu lapisan berdasarkan bentuk matematis. Berbeda dengan masker raster, yang menggunakan informasi berbasis piksel, masker vektor memanfaatkan jalur dan kurva untuk membuat area tersembunyi yang mulus dan dapat diperbesar.

Masker vektor pada dasarnya adalah jalur yang diterapkan pada satu lapisan. Bentuk jalur menentukan bagian dari lapisan yang terlihat dan bagian yang tersembunyi. Dengan memanipulasi titik kontrol dan kurva jalur, Anda dapat membuat area tersembunyi yang presisi dan rumit.

Silakan lihat [Halaman Masker Vektor](psd/id/net/layer-vector-mask/) untuk mendapatkan informasi tentang bagaimana masker vektor dapat ditambahkan menggunakan sumber daya.

## **Contoh**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentasi-Python-Aspose-psd-update-create-layer-mask.py" >}}

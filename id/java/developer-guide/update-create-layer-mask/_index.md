---
title: Bekerja dengan masker di Aspose.PSD untuk Java
weight: 100
type: docs
description: Contoh bagaimana cara kerja dengan Clipping, Raster, dan Vector Mask dalam Berkas PSD
keywords: [masker, masker lapisan, masker vektor, masker clipping, psd, psd api, java, contoh kode]
url: id/java/update-create-layer-mask/
---

## **Ikhtisar**

**Ikhtisar**
	
	Terdapat 3 jenis masker dalam berkas PSD:
	1. Masker Clipping
	2. Masker Raster
	3. Masker Vektor
	
	Artikel ini mencakup ketiga jenis tersebut.

** Masker Clipping **

Masker clipping adalah fitur kuat dalam perangkat lunak desain grafis dan pengeditan gambar, terutama di Java. Mereka memungkinkan kontrol yang tepat terhadap visibilitas satu lapisan berdasarkan bentuk dan konten lapisan lain. Pada dasarnya, masker clipping membatasi visibilitas lapisan ke bentuk lapisan lain di bawahnya.

Untuk menerapkan masker clipping di Java, Anda akan memerlukan dua lapisan: lapisan dasar dan lapisan yang akan Anda gunting. Lapisan dasar menentukan bentuk atau area yang akan tetap terlihat, sementara lapisan yang akan dipotong berisi konten yang akan disesuaikan dengan bentuk lapisan dasar.

Ketika masker clipping diterapkan di Java, konten lapisan yang dipotong hanya terlihat dalam batas lapisan dasar. Setiap konten di luar batas ini akan tersembunyi atau dipotong.

Masker clipping terbukti sangat berharga ketika menerapkan efek, seperti tekstur atau pola, ke area tertentu dari gambar atau karya seni. Dengan menggunakan masker clipping, Anda dapat membatasi efek pada area yang diinginkan tanpa memengaruhi bagian lain dari gambar.

Silakan lihat contoh di akhir halaman untuk penjelasan lebih lanjut.

** Masker Raster ** 

Masker raster dalam berkas Java digunakan untuk mengelola visibilitas area tertentu dalam lapisan. Berbeda dengan masker vektor, yang menggunakan bentuk matematika untuk mendefinisikan area yang di-masker, masker raster bergantung pada informasi berbasis piksel untuk menentukan area yang terlihat atau tersembunyi.

Sebuah masker raster terdiri dari gambar skala abu-abu yang diterapkan pada lapisan. Area putih pada masker menunjukkan visibilitas, sementara area hitam mewakili bagian tersembunyi. Bayangan abu-abu di antaranya dapat menciptakan transparansi parsial atau daerah semi-terlihat.

Silakan lihat contoh di akhir halaman untuk pemahaman yang lebih baik.

** Masker Vektor **

Masker vektor dalam berkas Java adalah alat serbaguna yang digunakan untuk menentukan visibilitas area tertentu dalam lapisan berdasarkan bentuk matematis. Berbeda dengan masker raster, yang bergantung pada data berbasis piksel, masker vektor menggunakan jalur dan kurva untuk menciptakan area tertutup yang halus dan dapat diskalakan.

Masker vektor pada dasarnya terdiri dari sebuah jalur yang diterapkan pada lapisan. Bentuk jalur ini menentukan bagian mana dari lapisan yang terlihat dan mana yang tersembunyi. Dengan memanipulasi titik kontrol dan kurva jalur, area yang tersembunyi dengan tepat dan rumit dapat dibuat.

Silakan lihat [halaman Masker Vektor](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) untuk informasi tentang menambahkan masker vektor menggunakan sumber daya.

## **Contoh**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentasi-Java-Aspose-psd-update-create-layer-mask.java" >}}

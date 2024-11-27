---
title: Gambaran Format PSD
type: docs
weight: 60
url: /id/net/psd-format-overview/
---

## **Deskripsi**
PSD, Dokumen Photoshop, mewakili format file asli Adobe Photoshop yang digunakan untuk desain dan pengembangan grafis.

## **Spesifikasi Format File**
Data dalam file PSD disimpan dalam urutan byte big-endian. Ini berarti menukar integer pendek dan panjang saat membaca atau menulis di platform Windows. Format file Photoshop terbagi menjadi lima bagian utama. Format ini memiliki banyak penanda panjang yang dapat digunakan untuk beralih dari satu bagian ke bagian berikutnya. Penanda panjang biasanya dilengkapi dengan byte untuk dibulatkan ke interval byte terdekat 2 atau 4. Lima bagian utamanya adalah:

- Header File
- Data Mode Warna
- Sumber Gambar
- Informasi Lapisan dan Masker
- Data Gambar

Untuk kesesuaian, data harus ditulis ke semua bidang ini di bagian, karena Photoshop dapat mencoba membaca seluruh bagian. Hal ini juga berarti bahwa nol harus ditulis ke bidang yang dilewati saat menulis ke file. Bidang panjang dalam bagian yang panjangnya ditentukan harus digunakan untuk menentukan kapan berhenti membaca. Dalam kebanyakan kasus, bidang panjang menunjukkan jumlah byte, bukan catatan, yang akan datang. Poin-poin berikut perlu diingat saat membaca sebuah file.

- Nilai-nilai dalam kolom "Panjang" dalam semua tabel adalah dalam byte.
- Semua nilai yang didefinisikan sebagai string Unicode terdiri dari:
- Bidang panjang 4 byte, yang mewakili jumlah karakter dalam string (bukan byte).
- String dari nilai Unicode, dua byte per karakter.

## **Fitur Format**
File PSD dapat mencakup lapisan gambar, lapisan penyesuaian, masker lapisan, catatan, informasi file, kata kunci, dan elemen-elemen spesifik Photoshop lainnya. File Photoshop memiliki ekstensi default sebagai .PSD dan memiliki batas tinggi dan lebar maksimum 30.000 piksel, serta batas panjang dua gigabyte.

## **Bagaimana Mencaritahui**
1. Sebuah alat untuk Psd Slicing.
1. [Mengonversi PSD](/psd/id/net/converting-psd-image-to-raster-format/) ke HTML
1. Menggunakan [PSD sebagai Templat](/psd/id/net/using-psd-files-as-templates-for-automation-business-cards-case/) untuk Email
1. PSD ke HTML CMS spesifik
1. Identikit dalam File PSD (Sketsa Polisi)
1. Buat gambar pratinjau pseudo-3D menggunakan Objek Pintar untuk barang-barang seperti botol, cangkir, kaos, dll.
1. Sunting cepat PSD: Auto-tone, Preset, Objek Pintar, Pemotongan Gambar Lapisan Teks

Dan masih banyak lagi. Jika Anda berhasil membuat sesuatu dengan Aspose.PSD, silakan bagikan studi kasus Anda dengan kami melalui [Forum Aspose](https://forum.aspose.com/).

Contoh tambahan yang bisa Anda pelajari dari:

- [Studi Kasus](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Pameran](/psd/id/net/showcases-html/)

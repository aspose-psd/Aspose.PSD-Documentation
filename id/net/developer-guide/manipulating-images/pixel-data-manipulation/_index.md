---
title: Memanipulasi Data Pixel menggunakan Aspose.PSD untuk C#
weight: 100
type: docs
description: Contoh bagaimana untuk langsung dan cepat memperbarui data pixel mentah menggunakan API C# PSD
keywords: [mengedit pixel, mengedit psd, mengedit lapisan, manipulasi data mentah, mengedit data psd, psd api, C#, csharp, contoh kode]
url: id/manipulasi-data-pixel/
---

## Pengantar

Aspose.PSD adalah perpustakaan yang kuat yang memungkinkan Anda untuk bekerja dengan file Adobe Photoshop (PSD) dalam C#. Dalam artikel ini, kita akan menjelajahi bagaimana untuk memanipulasi data pixel dalam file PSD menggunakan Aspose.PSD untuk C#.

## Gambaran

Kode yang diberikan menunjukkan bagaimana membuat file PSD, menambahkan lapisan baru, memanipulasi data pixel secara langsung, dan menyimpan gambar yang dimodifikasi.

### Langkah-langkah Memanipulasi Data Pixel

1. **Mengimpor Modul yang Diperlukan**:
   Impor modul-modul yang diperlukan. Anda perlu mengimpor kelas-kelas `PsdImage` dan `Layer` dari perpustakaan Aspose.PSD.

2. **Tentukan Jalur Berkas Masukan dan Keluaran**:
   Tentukan jalur berkas masukan dan keluaran.

3. **Buka Berkas Masukan sebagai Stream**:
   Buka berkas masukan sebagai stream menggunakan kelas `FileStream` dalam mode baca. Buat objek `PsdImage` dengan memuat stream.

4. **Membuat Gambar PSD Baru**:
   Buat gambar PSD baru menggunakan konstruktor `PsdImage` dan berikan lebar dan tinggi lapisan sebagai argumen.

5. **Memberikan Lapisan ke Gambar PSD**:
   Alokasikan lapisan ke properti `Layers` gambar PSD.

6. **Memanipulasi Data Pixel**:
   Muat pixel ARGB32 dari lapisan menggunakan metode `LoadArgb32Pixels`. Tentukan rentang indeks berdasarkan panjang array pixel dan modifikasi nilai pixel sesuai kebutuhan.

7. **Simpan Data Pixel yang Dimodifikasi**:
   Simpan data pixel yang dimodifikasi kembali ke lapisan menggunakan metode `SaveArgb32Pixels`.

8. **Simpan Gambar PSD**:
   Simpan gambar PSD ke berkas keluaran menggunakan metode `Save`.

### Contoh

Berikut contoh kode yang menunjukkan bagaimana memanipulasi data pixel menggunakan Aspose.PSD untuk C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### Ringkasan

Aspose.PSD untuk C# menyediakan serangkaian fitur yang kuat untuk memanipulasi data pixel dalam file PSD. Baik Anda perlu memodifikasi pixel berdasarkan kondisi tertentu atau membuat pola yang kompleks, Aspose.PSD membuat tugas-tugas ini menjadi mudah dan efisien.

Untuk informasi lebih detail dan contoh-contoh, silakan kunjungi [dokumentasi Aspose.PSD untuk C#](https://docs.aspose.com/psd/net/).

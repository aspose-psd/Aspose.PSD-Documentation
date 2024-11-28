---
title: Memperbarui Layer Isian PSD menggunakan Python
weight: 100
type: docs
description: Contoh penggunaan semua jenis layer penyesuaian termasuk Isian Warna, Isian Gradien, dan Isian Pola
keywords: [layer isian, Isian Warna, Isian Gradien, Isian Pola, api psd, python, contoh kode]
url: /id/python-net/psd-fill-layer-editing/
---

## **Ikhtisar**

Untuk membuat layer biasa, Anda dapat menggunakan fungsi create_regular_layer yang disediakan dalam kode. Fungsi ini mengambil parameter kiri, atas, lebar, dan tinggi untuk mendefinisikan posisi dan ukuran layer. Ini membuat layer baru, mengatur batasnya, dan mengisinya dengan warna tertentu.

Untuk membuat layer isian warna, Anda dapat menggunakan metode FillLayer.create_instance dengan parameter FillType.COLOR. Setelah membuat layer isian, Anda dapat mengakses pengaturan isian menggunakan properti fill_settings dan mengatur warna menggunakan properti warna dari kelas ColorFillSettings. Dalam kode yang disediakan, warnanya diatur ke Color.coral. Properti clipping layer isian diatur ke 1, yang membuat layer bertindak sebagai clipping mask.

Untuk membuat layer isian gradien, Anda dapat menggunakan metode FillLayer.create_instance dengan parameter FillType.GRADIENT. Sama seperti layer isian warna, Anda dapat mengakses pengaturan isian menggunakan properti fill_settings dan mengatur titik warna gradien dan titik transparansi. Dalam kode yang disediakan, titik-titik warna gradien didefinisikan menggunakan kelas GradientColorPoint, dan titik-titik transparansi didefinisikan menggunakan kelas GradientTransparencyPoint. Properti clipping layer isian juga diatur ke 1.

Untuk membuat layer isian pola, Anda dapat menggunakan metode FillLayer.create_instance dengan parameter FillType.PATTERN. Sekali lagi, Anda dapat mengakses pengaturan isian menggunakan properti fill_settings dan mengatur data pola dan properti lainnya. Dalam kode yang disediakan, data pola didefinisikan menggunakan kelas PatternFillSettings, dan properti clipping diatur ke 1.

Setelah membuat layer-layer isian, Anda dapat menambahkannya ke gambar PSD menggunakan metode add_layer. Anda juga dapat menentukan nama tampilan dan properti lainnya untuk setiap layer isian.

Terakhir, Anda dapat menyimpan gambar PSD dan gambar PNG yang sesuai menggunakan kode yang disediakan. Opsi PNG diatur untuk menggunakan warna sejati dengan alpha untuk transparansi.

Silakan periksa contoh lengkap.

## **Contoh**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentasi-Python-Aspose-psd-fill-layer-editing.py" >}}

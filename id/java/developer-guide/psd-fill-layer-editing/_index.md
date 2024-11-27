---
title: Memperbarui Lapisan Pengisian PSD menggunakan Java
weight: 100
type: docs
description: Contoh penggunaan semua jenis lapisan penyesuaian termasuk Pengisian Warna, Pengisian Gradien, dan Pengisian Pola
keywords: [lapisan pengisian, Pengisian Warna, Pengisian Gradien, Pengisian Pola, api psd, java, contoh kode]
url: id/java/psd-fill-layer-editing/
---

## **Ikhtisar**

Membuat lapisan reguler melibatkan penggunaan fungsi createRegularLayer, yang memerlukan parameter untuk mendefinisikan posisi dan ukuran lapisan. Fungsi ini membuat lapisan baru, menetapkan batasannya, dan mengisinya dengan warna yang ditentukan.

Untuk lapisan pengisian warna, Anda menggunakan metode FillLayer.createInstance dengan parameter FillType.Color. Setelah lapisan pengisian dibuat, akses pengaturan pengisian melalui properti fill_settings dan atur warna yang diinginkan menggunakan properti warna dari kelas ColorFillSettings. Dalam konteks ini, warna diatur menjadi Color.getCoral(). Selain itu, properti clipping dari lapisan pengisian diatur menjadi 1, sehingga berfungsi sebagai masker clipping.

Lapisan gradien pengisian dibuat dengan cara yang sama menggunakan metode FillLayer.create_instance, tetapi dengan parameter FillType.Gradient. Seperti lapisan pengisian warna, Anda mengakses pengaturan pengisian melalui fill_settings dan mengatur titik warna gradien dan titik transparansi. Contoh ini, titik warna gradien didefinisikan dengan kelas GradientColorPoint, dan titik transparansi didefinisikan dengan kelas GradientTransparencyPoint. Properti clipping dari lapisan pengisian juga diatur menjadi 1.

Lapisan pengisian pola dibuat menggunakan FillLayer.createInstance dengan parameter FillType.Pattern. Sekali lagi, akses pengaturan pengisian melalui fill_settings dan atur data pola dan properti lainnya. Dalam kode ini, data pola didefinisikan menggunakan kelas PatternFillSettings, dan properti clipping diatur menjadi 1.

Setelah lapisan pengisian dibuat, tambahkan mereka ke gambar PSD menggunakan metode addLayer, menentukan nama tampilan dan properti lainnya untuk setiap lapisan pengisian.

Terakhir, simpan gambar PSD dan gambar PNG yang sesuai dengan kode yang disediakan. Opsi PNG dikonfigurasi untuk menggunakan warna benar dengan alpha untuk transparansi.

Silakan lihat contoh lengkap untuk lebih jelasnya.

## **Contoh**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentasi-Java-Aspose-psd-fill-layer-editing.java" >}}

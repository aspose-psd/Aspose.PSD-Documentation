---
title: Menggunakan Lapisan Penyesuaian untuk Peningkatan PSD
weight: 100
type: docs
description: Contoh penggunaan lapisan penyesuaian melalui Aspose.PSD untuk C#
keywords: [lapisan penyesuaian, peningkatan foto, penyesuaian kurva, peningkatan level, balik, filter foto, psd api, C#, csharp, contoh kode]
url: id/peningkatan-lapisan-penyesuaian/
---

## Gambaran

Dalam artikel ini, kita akan menjelajahi pengeditan lapisan penyesuaian di Aspose.PSD untuk C#. Lapisan penyesuaian adalah fitur yang powerful dalam pengeditan gambar yang memungkinkan Anda melakukan perubahan non-destruktif pada gambar Anda. Aspose.PSD menyediakan serangkaian kelas lapisan penyesuaian yang komprehensif yang dapat Anda gunakan untuk memodifikasi berbagai aspek gambar Anda.

Untuk mendemonstrasikan pengeditan lapisan penyesuaian, kita akan menggunakan potongan kode contoh di akhir halaman yang memuat gambar PSD dan menerapkan penyesuaian yang berbeda ke lapisannya.

Pada potongan kode di bawah, kita mulai dengan memuat gambar PSD menggunakan metode `PsdImage.Load()`. Kemudian kita menyiapkan opsi untuk menyimpan file PNG keluaran. Kelas `PngOptions` memungkinkan kita untuk menentukan tipe warna untuk gambar keluaran.

Selanjutnya, kita melakukan iterasi melalui setiap lapisan dalam gambar PSD dan memeriksa tipe nya menggunakan metode `IsAssignable()`. Jika lapisan itu adalah jenis tertentu, kita menetapkannya ke tipe tersebut menggunakan metode `Cast()` dan menerapkan penyesuaian yang diinginkan. Sebagai contoh, kita menyesuaikan kecerahan dan kontras dari `BrightnessContrastLayer`, memodifikasi level dari `LevelsLayer`, menambahkan titik kurva ke `CurvesLayer`, dan lain-lain.

Anda dapat menambahkan kode tambahan untuk menerapkan penyesuaian lain ke lapisan mereka masing-masing. Aspose.PSD menyediakan berbagai kelas lapisan penyesuaian, seperti [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), dan lain-lain.

Terakhir, kita menyimpan gambar yang telah dimodifikasi menggunakan metode `Save()` dari kelas `PsdImage`.

Potongan kode ini memberikan gambaran dasar tentang bagaimana mengedit lapisan penyesuaian di Aspose.PSD untuk C#. Anda dapat menyesuaikan penyesuaian sesuai dengan kebutuhan Anda dan menjelajahi berbagai opsi yang tersedia dalam dokumentasi API.

## Contoh

Berikut contoh kode yang menunjukkan bagaimana menggunakan lapisan penyesuaian dengan Aspose.PSD untuk C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Untuk informasi lebih lanjut dan contoh, silakan kunjungi [dokumentasi Aspose.PSD untuk C#](https://docs.aspose.com/psd/net/).


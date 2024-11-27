---
title: Menggunakan Lapisan Penyesuaian untuk Peningkatan PSD
weight: 100
type: docs
description: Contoh penggunaan lapisan penyesuaian melalui Aspose.PSD for Python
keywords: [lapisan penyesuaian, meningkatkan foto, penyesuaian kurva, peningkatan level, balik, filter foto,  psd api, python, contoh kode]
url: id/python-net/peningkatan-lapisan-penyesuaian/
---

## **Gambaran**

Dalam artikel ini, kita akan menjelajahi pengeditan lapisan penyesuaian di Aspose.PSD untuk Python. Lapisan penyesuaian merupakan fitur yang kuat dalam pengeditan gambar yang memungkinkan Anda membuat perubahan yang tidak merusak pada gambar Anda. Aspose.PSD menyediakan serangkaian lengkap kelas lapisan penyesuaian yang dapat Anda gunakan untuk memodifikasi berbagai aspek gambar Anda.

Untuk mendemonstrasikan pengeditan lapisan penyesuaian, kita akan menggunakan potongan kode sampel di bagian akhir halaman yang memuat gambar PSD dan menerapkan berbagai penyesuaian pada lapisannya.

Pada potongan kode di bawah, kita mulai dengan memuat gambar PSD menggunakan metode PsdImage.load(). Kemudian, kita menyiapkan opsi untuk menyimpan file PNG keluaran. Kelas PngOptions memungkinkan kita untuk menentukan jenis warna untuk gambar keluaran.

Selanjutnya, kita melakukan iterasi melalui setiap lapisan dalam gambar PSD dan memeriksa tipe lapisannya menggunakan metode is_assignable(). Jika lapisan tersebut adalah tipe tertentu, kita mentransformasikannya ke tipe tersebut menggunakan metode cast() dan menerapkan penyesuaian yang diinginkan. Sebagai contoh, kita menyesuaikan kecerahan dan kontras dari BrightnessContrastLayer, memodifikasi level dari LevelsLayer, menambahkan titik kurva ke CurvesLayer, dan sebagainya.

Anda dapat menambahkan kode tambahan untuk menerapkan penyesuaian lain pada lapisan mereka masing-masing. Aspose.PSD menyediakan berbagai kelas lapisan penyesuaian, seperti [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), dan lain-lain.

Terakhir, kita menyimpan gambar yang telah dimodifikasi menggunakan metode save() dari kelas PsdImage.

Kode ini memberikan gambaran dasar tentang bagaimana mengedit lapisan penyesuaian di Aspose.PSD untuk Python. Anda dapat menyesuaikan penyesuaian sesuai kebutuhan Anda dan menjelajahi berbagai opsi yang tersedia dalam dokumentasi API.

Harap periksa contoh lengkap.

## **Contoh**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentasi-Python-Aspose-peningkatan-lapisan-penyesuaian.py" >}}

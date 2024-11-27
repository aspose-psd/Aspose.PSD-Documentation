---
title: Menggunakan Lapisan Penyesuaian untuk Peningkatan PSD
weight: 100
type: docs
description: Contoh penggunaan lapisan penyesuaian melalui Aspose.PSD untuk Java
keywords: [lapisan penyesuaian, peningkatan foto, penyesuaian kurva, peningkatan level, balik, filter foto, psd api, java, contoh kode]
url: id/java/peningkatan-lapisan-penyesuaian/
---

## **Ikhtisar**

Artikel ini menjelajahi pengeditan lapisan penyesuaian di Aspose.PSD untuk Java. Lapisan penyesuaian adalah fitur yang kuat dalam pengeditan gambar yang memungkinkan Anda membuat perubahan non-destruktif pada gambar Anda. Aspose.PSD menyediakan kumpulan lengkap kelas lapisan penyesuaian yang dapat Anda gunakan untuk memodifikasi berbagai aspek dari gambar Anda.

Untuk mendemonstrasikan pengeditan lapisan penyesuaian, kami akan menyediakan potongan kode contoh di akhir halaman yang memuat gambar PSD dan menerapkan penyesuaian berbeda ke lapisannya.

Pada potongan kode berikut, kami memulai dengan memuat gambar PSD menggunakan metode PsdImage.load(). Kemudian, kami menyiapkan opsi untuk menyimpan file PNG keluaran. Kelas PngOptions memungkinkan kita untuk menentukan tipe warna untuk gambar keluaran.

Selanjutnya, kami mengiterasi setiap lapisan dalam gambar PSD dan memeriksa tipe lapisannya menggunakan metode isAssignable(). Jika lapisan adalah tipe tertentu, kami melemparkannya ke tipe tersebut menggunakan metode cast() dan menerapkan penyesuaian yang diinginkan. Misalnya, kami menyesuaikan kecerahan dan kontras dari BrightnessContrastLayer, memodifikasi level dari LevelsLayer, menambahkan titik kurva ke CurvesLayer, dan lain sebagainya.

Anda dapat menambahkan kode tambahan untuk menerapkan penyesuaian lain ke lapisan masing-masing. Aspose.PSD menyediakan berbagai kelas lapisan penyesuaian, seperti [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), dan lain-lain.

Terakhir, kami menyimpan gambar yang telah dimodifikasi menggunakan metode save() dari kelas PsdImage.

Ini memberikan ikhtisar dasar tentang cara mengedit lapisan penyesuaian di Aspose.PSD untuk Java. Anda dapat menyesuaikan penyesuaian sesuai dengan kebutuhan Anda dan menjelajahi berbagai opsi yang tersedia dalam dokumentasi API.

Silakan periksa contoh lengkap di bawah ini.

## **Contoh**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentasi-Java-Aspose-peningkatan-lapisan-penyesuaian.java" >}}

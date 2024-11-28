---
title: Lapisan Penyesuaian Kecerahan Kontras
type: docs
weight: 30
url: /id/java/layer-types/adjustment-layer/kecerahan-kontras/
---

# Bekerja dengan lapisan penyesuaian Kecerahan/Kontras Photoshop di Java

Dalam artikel ini kami akan menerapkan penyesuaian Kecerahan/Kontras ke dokumen Adobe® Photoshop® menggunakan pustaka Aspose.PSD untuk Java®. Selain itu, kami akan mempelajari lebih lanjut tentang fitur-fitur pustaka terkait jenis lapisan penyesuaian ini sepanjang jalan.

Tetapi pertama-tama sedikit teori.

Lapisan penyesuaian Kecerahan/Kontras mengubah kecerahan dan kontras gambar. Namun tunggu sebentar, apa artinya sebenarnya? Meningkatkan kecerahan mencerahkan nilai warna hingga putih dan mengurangi kecerahan menggelapkan nilai warna hingga hitam. Meningkatkan kontras pada gilirannya akan meningkatkan perbedaan antara warna terang dan gelap dan mengurangi kontras akan mengurangi perbedaan tersebut secara respektif; artinya bahwa warna-warna terang menjadi lebih terang dan warna-warna gelap menjadi lebih gelap.

## Dukungan mode warna

Pustaka ini memungkinkan untuk menambahkan lapisan penyesuaian Kecerahan/Kontras ke gambar dalam mode warna RGB, CMYK, atau Lab.

## Perilaku saat ini dan legacy

Implementasi pustaka saat ini (v20.6 pada saat penulisan) menggunakan algoritma Photoshop default yang mempertahankan rentang tonal penuh dari bayangan hingga sorotan, namun belum mendukung perilaku warisan. Ini berarti bahwa pustaka mendukung lapisan penyesuaian Kecerahan/Kontras dalam dokumen yang dibuat dalam versi Photoshop terbaru (CS4 dan lebih tinggi). Namun, Anda dapat [meminta implementasi warisan dari lapisan penyesuaian Kecerahan/Kontras](https://forum.aspose.com/c/psd) di forum kami jika Anda membutuhkannya.

## Menyesuaikan kecerahan dan kontras

Sekarang mari kita deskripsikan bagaimana API tingkat tinggi dari lapisan penyesuaian Kecerahan/Kontras bekerja (melihat ke depan, API itu langsung). Kelas PsdImage berisi metode pabrik (addBrightnessContrastAdjustmentLayer) untuk menginstansiasi kelas BrightnessContrastLayer yang merupakan gerbang untuk penyesuaian kecerahan dan kontras. Kelas BrightnessContrastLayer hanya berisi sepasang getter dan setter untuk mengakses properti kecerahan dan kontras serta mengubah nilai-nilai mereka.

![|Contoh Lapisan Penyesuaian Kecerahan/Kontras dalam PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

Jadi, mari kita ambil gambar anjing (b), misalnya, untuk menyesuaikan kecerahan1 dan kontras2-nya (a), menggunakan hanya metode pabrik dengan argumen yang sesuai, untuk akhirnya mendapatkan gambar (c) yang terlihat lebih hidup:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Catatan:

1. Nilai kecerahan harus dalam rentang -150 hingga 150.
2. Nilai kontras harus dalam rentang -50 hingga 100.

Merujuk ke dokumentasi dari [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) untuk lebih jelasnya.

## Kesimpulan

Dalam artikel ini kita telah mendapatkan gambaran singkat tentang lapisan penyesuaian Kecerahan/Kontras dan belajar bagaimana menyesuaikan kecerahan dan kontras gambar menggunakan metode pabrik.

Merujuk ke serangkaian [artikel tentang API lapisan penyesuaian](/psd/id/java/layer-types/adjustment-layer/) dari Aspose.PSD untuk Java untuk mempelajari lebih lanjut.

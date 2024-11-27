---
title: Lapisan Penyesuaian Hitam dan Putih
type: docs
weight: 30
url: /id/java/layer-types/adjustment-layer/levels/
---

## Bekerja dengan Lapisan Penyesuaian Level Photoshop di Java

Dalam artikel ini kita akan belajar bagaimana menyesuaikan rentang tonal dan keseimbangan warna dari foto dalam format file [PSD](/id/psd/java/psd-format/) secara programatik di Java. Kami tidak menggunakan editor foto Adobe® Photoshop® itu sendiri. Sebagai gantinya, kami menggunakan perpustakaan Aspose.PSD untuk Java yang bekerja sendiri untuk memanipulasi dokumen Photoshop.

Walaupun, Aspose.PSD untuk Java mendukung lebih dari cukup [alat untuk mengedit foto](/id/psd/java/manipulating-images/) sesuai keinginan kita, mari **gunakan API lapisan penyesuaian Levels** yang merupakan salah satu cara termudah dan tercepat untuk melakukannya.

## Gambaran API

Implementasi saat ini (20.6 pada saat penulisan) dari API lapisan penyesuaian Levels **mendukung semua fitur dasar dari Levels Photoshop**, yaitu, menyesuaikan Level masukan dan keluaran untuk saluran komposit (RGB) serta untuk setiap saluran warna primer (merah, hijau, dan biru).

API lapisan penyesuaian Levels sangat mudah. Kelas [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) adalah titik masuk untuk penyesuaian Levels. Ini berisi beberapa metode untuk mengakses saluran warna: getMasterChannel dan getChannel(int). Kedua metode mengembalikan [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) yang memiliki properti yang sesuai untuk memanipulasi Level masukan dan keluaran. Perbedaannya adalah getMasterChannel digunakan untuk menyesuaikan saluran warna komposit (RGB) sedangkan getChannel mengakses saluran warna tertentu (merah, hijau, atau biru) berdasarkan indeksnya.

## Kompatibilitas dengan mode warna

Perlu diperhatikan bahwa lapisan penyesuaian Levels **kompatibel dengan sebagian besar mode warna** menurut Levels Photoshop. Oleh karena itu, memungkinkan untuk menyesuaikan Levels untuk gambar dalam mode warna Grayscale (saluran abu-abu), RGB (saluran RGB, merah, hijau, dan biru), CMYK (saluran CMYK, sian, magenta, kuning, dan hitam), Duotone (saluran monotone) dan LAB (kecerahan, a, dan b saluran).

## Menyesuaikan rentang tonal

Secara sederhana, koreksi tonal diterapkan pada gambar untuk memetakan ulang bayangan dan sorotan guna distribusi ton tengah yang lebih baik. Umumnya, **hal itu membuat gambar terlihat lebih kontras** , jika dilakukan dengan benar. Sebagai contoh, mari ambil foto seekor anjing (b) dan menyesuaikan rentang tonalnya (a – tangkapan layar diambil dari jendela Levels Photoshop untuk menjelaskan) untuk membuat foto terlihat lebih kontras (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Gambar 1 Lapisan Levels](levels-adjustment-figure-1.png)|

Untuk **menyesuaikan rentang tonal secara keseluruhan** dari sebuah gambar, Level masukan saluran utama harus diatur:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

Perlu diingat bahwa Level masukan seharusnya berada dalam rentang 0 hingga 253 untuk bayangan, 9,99 hingga 0,01 untuk ton tengah, dan 2 hingga 255 untuk sorotan. Rentang Level keluaran harus antara 0 dan 255.

Ingin melihat contoh lebih lanjut? Anda dapat menemukannya di [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) dan di [basis pengetahuan](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Kesimpulan

Untuk merangkum, Aspose.PSD untuk Java memiliki API yang praktis dan sederhana untuk mengubah rentang tonal dan keseimbangan warna dari sebuah gambar yang kompatibel dengan hampir semua mode warna. API lapisan penyesuaian Levels dari perpustakaan ini mirip dengan Levels Photoshop, oleh karena itu, sangat mudah untuk memulai meskipun jika Anda belum pernah bekerja dengan perpustakaan ini sebelumnya.

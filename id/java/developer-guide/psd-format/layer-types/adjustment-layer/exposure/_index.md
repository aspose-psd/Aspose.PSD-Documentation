---
title: Lapisan Penyesuaian Paparan
type: docs
weight: 30
url: /id/java/layer-types/adjustment-layer/exposure/
---

# Bekerja dengan Lapisan Penyesuaian Paparan Photoshop di Java

Dalam artikel ini, kita akan menambahkan lapisan penyesuaian paparan ke dokumen Adobe® Photoshop® menggunakan Aspose.PSD untuk Java - perpustakaan manipulasi format file PSD. Perpustakaan ini dapat berfungsi tanpa editor Photoshop yang terinstal karena menggunakan algoritma pemrosesan gambar sendiri. Kita juga telah mempelajari beberapa detail terkait API penyesuaian paparan perpustakaan.

## Gambaran API

Lapisan penyesuaian paparan dikonfigurasi melalui kelas [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) yang berisi properti berikut untuk bekerja dengan penyesuaian paparan:

- Mendefinisikan seberapa banyak cahaya yang ada dalam foto dengan merenggangkan atau memampatkan seluruh histogram relatif terhadap warna hitam. Oleh karena itu, ini memberikan pengaruh terutama pada sorotan.
- Berbeda dengan pengaturan offset paparan, yang memberikan pengaruh terutama pada bayangan.
- Koreksi gamma. Ini memperbaiki kecerahan gambar.

## Memperbaiki Paparan

Memperbaiki paparan dan properti terkait sama mudahnya dengan mengubah beberapa properti kelas. Mari terapkan beberapa penyesuaian paparan (a) ke foto underexposured dari sebuah perpustakaan (b) sehingga dapat dilihat oleh mata manusia (c).

![Contoh Lapisan Penyesuaian Paparan](exposure-adjustment-layer-figure-1.png)

Seluruh penyesuaian sebagian besar dilakukan menggunakan koreksi gamma. Namun, paparan dan offset juga disesuaikan sedikit. Yang perlu Anda lakukan adalah mengatur nilai-nilai yang sesuai ke properti yang sudah disebutkan:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Perhatikan bahwa nilai paparan harus berada dalam rentang dari -20.0 hingga 20.0, nilai offset harus berada dalam rentang dari -0.5 hingga 0.5, dan rentang nilai koreksi gamma harus antara 9.99 dan 0.01.

Lihat [referensi API lapisan penyesuaian paparan](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) untuk lebih banyak detail.

## Kesimpulan

Dalam artikel ini, kita telah belajar bagaimana menambahkan lapisan penyesuaian paparan ke file PSD untuk menerangi gambar serta mempertimbangkan beberapa detail API.

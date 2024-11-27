---
title: Penyesuaian Lapisan Filter Foto
type: docs
weight: 30
url: /id/java/layer-types/adjustment-layer/photo-filter/
---

# Bekerja dengan lapisan penyesuaian Filter Foto Photoshop di Java

Hari ini kita akan melihat bagaimana cara menerapkan lapisan penyesuaian Filter Foto ke dokumen Photoshop yang sudah ada menggunakan Aspose.PSD untuk Java yang merupakan perpustakaan untuk memanipulasi format file PSD.

**API lapisan penyesuaian Filter Foto** mengubah keseimbangan warna gambar dengan menggunakan sentuhan warna. Hasil gambar akan terlihat sama seperti saat menggunakan filter kamera sungguhan. Perlu diperhatikan bahwa API lapisan penyesuaian Filter Foto dari perpustakaan sedikit berbeda dari Photoshop karena belum ada filter bawaan. Namun, itu sama dalam semua hal lain. Ini berarti bahwa Anda dapat mengatur warna tint dan mengubah keintensitasannya (densitas) serta menggunakan opsi Preservasi Luminositas.

## Ikhtisar API

API lapisan penyesuaian Filter Foto cukup mudah digunakan. Ada kelas utama [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) yang berfungsi sebagai titik masuk ke lapisan penyesuaian ini dan hanya berisi tiga properti publik, yaitu, warna, densitas, dan mempertahankan luminositas yang merupakan alat penyesuaian.

## Menyesuaikan keseimbangan warna

Karena tidak ada banyak hal untuk dibicarakan, mari kita langsung pertimbangkan **contoh penyesuaian keseimbangan warna** menggunakan Filter Foto sekarang. Kami akan menambahkan filter pemanasan (a) secara manual untuk gambar patung rusa (b) untuk mendapatkan gambar dalam nada hangat (c) yang lebih menyenangkan untuk dilihat.

![Contoh Lapisan Penyesuaian Filter Foto](photo-filter-adjustment-layer-figure-1.png)

Pertama-tama, perhatikan bahwa [metode pabrik](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) berbeda dari metode untuk [lapisan penyesuaian lainnya](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers) karena tidak ada metode default (tanpa argumen). Oleh karena itu, untuk menambahkan lapisan penyesuaian Filter Foto ke dalam dokumen Photoshop yang dimuat diperlukan satu argumen saja yaitu [warna](https://reference.aspose.com/psd/java/com.aspose.psd/Color). Jadi, untuk membuat efek filter pemanasan langsung lewatkan warna oranye sebagai argumen ke metode pabrik, lalu atur densitas menggunakan setter yang sesuai:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Perlu ditambahkan bahwa properti Densitas memiliki nilai default yaitu 100 serta nilai true adalah nilai default untuk properti Preservasi Luminositas (alasan mengapa kita tidak secara eksplisit mengaktifkan opsi ini).

## Kesimpulan

Dalam artikel ini kita mempertimbangkan penggunaan API lapisan penyesuaian Filter Foto dari Aspose.PSD untuk Java. Alat ini mudah digunakan dan memungkinkan untuk menambahkan tint pada gambar dengan densitas variabel. Itu adalah cara cepat untuk menyesuaikan keseimbangan warna dari gambar keseluruhan.

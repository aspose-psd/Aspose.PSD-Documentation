---
title: Penyesuaian Lapisan Keseimbangan Warna
type: docs
weight: 30
url: /id/java/layer-types/adjustment-layer/color-balance/
---

# Bekerja dengan lapisan penyesuaian Keseimbangan Warna Photoshop di Java

Dalam artikel ini kita akan **mengatur keseimbangan warna dari gambar** dalam format file PSD di Java. Kita akan menggunakan pustaka khusus yang disebut Aspose.PSD untuk Java yang merupakan toolbox untuk manipulasi dokumen Photoshop.

Karena pustaka bekerja dengan format file PSD, pustaka ini mengandung hampir [semua fitur](https://docs.aspose.com/psd/java/features/) yang tersedia di editor Photoshop dan **lapisan penyesuaian Keseimbangan Warna**, yang sangat cocok untuk tugas ini, bukanlah sebuah pengecualian.

Lapisan penyesuaian Keseimbangan Warna memungkinkan untuk mengubah keseimbangan antara warna primer (RGB) dan warna subtraktif (CMY) untuk bayangan, midtones, dan highlight dengan cara yang sederhana dan cepat.

## Menyesuaikan Keseimbangan Warna

Seperti yang disebutkan sebelumnya, lapisan penyesuaian Keseimbangan Warna di Aspose.PSD untuk Java adalah **penyeimbang antara warna primer dan warna subtraktif**. Ini berarti ada tiga skala untuk setiap pasangan warna (cyan/merah, magenta/hijau, kuning/biru). Intensitas warna tertentu dalam pasangan warna akan meningkat jika nilainya bergerak ke arahnya dan sebaliknya. Selain itu, ketiga pasangan tersebut melekat pada setiap area jangkauan tonal (bayangan, midtones, dan highlight) yang meningkatkan fleksibilitas penyesuaian semacam ini.

Jadi, mari kita terapkan pengetahuan ini dalam praktek. Sebagai contoh, kita memilih foto wajah wanita yang berwarna kemerahan (b). Wajahnya sangat kemerahan dan kita akan memperbaikinya dengan **menambahkan lapisan penyesuaian Keseimbangan Warna** untuk mengurangi warna merah dan meningkatkan cyan pada dasarnya (a) untuk mendapatkan wajah yang terlihat lebih alami (c). Sekali lagi, masih banyak pekerjaan yang harus dilakukan dengan gambar ini tetapi dalam artikel ini, itulah yang akan kita lakukan.

![Contoh lapisan penyesuaian Keseimbangan Warna](color-balance-adjustment-layer-example-figure-1.png) API dari lapisan penyesuaian Keseimbangan Warna memiliki desain yang sederhana. Oleh karena itu, kelas [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) itulah yang Anda perlukan. Pertama-tama, pertahankan kecerahan karena itu dinonaktifkan secara default. Kemudian, tambahkan sedikit warna hijau dan lebih banyak warna kuning untuk bayangan menggunakan metode yang sesuai (nama dari area jangkauan tonal tertentu dan nama warna dalam pasangan warna), kemudian tambahkan lebih banyak cyan dan sedikit biru untuk midtones, dan terakhir tambahkan lebih banyak cyan selain sedikit magenta dan biru:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Sekarang, kita telah mendapatkan gambar yang kita inginkan! Sangatlah mudah, bukan?

Perhatikan bahwa _nilai dari setiap pasangan warna harus berada dalam kisaran dari -100 hingga 100_ yang merupakan nilai negatif untuk warna subtraktif dan positif untuk warna primer masing-masing, persis seperti di editor Photoshop.

Merujuk ke referensi API kami untuk mengetahui lebih banyak detail teknis tentang [lapisan penyesuaian Keseimbangan Warna](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Kesimpulan

Dalam artikel ini, kita telah membahas bagaimana mengatur Keseimbangan Warna dari gambar secara programatik dalam Java menggunakan pustaka Aspose.PSD untuk Java. Pustaka ini mengandung API yang lengkap untuk bekerja dengan lapisan penyesuaian Keseimbangan Warna dalam dokumen Photoshop.

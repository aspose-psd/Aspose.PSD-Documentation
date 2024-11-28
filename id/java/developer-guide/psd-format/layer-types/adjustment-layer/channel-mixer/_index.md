---
title: Layer Tipe Saluran Pengaturan
type: dokumentasi
weight: 30
url: /id/java/layer-types/adjustment-layer/channel-mixer/
---

# Bekerja dengan lapisan pengatur saluran Photoshop di Java

Hari ini kita akan melihat bagaimana cara mencampur warna saluran dalam dokumen Photoshop secara berbasis pemrograman di Java. Karena editor Photoshop tidak mendukung scripting Java, kita akan menggunakan perpustakaan manipulasi format file PSD khusus yang disebut Aspose.PSD untuk Java.

Perpustakaan ini berisi **API untuk bekerja dengan saluran warna**. Ada beberapa cara untuk mencampur warna tetapi, dalam artikel ini, kita akan fokus pada lapisan pengatur saluran Mixer Saluran.

API lapisan pengatur saluran Mixer **memungkinkan bermain dengan saluran warna** untuk membuat gambar berwarna tirus atau menciptakan efek warna kreatif yang berbeda atau bahkan mengkonversi gambar menjadi hitam dan putih. Selanjutnya, kita akan mempertimbangkan bagaimana menerapkan lapisan pengatur saluran Mixer ke dokumen Photoshop yang ada menggunakan Aspose.PSD untuk Java tetapi pertama-tama kita perlu membicarakan fitur API secara keseluruhan.

## Tinjauan API

Tidak ada yang spesial dalam pembuatan lapisan pengatur saluran Mixer. Ini dapat ditambahkan melalui [metode pabrik default](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) yang mengembalikan contoh kelas ChannelMixerLayer. Kelas ini berisi fungsionalitas umum seperti opsi Monochrome dan metode untuk mendapatkan saluran keluaran. Saluran keluaran tertentu dapat menjadi salah satu dari dua tipe: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) atau [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Tipe [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) tergantung pada [mode warna](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) dari gambar.

## Membuat gambar menjadi monokrom

Sekarang, mari kita pertimbangkan dan contoh penerapan lapisan pengatur saluran Mixer ke dalam dokumen Photoshop yang ada. Karena jenis lapisan pengatur seperti ini belum mendukung preses, kita akan **membuat ulang preset Photoshop Infrared Hitam & Putih (RGB)** (a). Preset akan diterapkan pada gambar pohon yang mekar (b). Sebagai hasilnya, kita ingin mencapai efek fotografi inframerah (c).

![Contoh Lapisan Pengatur Saluran Mixer](channel-mixer-adjustment-psd-layer-figure-1.png) Pertama, untuk membuat ulang preset Photoshop Infrared Hitam & Putih, perlu mengaktifkan tanda monokrom dan mengatur nilai mentah yang sesuai untuk setiap warna (merah, hijau, dan biru) untuk saluran keluaran Abu-abu:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

Gambar harus berada dalam mode warna RGB agar kode berfungsi (karena penyesuaian ke kelas RgbMixerChannel). Mode warna CMYK juga didukung tetapi hanya untuk gambar dengan mode warna yang sesuai.

Ingatlah bahwa nilai setiap warna serta properti Konstan harus berada dalam rentang -200 hingga 200.

## Kesimpulan

Dalam artikel ini, kita telah mempertimbangkan bagaimana cara bekerja dengan API Channel Mixer dari Aspose.PSD untuk Java untuk menyesuaikan warna dalam saluran warna serta mengkonversi gambar menjadi hitam dan putih.

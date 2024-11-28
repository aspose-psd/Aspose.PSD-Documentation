---
title: Penyesuaian Lapisan Terbalik
type: dokumen
weight: 30
url: /id/java/layer-types/adjustment-layer/invert/
---

# Bekerja dengan Lapisan Penyesuaian Terbalik Photoshop dalam Java

Dalam artikel ini, kami akan menunjukkan bagaimana mengubah gambar dalam dokumen Photoshop menjadi negatif secara terprogram dengan Java. Untuk tujuan ini, kami akan menggunakan pustaka manipulasi format file PSD yang disebut Aspose.PSD untuk Java.

API inversi warna memungkinkan untuk **menambahkan efek negatif pada gambar**. Anda mungkin sudah melihat bagaimana [membalik warna gambar menggunakan lapisan penyesuaian Kurva](/psd/id/id/java/layer-types/adjustment-layer/curves/). Namun, hari ini kami akan mempertimbangkan cara yang lebih cepat dan lebih mudah untuk melakukan pekerjaan dengan lapisan penyesuaian Terbalik.

## Gambaran API

**API lapisan penyesuaian Terbalik** terdiri dari kelas lapisan itu sendiri yang disebut [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Kelas ini tidak memiliki anggota publik sendiri, karena mewarisi semua anggota publik dari kelas induk ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). Hal ini membuat penggunaannya menjadi lebih sederhana karena yang perlu Anda lakukan hanyalah menambahkannya ke file PSD dan gambar tersebut menjadi negatif.

## Balik warna gambar

Jadi, meskipun tampak jelas tetapi biarlah kami tunjukkan untuk kejelasan bagaimana **menerapkan lapisan penyesuaian Terbalik pada gambar** seorang astronot (a) untuk membuat efek negatif pada gambar tersebut (b).

![Contoh Lapisan Penyesuaian Terbalik Sebelum dan Sesudah](invert-adjustment-layer-figure-1.png)

Untuk **membalik warna gambar**, cukup tambahkan lapisan penyesuaian Terbalik ke dalam PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

Itu saja! Tidak ada properti khusus yang perlu dikonfigurasi untuk jenis lapisan penyesuaian ini.

## Kesimpulan

Dalam artikel ini, kita belajar tentang API lapisan penyesuaian Terbalik dari Aspose.PSD untuk Java. Ini adalah alat yang mudah untuk mendapatkan gambar negatif karena API dari lapisan penyesuaian ini tidak mendeklarasikan anggota publik apa pun.

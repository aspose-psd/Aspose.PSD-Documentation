---
title: Layer Penyesuaian Kurva
type: docs
weight: 30
url: /id/java/layer-types/adjustment-layer/curves/
---

# Bekerja dengan lapisan penyesuaian Kurva Photoshop di Java

Tujuan dari artikel ini adalah untuk menunjukkan kemampuan pustaka Aspose.PSD untuk Java saat **bekerja dengan lapisan penyesuaian Kurva** di dokumen Adobe® Photoshop®. Pustaka ini sepenuhnya otonom. Oleh karena itu, pustaka ini berfungsi tanpa menginstal editor foto Photoshop. [Daftar lengkap fitur](https://docs.aspose.com/psd/java/features/) dapat ditemukan di basis pengetahuan kami. Nah, sekarang kembali ke Kurva.

## Tinjauan API

Alat Kurva dapat diwakili sebagai garis diagonal (kurva) pada grafik dengan sorotan di sudut kanan atas dan bayangan di sudut kanan bawah.

Pustaka menyediakan API untuk bekerja dengan kurva, yaitu kelas [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Namun, kelas ini mempunyai **dua pendekatan yang benar-benar berbeda** untuk bekerja dengan kurva. Oleh karena itu, kurva tersebut dapat diedit dalam satu dari dua mode sekali pada suatu waktu:

- Berkelanjutan (kurva diwakili sebagai jalur dengan titik-titik di tempat pembelokan)
- Diskrit (kurva diwakili sebagai garis titik-titik)

Jadi, pustaka tersebut memiliki dua cara untuk memodifikasi kurva menggunakan [manajer berkelanjutan](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) dan [manajer diskrit](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) secara berturut-turut. Selanjutnya, kami akan menjelaskan bagaimana cara menggunakan masing-masing dari mereka pada contoh spesifik.

## Sesuaikan warna dan nada menggunakan Manajer Berkelanjutan Kurva

[Manajer Berkelanjutan Kurva](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **mengonfigurasi titik-titik pembengkokan dari kurva berkelanjutan** untuk saluran komposit (RGB) serta untuk setiap saluran warna tertentu. Untuk tujuan demonstrasi, beberapa penyesuaian Kurva (a) akan diterapkan pada gambar tergelap dari orkestra (b) untuk mendapatkan gambar yang lebih terang dengan warna yang lebih hangat (c):

![Gambar Lapisan Penyesuaian Kurva Figur 1](kurves-psd-lapisan-penyesuaian-gambar-1.png)

Karena ada dua manajer, perlu untuk secara eksplisit memilih satu (manajer berkelanjutan dalam hal ini), sebelum memperolehnya. Selanjutnya, kita dapat langsung menambahkan titik kurva pada koordinat tertentu untuk saluran warna yang diinginkan (komposit RGB, merah, dan biru secara berturut-turut) untuk merekonstruksi bentuk kurva:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

Asal koordinat berada di sudut kiri bawah. Nilai koordinat maksimum dari suatu titik terbatas pada jenis data (byte) dan sama dengan 255 (127 untuk tipe yang ditandatangani).

Terdapat juga beberapa [metode lainnya](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) yang dapat Anda gunakan.

## Sesuaikan nada menggunakan Manajer Diskrit Kurva

Manajer Diskrit Kurva juga memungkinkan untuk menempatkan titik kurva (mengubah warna dan nada sebenarnya), tetapi perbedaannya adalah bahwa mereka melakukannya dengan cara yang berbeda. Pertama, **kurva terdiri dari titik-titik** atau titik-titik (bukan garis solid). Kedua, manajer ini **tidak menempatkan titik di mana pun** pada grafik. Sebaliknya, ia **menggeser titik ke atas atau ke bawah** dengan rentang nilai antara 255 dan 0 berturut-turut. Secara default, nilai titik kurva bertambah secara inkremental untuk membentuk kurva yang berada pada sudut 45 derajat.

Dengan demikian, dengan mempertimbangkan hal tersebut, mudah untuk merekonstruksi preset Photoshop &quot;Negatif (RBG)&quot; (a) dan menerapkannya pada gambar skala abu-abu dari lembah (b) untuk pada akhirnya mendapatkan representasi negatif dari lembah (c).

![Gambar Lapisan Penyesuaian Kurva Figur 2](kurves-psd-lapisan-penyesuaian-gambar-2.png) Pertama-tama, jangan lupa untuk memilih manajer yang sesuai untuk dapat menggunakannya dan kemudianatur nilai titik kurva secara menurun dimulai dari 255 hingga 0 untuk setiap titik kurva (total 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Manajer ini juga menyediakan beberapa [metode lainnya](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) untuk mengelola kurva.

## Kesimpulan

Dalam artikel ini kita telah belajar bagaimana bekerja dengan lapisan penyesuaian Kurva di dokumen Photoshop menggunakan Aspose.PSD untuk Java dalam dua cara yang benar-benar berbeda (melalui manajer berkelanjutan dan diskrit).

---
title: Dukungan untuk Lapisan Isian
type: docs
weight: 50
url: /id/java/dukungan-untuk-lapisan-isian/
---

## **Dukungan untuk Lapisan Isian dengan Isian Warna**
Artikel ini menunjukkan bagaimana mengisi lapisan PSD dengan Warna. Silakan menggunakan Aspose.PSD.FileFormats.Psd.Layers.FillLayer untuk menambahkan Warna ke lapisan PSD. Potongan kode berikut memuat file PSD, mengakses kelas Filllayer, dan mengatur warna menggunakan properti FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Dukungan untuk Lapisan Isian dengan Isian Gradien**
Artikel ini menunjukkan penggunaan isian Gradien untuk mengisi lapisan PSD. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD telah mengekspos kelas GradientColorPoint dan GradientTransparencyPoint untuk menambahkan efek Gradien ke lapisan.

Langkah-langkah untuk mengisi lapisan PSD dengan isian Gradien adalah sebagai berikut:

- Memuat file PSD sebagai gambar menggunakan metode Load yang diekspos oleh kelas Image.
- Mengatur properti pengaturan objek FillLayer.
- Membuat daftar ColorPoints dengan warna yang diperlukan dan posisi warna.
- Membuat daftar TransparencyPoints dengan opacity yang diperlukan dan posisi titik transparansi.
- Panggil metode FillLayer.Update.
- Simpan hasilnya.

Potongan kode berikut menunjukkan bagaimana menambahkan isian Gradien untuk mengisi lapisan PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Efek Stroke dengan Isian Warna**
Artikel ini menunjukkan bagaimana merender efek stroke dengan isian warna. Efek Stroke digunakan untuk menambahkan garis-garis dan batas ke lapisan dan bentuk. Ini dapat digunakan untuk membuat garis berwarna solid, gradien yang berwarna-warni, serta batas bergaya.

Langkah-langkah untuk merender efek Stroke dengan isian warna adalah sebagai berikut:

- Mengatur properti **LoadEffectsResource**.
- Memuat file PSD sebagai gambar menggunakan metode Load yang diekspos oleh kelas Image dan mendefinisikan **PsdLoadOptions**.
- Mengatur properti pengaturan **ColorFillSetting.**
- Simpan hasilnya.

Potongan kode berikut menunjukkan bagaimana merender efek Stroke dengan isian warna.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}

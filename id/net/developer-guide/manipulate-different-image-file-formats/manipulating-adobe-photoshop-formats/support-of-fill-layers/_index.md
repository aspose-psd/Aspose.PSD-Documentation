---
title: Dukungan Lapisan Isian
type: docs
weight: 90
url: /id/net/support-of-fill-layers/
---


## **Lapisan Isian dengan Pola Isian**
Artikel ini menunjukkan cara mengisi lapisan [PSD](https://wiki.fileformat.com/image/psd/) dengan pola isian. Pola adalah gambar, warna, bayangan, atau garis yang digunakan untuk mengisi area gambar. Gunakan Aspose.PSD.FileFormats.Psd.Layers.FillLayer untuk menambahkan Pola ke lapisan PSD. Potongan kode berikut memuat file PSD, mengakses kelas [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer), dan mengatur Pola menggunakan properti [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}

Berikut contoh lain yang menunjukkan bagaimana [Aspose.PSD](https://products.aspose.com/psd/net) merender pola dengan menggunakan [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) dan [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}

## **Lapisan Isian dengan Isian Gradien**
Artikel ini memperlihatkan penggunaan isian Gradien untuk mengisi lapisan PSD. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD telah mengekspos kelas [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) dan [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) untuk menambahkan efek Gradien ke lapisan.

Langkah-langkah untuk mengisi lapisan PSD dengan isian Gradien adalah sebagai berikut:

- Memuat file PSD sebagai gambar menggunakan metode pabrik [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) yang diekspos oleh kelas [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Tentukan properti pengaturan dari objek [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Buat daftar [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) dengan warna yang diperlukan dan posisi warna.
- Buat daftar titik transparansi dengan opasitas yang diperlukan dan posisi titik transparansi.
- Panggil metode [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Simpan hasilnya.

Potongan kode berikut menunjukkan cara menambahkan isian Gradien ke lapisan PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}

**Berikut contoh lain yang menggunakan properti [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** untuk mengisi lapisan PSD dengan isian Gradien. Aspose.PSD mendukung jenis gradien berikut melalui enumerasi GradientType:

- **GradientType.Linear:**       Dalam gradien linear, transisi warna dari hue awal ke akhir dalam garis lurus.
- **GradientType.Radial:**       Dalam gradien radial, warna menjalar dari titik awal dalam pola lingkaran.
- **GradientType.Angle:**        Gradien sudut berputar berlawanan arah jarum jam sekitar titik mulai.
- **GradientType.Reflected:** Dalam gradien pantulkan, warna dipantulkan di kedua sisi titik mulai.
- **GradientType.Diamond:**   Gradien berlian menciptakan bentuk berlian dari titik mulai.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}

## **Dukungan untuk Properti Skala pada Lapisan Isian Gradien**
Artikel ini menunjukkan cara menyesuaikan lapisan FillLayer dengan isian gradien menggunakan Aspose.PSD untuk .NET. Untuk tujuan ini, properti baru [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) telah ditambahkan dalam [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings)**.** 

Berikut adalah demonstrasi kode yang menunjukkan cara menggunakan properti **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}

## **Lapisan Isian dengan Isian Warna**
Artikel ini menunjukkan cara mengisi lapisan [PSD](https://wiki.fileformat.com/image/psd/) dengan Warna. Silakan gunakan kelas [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) untuk menambahkan Warna ke lapisan PSD. Potongan kode berikut memuat file PSD, mengakses kelas lapisan Fill, dan mengatur warna menggunakan properti [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}


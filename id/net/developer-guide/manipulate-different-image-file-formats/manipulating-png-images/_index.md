---
title: Memanipulasi Gambar PNG
type: docs
weight: 40
url: /id/net/memanipulasi-gambar-png/
---

## **Menentukan Transparansi untuk Gambar PNG**
Salah satu kelebihan menyimpan gambar dalam format PNG adalah PNG dapat memiliki latar belakang transparan. Aspose.PSD untuk .NET menyediakan fitur untuk menentukan transparansi untuk Gambar PNG & gambar Raster seperti yang ditunjukkan dalam bagian di bawah ini. Aspose.PSD untuk .NET API dapat digunakan untuk menetapkan warna apa pun sebagai transparan saat membuat gambar PNG baru atau mengonversi gambar yang ada ke format PNG. Untuk tujuan ini, Aspose.PSD untuk .NET API telah mengekspos properti [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) dan enumerasi [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) yang dapat diatur untuk menentukan warna mana yang akan dirender sebagai transparan dalam gambar PNG. Potongan kode di bawah ini menunjukkan bagaimana mengonversi gambar PSD yang ada ke gambar PNG dengan menentukan warna yang diinginkan sebagai transparan.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **Mengatur Resolusi untuk Gambar PNG**
Aspose.PSD untuk .NET mengekspos kelas ResolutionSetting yang dapat digunakan untuk mengatur resolusi untuk semua format gambar termasuk PNG. Artikel ini menunjukkan penggunaan Aspose.PSD untuk .NET API untuk mengatur parameter resolusi horizontal & vertikal untuk format gambar PNG. Potongan kode di bawah ini memuat gambar PSD yang ada dan mengonversinya ke format PNG sambil mengubah resolusinya.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **Mengkompresi File PNG**
Portable Network Graphic (PNG) adalah format kompresi lossless untuk mentransmisikan bitmap melalui jaringan. Saat Anda menyimpan gambar sebagai file PNG dalam program apa pun, Anda mungkin diminta untuk memilih tingkat kompresi dalam rentang dari 0 hingga level maksimum tertentu. Mengatur nilai ini sebenarnya mengompresi ukuran file dan tidak mengurangi kualitas gambar. Artikel ini menjelaskan bagaimana API Aspose.PSD memungkinkan Anda mengontrol ukuran file PNG. API Aspose.PSD dapat digunakan untuk mengatur Tingkat Kompresi untuk format file PNG dengan menggunakan kelas PngOptions yang memiliki properti int tipe [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel). Properti ini menerima nilai dari 0 hingga 9 di mana 9 adalah kompresi maksimum. Potongan kode di bawah ini menunjukkan bagaimana mengatur Tingkat Kompresi menggunakan Aspose.PSD untuk API .NET.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **Menentukan Kedalaman Bit untuk Gambar PNG**
Kedalaman bit dalam penggambaran adalah jumlah bit yang digunakan untuk menunjukkan warna dari satu piksel dalam gambar bitmap. Seperti semua format bitmap lainnya, kedalaman warna PNG juga direpresentasikan dalam bit seperti 1-bit (2 warna), 2-bit (4 warna), 4-bit (16 warna) dan 8-bit (256 warna). Aspose.PSD untuk API .NET dapat digunakan untuk mengatur kedalaman bit untuk gambar PNG dengan menggunakan properti [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) yang diekspos oleh kelas PngOptions. Saat ini, properti BitDepth dapat diatur ke 1, 2, 4, atau 8 bit untuk tipe warna grayscale dan indexed. Untuk semua tipe warna lainnya, hanya 8 bit yang didukung. Potongan kode di bawah ini menunjukkan bagaimana mengatur Kedalaman Bit untuk gambar PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **Menerapkan Metode Filter pada Gambar PNG**
Kedalaman bit dalam penggambaran adalah jumlah bit yang digunakan untuk menunjukkan warna dari satu piksel dalam gambar bitmap. Seperti semua format bitmap lainnya, kedalaman warna PNG juga direpresentasikan dalam bit seperti 1-bit (2 warna), 2-bit (4 warna), 4-bit (16 warna) dan 8-bit (256 warna). Aspose.PSD untuk API .NET dapat digunakan untuk mengatur kedalaman bit untuk gambar PNG menggunakan properti BitDepth yang diekspos oleh kelas PngOptions. Saat ini, properti BitDepth dapat diatur ke 1, 2, 4, atau 8 bit untuk tipe warna grayscale dan indexed. Untuk semua tipe warna lainnya, hanya 8 bit yang didukung. Potongan kode di bawah ini menunjukkan bagaimana mengatur Kedalaman Bit untuk gambar PNG.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **Mengubah Warna Latar Belakang dari Gambar PNG Transparan**
Gambar format PNG dapat memiliki latar belakang transparan. Aspose.PSD untuk .NET menyediakan fitur untuk mengubah warna latar belakang dari gambar PNG yang memiliki latar belakang transparan. Aspose.PSD untuk .NET API dapat digunakan untuk menetapkan/mengubah warna gambar PNG transparan. Potongan kode di bawah ini menunjukkan bagaimana menetapkan/mengubah warna latar belakang dari gambar PNG transparan.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}

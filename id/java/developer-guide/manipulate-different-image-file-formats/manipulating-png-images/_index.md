---
title: Memanipulasi Gambar PNG
type: docs
weight: 30
url: /id/java/memanipulasi-gambar-png/
---

## **Menentukan Transparansi untuk Gambar PNG**
Salah satu keuntungan menyimpan gambar dalam format PNG adalah bahwa PNG dapat memiliki latar belakang transparan. Aspose.PSD untuk Java menyediakan fitur untuk menentukan transparansi untuk kelas PngImage & RasterImage seperti yang ditunjukkan dalam bagian di bawah ini. Aspose.PSD untuk Java API dapat digunakan untuk menentukan warna apa pun sebagai transparan saat membuat gambar PNG baru atau mengonversi gambar yang ada ke format PNG. Untuk tujuan ini, API Aspose.PSD untuk Java telah mengekspos properti TransparentColor dan enumerasi PngColorType yang dapat diatur untuk menentukan warna mana yang akan di-render sebagai transparan dalam gambar PNG. Potongan kode di bawah ini mendemonstrasikan bagaimana mengonversi gambar PSD yang ada ke gambar PNG dengan menggunakan konstruktor overload PngImage dan menentukan warna yang diinginkan sebagai transparan.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Mengatur Resolusi untuk Gambar PNG**
Aspose.PSD untuk Java mengekspos kelas ResolutionSetting yang dapat digunakan untuk mengatur resolusi untuk semua format gambar termasuk PNG. Artikel ini mendemonstrasikan penggunaan API Aspose.PSD untuk Java untuk mengatur parameter resolusi horizontal & vertikal untuk format gambar PNG. Potongan kode di bawah ini memuat gambar PSD yang ada dan mengonversinya ke format PNG serta mengubah resolusinya.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **Mengompresi Berkas PNG**
Portable Network Graphic (PNG) adalah format kompresi lossless untuk mentransmisikan bitmap melalui jaringan. Ketika Anda menyimpan gambar sebagai berkas PNG dalam program apa pun, Anda mungkin diminta untuk memilih tingkat kompresi dalam rentang dari 0 hingga tingkat maksimum. Mengatur nilai ini sebenarnya akan mengompresi ukuran berkas dan tidak akan menurunkan kualitas gambar. Artikel ini menjelaskan bagaimana API Aspose.PSD memungkinkan Anda mengontrol ukuran berkas PNG. API Aspose.PSD dapat digunakan untuk mengatur Tingkat Kompresi untuk format berkas PNG menggunakan kelas PngOptions yang memiliki properti CompressionLevel bertipe int. Properti ini menerima nilai dari 0 hingga 9 di mana 9 adalah kompresi maksimum. Potongan kode di bawah ini mendemonstrasikan cara mengatur Tingkat Kompresi menggunakan Aspose.PSD untuk Java API.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Menentukan Kedalaman Bit untuk Gambar PNG**
Kedalaman bit dalam pengindraan adalah jumlah bit yang digunakan untuk menunjukkan warna dari satu piksel tunggal dalam gambar bitmap. Seperti semua format bitmap lainnya, kedalaman warna PNG juga direpresentasikan dalam bit seperti 1-bit (2 warna), 2-bit (4 warna), 4-bit (16 warna) dan 8-bit (256 warna). API Aspose.PSD untuk Java dapat digunakan untuk mengatur kedalaman bit untuk gambar PNG menggunakan properti BitDepth yang diekspos oleh kelas PngOptions. Saat ini, properti BitDepth dapat diatur ke 1, 2, 4, atau 8 bit untuk tipe warna grayscale dan indexed. Untuk semua tipe warna lainnya hanya 8 bit yang didukung. Potongan kode di bawah ini mendemonstrasikan cara mengatur Kedalaman Bit untuk gambar PNG.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Menerapkan Metode Filter pada Gambar PNG**
Aspose.PSD untuk Java mengekspos enumerasi PngFilterType  yang dapat digunakan untuk mengatur jenis filter untuk gambar PNG. Potongan kode di bawah ini mendemonstrasikan bagaimana menerapkan filter pada berkas PSD yang ada untuk gambar PNG dengan menggunakan PngFilterType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Mengubah Warna Latar Belakang dari Gambar PNG Transparan**
Gambar format PNG dapat memiliki latar belakang transparan. Aspose.PSD untuk Java menyediakan fitur untuk mengubah warna latar belakang dari gambar PNG yang memiliki latar belakang transparan. API Aspose.PSD untuk Java dapat digunakan untuk mengatur/mengubah warna dari gambar PNG transparan. Potongan kode di bawah ini mendemonstrasikan bagaimana mengatur/mengubah warna latar belakang dari gambar PNG transparan.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}

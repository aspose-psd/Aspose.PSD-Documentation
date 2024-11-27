---
title: Header Berkas PSD dan PSB
type: docs
weight: 40
url: /id/net/psd-dan-psb-file-header/
---

## **Deskripsi**
Header Berkas Adobe Photoshop berisi informasi tentang versi Berkas (1 untuk PSD dan 2 untuk PSB), Jumlah Saluran, Mode Warna, dan Kedalaman Bit.

Anda dapat mempelajari Kombinasi Mode Warna dan Kedalaman Bit yang didukung oleh Aspose.PSD dari artikel terkait.


Header berkas berisi properti dasar dari gambar.

|**Panjang**|**Deskripsi**|
| :- | :- |
|4|Tanda Tangan: selalu sama dengan *"8BPS"*|
|2|[Versi PSD](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): selalu sama dengan 1 untuk Berkas PSD dan 2 untuk Berkas PSB. Aspose.PSD dapat mendeteksi versi Format Berkas dan membacanya dengan benar.|
|6|Dipesan: harus nol.|
|2|Jumlah saluran dalam gambar, termasuk saluran alpha apa pun. Rentang yang didukung adalah 1 hingga 56.|
|4|Tinggi gambar dalam piksel. Rentang yang didukung adalah 1 hingga 30.000. Berkas PSB mendukung tinggi hingga 300.000 piksel. Berkas PSB juga didukung oleh Aspose.PSD.|
|4|Lebar gambar dalam piksel. Rentang yang didukung adalah 1 hingga 30.000. Berkas PSB mendukung lebar hingga 300.000 piksel. Pengolahan batch berkas PSD/PSB besar juga didukung oleh Aspose.PSD.|
|2|Kedalaman: jumlah bit per saluran. Nilai yang didukung adalah 1, 8, 16, dan 32. Namun tidak setiap Mode Warna bekerja dengan setiap kedalaman.|
|2|Mode warna [PSD](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes) dari berkas. Nilai yang didukung adalah: Bitmap = 0; Grayscale = 1; Indexed = 2; RGB = 3; CMYK = 4; Multichannel = 7; Duotone = 8; Lab = 9.|
Anda dapat memeriksa [Referensi API PSD](https://reference.aspose.com/psd) kami untuk itu.

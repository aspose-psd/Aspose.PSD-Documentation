---
title: Kombinasi Mode Warna Dan Kedalaman Bit yang Didukung dalam PSD
type: docs
weight: 80
url: /id/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **Deskripsi**
Aspose.PSD Mendukung pembukaan File PSD dengan setiap kombinasi Mode Warna dan Kedalaman Bit di Adobe Photoshop PSD Files. Anda dapat membuka file-file tersebut dan menggunakan API Tingkat Rendah untuk memodifikasi konten dari file tersebut. Namun, untuk beberapa kombinasi yang kurang populer dapat terdapat isu spesifik, beberapa di antaranya terkait dengan Batasan Mode Warna.

## **Kombinasi Mode Warna Dan Kedalaman Bit yang Didukung dalam PSD dalam mode hanya baca**

| |Bitmap|Grayscale|Indexed|RGB|CMYK|Multichannel|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Kedalaman 1|Ya[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Kedalaman 8|-|Ya|Ya|Ya|Ya|Tidak Q3-Q4|Tidak Q3-Q4|Ya[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Kedalaman 16|-|Ya|-|Ya|Ya|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Tidak (Q3-Q4)|
|Kedalaman 32|-|Ya*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Ya*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Isu minor dalam beberapa kasus

## **Kombinasi Mode Warna Dan Kedalaman Bit yang Didukung dalam PSD dalam mode dapat diedit**

| |Bitmap|Grayscale|Indexed|RGB|CMYK|Multichannel|Duotone|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Kedalaman 1|Ya|-|-|-|-|-|-|-|
|Kedalaman 8|-|Ya|Tidak|Ya|Ya|Tidak Q3-Q4|Tidak Q3-Q4|Ya*|
|Kedalaman 16|-|Ya|-|Ya|Ya*|-|-|Tidak (Q3-Q4)|
|Kedalaman 32|-|Tidak (Q3-Q4)|-|Tidak (Q3-Q4)|-|-|-|-|
\* Isu minor dalam beberapa kasus

Jika Anda membutuhkan dukungan untuk Kombinasi Mode Warna / Kedalaman Bit yang spesifik, Anda dapat mempostingnya di [Aspose Forums](https://forum.aspose.com/c/psd)

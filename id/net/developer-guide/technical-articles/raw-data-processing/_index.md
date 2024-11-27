---
title: Pengolahan Data Mentah
type: docs
weight: 50
url: /id/pengolahan-data-mentah/
---

## **Pengolahan Data Mentah**
Untuk meningkatkan kinerja API Aspose.PSD kami, kami memperkenalkan metode pengolahan data mentah dengan versi 2.4.0. Pengolahan data mentah saat ini digunakan secara internal dan memiliki API eksternal sehingga dapat digunakan dari luar perpustakaan untuk meningkatkan kinerja keseluruhan. Kadang-kadang, proses ini bisa sedikit rumit dan memerlukan penjelasan. Pengolahan data mentah saat ini hanya tersedia untuk format BMP.

Untuk membantu para pengembang memperoleh kinerja terbaik, API Aspose.PSD menyediakan sistem pengolahan data mentah yang memiliki API eksternal untuk kustomisasi. Para pengembang memanggil metode keluarga [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) dan [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) untuk menggunakan pengolahan data mentah. Metode-metode ini juga memerlukan format data mentah yang diinginkan diatur menggunakan kelas [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings). Kelas RawDataSettings memungkinkan para pengembang untuk menentukan format data mentah apa pun. Namun, untuk mencapai kinerja terbaik, Anda perlu menggunakan format data mentah di mana data disimpan. RawDataSettings yang didefinisikan dalam kelas [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) membantu menentukan format [data mentah](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat) gambar tersebut. Saat meneruskan instance RawDataSettings ke metode LoadRawData, data dikembalikan apa adanya, tanpa konversi yang diterapkan, dan dapat meningkatkan kinerja. Di sisi lain, Anda perlu memperhatikan semua layout format data mentah yang mungkin terkadang agak rumit.

Untuk menyederhanakan proses penanganan, dengan mengurangi kinerja sedikit, Anda dapat menentukan RawDataSettings yang diinginkan dengan menginisialisasi kelas dengan pengaturan data mentah yang diinginkan. Ada kasus di mana tidak mungkin mengembalikan data mentah dalam format yang ditentukan (misalnya konversi dari ruang warna CMYK ke RGB tidak tersedia di versi 2.4.0). Selain itu, mungkin ada skenario di mana pengolahan data mentah tidak tersedia sama sekali untuk suatu format gambar. Untuk mengetahui apakah Anda dapat menggunakan metode keluarga LoadRawData dan SaveRawData, Anda perlu menanyakan properti [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable).
### **Wawasan**
Untuk format [data pixel RGB](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) terdapat format data mentah berbasis palet (indeks) dan RGB. Format data mentah indeks berisi indeks entri palet dalam rentang 0..(2^jumlah bit – 1). Format data mentah indeks adalah 1, 2, 4, dan 8 bit per pixel. Sisanya adalah format data mentah berbasis RGB. Saat memuat data mentah, pastikan bahwa tersedia byte yang cukup untuk memuat data, jika tidak, akan dilemparkan pengecualian yang sesuai. Anda dapat memperkirakan ukuran array byte dengan mengalikan ukuran baris dengan jumlah baris yang diperlukan. Ukuran baris bisa bervariasi tergantung pada format penyimpanan data mentah.

Untuk mencapai kinerja terbaik, selalu gunakan ukuran baris data mentah yang sama dengan nilai properti [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize). Namun, terkadang Anda mungkin perlu menambahkan padding tambahan ke baris data mentah, atau menguranginya, dan jika demikian, ukuran baris yang berbeda dapat digunakan. Jika diperlukan subset dari persegi panjang pembatas gambar, maka perhatikan pergeseran bit yang mungkin terjadi untuk format pixel RGB indeks. Sebagai contoh, mari kita pertimbangkan sebuah gambar dengan dimensi 100x100 pixel dan format data mentah 1 bit per pixel. Anda ingin memuat persegi panjang data mentah dengan lokasi (7,0) dan dimensi (2,1), atau dengan kata lain, Anda memerlukan 2 pixel dimulai dari x=7 dan y=0. Dalam hal ini, Anda akan menerima tata letak data berikut:



![todo:image_alt_text](raw-data-processing_1.png)

Ini berarti Anda menerima 2 byte di mana byte pertama berisi 7 piksel yang tidak diinginkan, kemudian 1 piksel yang diinginkan, dan byte kedua berisi 1 piksel yang diinginkan dan kemudian 7 yang tidak diinginkan. Anda mungkin bertanya mengapa kami tidak melakukan pergeseran data dan menyatukan kedua piksel tersebut ke dalam satu byte? Jawabannya sederhana: untuk menjaga kinerja tinggi. Semua pemrosesan internal biasanya dilakukan dengan semua data dimulai dari piksel pertama dan berakhir dengan piksel terakhir yang tersedia. Jarang ada situasi di mana subset piksel diperlukan. Selain itu, kita tidak tahu bagaimana piksel-piksel tersebut akan diproses setelahnya, sehingga pergeseran akan menurunkan kinerja dan membuat kode menjadi tidak perlu kompleks. Selalu perkirakan bit yang tepat (tidak perlu menentukan byte yang tepat karena data selalu datang dengan byte pertama terisi) di mana piksel yang diminta akan dimulai. Untuk menghitung bit yang tepat, dapat digunakan formula sederhana: (rect.Kiri * jumlah bit) % 8.
### **Konversi Warna RGB Indeks**
Untuk mendapatkan kinerja tertinggi mungkin, selalu gunakan pengaturan data mentah, format piksel, dan ukuran baris sumber dan tujuan yang sama. Namun, terkadang Anda mungkin perlu melakukan konversi data. Misalnya, Anda mungkin memuat gambar RGB 1 bit per pixel dan menyimpannya dengan 2 bit per pixel, atau memuat gambar RGB 4 bit dan mengurangi rentang warna menjadi 2 bit per pixel. Dalam kedua kasus ini, konversi warna harus diterapkan. Mengonversi gambar RGB indeks kadang-kadang bisa sulit dan tidak dapat dilakukan tanpa beberapa pengaturan yang diterapkan. Kita perlu menentukan bagaimana rentang warna sumber dipetakan ke ruang warna target. Untuk menyelesaikan tugas ini, kita memiliki  [mode](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods) berbeda:

- Pemetaan palet (DitheringMethods.PaletteConversion)
- Pemetaan data mentah (DitheringMethods.PaletteIgnore)
- Konversi kustom (DitheringMethods.CustomConverter)

Saat pemetaan palet digunakan, ruang warna sumber berusaha mencocokkan ruang warna target seserupa mungkin. Sebagai contoh, mari kita asumsikan kita memiliki gambar 4 bit dengan warna berikut:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

Gambar sumber terlihat sebagai berikut:



![todo:image_alt_text](raw-data-processing_2.png)

Dan kita mengonversi gambar 4 bit menjadi gambar 1 bit dengan palet warna berikut ditentukan:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Dalam mode konversi palet, konverter membaca warna sumber dan menentukan indeks target menggunakan metode [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) dari palet target. Nilai properti [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) digunakan jika metode GetNearestColorIndex dari palet memberikan indeks di luar jangkauan. Ini mengonversi warna sumber ke warna target terdekat dalam hal nilai intensitas. Gambar target cocok dengan gambar sumber sesedekat mungkin. Anda dapat melihat hasil berikut:


![todo:image_alt_text](raw-data-processing_3.png)

Dalam mode pemetaan data mentah, digunakan skenario yang berbeda. Palet warna sumber dan target hanya diabaikan dan indeks sumber dipetakan ke indeks tujuan. Ketika ditemukan nilai yang tidak dapat dipetakan ke dalam rentang tujuan (ketika mengubah jumlah bit), maka nilai properti [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) digunakan. Nilai ini secara default adalah 0 dan akan dipetakan ke warna pertama dalam palet tujuan. Jika nilai properti ini berada di luar rentang tujuan, maka pengecualian yang sesuai akan dilemparkan. Hal ini mengarah pada hasil yang kurang dapat diprediksi yang dapat ditunjukkan pada gambar berikut:


![todo:image_alt_text](raw-data-processing_4.png)

Mode konversi palet adalah solusi yang lebih tepat untuk masalah pemetaan warna tetapi juga membutuhkan sedikit lebih banyak waktu untuk menyelesaikan karena perhitungan yang perlu dilakukan untuk memperkirakan pemetaan palet yang benar. (Secara umum ada perbedaan kinerja yang sangat kecil antara kedua metode ini.) Di sisi lain, mode pemetaan data mentah bekerja sedikit lebih cepat dan dapat digunakan untuk konversi warna kasar ketika pemetaan warna yang tepat tidak terlalu penting. Misalnya, ada kasus di mana palet warna sumber dipangkas dan dapat dengan aman dikonversi ke jumlah bit lebih sedikit karena bit ekstra belum digunakan sama sekali.

Untuk menggunakan salah satu pendekatan ini, gunakan properti RawDitheringMethod kelas RasterImage. Secara default, properti ini diatur ke metode konversi palet untuk mencapai hasil yang terlihat terbaik. Anda dapat mengubah properti ini sebelum konversi dilakukan (misalnya saat menyimpan gambar ke stream). Perhatikan bahwa metode dithering pemetaan palet dan konversi palet tidak akan berlaku jika Anda telah memuat gambar dan menulis kembali sebagian data piksel asli karena data baru masuk ke cache dan cache menyimpan data dalam format maksimal yang tersedia 32ARGB (sebagaimana pada versi 2.4.0, bisa berubah). Format ini digunakan untuk mengatasi masalah dengan rentang warna yang mungkin berbeda untuk gambar yang dimuat dan disimpan. Selain itu metode dithering pemetaan palet dan konversi palet akan diabaikan ketika gambar dimuat dalam mode RGB dan dikonversi ke mode indeks atau sebaliknya.
### **Konverter Warna Kustom**
Kadang-kadang tidak cukup hanya menggunakan pendekatan standar untuk konversi warna. Anda mungkin ingin menggunakan algoritma kustom untuk mendapatkan kebebasan penuh saat menggunakan rutinitas konversi warna. Ketika format piksel gambar sumber dan target keduanya adalah format RGB indeks, sebuah antarmuka yang lebih sederhana, [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter), dapat digunakan. Anda perlu mengatur properti [RasterImage.RawIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawindexedcolorconverter) ke suatu contoh antarmuka IIndexedColorConverter dan menggunakan [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter untuk nilai properti RawDitheringMethod. Ketika kombinasi ini diimkan, maka konversi warna indeks akan melalui instance IIndexedColorConverter yang ditentukan. Konverter warna indeks kustom memiliki metode berikut didefinisikan:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}


Metode FillIndexedtoIndexedMap dipanggil saat konversi diperlukan dari gambar RGB indeks ke format gambar RGB indeks (ketika salah satu dari 1,2,4 atau 8 hitung bit dikonversi satu sama lain). Array peta memiliki panjang seluruh entri format sumber yang mungkin. Anda perlu mengisi array tersebut untuk memetakan dari entri palet warna sumber ke entri palet warna tujuan. Selalu perhatikan bahwa nilai indeks tujuan berada dalam rentang 0..(jumlah bit - 1), atau pengecualian yang sesuai akan dilemparkan.

Jika kebutuhan adalah untuk melakukan skenario konversi warna yang lebih kustom, maka properti [RasterImage.RawCustomColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawcustomcolorconverter) harus diatur ke suatu contoh antarmuka [IColorConverter](https://reference.aspose.com/psd/net/aspose.psd/icolorconverter). Properti RawCustomColorConverter akan selalu mengesampingkan properti RawIndexedColorConverter jika keduanya diatur dan konverter warna indeks tidak akan digunakan dalam kasus tersebut. IColorConverter memiliki satu metode:



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}


Metode Convert dipanggil setiap kali konversi warna diperlukan. Metode menerima data mentah sumber dalam format sumber dan memiliki buffer output untuk menerima format warna yang diubah ke tujuan. Buffer tujuan harus mencukupi untuk menerima data yang diubah (jika panggilan antarmuka dilakukan secara internal oleh perpustakaan Aspose.PSD) dan harus berisi data mentah yang diubah saat metode ini selesai. Metode Convert dapat dipanggil beberapa kali sampai seluruh data sumber tercakup.

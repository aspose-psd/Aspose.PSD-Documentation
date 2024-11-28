---
title: Pengolahan Data Mentah
type: docs
weight: 70
url: /id/java/pengolahan-data-mentah/
---

## **Pengolahan Data Mentah**
Untuk meningkatkan kinerja API Aspose.PSD, kami memperkenalkan metode pengolahan data mentah dengan versi 2.4.0. Pengolahan data mentah saat ini digunakan secara internal dan memiliki API eksternal sehingga dapat digunakan dari luar perpustakaan untuk meningkatkan kinerja keseluruhan. Kadang-kadang pengolahan ini sedikit rumit dan membutuhkan penjelasan. Pengolahan data mentah saat ini hanya tersedia untuk format BMP.

Untuk membantu para pengembang mendapatkan kinerja terbaik, API Aspose.PSD menyediakan sistem pengolahan data mentah yang memiliki API eksternal untuk disesuaikan. Pengembang memanggil keluarga metode LoadRawData dan SaveRawData untuk menggunakan pengolahan data mentah. Metode ini juga memerlukan format data mentah yang diinginkan yang diatur menggunakan kelas RawDataSettings. Kelas RawDataSettings memungkinkan pengembang untuk menentukan format data mentah apa pun. Namun, untuk mencapai kinerja terbaik, Anda perlu menggunakan format data mentah tempat data disimpan. RawDataSettings yang didefinisikan dalam kelas RasterImage membantu menentukan format data mentah gambar. Ketika meneruskan instance RawDataSettings ke dalam metode LoadRawData, data dikembalikan seperti apa adanya, tanpa konversi yang diterapkan, dan dapat meningkatkan kinerja. Di sisi lain, Anda perlu memperhatikan semua layout format data mentah yang mungkin terkadang agak rumit.

Untuk menyederhanakan proses penanganan, dengan biaya sedikit penalti kinerja, Anda dapat menentukan RawDataSettings yang diinginkan dengan menginisialisasi kelas dengan pengaturan data mentah yang diinginkan. Ada kasus di mana tidak mungkin mengembalikan data mentah dalam format yang ditentukan (misalnya konversi dari ruang warna CMYK ke RGB tidak tersedia dalam versi 2.4.0). Selain itu, mungkin ada skenario di mana pengolahan data mentah sama sekali tidak tersedia untuk format gambar tertentu. Untuk menentukan apakah Anda dapat menggunakan keluarga metode LoadRawData dan SaveRawData, Anda perlu memeriksa properti IsRawDataAvailable.
### **Wawasan**
Untuk format data piksel RGB ada format data mentah berbasis indeks (palet) dan RGB tersedia. Format data mentah berbasis indeks berisi indeks entri palet dalam rentang 0..(2^bits count - 1). Format data mentah berbasis indeks adalah 1, 2, 4, dan 8 bit per piksel. Yang lainnya adalah format data mentah berbasis RGB. Saat memuat data mentah, pastikan bahwa ada cukup byte yang tersedia untuk memuat data, jika tidak, pengecualian yang sesuai akan dilemparkan. Anda dapat mengestimasi ukuran array byte dengan mengalikan ukuran baris dengan jumlah baris yang diperlukan. Ukuran baris dapat bervariasi dan tergantung pada format penyimpanan data mentah.

Untuk mencapai kinerja terbaik, selalu gunakan ukuran baris data mentah yang sama dengan nilai properti RasterImage.RawLineSize. Namun, terkadang Anda mungkin perlu menambahkan padding tambahan ke baris data mentah, atau menguranginya, dan dalam hal ini ukuran baris yang berbeda dapat digunakan. Jika diperlukan subset persegi panjang gambar, maka pertimbangkan pergeseran bit yang mungkin terjadi untuk format piksel RGB yang diindeks. Sebagai contoh, pertimbangkan gambar dengan dimensi 100x100 piksel dan format data mentah 1 bit per piksel. Anda ingin memuat persegi panjang data mentah dengan lokasi (7,0) dan dimensi (2,1), atau dengan kata lain, Anda memerlukan 2 piksel mulai dari x=7 dan y=0. Dalam kasus ini, Anda akan menerima tata letak data berikut:




![todo:image_alt_text](raw-data-processing_1.png)

Ini berarti Anda menerima 2 byte di mana byte pertama berisi 7 piksel yang tidak diinginkan, kemudian 1 piksel yang diinginkan, dan byte kedua berisi 1 piksel yang diinginkan dan kemudian 7 yang tidak diinginkan. Anda mungkin bertanya mengapa kami tidak melakukan pergeseran data dan meletakkan kedua piksel itu ke dalam satu byte? Jawabannya sederhana: untuk menjaga kinerja tetap tinggi. Semua pemrosesan internal biasanya dilakukan dengan semua data dimulai dari piksel pertama dan berakhir dengan piksel terakhir yang tersedia. Ada situasi langka di mana subset piksel diperlukan. Selain itu, kami tidak tahu bagaimana piksel-piksel itu akan diproses setelahnya sehingga pergeseran akan menurunkan kinerja dan membuat kode menjadi tidak perlu rumit. Selalu perkirakan bit yang tepat (tidak perlu menentukan byte yang tepat karena data selalu datang dengan byte pertama terisi) di mana piksel yang diminta akan dimulai. Untuk menghitung bit yang tepat, bisa digunakan rumus sederhana: (rect.Left * bitsCount) % 8.

### **Konversi Warna RGB Berindeks**
Untuk mendapatkan kinerja tertinggi, selalu gunakan pengaturan data sumber dan tujuan yang sama, format piksel, dan ukuran baris. Namun, terkadang Anda mungkin perlu melakukan konversi data. Sebagai contoh, Anda dapat memuat gambar RGB 1 bit per piksel dan menyimpannya dengan 2 bit per piksel, atau memuat gambar RGB 4 bit dan menurunkan rentang warnanya menjadi 2 bit per piksel. Dalam kedua kasus tersebut, konversi warna harus diterapkan. Mengonversi gambar RGB berindeks terkadang membingungkan dan tidak bisa dilakukan tanpa beberapa pengaturan yang diterapkan. Kami perlu menentukan bagaimana rentang warna sumber dipetakan ke ruang warna tujuan. Untuk mencapai tugas ini, kami memiliki mode yang berbeda:

- Pemetaan palet (DitheringMethods.PaletteConversion)
- Pemetaan data mentah (DitheringMethods.PaletteIgnore)
- Konversi kustom (DitheringMethods.CustomConverter)

Ketika konversi palet digunakan, ruang warna sumber berupaya untuk sesuai dengan ruang warna tujuan sebaik mungkin. Misalnya, mari kita asumsikan kita memiliki gambar 4 bit dengan warna berikut:
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

Gambar sumber terlihat seperti di bawah ini:




![todo:image_alt_text](raw-data-processing_2.png)

Dan kita mengonversi gambar 4 bit menjadi gambar 1 bit dengan palet warna berikut:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Pada mode konversi palet, konverter membaca warna sumber dan menentukan indeks tujuan menggunakan metode GetNearestColorIndex palet tujuan. Nilai properti RasterImage.RawFallbackIndex digunakan jika metode GetNearestColorIndex palet memberikan indeks di luar jangkauan. Ini mengonversi warna sumber ke warna tujuan yang paling mendekati. Gambar tujuan cocok dengan gambar sumber sesempurna mungkin. Anda dapat melihat hasil berikut:




![todo:image_alt_text](raw-data-processing_3.png)

Pada mode pemetaan data mentah, digunakan skenario yang berbeda. Palet warna sumber dan tujuan sederhana dihiraukan dan indeks sumber dipetakan ke indeks tujuan. Ketika nilai ditemukan yang tidak dapat dipetakan ke dalam rentang tujuan (saat mengurangi jumlah bit), maka nilai properti RasterImage.RawFallbackIndex digunakan. Nilai tersebut secara default adalah 0 dan akan dipetakan ke warna pertama dalam palet tujuan. Jika nilai properti ini berada di luar rentang tujuan, pengecualian yang sesuai akan dilemparkan. Hal ini mengarah pada hasil yang kurang dapat diprediksi yang dapat ditunjukkan pada gambar berikut:




![todo:image_alt_text](raw-data-processing_4.png)

Mode konversi palet adalah solusi yang lebih benar untuk masalah pemetaan warna tetapi juga membutuhkan sedikit lebih banyak waktu untuk menyelesaikan karena perhitungan harus dilakukan untuk memperkiraan pemetaan palet yang benar. (Umumnya ada perbedaan kinerja yang sangat kecil antara kedua metode ini.) Di sisi lain, mode pemetaan data mentah dapat berjalan sedikit lebih cepat dan dapat digunakan untuk konversi warna yang lebih kasar ketika pemetaan warna yang tepat tidak terlalu penting. Misalnya, ada kasus di mana palet warna sumber dipangkas dan dapat dengan aman dikonversi ke jumlah bit yang lebih sedikit karena bit tambahan tidak digunakan sama sekali.

Untuk menggunakan salah satu pendekatan ini, gunakan properti RasterImage RawDitheringMethod. Secara default, properti ini diatur ke metode konversi palet untuk mencapai hasil terlihat terbaik. Anda dapat mengubah properti ini sebelum konversi dilakukan (misalnya saat menyimpan gambar ke aliran). Harap dicatat bahwa metode dithering pembuangan palet dan konversi palet tidak akan berlaku jika Anda telah memuat gambar dan menulis kembali sebagian data piksel asli karena data baru masuk ke cache dan cache menyimpan data dalam format maksimal yang tersedia 32ARGB (sejak versi 2.4.0, dapat berubah). Format ini digunakan untuk mengatasi masalah dengan rentang warna yang mungkin berbeda untuk gambar yang dimuat dan disimpan. Selain itu, metode dithering pembuangan palet dan konversi palet tidak akan diberlakukan saat gambar dimuat dalam mode RGB dan diubah ke mode indeks atau sebaliknya.
### **Konverter Warna Kustom**
Terkadang tidak cukup menggunakan pendekatan standar untuk konversi warna. Anda mungkin ingin menggunakan algoritma kustom untuk mendapatkan kebebasan sepenuhnya saat menggunakan rutinitas konversi warna. Ketika format piksel gambar sumber dan tujuan keduanya adalah format RGB berindeks, antarmuka yang lebih sederhana, IIndexedColorConverter, mungkin digunakan. Anda perlu mengatur properti RasterImage RawIndexedColorConverter ke sebuah instance yang implementasi dari antarmuka IIndexedColorConverter dan menggunakan DitheringMethods.CustomConverter untuk nilai properti RawDitheringMethod. Ketika kombinasi ini diimplikasikan, maka setiap konversi warna indeks akan melalui instance IIndexedColorConverter yang ditetapkan. Antarmuka konverter warna indeks kustom memiliki metode berikut yang didefinisikan:




{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



Metode FillIndexedtoIndexedMap dipanggil saat konversi diperlukan dari gambar RGB berindeks ke format gambar RGB berindeks (ketika salah satu dari 1,2,4 atau 8 bit diubah menjadi satu sama lain). Array peta memiliki panjang semua kemungkinan entri format sumber. Anda perlu mengisi array tersebut untuk pemetaan dari entri palet warna sumber ke entri palet warna tujuan. Pastikan bahwa nilai indeks tujuan berada dalam rentang 0..(bits count - 1), atau pengecualian yang sesuai akan dilemparkan.

Jika kebutuhan adalah untuk melakukan skenario konversi warna yang lebih kustom, maka properti RasterImage RawCustomColorConverter harus diatur ke sebuah instance yang implementasi dari antarmuka IColorConverter. Properti RawCustomColorConverter selalu mengesampingkan properti RawIndexedColorConverter jika keduanya diatur dan konverter warna indeks tidak akan digunakan dalam kasus seperti itu. IColorConverter memiliki satu metode:




{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}



Metode Convert dipanggil setiap kali konversi warna diperlukan. Metode menerima data mentah sumber dalam format sumber dan memiliki buffer keluaran untuk menerima format warna yang dikonversi ke tujuan. Buffer tujuan harus mencukupi untuk menerima data yang dikonversi (jika panggilan antarmuka dilakukan secara internal oleh perpustakaan Aspose.PSD) dan harus berisi data mentah yang dikonversi saat metode tersebut mengembalikan. Metode Convert dapat dipanggil beberapa kali hingga seluruh data sumber tercakup.
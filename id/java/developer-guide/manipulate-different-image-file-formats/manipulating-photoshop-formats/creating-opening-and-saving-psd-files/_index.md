---
title: Membuat, Membuka, dan Menyimpan Berkas PSD
type: docs
weight: 10
url: /id/membuat-membuka-dan-menyimpan-berkas-psd/
---

## **Mengekspor Gambar ke PSD**
PSD, dokumen PhotoShop, adalah format berkas default yang digunakan oleh Adobe PhotoShop untuk bekerja dengan gambar. Aspose.PSD memungkinkan Anda untuk memuat, mengedit, dan menyimpan berkas ke PSD sehingga dapat dibuka dan diedit di PhotoShop. Artikel ini menunjukkan cara menyimpan berkas ke PSD dengan Aspose.PSD, dan juga membahas beberapa pengaturan yang dapat digunakan saat menyimpan ke format ini. PsdOptions adalah kelas khusus di namespace ImageOptions yang digunakan untuk mengekspor gambar ke PSD. Untuk mengekspor ke PSD, buat sebuah instansi dari kelas Image, baik dimuat dari berkas gambar yang ada (misalnya miniatur) atau dibuat dari awal. Artikel ini menjelaskan cara melakukannya. Pada contoh di bawah ini, sebuah gambar dibuat dari awal. Setelah itu dibuat dan data pikselnya diisi, simpan gambar menggunakan metode Save dari kelas Image, dan sediakan objek PsdOptions sebagai argumen kedua. Beberapa properti kelas PsdOptions dapat diatur untuk konversi yang lebih canggih. Beberapa propertinya adalah ColorMode, CompressionMethod, dan Version. Aspose.PSD mendukung beberapa metode kompresi berikut melalui enumerasi CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Mode warna berikut didukung melalui enumerasi ColorModes:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Sumber daya tambahan dapat ditambahkan, seperti sumber daya miniatur untuk PSD v4.0, v5.0 dan lebih tinggi, atau sumber daya grid dan panduan untuk PSD v4.0 dan lebih tinggi. Kode di bawah ini membuat berkas BMP dari awal, mengisi piksel, dan menyimpannya ke PSD dengan kompresi RLE dan mode warna grayskale. Potongan kode berikut ini menunjukkan bagaimana cara mengekspor Gambar ke PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Mengimpor gambar ke lapisan PSD**
Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk menambah atau mengimpor gambar ke lapisan PSD. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD telah mengekspos metode DrawImage dari kelas Layer untuk menambah/mengimpor gambar ke dalam berkas PSD. Metode DrawImage memerlukan lokasi dan nilai gambar untuk menambah/mengimpor gambar ke dalam berkas PSD. Langkah-langkah untuk mengimpor gambar ke lapisan PSD adalah sebagai berikut:

- Memuat berkas PSD sebagai gambar menggunakan metode pabrik Load yang diekspos oleh kelas Image.
- Buat sebuah instansi kelas Layer dan berikan lapisan gambar PSD kepadanya.
- Muat gambar yang perlu ditambahkan atau buat satu dari awal.
- Panggil metode Layer.DrawImage sambil menentukan lokasi dan instansi gambar.
- Simpan hasilnya.



Potongan kode berikut ini menunjukkan bagaimana cara mengimpor gambar ke lapisan PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Membuat Miniatur dari Berkas PSD**
PSD adalah format dokumen asli dari aplikasi Photoshop Adobe. Adobe Photoshop (versi 5.0 dan lebih tinggi) menyimpan informasi miniatur untuk tampilan pratinjau dalam blok sumber daya gambar yang terdiri dari header awal 28 byte, diikuti miniatur JFIF dalam urutan RGB (merah, hijau, biru). API Aspose.PSD menyediakan mekanisme yang mudah digunakan untuk mengakses sumber daya berkas PSD. Sumber daya ini juga termasuk sumber miniatur yang pada gilirannya dapat diambil dan disimpan ke disk sesuai kebutuhan aplikasi. Potongan kode berikut ini menunjukkan bagaimana cara membuat miniatur dari Berkas PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Membuat Berkas PSD Bereks Indeks**
Aspose.PSD untuk API Java dapat membuat berkas PSD Bereks Indeks dari awal. Artikel ini mendemonstrasikan penggunaan kelas PsdOptions dan PsdImage untuk membuat sebuah PSD Bereks Indeks sambil menggambar beberapa bentuk di atas kanvas yang baru dibuat. Langkah-langkah sederhana berikut diperlukan untuk membuat sebuah berkas PSD Bereks Indeks.

- Buat instansi PsdOptions dan tetapkan sumbernya.
- Tetapkan properti ColorMode dari PsdOptions ke ColorModes.Indexed.
- Buat palet baru warna dari ruang RGB dan tetapkan sebagai properti Palette dari PsdOptions.
- Tetapkan properti CompressionMethod ke algoritma kompresi yang dibutuhkan.
- Buat gambar PSD baru dengan memanggil metode PsdImage.Create.
- Gambar grafik atau lakukan operasi lain sesuai kebutuhan.
- Panggil metode PsdImage.Save untuk menerapkan semua perubahan.



Potongan kode berikut ini menunjukkan bagaimana cara membuat berkas PSD Bereks Indeks.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **Mengekspor Lapisan PSD ke Gambar Raster**
Aspose.PSD untuk Java memungkinkan Anda untuk mengekspor lapisan dalam berkas PSD ke dalam gambar raster. Harap gunakan metode Aspose.PSD.FileFormats.Psd.Layers.Layer.Save untuk mengekspor lapisan ke gambar. Potongan kode contoh berikut memuat berkas PSD dan mengekspor setiap lapisannya ke dalam gambar PNG menggunakan Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Setelah semua lapisan diekspor ke dalam gambar PNG, Anda dapat membukanya menggunakan penampil gambar favorit Anda. Potongan kode berikut ini menunjukkan bagaimana cara mengekspor lapisan PSD ke gambar raster.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}

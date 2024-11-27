---
title: Memanipulasi Format Adobe Photoshop
type: dokumen
weight: 20
url: /id/memanipulasi-format-adobe-photoshop/
---

## **Menggabungkan Layer PSD ke Layer Lain**

## **Mengekspor Gambar ke PSD**
PSD, dokumen PhotoShop, adalah format file default yang digunakan oleh Adobe Photoshop untuk bekerja dengan gambar. Aspose.PSD memungkinkan Anda untuk memuat, mengedit, dan menyimpan file ke dalam format PSD sehingga dapat dibuka dan diedit di Photoshop. Artikel ini menunjukkan cara menyimpan file ke PSD dengan Aspose.PSD, dan juga membahas beberapa pengaturan yang dapat digunakan saat menyimpan ke format ini. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) adalah kelas khusus dalam namespace [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) yang digunakan untuk mengekspor gambar ke PSD. Untuk mengekspor ke PSD, buat sebuah instansi dari kelas Image, baik dimuat dari file gambar yang ada (misalnya miniatur) atau dibuat dari awal. Artikel ini menjelaskan cara melakukannya. Dalam contoh di bawah ini, sebuah gambar dibuat dari awal. Setelah dibuat dan data piksel diisi, simpan gambar menggunakan metode Save dari kelas Image, dan berikan objek PsdOptions sebagai argumen kedua. Beberapa properti kelas PsdOptions dapat diatur untuk konversi tingkat lanjut. Beberapa properti tersebut adalah ModeWarna, [MetodeKompresi](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) dan Versi. Aspose.PSD mendukung metode kompresi berikut melalui enumerasi CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Mode warna berikut didukung melalui enumerasi [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


Sumber daya tambahan dapat ditambahkan, seperti sumber daya miniatur untuk PSD v4.0, v5.0 dan yang lebih tinggi, atau grid dan panduan sumber daya untuk PSD v4.0 dan yang lebih tinggi. Kode di bawah membuat file Image dari awal, mengisi pikselnya, dan menyimpannya ke dalam PSD dengan kompresi RLE dan mode warna grayscale. Potongan kode berikut menunjukkan bagaimana cara mengekspor Gambar ke PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **Mengimpor gambar ke lapisan PSD**
Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk menambahkan atau mengimpor gambar ke lapisan PSD. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD telah mengekspos metode [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) dari kelas Layer untuk menambahkan/mengimpor gambar ke dalam file PSD. Metode DrawImage membutuhkan nilai lokasi dan gambar untuk menambahkan/mengimpor gambar ke dalam file PSD. Langkah-langkah untuk mengimpor gambar ke lapisan PSD adalah sebagai berikut:

- Memuat file PSD sebagai gambar menggunakan metode factory Load yang diekspos oleh kelas Image.
- Membuat sebuah instansi kelas Layer dari aliran dengan file Png, Jpeg, Tiff, Gif, Bmp, Psd, atau j2k.
- Menambahkan Layer ke Psd menggunakan metode AddLayer
- Menyimpan hasil.


Potongan kode berikut menunjukkan cara mengimpor gambar ke lapisan PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Penggantian Warna dalam Lapisan PSD**
Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk menambahkan atau mengimpor gambar ke lapisan PSD. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD telah mengekspos metode DrawImage dari kelas Layer untuk menambahkan/mengimpor gambar ke dalam file PSD. Metode DrawImage membutuhkan nilai lokasi dan gambar untuk menambahkan/mengimpor gambar ke dalam file PSD. Langkah-langkah untuk mengimpor gambar ke lapisan PSD adalah sebagai berikut:

- Memuat file PSD sebagai gambar menggunakan metode factory Load yang diekspos oleh kelas Image.
- Membuat sebuah instansi kelas Layer dan mengaitkan lapisan gambar PSD ke dalamnya.
- Memuat gambar yang perlu ditambahkan atau membuatnya dari awal.
- Memanggil metode Layer.DrawImage sambil menentukan lokasi dan instansi gambar.
- Menyimpan hasil.


Potongan kode berikut menunjukkan cara mengimpor gambar ke lapisan PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}
## **Membuat Simpangan dari File PSD**
PSD adalah format dokumen asli aplikasi Adobe Photoshop. Adobe Photoshop (versi 5.0 dan seterusnya) menyimpan informasi miniatur untuk tampilan pratinjau dalam blok sumber daya gambar yang terdiri dari header 28 byte awal, diikuti oleh miniatur JFIF dalam urutan RGB (merah, hijau, biru). API Aspose.PSD menyediakan mekanisme yang mudah digunakan untuk mengakses sumber daya file PSD. Sumber daya ini juga termasuk sumber miniatur yang pada akhirnya dapat diambil dan disimpan ke disk sesuai kebutuhan aplikasi. Potongan kode berikut menunjukkan bagaimana cara membuat miniatur dari File PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}
## **Membuat File PSD Indeks**
Aspose.PSD untuk API .NET dapat membuat file PSD indeks dari awal. Artikel ini mendemonstrasikan penggunaan kelas PsdOptions dan [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) untuk membuat PSD Indeks sambil menggambar beberapa bentuk di atas kanvas yang baru dibuat. Langkah-langkah sederhana berikut diperlukan untuk membuat file PSD Indeks.

- Buat instansi PsdOptions dan atur sumbernya.
- Atur properti ColorMode dari PsdOptions ke ColorModes.Indexed.
- Buat palet warna baru dari ruang RGB dan aturnya sebagai properti Palet PsdOptions.
- Atur properti CompressionMethod ke algoritma kompresi yang dibutuhkan.
- Buat gambar PSD baru dengan memanggil metode PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- Gambar grafis atau lakukan operasi lain sesuai kebutuhan.
- Panggil metode PsdImage.Save untuk menyimpan semua perubahan.


Potongan kode berikut menunjukkan cara membuat file PSD indeks.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
## **Mengekspor Layer PSD ke Gambar Raster**
Aspose.PSD .NET memungkinkan Anda untuk mengekspor layer dalam file PSD ke dalam gambar raster. Silakan gunakan metode [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) untuk mengekspor lapisan ke gambar. Potongan kode berikut memuat file PSD dan mengekspor masing-masing layer ke gambar PNG menggunakan Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Setelah semua layer diekspor ke gambar PNG, Anda dapat membukanya menggunakan penampil gambar favorit Anda. Potongan kode berikut menunjukkan cara mengekspor lapisan PSD ke gambar raster.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}
## **Memperbarui Layer Teks dalam File PSD**
Aspose.PSD untuk .NET memungkinkan Anda untuk memanipulasi teks dalam layer teks dari file PSD. Gunakan kelas [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) untuk memperbarui teks dalam lapisan PSD. Potongan kode berikut memuat file PSD, mengakses layer teks, memperbarui teks, dan menyimpan file PSD dengan nama baru menggunakan metode [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **Mendeteksi Flattened PSD**
Aspose.PSD untuk .NET memungkinkan Anda untuk mendeteksi apakah file PSD yang diberikan sudah tersusun rapi atau tidak. Properti IsFlatten telah diperkenalkan dalam kelas Aspose.PSD.FileFormats.Psd.PsdImage untuk mencapai fungsi ini. Potongan kode berikut memuat file PSD dan mengakses properti [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}
## **Menggabungkan Layer PSD**
Artikel ini menunjukkan bagaimana cara menggabungkan layer dalam file PSD saat mengonversi file PSD ke JPG dengan Aspose.PSD. Dalam contoh di bawah ini, file PSD yang ada dimuat dengan melewatkan jalur file ke metode statis Load dari kelas Image. Begitu dimuat, konversi/cetak gambar ke PsdImage. Buat instansi dari kelas JpegOptions dan atur berbagai propertinya. Sekarang panggil metode Save dari instansi PsdImage. Potongan kode berikut menunjukkan cara menggabungkan layer PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergePSDlayers-MergePSDlayers.cs" >}}
## **Dukungan Grayscale Dengan Alfa untuk PSD**
Artikel ini menunjukkan bagaimana mendukung Grayscale dengan alfa untuk file PSD saat mengonversi file PSD ke PNG dengan Aspose.PSD. Dalam contoh di bawah ini, file PSD yang ada dimuat dengan melewatkan jalur file ke metode statis Load dari kelas Image. Setelah itu dimuat, konversi/cetak gambar ke PsdImage. Buat sebuah instansi dari kelas PngOptions dan atur berbagai propertinya. Atur properti [TipeWarna](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) ke TruecolorWithAlpha. Sekarang panggil metode Save dari instansi PngOptions. Potongan kode berikut menunjukkan cara mengonversi menjadi PNG Grayscale dengan Alfa.


{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GrayscaleSupportForAlpha-GrayscaleSupportForAlpha.cs" >}}
## **Dukungan Efek Layer Untuk PSD**
Artikel ini menunjukkan cara mendukung berbagai efek seperti **Blur**, **Inner** **Glow**, dan **Outer Glow** untuk layer PSD. Potongan kode berikut menunjukkan bagaimana mendukung efek layer.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.cs" >}}
## **Dukungan Tanggal dan Waktu Pembuatan Layer**
Artikel ini menunjukkan cara mendukung pembuatan layer tanggal dan waktu untuk layer PSD. Potongan kode berikut menunjukkan bagaimana membuat layer.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LayerCreationDateTime-LayerCreationDateTime.cs" >}}
## **Dukungan Highlight Warna Sheet**
Artikel ini menunjukkan cara memuat gambar PSD lalu mengubah dan menyorot warna lembar serta menyimpannya sebagai gambar. Potongan kode telah disediakan.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SheetColorHighlighting-SheetColorHighlighting.cs" >}}
## **Dukungan Masker Layer**
Artikel ini menunjukkan bagaimana mendukung layer mask untuk gambar PSD lalu menyimpan gambar tersebut. Potongan kode telah disediakan di bawah.

{{< gist "aspose-com-gists" "8a7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLayerMask-SupportOfLayerMask.cs" >}}
## **Dukungan Masker Vektor Layer**
Artikel ini menunjukkan Dukungan masker vektor layer untuk Aspose.PSD. Potongan kode di bawah ini menunjukkan bagaimana Aspose.PSD mendukung masker vektor layer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLayerVectorMask-SupportOfLayerVectorMask.cs" >}}
## **Dukungan Layer Teks saat Runtime**
Artikel ini menunjukkan cara menambahkan layer teks saat runtime untuk gambar PSD. Potongan kode telah disediakan di bawah.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
## **Dukungan Layer Penyesuaian**
Artikel ini menunjukkan cara menyesuaikan layer dan jika layer kosong, kemudian menggabungkan layer dan menyimpannya sebagai gambar PSD. Potongan kode telah disediakan di bawah.

{{< gist "aspose-psd" "c68d1f8aa6f2af15b98e4d34e14a504a" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfAdjusmentLayers-SupportOfAdjusmentLayers.cs" >}}
## **Mengelola Kecerahan dan Kontras dalam Layer Penyesuaian**
Artikel ini menunjukkan bagaimana merubah layer dan mengatur kecerahan serta kontras dalam layer lalu menyimpannya sebagai gambar PSD. Potongan kode telah disediakan di bawah.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ManageBrightnessContrastAdjustmentLayer-ManageBrightnessContrastAdjustmentLayer.cs" >}}
## **Mengelola Layer Paparan**
Artikel ini menunjukkan bagaimana menambahkan dan mengedit layer paparan lalu mengelola layer paparan lalu menyimpannya sebagai gambar PSD. Potongan kode telah disediakan
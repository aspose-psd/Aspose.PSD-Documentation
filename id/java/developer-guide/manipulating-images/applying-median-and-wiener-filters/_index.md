---
title: Menerapkan Filter Median dan Wiener
type: docs
weight: 10
url: /id/java/menerapkan-filter-median-dan-wiener/
---

## **Menerapkan Filter Median dan Wiener**
Filter median adalah teknik penyaringan digital nonlinier, sering digunakan untuk menghilangkan noise. Pengurangan noise seperti ini adalah langkah pra-pemrosesan khas untuk meningkatkan hasil pemrosesan selanjutnya. Filter Wiener adalah filter linier stasioner optimal MSE (mean squared error) untuk gambar yang terdegradasi oleh noise tambahan dan kabur. Dengan menggunakan Aspose.PSD untuk para pengembang API Java, kita dapat menerapkan filter median untuk membersihkan noise pada gambar dan dapat menerapkan filter Gauss Wiener pada gambar-gambar. Artikel ini mendemonstrasikan bagaimana filter median dan filter Gauss Wiener dapat diterapkan pada gambar.
### **Menerapkan Filter Median**
Aspose.PSD menyediakan kelas MedianFilterOptions untuk menerapkan filter pada RasterImage. Potongan kode di bawah ini mendemonstrasikan cara menerapkan filter median pada gambar raster.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Menerapkan Filter Gauss Wiener**
Aspose.PSD menyediakan kelas GaussWienerFilterOptions untuk menerapkan filter pada RasterImage. Potongan kode di bawah ini mendemonstrasikan cara menerapkan filter Gauss Wiener pada gambar raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Menerapkan Filter Gauss Wiener Untuk Gambar Berwarna**
Aspose.PSD menyediakan GaussWienerFilterOptions untuk gambar berwarna juga. Potongan kode di bawah ini mendemonstrasikan cara menerapkan filter Gauss Wiener pada gambar berwarna.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Menerapkan Filter Wiener Gerak**
Aspose.PSD menyediakan kelas MotionWienerFilterOptions untuk menerapkan filter pada RasterImage. Potongan kode di bawah ini mendemonstrasikan cara menerapkan filter Wiener gerak pada gambar raster.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Menerapkan Filter Koreksi Pada Sebuah Gambar**
Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk Java untuk melakukan filter koreksi pada sebuah gambar. API Aspose.PSD telah mengekspos metode-metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD untuk Java telah mengekspos kelas BilateralSmoothingFilterOptions dan SharpenFilterOptions untuk filtrasi. Kelas BilateralSmoothingFilterOptions membutuhkan tipe data integer sebagai ukuran. Langkah-langkah untuk melakukan Resize adalah sebagai berikut:


1. Muat gambar menggunakan metode pabrik Load yang diekspos oleh kelas Image.
1. Konversi gambar menjadi RasterImage.
1. Buat instance dari kelas BilateralSmoothingFilterOptions dan SharpenFilterOptions.
1. Panggil metode RasterImage.Filter sambil menentukan persegi panjang sebagai batas gambar dan instance kelas BilateralSmoothingFilterOptions.
1. Panggil metode RasterImage.Filter sambil menentukan persegi panjang sebagai batas gambar dan instance kelas SharpenFilterOptions.
1. Sesuaikan kontras
1. Atur kecerahan
1. Simpan hasil.

Potongan kode berikut menunjukkan bagaimana menerapkan filter koreksi.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Menggunakan algoritma ambang Bradley threshold**
Pemambangan gambar digunakan dalam aplikasi grafis. Tujuan dari pemambangan gambar adalah mengklasifikasikan piksel sebagai "gelap" atau "terang". API Aspose.PSD memungkinkan Anda menggunakan ambang Bradley saat mengonversi gambar. Potongan kode berikut menunjukkan cara mendefinisikan nilai ambang dan kemudian memanggil algoritma ambang Bradley.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}

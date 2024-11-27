---
title: Mengaplikasikan Filter Median dan Wiener
type: docs
weight: 10
url: /id/menerapkan-filter-median-dan-wiener/
---

## **Menerapkan Filter Median dan Wiener**
Filter median adalah teknik penyaringan digital nonlinier, sering digunakan untuk menghilangkan noise. Pengurangan noise seperti ini adalah langkah pra-pemrosesan khas untuk meningkatkan hasil pemrosesan selanjutnya. Filter Wiener adalah filter linier optimal MSE (mean squared error) stasioner untuk gambar yang terdegradasi oleh noise tambahan dan kabur. Dengan menggunakan Aspose.PSD untuk pengembang API .NET, kita dapat menerapkan filter median untuk mengurangi noise pada gambar dan dapat menerapkan filter gauss wiener pada gambar. Artikel ini menjelaskan bagaimana filter median dan filter gauss wiener dapat diterapkan pada gambar.

### **Menerapkan Filter Median**
Aspose.PSD menyediakan kelas [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) untuk menerapkan filter pada [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Potongan kode di bawah ini menunjukkan bagaimana cara menerapkan filter median pada gambar raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Menerapkan Filter Gauss Wiener**
Aspose.PSD menyediakan kelas [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) untuk menerapkan filter pada [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Potongan kode di bawah ini menunjukkan bagaimana cara menerapkan filter gauss wiener pada gambar raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Menerapkan Filter Gauss Wiener untuk Gambar Berwarna**
Aspose.PSD menyediakan [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) untuk gambar berwarna juga. Potongan kode di bawah ini menunjukkan bagaimana cara menerapkan filter gauss wiener pada gambar berwarna.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Menerapkan Filter Motion Wiener**
Aspose.PSD menyediakan kelas [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) untuk menerapkan filter pada [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Potongan kode di bawah ini menunjukkan bagaimana cara menerapkan filter motion wiener pada gambar raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Menerapkan Filter Koreksi pada Gambar**
Artikel ini menjelaskan penggunaan Aspose.PSD untuk .NET untuk melakukan filter koreksi pada gambar. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD untuk .NET telah mengekspos kelas [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) dan [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) untuk filtrasi. Kelas BilateralSmoothingFilterOptions memerlukan bilangan bulat sebagai ukuran. Langkah-langkah untuk melakukan Resize adalah sebagai berikut:

1. Memuat gambar menggunakan metode pabrik Load yang ditampilkan oleh kelas Image.
1. Mengonversi gambar menjadi RasterImage.
1. Membuat sebuah instance kelas BilateralSmoothingFilterOptions dan SharpenFilterOptions.
1. Memanggil metode [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) sambil menentukan persegi panjang sebagai batas gambar dan instansi kelas BilateralSmoothingFilterOptions.
1. Memanggil metode [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) sambil menentukan persegi panjang sebagai batas gambar dan instansi kelas SharpenFilterOptions.
1. Menyesuaikan kontras
1. Mengatur kecerahan
1. Menyimpan hasilnya.


## **Menggunakan Algoritma Ambang Bradley**
Pemberian ambang pada gambar digunakan dalam aplikasi grafis. Tujuan memberikan ambang pada gambar adalah untuk mengklasifikasikan piksel sebagai "gelap" atau "terang". API Aspose.PSD memungkinkan Anda menggunakan pemberian ambang Bradley saat mengonversi gambar. Potongan kode berikut menunjukkan bagaimana mendefinisikan nilai ambang dan kemudian memanggil algoritma ambang Bradley.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}

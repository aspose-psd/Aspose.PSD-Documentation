---
title: Memodifikasi Gambar
type: dokumen
weight: 50
url: /id/net/memodifikasi-gambar/
---

## **Dithering untuk Gambar Raster**
Dithering adalah sebuah teknik untuk menciptakan ilusi warna dan bayangan baru dengan memvariasikan pola titik yang sebenarnya menciptakan sebuah gambar. Ini adalah cara yang paling umum untuk mengurangi rentang warna gambar menjadi 256 (atau kurang) warna. Aspose.PSD menyediakan dukungan dithering untuk kelas [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) dengan memperkenalkan metode Dither yang menerima dua parameter. Pertama adalah tipe DitheringMethod yang akan diterapkan dengan dua opsi yang mungkin yaitu FloydSteinbergDithering dan ThresholdDithering. Parameter kedua untuk metode [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) adalah BitCount dalam bentuk integer. BitCount mendefinisikan ukuran sampel untuk hasil dithering. Nilai default adalah 1 yang mewakili hitam dan putih, sedangkan nilai yang diperbolehkan adalah 1, 4, 8 menghasilkan palet dengan 2, 4, dan 256 warna secara berturut-turut.

## **Mengatur Kecerahan, Kontras, dan Gamma**
Penyesuaian warna pada gambar digital adalah salah satu fitur inti yang banyak disediakan oleh perpustakaan pemrosesan gambar. Penyesuaian warna dapat dikategorikan sebagai berikut.

1. Kecerahan mengacu pada tingkat kecerahan atau kegelapan warna. Meningkatkan kecerahan gambar akan mencerahkan semua warna sedangkan mengurangi kecerahan akan menggelapkan semua warna.
1. Kontras mengacu pada membuat objek atau detail dalam gambar lebih jelas. Meningkatkan kontras gambar akan meningkatkan perbedaan antara area terang dan gelap sehingga area terang menjadi lebih terang dan area gelap menjadi lebih gelap. Mengurangi kontras akan membuat area terang dan gelap tetap kurang lebih sama namun gambar secara keseluruhan menjadi lebih homogen.
1. Gamma mengoptimalkan kontras dan kecerahan pencahayaan tidak langsung yang menerangi objek dalam gambar.
### **Mengatur Kecerahan**
Aspose.PSD untuk API .NET menyediakan metode [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) untuk kelas [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) yang dapat digunakan untuk mengatur kecerahan gambar dengan melewatkan nilai integer sebagai parameter. Nilai parameter tertinggi menandakan gambar yang lebih cerah. Berikut adalah gambar asli dan gambar hasilnya untuk perbandingan.

### **Mengatur Kontras**
Metode [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) yang terpapar oleh kelas [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) dapat digunakan untuk mengatur Kontras gambar dengan melewati nilai float sebagai parameter.

Nilai parameter tertinggi menunjukkan kontras yang lebih tinggi dalam gambar yang diberikan. Berikut adalah gambar asli dan gambar hasilnya untuk perbandingan.

### **Mengatur Gamma**
Metode [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) yang terpapar oleh kelas [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) memiliki dua versi. Salah satu berlebihan menerima satu nilai float dan melakukan koreksi Gamma untuk koefisien kanal merah, biru, dan hijau. Sedangkan parameter overlain menerima tiga parameter float mewakili masing-masing koefisien warna secara terpisah. Contoh kode berikut mendemonstrasikan cara Menyesuaikan Gamma pada gambar.

## **Memfokuskan Sebuah Gambar**
Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk .NET untuk memberikan efek Blur pada gambar. API Aspose.PSD memiliki metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD untuk .NET telah mengekspos kelas [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) untuk membuat efek blur secara langsung. Kelas [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) memerlukan nilai radius dan sigma untuk membuat efek blur pada gambar. Langkah-langkah untuk melakukan Resize adalah sebagai berikut:

1. Muat sebuah gambar menggunakan metode factory Load yang terpapar oleh kelas Image.
1. Konversi gambar menjadi [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Buat sebuah contoh kelas [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) dengan konstruktor default atau sediakan nilai radius dan sigma dalam konstruktor.
1. Panggil metode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter sambil menentukan persegi panjang sebagai batas gambar dan contoh kelas [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Simpan hasil.

Contoh kode berikut mendemonstrasikan cara membuat efek blur pada gambar.

## **Memverifikasi Ketransparanan Gambar**
Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk .NET untuk memeriksa ketransparanan gambar. Langkah-langkah untuk memeriksa ketransparanan gambar adalah sebagai berikut:

1. Muat sebuah gambar menggunakan metode factory [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) yang terpapar oleh kelas [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Periksa opasitas gambar jika opasitas adalah nol gambar itu transparan.
1. Contoh kode berikut mendemonstrasikan cara memeriksa apakah gambar transparan atau tidak.

## **Mengimplementasikan Kompresor GIF Yang Merugikan**
Dengan menggunakan Aspose.PSD untuk .NET, para pengembang dapat mengatur perbedaan piksel. Kompresi GIF didasarkan pada "kamus" dari string piksel yang terlihat. Pengekoder normal mencari kamus untuk string terpanjang dari piksel yang sama persis dengan piksel dalam gambar. Pengekoder merugikan memilih string terpanjang dari piksel yang "cukup mirip" dengan piksel dalam gambar. Berikut adalah demonstrasi kode dari fungsionalitas tersebut.

## **Mengimplementasikan Resampling Bicubic**
Resampling berarti Anda mengubah dimensi piksel dari sebuah gambar. Saat Anda mendownsampling, Anda menghilangkan piksel dan oleh karena itu menghapus informasi dan detail dari gambar Anda. Saat Anda upsampling, Anda menambahkan piksel. Photoshop menambahkan piksel ini dengan menggunakan interpolasi. Artikel ini mendemonstrasikan bagaimana Anda dapat melakukan Resampling Bicubic menggunakan Aspose.PSD untuk .NET.

Berikut adalah demonstrasi kode dari fungsionalitas tersebut.

## **Layer Penyesuaian Keseimbangan Warna**
Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk .NET untuk melakukan **layer penyesuaian keseimbangan warna** pada gambar. Layer penyesuaian keseimbangan warna memberi Anda kemampuan untuk melakukan penyesuaian pada pengecatan gambar mereka. Ini menyajikan tiga saluran warna dan warna komplementernya dan Anda dapat menyesuaikan keseimbangan dari pasangan-pasangan ini untuk mengubah penampilan sebuah foto.

Berikut adalah demonstrasi kode dari fungsionalitas tersebut.

## **Layer Penyesuaian Invert**
Artikel ini mendemonstrasikan bagaimana Anda dapat melakukan **layer penyesuaian Invert** dengan menggunakan Aspose.PSD untuk .NET. Layer penyesuaian adalah jenis layer khusus yang digunakan terutama untuk koreksi warna. Daripada memiliki konten mereka sendiri, mereka menyesuaikan informasi pada layer di bawahnya. Layer penyesuaian Invert membuat efek foto negatif dengan membalikkan warna gambar.

Berikut adalah demonstrasi kode dari fungsionalitas tersebut.

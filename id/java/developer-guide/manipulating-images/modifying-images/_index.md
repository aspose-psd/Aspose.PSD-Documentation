---
title: Memodifikasi Gambar
type: dokumen
weight: 50
url: /id/java/memodifikasi-gambar/
---

## **Dithering untuk Gambar Raster**
Dithering adalah teknik untuk menciptakan ilusi warna dan bayangan baru dengan memvariasikan pola titik yang sebenarnya membuat sebuah gambar. Ini adalah cara paling umum untuk mengurangi rentang warna gambar menjadi 256 (atau kurang) warna. Aspose.PSD menyediakan dukungan dithering untuk kelas RasterImage dengan mengenalkan metode Dither yang menerima dua parameter. Pertama adalah tipe DitheringMethod yang akan diterapkan dengan dua opsi yang mungkin, yaitu FloydSteinbergDithering dan ThresholdDithering. Parameter kedua untuk metode Dither adalah BitCount dalam bentuk integer. BitCount menentukan ukuran sampel untuk hasil dithering. Nilai defaultnya adalah 1 yang mewakili hitam dan putih, sedangkan nilai yang diperbolehkan adalah 1, 4, 8 yang menghasilkan palet dengan 2, 4, dan 256 warna secara berturut-turut.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.java" >}}
## **Mengatur Kecerahan, Kontras, dan Gamma**
Penyesuaian warna pada gambar digital adalah salah satu fitur inti yang banyak diberikan oleh perpustakaan pengolahan gambar. Penyesuaian warna dapat dikategorikan sebagai berikut.

1. Kecerahan mengacu pada kecerahan atau kegelapan warna. Meningkatkan kecerahan gambar akan menerangi semua warna sementara mengurangi kecerahan akan membuat warna menjadi lebih gelap.
1. Kontras mengacu pada membuat objek atau detail dalam gambar lebih jelas. Meningkatkan kontras gambar akan meningkatkan perbedaan antara area terang dan gelap sehingga area terang menjadi lebih terang dan area gelap menjadi lebih gelap. Menurunkan kontras akan membuat area terang dan gelap tetap hampir sama tetapi gambar secara keseluruhan menjadi lebih homogen.
1. Gamma mengoptimalkan kontras dan kecerahan pencahayaan tidak langsung yang menerangi suatu objek dalam gambar.
### **Mengatur Kecerahan**
Aspose.PSD untuk Java API menyediakan metode AdjustBrightness untuk kelas RasterImage yang dapat digunakan untuk menyesuaikan kecerahan gambar dengan melewati nilai integer sebagai parameter. Nilai parameter tertinggi menandakan gambar yang lebih cerah. Berikut adalah gambar asli dan gambar hasilnya untuk perbandingan.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.java" >}}
### **Mengatur Kontras**
Metode AdjustContrast yang terpapar oleh kelas RasterImage dapat digunakan untuk menyesuaikan Kontras gambar dengan melewati nilai float sebagai parameter.

Nilai parameter tertinggi menandakan kontras yang lebih tinggi dalam gambar yang diberikan. Berikut adalah gambar asli dan gambar hasilnya untuk perbandingan.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.java" >}}
### **Mengatur Gamma**
Metode AdjustGamma yang terpapar oleh kelas RasterImage memiliki dua versi. Salah satu overloading menerima satu nilai float dan melakukan koreksi Gamma untuk koefisien kanal merah, biru, dan hijau. Sementara overloading lain menerima tiga parameter float yang mewakili masing-masing koefisien warna secara terpisah. Contoh kode berikut mendemonstrasikan bagaimana Mengatur Gamma pada sebuah gambar.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.java" >}}
## **Berkabutkan Gambar**
Artikel ini menunjukkan penggunaan Aspose.PSD untuk Java untuk melakukan efek Blur pada sebuah gambar. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD untuk Java telah mengekspos kelas GaussianBlurFilterOptions untuk membuat efek blur secara langsung. Kelas GaussianBlurFilterOptions memerlukan nilai radius dan sigma untuk membuat efek blur pada sebuah gambar. Langkah-langkah untuk melakukan Resize sangat sederhana seperti di bawah ini:

1. Memuat gambar menggunakan metode pabrik Load yang terpapar oleh kelas Image.
1. Mengonversi gambar menjadi RasterImage.
1. Membuat sebuah instance dari kelas GaussianBlurFilterOptions dengan konstruktor default atau memberikan nilai radius dan sigma dalam konstruktor.
1. Memanggil metode RasterImage.Filter sambil menentukan persegi panjang sebagai batas gambar dan instance kelas GaussianBlurFilterOptions.
1. Menyimpan hasilnya.

Contoh kode berikut mendemonstrasikan bagaimana membuat efek blur pada sebuah gambar.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-BlurAnImage-BlurAnImage.java" >}}
## **Memverifikasi Transparansi Gambar**
Artikel ini menunjukkan penggunaan Aspose.PSD untuk Java untuk memeriksa transparansi gambar. Langkah-langkah untuk memeriksa transparansi gambar sangat sederhana seperti di bawah ini:

1. Memuat gambar menggunakan metode pabrik Load yang terpapar oleh kelas Image.
1. Memeriksa keopakan gambar jika opasitas adalah nol, gambar tersebut transparan.
1. Contoh kode berikut mendemonstrasikan bagaimana memeriksa apakah gambar transparan atau tidak.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.java" >}}
## **Menerapkan Kompresor GIF yang Bersifat Hilang**
Dengan menggunakan Aspose.PSD untuk Java, pengembang dapat mengatur perbedaan piksel. Kompresi GIF didasarkan pada "kamus" dari rangkaian string piksel yang dilihat. Pengenkoder normal mencari kamus untuk rangkaian string piksel terpanjang yang tepat cocok dengan piksel dalam gambar. Pengenkoder yang bersifat hilang memilih rangkaian string piksel terpanjang yang "cukup mirip" dengan piksel dalam gambar. Di bawah ini adalah demonstrasi kode dari fungsionalitas tersebut.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.java" >}}
## **Menerapkan Resampling Bicubic**
Resampling berarti Anda mengubah dimensi piksel sebuah gambar. Ketika Anda menyusutkan, Anda menghilangkan piksel dan oleh karena itu menghapus informasi dan detail dari gambar Anda. Saat Anda memperbesar, Anda menambahkan piksel. Photoshop menambahkan piksel ini dengan menggunakan interpolasi. Artikel ini mendemonstrasikan bagaimana Anda dapat melakukan Resampling Bicubic dengan menggunakan Aspose.PSD untuk Java.

Di bawah ini adalah demonstrasi kode dari fungsionalitas tersebut.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.java" >}}
## **Lapisan Penyesuaian Melawanin**
Artikel ini menunjukkan cara Anda dapat melaksanakan **lapisan penyesuaian melawanin** dengan menggunakan Aspose.PSD untuk Java. Sebuah lapisan penyesuaian adalah jenis lapisan khusus yang digunakan terutama untuk koreksi warna. Daripada memiliki konten mereka sendiri, mereka menyesuaikan informasi pada lapisan di bawahnya. Lapisan penyesuaian melawanin membuat efek gambar negatif dengan membalikkan warna dalam sebuah gambar.

Di bawah ini adalah demonstrasi kode dari fungsionalitas tersebut.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.java" >}}


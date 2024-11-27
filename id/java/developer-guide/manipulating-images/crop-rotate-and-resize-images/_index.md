---
title: Memangkas, Memutar, dan Mengubah Ukuran Gambar
type: docs
weight: 40
url: /id/java/memangkas-memutar-dan-mengubah-ukuran-gambar/
---

## **Memangkas Gambar**
Memangkas gambar biasanya merujuk pada penghapusan bagian luar gambar untuk membantu meningkatkan framing. Memangkas juga dapat digunakan untuk memotong sebagian dari gambar untuk meningkatkan fokus pada area tertentu. API Aspose.PSD mendukung dua pendekatan yang berbeda untuk memangkas gambar: dengan pergeseran dan persegi panjang.
### **Memangkas dengan Pergeseran**
Kelas RasterImage menyediakan versi overload dari metode Crop yang menerima 4 nilai integer yang menyatakan Kiri, Kanan, Atas & Bawah. Berdasarkan empat nilai ini, metode Crop memindahkan batas gambar ke arah pusat gambar sambil membuang bagian luar. Potongan kode di bawah ini mendemonstrasikan cara memangkas gambar dengan pergeseran.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Memangkas dengan Persegi Panjang**
Kelas RasterImage menyediakan versi overload lain dari metode Crop yang menerima contoh kelas Rectangle. Anda dapat memotong bagian mana pun dari gambar dengan memberikan batas-batas yang diinginkan pada objek Rectangle. Potongan kode di bawah ini mendemonstrasikan cara Memotong gambar dengan Persegi Panjang.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Memutar dan Membalik Gambar**
Aspose.PSD untuk Java adalah perpustakaan yang mudah digunakan karena menyediakan metode sederhana untuk melakukan operasi yang kompleks. Misalnya, Aspose.PSD untuk Java telah menyediakan metode RotateFlip untuk kelas dasarnya Image jika aplikasi memerlukan memutar gambar. Terlepas dari format gambar, perpustakaan dapat melakukan prosedur Rotate & Flip tertentu padanya.
### **Memutar Gambar**
Metode Image.RotateFlip dapat digunakan untuk memutar gambar sebesar 90/180/270 derajat dan membalikkan gambar secara horizontal atau vertikal. Metode Image.RotateFlip menerima parameter RotateFlipType yang menentukan jenis rotasi dan balik yang akan diterapkan pada gambar. Langkah-langkah untuk melakukan Rotasi & Balik sebegai berikut,

1. Memuat gambar menggunakan metode pabrik Load yang diungkapkan oleh kelas Image.
1. Memanggil metode Image.RotateFlip sambil menentukan RotateFlipType yang sesuai.
1. Menyimpan hasilnya.

Contoh kode di bawah ini mendemonstrasikan bagaimana mengatur properti RotateFlip dari sebuah Image dan enumerasi RotateFlipType.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Memutar Gambar pada Sudut Tertentu**
Aspose.PSD untuk Java API mengekspos metode RasterImage.Rotate untuk memudahkan penggunanya yang ingin memutar gambar pada sudut tertentu. Tidak seperti metode RasterImage.RotateFlip, metode RasterImage.Rotate menerima tiga parameter:

1. Sudut rotasi: Parameter tipe float yang menentukan sudut rotasi yang ingin diterapkan pada gambar. Nilai positif memutar gambar searah jarum jam; nilai negatif melakukan rotasi berlawanan arah jarum jam.
1. Resize proporsional: Parameter tipe Boolean menentukan apakah ukuran gambar harus berubah sesuai dengan proyeksi persegi panjang yang diputar. Jika diatur false, dimensi gambar tidak akan diubah dan hanya konten gambar internal yang diputar.
1. Warna latar belakang: Parameter tipe Color menentukan warna yang akan diisi di latar belakang gambar yang diputar.

Potongan kode di bawah ini mendemonstrasikan penggunaan metode RasterImage.Rotate.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Mengubah Ukuran Gambar**
Artikel ini menunjukkan penggunaan Aspose.PSD untuk Java untuk melakukan operasi Resize pada gambar. API Aspose.PSD telah mengekspos metode yang efisien dan mudah digunakan untuk mencapai tujuan ini. Aspose.PSD untuk Java telah mengekspos metode Resize untuk kelas Image yang dapat digunakan untuk mengubah ukuran gambar yang ada secara langsung. Ada dua overload dari metode Resize untuk memenuhi kebutuhan aplikasi.
### **Pengubahan Ukuran Sederhana**
Langkah-langkah untuk melakukan Resize adalah sebagaimana berikut:

1. Memuat gambar menggunakan metode pabrik Load yang diungkapkan oleh kelas Image.
1. Memanggil metode Image.Resize sambil menentukan Tinggi & Lebar baru.
1. Menyimpan hasilnya.

Contoh kode di bawah ini mendemonstrasikan bagaimana Meresize sebuah gambar.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Mengubah Ukuran dengan Enumerasi ResizeType**
Aspose.PSD API telah mengekspos enumerasi ResizeType yang dapat digunakan dengan Image.Resize untuk mencapai hasil yang diinginkan. Potongan kode yang diberikan di bawah ini mendemonstrasikan penggunaan enumerasi ResizeType, sementara rincian anggota enumerasi ResizeType dapat ditemukan di bagian bawah halaman ini.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}

Jika Anda berniat untuk mendapatkan hasil berkualitas setelah menerapkan penyesuaian ukuran, disarankan untuk selalu menggunakan ResizeType.LanczosResample karena akan menghasilkan hasil yang sangat berkualitas namun mungkin bekerja lebih lambat daripada ResizeType.NearestNeighbourResample. Di sisi lain, algoritma ResizeType.NearestNeighbourResample khusus digunakan untuk pengubahan ukuran yang cepat sambil mengorbankan kualitas gambar. Metode ini mungkin berguna untuk pembuatan thumbnail secara real-time atau proses serupa di mana kinerja diperlukan.
## **Mengubah Ukuran Gambar Secara Proporsional**
Anda dapat mengubah ukuran gambar dengan memasukkan nilai tinggi dan lebar baru sebagai parameter ke metode Image.Resize namun dalam kasus tersebut Anda harus menghitung rasio aspek sendiri. Hal ini karena ketika lebar atau tinggi gambar diubah, gambar akan diperbesar atau diperkecil untuk mengisi ukuran baru. Jika perubahan lebar dan tinggi gambar tidak sebanding, hal ini dapat mengakibatkan hasil yang terdistorsi. Artikel ini mendemonstrasikan penggunaan Aspose.PSD untuk API Java untuk mengubah ukuran gambar dengan memasukkan tinggi atau lebar baru sambil membiarkan API secara otomatis menghitung nilai proporsional lainnya.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **Enumerasi ResizeType**
ResizeType menentukan jenis re-size yang akan dilakukan pada gambar berdasarkan filter yang dipilih.

Anggota Enumerasi ResizeType

|**Nama Anggota**|**Nilai**|**Deskripsi**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Titik kiri atas gambar baru akan sama dengan titik kiri atas gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|RightTopToRightTop|1|Titik kanan atas gambar baru akan sama dengan titik kanan atas gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|RightBottomToRightBottom|2|Titik kanan bawah gambar baru akan sama dengan titik kanan bawah gambar asli. Pemangkasan akan terjadi jika diperluan.|
|LeftBottomToLeftBottom|3|Titik kiri bawah gambar baru akan sama dengan titik kiri bawah gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|CenterToCenter|4|Pusat gambar baru akan sama dengan pusat gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|LanczosResample|5|Melakukan Resample menggunakan algoritma Lanczos menggunakan masker 7x7.|
|NearestNeighbourResample|6|Melakukan Resample menggunakan algoritma tetangga terdekat.|


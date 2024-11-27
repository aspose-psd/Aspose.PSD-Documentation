---
title: Memotong, Memutar, dan Mengubah Ukuran Gambar
type: docs
weight: 40
url: /id/net/memotong-memutar-dan-merubah-ukuran-gambar/
---

## **Memotong Gambar**
Pemotongan gambar biasanya mengacu pada penghapusan bagian luar gambar untuk membantu meningkatkan framing. Pemotongan juga dapat digunakan untuk memotong beberapa bagian gambar untuk meningkatkan fokus pada area tertentu. API Aspose.PSD mendukung dua pendekatan yang berbeda untuk pemotongan gambar: dengan pergeseran dan persegi panjang.
### **Pemotongan dengan Pergeseran**
Kelas [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) menyediakan versi berlebihan dari metode Crop yang menerima 4 nilai bulat yang menunjukkan Kiri, Kanan, Atas, & Bawah. Berdasarkan empat nilai ini, metode Crop memindahkan batas gambar ke arah pusat gambar sambil membuang bagian luar. Contoh kode di bawah ini menunjukkan bagaimana memotong gambar dengan pergeseran.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **Pemotongan dengan Persegi Panjang**
Kelas [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) menyediakan versi lain dari metode Crop yang menerima contoh dari kelas Rectangle. Anda dapat memotong bagian apa pun dari gambar dengan memberikan batas yang diinginkan ke objek Persegi Panjang. Contoh kode di bawah ini menunjukkan bagaimana memotong gambar dengan Persegi Panjang.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **Memutar dan Membalik Gambar**
Aspose.PSD untuk .NET adalah pustaka yang mudah digunakan karena menyediakan metode sederhana untuk melakukan operasi kompleks. Misalnya, Aspose.PSD untuk .NET telah menyediakan metode RotateFlip untuk kelas dasarnya Gambar jika sebuah aplikasi memerlukan memutar gambar. Terlepas dari format gambar, pustaka ini dapat melakukan Pemutaran & Pembalikan spesifik di atasnya.
### **Memutar Gambar**
Metode Image.RotateFlip dapat digunakan untuk memutar gambar sebesar 90/180/270-derajat dan membalikkan gambar secara horizontal atau vertikal. Metode Image.RotateFlip menerima parameter RotateFlipType yang menentukan jenis rotasi dan flip yang akan diterapkan pada gambar. Langkah-langkah untuk melakukan Putar & Balik sebagaimana berikut,

1. Memuat gambar menggunakan metode pabrik Load yang terbuka oleh kelas Gambar.
1. Panggil metode Image.RotateFlip sambil menentukan RotateFlipType yang sesuai.
1. Simpan hasilnya.

Contoh kode berikut menunjukkan bagaimana mengatur properti RotateFlip dari Gambar dan enumerasi RotateFlipType.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **Memutar Gambar dengan Sudut Tertentu**
Aspose.PSD untuk API .NET mengekspos metode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate untuk memudahkan pengguna yang ingin memutar gambar pada sudut tertentu. Tidak seperti metode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip, metode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate menerima tiga parameter:

1. Sudut rotasi: Parameter tipe float yang menentukan sudut rotasi agar gambar diputar. Nilai positif memutar gambar searah jarum jam; nilai negatif melakukan rotasi berlawanan arah jarum jam.
1. Mengubah Proporsional: Parameter tipe Boolean yang menentukan apakah ukuran gambar harus diubah sesuai dengan proyeksi persegi panjang yang diputar. Jika diatur ke false, dimensi gambar tidak akan berubah dan hanya konten gambar internal yang diputar.
1. Warna latar belakang: Parameter tipe Color yang menentukan warna yang akan diisi di latar belakang gambar yang diputar.

Contoh kode di bawah ini menunjukkan penggunaan metode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **Mengubah Ukuran Gambar**
Artikel ini menunjukkan penggunaan Aspose.PSD untuk .NET untuk melakukan operasi Resize pada gambar. API Aspose.PSD telah mengekspos metode yang efisien & mudah digunakan untuk mencapai tujuan ini. Aspose.PSD untuk .NET telah mengekspos metode Resize untuk kelas Gambar yang dapat digunakan untuk mengubah ukuran gambar yang ada secara langsung. Ada dua overloads dari metode Resize untuk memenuhi kebutuhan aplikasi.
### **Pengubahan Ukuran Sederhana**
Langkah-langkah untuk melakukan Resize sebagaimana berikut:

1. Memuat gambar menggunakan metode pabrik Load yang terbuka oleh kelas Gambar.
1. Panggil metode Image.Resize sambil menentukan Tinggi & Lebar baru.
1. Simpan hasilnya.

Contoh kode berikut menunjukkan bagaimana mengubah ukuran gambar.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **Mengubah Ukuran dengan Perbesaran Enumeration**
API Aspose.PSD telah mengekspos enumerasi ResizeType yang dapat digunakan dengan Image.Resize untuk mencapai hasil yang diinginkan. Contoh kode yang disediakan di bawah ini menunjukkan penggunaan enumerasi ResizeType, sedangkan detail anggota enumerasi ResizeType terdapat di bagian bawah halaman ini.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



Jika Anda berniat untuk mendapatkan hasil berkualitas setelah menerapkan perubahan ukuran, disarankan untuk selalu menggunakan ResizeType.LanczosResample karena akan menghasilkan hasil yang sangat berkualitas namun mungkin bekerja lebih lambat dibandingkan ResizeType.NearestNeighbourResample. Di sisi lain, algoritma ResizeType.NearestNeighbourResample digunakan khusus untuk perubahan ukuran cepat sambil mengorbankan kualitas gambar. Metode ini mungkin berguna untuk pembuatan thumbnail secara real time atau proses serupa di mana kinerja diperlukan.
## **Mengubah Ukuran Gambar Secara Proporsional**
Anda dapat mengubah ukuran gambar dengan melewatkan nilai tinggi & lebar baru sebagai parameter ke metode Image.Resize namun dalam hal tersebut Anda harus menghitung rasio aspek sendiri. Hal ini karena ketika lebar atau tinggi gambar diubah, gambar tersebut akan di skalakan atau diperkecil untuk mengisi ukuran baru. Jika perubahan lebar dan tinggi gambar tidak sebanding ini dapat menghasilkan hasil yang direntangkan dan distorsi. Artikel ini menunjukkan penggunaan API Aspose.PSD untuk .NET untuk mengubah ukuran gambar dengan melewatkan entah tinggi atau lebar baru sambil membiarkan API secara otomatis menghitung nilai proporsional yang lain.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **Enumerasi ResizeType**
ResizeType menentukan jenis perubahan ukuran yang akan dilakukan pada gambar berdasarkan filter yang dipilih.

Anggota dari [Enumerasi ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)

|**Nama Anggota**|**Nilai**|**Deskripsi**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Titik kiri atas gambar baru akan bertepatan dengan titik kiri atas gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|RightTopToRightTop|1|Titik kanan atas gambar baru akan bertepatan dengan titik kanan atas gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|RightBottomToRightBottom|2|Titik kanan bawah gambar baru akan bertepatan dengan titik kanan bawah gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|LeftBottomToLeftBottom|3|Titik kiri bawah gambar baru akan bertepatan dengan titik kiri bawah gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|CenterToCenter|4|Pusat gambar baru akan bertepatan dengan pusat gambar asli. Pemangkasan akan terjadi jika diperlukan.|
|LanczosResample|5|Resampling menggunakan algoritma Lanczos menggunakan masker 7x7.|
|NearestNeighbourResample|6|Resampling menggunakan algoritma tetangga terdekat.|


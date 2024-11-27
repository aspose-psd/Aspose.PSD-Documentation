---
title: Menghindari Penurunan Kinerja saat Menggambar di atas Gambar yang Tersampel
type: docs
weight: 40
url: /id/java/menghindari-penurunan-kinerja-saat-menggambar-di-atas-gambar-yang-tersampel/
---

## **Menghindari Penurunan Kinerja saat Menggambar di atas Gambar yang Tersampel**
Ada saat-saat ketika Anda ingin melakukan operasi grafis yang sangat ekstensif pada gambar yang tersampel. Saat Aspose.PSD harus menyampel dan mengompresi gambar secara langsung, penurunan kinerja dapat terjadi. Menggambar di atas gambar yang tersampel juga dapat membawa hukuman kinerja.
### **Solusi**
Untuk menghindari penurunan kinerja, kami merekomendasikan agar Anda mengonversikan gambar ke format tidak terkompresi, atau raw, sebelum melakukan operasi grafis.
### **Menggunakan Path Berkas**
Pada contoh berikut, gambar PSD dikonversikan ke format raw (tanpa kompresi) dan disimpan ke disk. Gambar tidak terkompresi kemudian dimuat kembali sebelum operasi grafis dilakukan padanya. Teknik yang sama berlaku untuk berkas BMP dan GIF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Menggunakan Objek Aliran (Stream)**
Potongan kode berikut menunjukkan bagaimana gambar PSD dikonversikan ke format raw (tanpa kompresi) dan disimpan ke disk menggunakan Stream.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}

---
title: Menghindari Penurunan Kinerja saat Menggambar di atas Gambar Terkompresi
type: docs
weight: 10
url: /id/net/hindari-penurunan-kinerja-saat-menggambar-di-atas-gambar-terkompresi/
---

## **Menghindari Penurunan Kinerja saat Menggambar di atas Gambar Terkompresi**

Ada saat-saat ketika Anda ingin melakukan operasi grafis yang sangat ekstensif pada gambar terkompresi. Ketika Aspose.PSD harus mengompres dan mendekompresi gambar secara langsung, penurunan kinerja dapat terjadi. Menggambar di atas gambar terkompresi juga dapat membawa hukuman kinerja.

### **Solusi**
Untuk menghindari penurunan kinerja, kami merekomendasikan Anda mengonversi gambar ke format yang tidak terkompresi, atau mentah, sebelum melakukan operasi grafis.

### **Menggunakan Path Berkas**
Pada contoh berikut, gambar PSD dikonversi ke format mentah (tidak terkompresi) dan disimpan ke disk. Gambar tidak terkompresi kemudian dimuat kembali sebelum operasi grafis dilakukan padanya. Teknik yang sama berlaku untuk berkas BMP dan GIF.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}

### **Menggunakan Objek Aliran (Stream)**
Potongan kode berikut menunjukkan bagaimana gambar PSD dikonversi ke format mentah (tidak terkompresi) dan disimpan ke disk menggunakan MemoryStream.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}

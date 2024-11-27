---
title: Mengedit layer raster mask dalam file PSD via API
type: docs
weight: 20
url: /id/mengedit-layer-raster-mask-dalam-file-psd-via-api/
---

## **Ikhtisar**
**Untuk mengotomatisasi penyuntingan format PSD dan mengubah file PSD tanpa Adobe® Photoshop®, Anda dapat menggunakan API Aspose.PSD yang disediakan di bawah ini. Ada fragmen kode C# dan .NET yang dapat membantu Anda memodifikasi file PSD.**

Dengan Menggunakan Masker Lapisan dan Vektor PSD kita dapat menyembunyikan dan menampilkan piksel lapisan tanpa menghapusnya secara permanen. Masker raster juga disebut sebagai masker lapisan atau masker pengguna. Akses ke masker raster dan vektor dalam Aspose.PSD disediakan melalui properti lapisan [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) yang dapat menjadi contoh dari kelas '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' dan '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' yang merupakan turunan dari kelas abstrak 'LayerMaskData'. Jika sebuah lapisan memiliki masker raster dan vektor maka contoh [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull) disediakan. Jika lapisan hanya memiliki masker raster atau vektor maka contoh [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort) disediakan. Jika properti LayerMaskData null maka lapisan tersebut tidak memiliki masker atau hanya memiliki masker vektor yang dinonaktifkan.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Masker raster dan masker vektor yang dinonaktifkan LayerMaskDataShort</p><p>Masker raster yang dinonaktifkan LayerMaskDataShort</p><p>Masker raster dan masker vektor LayerMaskDataFull</p><p>Masker raster LayerMaskDataShort</p><p>Masker vektor LayerMaskDataShort</p><p>Masker vektor yang dinonaktifkan null (Tetapi sumber vektor hadir)</p>|
| :- | :- |
## **Bagaimana cara mendapatkan masker raster lapisan dalam file PSD?**
Pertama, kita harus mencari tahu apakah sebuah lapisan memiliki masker vektor dan masker lapisan:

Berikut adalah contoh kode sampel yang menunjukkan cara mendapatkan masker raster lapisan

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

Jika tidak, jenis properti lapisan LayerMaskData adalah LayerMaskDataShort. Dalam hal ini, mari kita periksa jika lapisan hanya memiliki masker raster dengan memeriksa properti Flags. Properti tersebut tidak boleh mengandung [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData** flag, jika tidak maskernya adalah cache masker vektor**.**

Kode untuk mendapatkan masker:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Jika Anda perlu **mengambil masker raster** sebagai LayerMaskDataShort (untuk manipulasi lebih lanjut) bahkan ketika kedua masker ada, maka LayerMaskDataFull harus diambil dan dikonversi menjadi LayerMaskDataShort. Kode berikut dapat digunakan untuk kedua kasus:

Mengekstrak masker raster dari PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **Bagaimana cara memeriksa apakah sebuah lapisan dalam file PSD memiliki masker raster?**
Kode C# berikut dapat membantu Anda memeriksa apakah sebuah lapisan memiliki masker raster:

Cara mengetahui apakah masker raster diterapkan ke [Lapisan PSD](/psd/id/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **Bagaimana cara menghapus / menambah / memperbarui masker raster lapisan dalam file PSD?**
Hanya menghapus / menambah / memperbarui LayerMaskData tidak cukup untuk menyimpan dengan benar karena saluran tidak diperbarui; meskipun mungkin memberikan rendering yang benar. Ini tidak mengubah saluran masker:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Kita harus menggunakan metode AddLayerMask lapisan untuk menghapus / menambah / memperbarui.

Ini menambah/memperbarui baik masker maupun saluran:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Ini menghapus baik masker maupun saluran:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **Menghapus masker raster lapisan dalam gambar PSD**
Pertama, kita periksa apakah maskernya dalam format pendek dan jika bukan vektor kita hanya dapat memanggil metode AddLayerMask dengan null untuk menghapus masker raster. Tetapi jika maskernya dalam format penuh kita harus mengonversinya ke format pendek sehingga meninggalkan masker vektor saja. Untuk menghapus masker lapisan ini dapat digunakan contoh kode C# .NET berikut:

Potongan kode cara menghapus Layer Mask dari File PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **Memperbarui masker raster lapisan dalam gambar PSD**
Ini cukup langsung: jika masker dalam format pendek kita harus mengubah ImageData dan MaskRectangle jika perlu, jika tidak [UserDataMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)dan [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle) harus diubah. Contoh kode C# .NET berikut dapat digunakan untuk memperbarui masker lapisan:

Perbarui Masker Lapisan PSD menggunakan C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Berikut contoh tindakan yang mungkin mengubah masker raster. Ini membalikkan masker pengguna lapisan:

Perbarui Masker Lapisan PSD menggunakan C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **Memperbarui masker vektor dalam file PSD ketika masker raster lapisan ada**
Diasumsikan bahwa pengguna telah mengubah sumber jalur vektor. Kemudian bisa memperbarui masker vektor dengan mudah dengan memanggil metode AddLayerMask lapisan:

Perbarui [Masker Vektor Lapisan PSD](/psd/id/net/layer-vector-mask/) menggunakan C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **Menambahkan masker raster lapisan dalam file PSD**
Jika sebuah lapisan tidak memiliki masker kita dapat menambahkan masker raster yang diberikan dengan memanggil metode AddLayerMask.

Jika masker tidak memiliki [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)flag maka maskernya sudah memiliki masker raster dan kita harus memperbarui seperti yang dijelaskan di atas. Jika tidak, jika masker ini dalam format pendek kita mengonversinya ke format penuh. Jika tidak kita menggunakannya apa adanya. Kemudian memperbarui UserMaskData, UserMaskRectangle, dan properti lain dengan properti masker yang diberikan. Contoh kode C# .NET berikut dapat digunakan untuk menambahkan (memperbarui) masker lapisan:

Tambahkan Layer Mask baru ke PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Bagaimana cara memeriksa apakah sebuah masker lapisan diaktifkan?**
Untuk mengetahui keadaan masker raster lapisan yang diaktifkan kita dapat memeriksa keadaan bendera LayerMaskFlags.Disabled di properti Flags untuk LayerMaskDataShort atau di RealFlags untuk LayerMaskDataFull. Contoh kode C# .NET berikut dapat digunakan untuk mendapatkan keadaan masker lapisan yang diaktifkan:

Periksa jika sebuah masker diaktifkan:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}
## **Bagaimana cara mengaktifkan atau menonaktifkan masker raster lapisan?**
Untuk mengaktifkan atau menonaktifkan masker raster lapisan kita dapat mengubah keadaan flag LayerMaskFlags.Disabled di properti Flags untuk LayerMaskDataShort atau di RealFlags untuk LayerMaskDataFull. Contoh kode C# .NET berikut dapat digunakan untuk mengubah keadaan masker lapisan yang diaktifkan:

Aktifkan atau nonaktifkan Masker Raster Lapisan:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}

---
title: Menggunakan file PSD sebagai template untuk otomatisasi - Kasus Kartu Bisnis
type: docs
weight: 10
url: /id/net/menggunakan-file-psd-sebagai-template-untuk-otomatisasi-kasus-kartu-bisnis/
---

### **Ikhtisar**
Artikel ini menjelaskan kasus yang sering digunakan ketika Anda perlu memperbarui beberapa lapisan di [File PSD](https://wiki.fileformat.com/image/psd/) secara otomatis, di mana file PSD/PSB memiliki struktur mirip template yang sudah dikenal. Hal ini dapat digunakan untuk membuat sejumlah besar Kartu Bisnis untuk orang yang berbeda (Kasus Kartu Bisnis). Atau Anda perlu menerjemahkan file PSD ke berbagai bahasa dengan penggantian beberapa materi grafis di dalamnya.

Setelah membaca artikel ini, Anda akan tahu bagaimana Anda dapat melakukan hal ini:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)

## **Kasus Sederhana**
Sebagai contoh, Anda memiliki beberapa Template PSD dengan Nama Lapisan yang sudah dikenal. Jadi, Anda perlu mengubah, memperbarui, atau mengganti Lapisan PSD melalui C#. Pertama-tama, Anda perlu membuka file template dengan Aspose.PSD.

Bagaimana cara membuka File PSD via C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

Kemudian kita perlu menemukan lapisan yang ingin kita ganti berdasarkan namanya. Berikut adalah implementasi sederhana untuk ini.

Bagaimana cara menemukan lapisan dalam file PSD berdasarkan namanya?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}

Ketika lapisan sudah ditemukan, kita dapat memperbarui lapisan tersebut dengan cara biasa, menggunakan [Grafik](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Bagaimana Cara Menggambar pada Grafik Lapisan PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

Dalam kasus ini, kita menggambar gambar [PNG yang baru dimuat](https://wiki.fileformat.com/image/png/) pada lapisan PSD yang ada, sehingga data lama akan hilang dalam file baru.

Tetapi bagaimana jika kita juga perlu memperbarui teks? Prosesnya akan serupa. Temukan [Lapisan Teks](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) berdasarkan namanya lalu kita secara programatik [memperbarui Lapisan Teks dari File Photoshop](/psd/id/net/render-text-with-different-colors-in-text-layer/) tersebut.

Bagaimana cara memperbarui Lapisan Teks di Photoshop menggunakan C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}

Pada akhirnya, kita perlu menyimpan perubahan kita:

Bagaimana cara menyimpan file PSD yang telah diubah menggunakan [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}

Gambar hasilnya:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)

## **Kasus Kompleks dengan fitur tambahan**
Di atas kita menunjukkan cara paling sederhana untuk mengganti gambar dalam lapisan File PSD.

Namun, Aspose.PSD dapat menawarkan fitur tambahan yang lebih kompleks seperti menambahkan lapisan baru, menghapus lapisan lama, dan memperbarui lapisan teks dengan gaya berbeda pada teks multi-baris.

Kita dapat menemukan [Lapisan](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) yang ingin kita ganti, kemudian menemukan indeksnya dalam Daftar Lapisan, menghapusnya dan menyisipkan lapisan baru setelah diciptakan dari [File Jpeg](https://wiki.fileformat.com/image/jpeg/) ke tempat yang sama.

Membuat lapisan baru dari file dan menyisipkannya ke Gambar PSD menggunakan [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}

Pada akhir file cuplikan kode ini, kita memperbaiki posisi lapisan dan menyimpan array Lapisan baru ke Gambar Psd.

Bagaimana cara menyalin properti Lapisan [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}

Dan setelah semua itu, kita perlu memperbarui lapisan teks dalam gambar PSD yang ada menggunakan C#. Aspose.PSD mendukung [pembaruan TextLayer secara Portion](/psd/id/net/working-with-text-layers/). Setiap [bagian teks](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) memiliki kombinasi unik dari properti Gaya dan Paragraf.

Bagaimana cara menyalin properti Lapisan [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}

Sebagai hasilnya, kami telah mengubah template PSD melalui kode dengan lapisan baru dari file Jpeg, Png, J2k, Bmp, Gif, atau Tiff serta [teks multi-baris dengan gaya berbeda](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) pada setiap baris.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)

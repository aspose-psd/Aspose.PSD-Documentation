---
title: Bekerja dengan Lapisan
type: docs
weight: 150
url: /id/net/working-with-layers/
---

## **Membuat Kelompok Lapisan**
Sebuah kelompok lapisan terdiri dari satu atau lebih lapisan dan membantu dalam menyusun lapisan-lapisan yang serupa atau terkait. Dengan menggunakan Aspose.PSD untuk .NET Anda dapat membuat kelompok lapisan. Untuk tujuan ini, sebuah metode baru [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) telah ditambahkan dalam kelas **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** untuk menambahkan kelompok lapisan.

Langkah-langkah untuk membuat kelompok lapisan adalah sebagai berikut:

- Buat sebuah instansi gambar menggunakan kelas PsdImage dengan lebar, tinggi, dan opsi gambar yang spesifik.
- Buat sebuah [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) dengan nama grup dan indeks yang ditentukan.
- Buat sebuah instansi kelas Layer dan berikan gambar PSD padanya.
- Tambahkan lapisan yang dibuat ke kelompok lapisan menggunakan metode AddLayer yang terpapar oleh kelas LayerGroup.
- Simpan hasilnya.

Potongan kode berikut menunjukkan bagaimana cara membuat kelompok lapisan.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}

## **Mengganti Nama Lapisan**
Anda dapat menggunakan nama apa pun yang Anda inginkan, tetapi praktik umum adalah menggunakan deskripsi umum dari objek atau elemen yang berada di lapisan tersebut. Artikel ini menunjukkan bagaimana Anda dapat mengubah nama sebuah lapisan menggunakan Aspose.PSD untuk .NET. Untuk tujuan ini, properti baru [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) telah ditambahkan dalam kelas Layer untuk menampilkan nama lapisan dengan benar. Telah diamati bahwa ketika Photoshop menyimpan sebuah nama lapisan menggunakan properti [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), maka karakter Korea disimpan sebagai byte 63 '?' dalam ASCII. Jadi, jika Anda ingin menampilkan nama lapisan dengan benar, gunakan properti **DisplayName** karena properti **Name** tidak mendukung karakter Korea.

Contoh kode berikut menunjukkan bagaimana Anda dapat mengganti nama lapisan.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **Dukungan untuk Lapisan Terhubung**
Menghubungkan lapisan mirip dengan mengelompokkan lapisan-lapisan tersebut. Jika Anda menghubungkan dua atau lebih lapisan maka akan memungkinkan Anda untuk melakukan perubahan tertentu terhadap kedua lapisan yang terhubung tersebut. Misalnya, jika Anda menerapkan transformasi pada satu lapisan maka itu akan diterapkan pada semua lapisan terhubung lainnya. Artikel ini menunjukkan bagaimana Anda dapat mendapatkan dan membatalkan penghubungan lapisan terhubung dengan menggunakan [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}

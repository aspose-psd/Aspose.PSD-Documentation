---
title: Contoh penggunaan kelompok layer dalam Aspose.PSD untuk C#
weight: 100
type: docs
description: Penggunaan Kelompok Layer dari Berkas PSD melalui C#
keywords: [kelompok layer, layer kelompok, tambahkan layer ke kelompok, psd api, C#, csharp, contoh kode]
url: id/psd-group-layer/
---

## Ikhtisar

Kelompok layer dalam Aspose.PSD untuk C# memungkinkan untuk pengorganisasian dan manipulasi yang efisien dari layer dalam sebuah berkas PSD. Dengan menggunakan folder layer, Anda dapat mengelompokkan beberapa layer bersama dan menerapkan transformasi atau efek ke seluruh kelompok.

Contoh ini menunjukkan pembuatan gambar PSD baru dengan `PsdImage.Create`. Kemudian, objek `LayerGroup` baru dibuat menggunakan `AddLayerGroup` dari objek 'PsdImage'. Layer grup dinamai "Folder," dimasukkan pada indeks 0, dan diatur menjadi terlihat.

Selanjutnya, dua objek `Layer` dibuat dengan properti `DisplayName` mereka diatur. Layer-layer ini ditambahkan ke dalam layer grup menggunakan `AddLayer`.

Layer dalam grup dapat diakses melalui properti `Layers` dari objek `LayerGroup`. Contoh ini menegaskan bahwa nama tampilan lapisan pertama dan kedua dalam grup adalah "Layer 1" dan "Layer 2".

Setelah memodifikasi kelompok layer, gambar PSD yang diperbarui disimpan dengan metode `Save` dari objek `PsdImage`.

Contoh dasar ini mengenalkan cara kerja dengan kelompok layer menggunakan Aspose.PSD untuk C#. Perpustakaan ini menawarkan fitur canggih untuk memanipulasi dan mentransformasi layer dalam berkas PSD. Silakan lihat dokumentasi Aspose.PSD untuk C# untuk contoh dan fitur yang lebih detail.

Berikut ini adalah potongan kode contoh yang menunjukkan penggunaan kelompok layer dalam Aspose.PSD untuk C#:

## Contoh

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Untuk informasi lebih detail dan contoh, silakan kunjungi [dokumentasi Aspose.PSD untuk C#](https://docs.aspose.com/psd/net/).


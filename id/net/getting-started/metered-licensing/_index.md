---
title: Lisensi Berbasis Meter
type: docs
weight: 80
url: /id/net/lisensi-berbasis-meter/
description: PSD Photoshop C# Library memungkinkan pengembang untuk menerapkan kunci berbasis meter yang merupakan mekanisme lisensi baru dan akan digunakan bersama dengan metode lisensi yang sudah ada.
---

{{% alert color="primary" %}} 

Aspose.PSD memungkinkan pengembang untuk menerapkan kunci berbasis meter. Ini adalah mekanisme lisensi baru. Mekanisme lisensi baru ini akan digunakan bersama dengan metode lisensi yang sudah ada. Pelanggan yang ingin ditagih berdasarkan penggunaan fitur API dapat menggunakan lisensi berbasis meter. Untuk informasi lebih lanjut, silakan lihat bagian [FAQ Lisensi Berbasis Meter](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}} 
## **Lisensi Berbasis Meter**
Berikut adalah langkah-langkah sederhana untuk menggunakan kelas Metered.

1. Buat instance kelas Metered.
1. Lewatkan kunci publik & privat ke metode setMeteredKey.
1. Lakukan pemrosesan (lakukan tugas).
1. Panggil metode getConsumptionQuantity dari kelas Metered.
1. Ini akan mengembalikan jumlah/kuantitas permintaan API yang telah Anda gunakan sejauh ini.

Berikut adalah contoh kode yang menunjukkan cara mengatur kunci publik dan privat berbasis meter.

{{< highlight java >}}

 // Buat instance kelas Metered PSD

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Akses properti setMeteredKey dan lewatkan kunci publik dan privat sebagai parameter

metered.SetMeteredKey("*****", "*****");



// Dapatkan jumlah data metered sebelum memanggil API

decimal jumlahSebelumnya = Aspose.PSD.Metered.GetConsumptionQuantity();



// Tampilkan informasi

Console.WriteLine("Jumlah yang Dikonsumsi Sebelumnya: " + jumlahSebelumnya.ToString());

// Dapatkan jumlah data metered setelah memanggil API

decimal jumlahSetelah = Aspose.PSD.Metered.GetConsumptionQuantity();



// Tampilkan informasi

Console.WriteLine("Jumlah yang Dikonsumsi Setelah: " + jumlahSetelah.ToString());

{{< /highlight >}}

---
title: Aplikasi Editor NLP CLI Aspose.PSD untuk .NET
type: docs
weight: 10
url: /id/net/cli/nlp-editor/
is_root: false
keywords: CLI Alat Photoshop NLP Pemrosesan Bahasa Alami PSD Konsol Pustaka C# API PSD
description: Aplikasi Editor NLP CLI berbasis Aspose.PSD untuk format file PSD, PSB, dan AI. Automasi CI/CD tanpa kode. Mendukung pemrosesan bahasa alami untuk mengedit file PSD. Cukup tuliskan permintaan Anda dalam bahasa alami untuk melakukan berbagai operasi seperti konversi, penyesuaian, penyesuaian ukuran, dan lainnya. Tidak memerlukan Adobe Photoshop atau Adobe Illustrator terinstal dan dapat dijalankan dari konsol tanpa kode tambahan.
---

**![Logo Produk Aspose.PSD for .NET](home_1.png)**

**Selamat datang di Aplikasi Editor NLP CLI Aspose.PSD untuk .NET**

Aplikasi Editor NLP CLI Aspose.PSD adalah utilitas konsol ringan untuk mengedit file PSD menggunakan perintah bahasa alami. Integrasi mudah ke dalam Pipa CI/CD.

**Penolakan**

Ini adalah aplikasi eksperimental. Silakan coba dan berikan umpan balik. Setiap umpan balik sangat dihargai. Kami ingin membawa aplikasi Tanpa Kode ke tingkat berikutnya. Integrasi mudah ke pipa pembangunan atau proses bisnis apa pun adalah tujuan kami.

**Fungsionalitas Utama Aplikasi Editor NLP CLI Aspose.PSD untuk .NET**

1. Melakukan operasi pada file PSD, PSB, AI menggunakan perintah bahasa alami.
2. Mendukung berbagai operasi seperti konversi, penyesuaian, penyesuaian ukuran, dan lainnya.
3. Automasi CI/CD tanpa kode.
4. Mendukung penulisan permintaan dalam bahasa alami untuk mengedit file PSD.

## **Penggunaan dari baris perintah:**

{{% alert color="primary" %}}
Pertama-tama instalasi alat dotnet ini:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Kami merekomendasikan sebelum penggunaan pertama jalankan perintah berikut:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Setelah perintah ini Anda akan dapat menjalankan aplikasi ini dengan nama singkat nlp.cli alih-alih Aspose.PSD.CLI.NLP.Editor. Anda dapat menentukan nama singkat Anda sendiri.
{{% /alert %}}

**Parameter yang Tersedia untuk Aplikasi Cropping CLI Aspose.PSD.CLI**

| **Argumen** | **Deskripsi**                         |
|:------------|:--------------------------------------|
| teks apa pun | Diperlukan. Perintah Anda dalam bahasa alami untuk memperbarui File PSD atau PSB      |
| lisensi     | Path ke lisensi.                    |
| verbose     | Tampilkan informasi lebih banyak tentang perintah tertentu. |
| setup       | Membuat file bat di folder alat untuk panggilan cepat dari konsol. Contoh: --setup psd.nlp. Lalu Anda dapat memanggil alat dengan perintah psd.nlp |

**Contoh penggunaan**

1. Perintah ini akan mengonversi file pertama yang ditemukan (yang dapat dibuka dengan aspose.psd) dari folder saat ini dan akan menyimpannya dalam format png dengan transparansi. Juga, lisensi akan diatur. Anda perlu menentukan lisensi hanya sekali. Lisensi berikutnya akan digunakan dari path yang ditentukan. Perintah ini akan menampilkan log verbose pemrosesan NLP jika tersedia. 
{{< highlight bash >}}
  nlp.cli Konversi file dari folder ini ke format png dengan alpha --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. Perintah ini akan mencari file dengan nama yang paling mirip dengan "smth.psd". Lalu akan menyesuaikan kontras dan akan menyimpannya ke jpeg dengan kualitas terbaik. Nama file keluaran akan dicetak. Itu akan menjadi smth.jpg
{{< highlight bash >}}
Atur kontras pada 10 lapisan dengan nama elips dalam file smth.psd dan simpan ke output.jpg dengan kualitas terbaik
{{< /highlight >}}

3. Perintah ini akan membuka file pada path yang ditentukan, dan akan mengurangi ukurannya menjadi 25%. File keluaran akan dicetak. Akan disimpan dalam folder saat ini dari konsol.
{{< highlight bash >}}
Ubah ukuran file C:\Users\someuser\Desktop\input.psd menjadi 25%
{{< /highlight >}}

4. Perintah ini akan menemukan file input.psd di C:\Users\someuser\Desktop\. Lalu akan menemukan lapisan dengan indeks 3 dan akan mengubah ukurannya menjadi lebar 50px dan tinggi 100px. Lalu lapisan ini akan disimpan sebagai PDF di C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
 Ubah ukuran lapisan dengan indeks 3 dari C:\Users\someuser\Desktop\input.psd menjai lebar 50 dan tinggi 100 dan simpan ke C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

 5. Perintah ini akan membuka smth.psd di folder saat ini, tetapi semua efek akan dinonaktifkan. Lalu file ini akan dikonversi ke format BMP dan sebagai output.bmp dalam folder saat ini.
 {{< highlight bash >}}
 Buka smth.psd tanpa efek dan simpan ke output.bmp
  {{< /highlight >}}

**Harap periksa aplikasi CLI Aspose.PSD lainnya [di sini](https://docs.aspose.com/psd/net/cli) untuk .NET jika Anda memerlukan menambahkan dukungan untuk format PSD, PSB, dan AI ke alur kerja Anda**

1. [Aspose.PSD CLI Konversi](/psd/id/net/cli/konversi)
2. [Aspose.PSD CLI Cropping](/psd/id/net/cli/cropping)
3. [Aspose.PSD CLI Resize](/psd/id/net/cli/resize)
4. [Aspose.PSD CLI Ekspor](/psd/id/net/cli/export)
5. [Aspose.PSD CLI Editor NLP](/psd/id/net/cli/nlp-editor)

**Harap periksa Aspose.PSD untuk .NET atau [platform lainnya]**

Aplikasi CLI Aspose.PSD adalah solusi siap pakai untuk operasi populer. Jika Anda membutuhkan solusi yang fleksibel, harap periksa versi lengkap dari Aspose.PSD

1. [Aspose.PSD untuk .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD untuk Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD untuk Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Sumber Daya Aspose.PSD untuk .NET**

Berikut adalah tautan ke beberapa sumber daya yang berguna yang mungkin Anda butuhkan untuk menyelesaikan tugas Anda.

- [Dokumentasi Online Aplikasi CLI Aspose.PSD untuk .NET](/psd/id/net/cli/konversi)
- [Catatan Rilis untuk Aplikasi CLI Aspose.PSD untuk .NET](/psd/id/net/cli/konversi/catatan-rilis/)
- [Halaman Produk Aplikasi CLI Aspose.PSD untuk .NET](https://products.aspose.com/psd/net/cli)
- [Panduan Referensi API Aspose.PSD untuk .NET](https://reference.aspose.com/net/psd)
- [Unduh Contoh di Repositori GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Forum Dukungan Gratis Aspose.PSD untuk .NET](https://forum.aspose.com/c/psd)
- [Layanan Bantuan Dukungan Berbayar Aspose.PSD untuk .NET](https://helpdesk.aspose.com/)


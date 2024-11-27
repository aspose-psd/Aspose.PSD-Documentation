---
title: Catatan Rilis Aspose.PSD CLI NLP Editor untuk .NET 24.6
type: docs
weight: 90
url: /id/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD CLI NLP Editor untuk .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                               | **Kategori**  |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Rilis Awal Aplikasi CLI Aspose.PSD: Aspose.PSD.CLI.Export dan Aspose.PSD.CLI.NLP.Editor     | Peningkatan   |


## **Contoh Penggunaan:**

**PSDNET-2110. Rilis awal Aplikasi CLI Aspose.PSD NLP Editor**


## **Penggunaan dari baris perintah:**

{{% alert color="primary" %}}
Pertama-tama, instalasikan alat dotnet ini:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Kami sarankan sebelum penggunaan pertama, jalankan perintah berikut:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Setelah perintah ini dijalankan, Anda akan dapat menjalankan aplikasi ini dengan nama singkat nlp.cli alih-alih Aspose.PSD.CLI.NLP.Editor. Anda dapat menentukan nama singkat Anda sendiri.
{{% /alert %}}

**Contoh penggunaan**

1. Perintah ini akan mengonversi file yang ditemukan pertama (yang dapat dibuka dengan aspose.psd) dari folder saat ini dan menyimpannya dalam format png dengan transparansi. Juga, lisensi akan diatur. Anda hanya perlu menentukan lisensi sekali. Lisensi akan digunakan dari jalur yang ditentukan pada run berikutnya. Perintah ini akan menampilkan log verbor NLP processing jika tersedia.
{{< highlight bash >}}nlp.cli Convert file dari folder ini ke format png dengan alpha --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. Perintah ini akan mencari file dengan nama paling mirip dengan "smth.psd". Kemudian akan menyesuaikan kontras dan menyimpannya dalam jpeg dengan kualitas terbaik. Nama file output akan ditampilkan. Ini akan menjadi smth.jpg
{{< highlight bash >}}Sesuaikan kontras pada 10 lapisan dengan nama ellipse di file smth.psd dan simpan ke output.jpg dengan kualitas terbaik{{< /highlight >}}

3. Perintah ini akan mengatur file pada jalur yang ditentukan, dan akan mengurangi ukurannya menjadi 25%. File output akan ditampilkan. Itu akan disimpan dalam folder saat ini di konsol.
{{< highlight bash >}}Resize file C:\Users\someuser\Desktop\input.psd menjadi 25%{{< /highlight >}}

4. Perintah ini akan menemukan file input.psd di C:\Users\someuser\Desktop\. Kemudian akan menemukan lapisan dengan indeks 3 dan akan mengubah ukurannya menjadi lebar 50px dan tinggi 100px. Kemudian lapisan ini akan disimpan sebagai PDF di C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Resize lapisan dengan indeks 3 dari C:\Users\someuser\Desktop\input.psd menjadi lebar 50 dan tinggi 100 dan simpan ke C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. Perintah ini akan membuka smth.psd di folder saat ini, namun semua efek akan dinonaktifkan. Dan kemudian file ini akan dikonversi ke format BMP dan disimpan sebagai output.bmp di folder saat ini.
{{< highlight bash >}}Buka smth.psd tanpa efek dan simpan ke output.bmp{{< /highlight >}}

**Penolakan**

Ini adalah aplikasi eksperimental. Silakan coba dan beri masukan. Setiap masukan sangat dihargai. Kami ingin membawa aplikasi Tanpa Kode ke tingkat berikutnya. Integrasi mudah ke pipa pembangunan atau proses bisnis apa pun adalah tujuan kami.

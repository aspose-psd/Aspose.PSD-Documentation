---
title: Lisensi
type: docs
weight: 70
url: /id/net/licensing/
description: Mengevaluasi PSD Photoshop C# Library dari NuGet dan menerapkan lisensi menggunakan file atau stream untuk menghapus batasan dari evaluasi yang terinstal.
---

## **Batasan Versi Evaluasi**
Anda dapat mengunduh versi evaluasi Aspose.PSD untuk .NET dari [NuGet](https://www.nuget.org/packages/Aspose.psd/). Versi evaluasi menyediakan fitur yang sama dengan versi berlisensi penuh dari komponen dengan beberapa batasan. Saat Anda membeli Aspose.PSD, hanya dengan menerapkan lisensi maka semua batasan dari evaluasi yang terinstal akan dihapus. Versi evaluasi Aspose.PSD untuk .NET menyediakan fungsionalitas produk lengkap, dengan hanya dua batasan:

- **Tanda air pada setiap gambar**: Setiap gambar yang Anda simpan, ubah, atau ekspor memiliki tanda air yang membaca "Evaluation Only. Created with Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". Gambar-gambar kecil, di mana tanda air penuh tidak muat, memiliki dua garis diagonal melintasi gambar tersebut.
- **Tidak ada dukungan untuk fungsionalitas dasar menggambar**: Dalam mode evaluasi, piksel gambar tidak dapat dimuat atau disimpan ke gambar. Untuk menggambar gambar, gunakan fungsionalitas menggambar lanjutan. Batasan ini memengaruhi fungsionalitas yang bergantung pada fungsionalitas dasar menggambar. Aspose.PSD untuk .NET memungkinkan Anda mendaftarkan format file Anda sendiri. Namun, fitur ini bergantung pada fungsionalitas dasar menggambar sehingga tidak masuk akal untuk menggunakannya dalam mode evaluasi karena Anda tidak dapat mengubah konten dari file-file tersebut.

Jika Anda ingin menguji Aspose.PSD untuk .NET tanpa batasan evaluasi, minta lisensi sementara 30 hari. Silakan lihat [Cara Mendapatkan Lisensi Sementara?](https://purchase.aspose.com/temporary-license) untuk informasi lebih lanjut.
## **Tentang Berkas Lisensi**
Setelah Anda puas dengan evaluasi Aspose.PSD, Anda dapat membeli lisensi di [situs web Aspose](https://purchase.aspose.com/default.aspx). Kenali berbagai jenis langganan yang ditawarkan. Jika Anda memiliki pertanyaan, jangan ragu untuk menghubungi [tim penjualan Aspose](https://company.aspose.com/contact). Setiap lisensi Aspose dilengkapi dengan langganan satu tahun untuk pembaruan perangkat lunak. Setelah tahun pertama, perbarui langganan Anda untuk terus mendapatkan fitur-fitur terbaru dan perbaikan. Dukungan teknis gratis dan tidak terbatas diberikan kepada pengguna berlisensi maupun evaluasi melalui [Forum Dukungan](https://forum.aspose.com/) kami. Lisensi ini berupa berkas XML yang berisi detail seperti nama produk, jumlah pengembang yang dilisensikan, tanggal kedaluwarsa langganan, dan sebagainya. Berkas ini ditandatangani digital, jadi jangan mengubahnya: bahkan secara tidak sengaja menambahkan jeda baris tambahan akan membuat berkas tersebut tidak valid. Setelah membeli Aspose.PSD, Anda perlu menerapkan lisensi sebelum membuat, mengedit, atau memanipulasi gambar.

## **Tempat Menyertakan Lisensi dalam Aplikasi Anda**
Di mana Anda menyertakan lisensi tergantung pada jenis aplikasi yang Anda kembangkan. Ikuti aturan sederhana berikut:

- Hanya menerapkan lisensi sekali per domain aplikasi. Memanggil License.SetLicense beberapa kali tidak merugikan tapi membuang waktu prosesor.
- Terapkan lisensi sebelum memanggil kelas Aspose.PSD untuk .NET apa pun.
- **Aplikasi Windows Forms atau konsol**: panggil License.SetLicense di kode startup, sebelum menggunakan kelas Aspose.PSD untuk .NET apa pun.
- **Aplikasi ASP.NET**: panggil License.SetLicense dari file Global.asax.cs (Global.asax.vb), dalam metode yang dilindungi Application_Start. Dengan cara ini, lisensi dijalankan sekali saat aplikasi mulai. Jangan memanggil License.SetLicense dari dalam metode Page_Load atau lisensi akan dimuat setiap kali halaman web dimuat.
- **Aplikasi Silverlight**: panggil License.SetLicense dari acara Application_Startup di file App.xaml.cs (App.xaml.vb).
- **Pustaka Kelas**: panggil License.SetLicense dari konstruktor statis dari kelas yang menggunakan Aspose.PSD. Konstruktor statis dieksekusi sebelum sebuah instance dari kelas Anda dibuat, memastikan bahwa lisensi Aspose.PSD telah diatur dengan benar.
## **Menerapkan Lisensi**
Anda dapat dengan mudah mengunduh versi evaluasi Aspose.PSD dari NuGet [halaman unduhan](https://www.nuget.org/packages/Aspose.psd/). Versi evaluasi memberikan kemampuan yang sama persis dengan versi berlisensi Aspose.PSD. Selain itu, versi evaluasi akan menjadi berlisensi saat Anda membeli lisensi dan menambahkan beberapa baris kode untuk menerapkan lisensi.
### **Menggunakan Berkas atau Stream**
Jika Anda ingin menghindari bekerja dengan batasan evaluasi, Anda perlu menyetel lisensi sebelum menggunakan Aspose.PSD. Anda hanya perlu menyetel lisensi sekali per aplikasi (atau proses).
### **Menerapkan lisensi dari berkas**
Cara termudah untuk menerapkan lisensi adalah dengan meletakkan berkas lisensi di folder yang sama dengan Aspose.PSD.dll. Kemudian Anda dapat menentukan nama berkas dalam kode alih-alih jalur lengkap.



{{< highlight java >}}

 // Menginisialisasi sebuah instance lisensi dan menerapkan lisensi menggunakan jalur lengkap

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



Saat Anda memanggil metode SetLicense, nama lisensi harus sama dengan nama berkas lisensi Anda. Misalnya, jika Anda mengubah nama berkas lisensi menjadi "Aspose.PSD.lic.xml", Anda harus menggunakan nama lisensi ini untuk metode SetLicense.
### **Menerapkan lisensi menggunakan stream**
Juga mungkin untuk memuat lisensi dari stream seperti yang ditunjukkan di bawah ini.



{{< highlight java >}}



// Menginisialisasi sebuah instance lisensi dan menerapkan lisensi menggunakan stream

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);



{{< /highlight >}}
### **Memeriksa status lisensi**
Kelas Aspose.PSD.License memiliki properti IsLicensed yang akan mengembalikan true jika lisensi telah diatur dengan benar.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Lisensi diatur!");

}

{{< /highlight >}}
### **Menggunakan Sumber Daya Tersemat**
Cara praktis untuk memaket lisensi dengan aplikasi Anda dan memastikan tidak hilang, adalah dengan menyertakannya sebagai sumber daya tersemat ke salah satu perakitan yang memanggil Aspose.PSD. Untuk menyertakan berkas lisensi sebagai sumber daya tersemat:

1. Di Visual Studio .NET, klik menu **File** dan pilih **Add Existing Item**.
1. Sertakan berkas lisensi (ekstensi .lic) dalam proyek.
1. Pilih berkas dalam Penjelajah Solusi.
1. Di jendela Properti, atur **Tindakan Build** menjadi **Sumber Daya Tersemat**.

Tidak perlu memanggil metode GetExecutingAssembly atau GetManifestResourceStream dari System.Reflection.Assembly dalam Microsoft .NET Framework untuk mengakses lisensi tersemat. Sebaliknya, sematkan berkas sebagai sumber daya dalam proyek dan kemudian lewatkan nama berkas lisensi ke metode SetLicense. Kelas License secara otomatis menemukan berkas lisensi dalam sumber daya tersemat. Contoh di bawah menunjukkan bagaimana cara menyertakan lisensi sebagai sumber daya tersemat dan menerapkannya ke aplikasi Anda.



{{< highlight java >}}

 // Menginisialisasi kelas Lisensi

Aspose.PSD.License license = new Aspose.PSD.License();



// Lewatkan nama berkas lisensi yang dapat disematkan

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Memeriksa status lisensi**
Kelas Aspose.PSD.License memiliki properti IsLicensed yang akan mengembalikan true jika lisensi telah diatur dengan benar.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Lisensi diatur!");

}

{{< /highlight >}}

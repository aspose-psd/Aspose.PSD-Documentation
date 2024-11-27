---
title: Lisensi
type: dokumen
weight: 60
url: /id/java/lisensi/
---

## **Batasan Versi Evaluasi**
Anda dapat mengunduh versi evaluasi Aspose.PSD for Java dari [halaman unduh](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). Versi evaluasi menyediakan fitur yang sama dengan versi berlisensi penuh dari komponen tersebut dengan beberapa pembatasan. Ketika Anda membeli Aspose.PSD, pengaplikasian lisensi akan menghapus batasan apa pun dari versi evaluasi yang terpasang.

Versi evaluasi Aspose.PSD for Java menyediakan fungsionalitas produk secara penuh, dengan hanya dua pembatasan:

- **Watermark pada setiap gambar**: Setiap gambar yang Anda simpan, modifikasi, atau ekspor memiliki watermark bertuliskan "Hanya Evaluasi. Dibuat dengan Aspose.PSD. Hak Cipta 2018-2019 Aspose Pty Ltd.". Gambar-gambar kecil, di mana watermark penuh tidak muat, memiliki dua garis diagonal melintasi gambar tersebut.
- **Tidak ada dukungan untuk fungsionalitas utama menggambar**: Dalam mode evaluasi, piksel gambar tidak dapat dimuat atau disimpan ke gambar. Untuk menggambar gambar, gunakan fungsionalitas menggambar lanjutan. Pembatasan ini memengaruhi fungsionalitas yang bergantung pada fungsionalitas utama menggambar. Aspose.PSD for Java memungkinkan Anda mendaftarkan format file Anda sendiri. Namun, fitur ini bergantung pada fungsionalitas utama menggambar sehingga tidak masuk akal untuk menggunakannya dalam mode evaluasi karena Anda tidak dapat mengubah konten dari file-file tersebut.

{{% alert color="primary" %}}

Jika Anda ingin menguji Aspose.PSD for Java tanpa batasan evaluasi, mintalah lisensi sementara 30 hari. Silakan lihat [Cara Mendapatkan Lisensi Sementara?](https://purchase.aspose.com/temporary-license) untuk informasi lebih lanjut.

{{% /alert %}} 
## **Tentang File Lisensi**
Setelah Anda puas dengan evaluasi Aspose.PSD, Anda dapat membeli lisensi di [situs web Aspose](https://purchase.aspose.com/default.aspx). Kenali berbagai jenis langganan yang ditawarkan. Jika Anda memiliki pertanyaan, jangan ragu untuk menghubungi [tim penjualan Aspose](https://company.aspose.com/contact).

Setiap lisensi Aspose dilengkapi dengan langganan satu tahun untuk pembaruan perangkat lunak. Setelah tahun pertama, perbarui langganan Anda untuk terus mendapatkan fitur-fitur terbaru dan perbaikan. Dukungan teknis gratis dan tanpa batas disediakan baik kepada pengguna berlisensi maupun evaluasi melalui [Forum Dukungan](https://forum.aspose.com/).

Lisensi adalah file XML yang berisi detail seperti nama produk, jumlah pengembang yang dilisensikan, tanggal kadaluwarsa langganan, dan sebagainya. File ini ditandatangani digital, jadi jangan mengubahnya: bahkan menambahkan jeda baris tambahan secara tidak sengaja akan membuat file tersebut tidak valid.

Setelah membeli Aspose.PSD, Anda perlu mengaplikasikan lisensi sebelum membuat, mengedit, atau memanipulasi gambar. Jika Anda lupa mengaplikasikan lisensi, gambar output akan memiliki watermark evaluasi. 
Anda hanya perlu menetapkan lisensi sekali per aplikasi atau proses yang Anda kembangkan.
## **Menerapkan Lisensi**
Anda dapat mengunduh versi evaluasi **Aspose.PSD** untuk Java dari [halaman unduhnya](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/). Versi evaluasi menyediakan kemampuan yang sama persis dengan versi berlisensi dari produk. Selain itu, versi evaluasi hanya menjadi berlisensi saat Anda membeli lisensi dan menambahkan beberapa baris kode untuk menerapkan lisensi.

Setelah Anda puas dengan evaluasi **Aspose.PSD**, Anda dapat [membeli lisensi](http://www.aspose.com/Purchase/Components/Default.aspx) di situs web Aspose. Kenali berbagai jenis langganan yang ditawarkan. Jika Anda memiliki pertanyaan, jangan ragu untuk menghubungi tim penjualan Aspose.

Setiap lisensi Aspose membawa langganan satu tahun untuk pembaruan gratis ke versi atau perbaikan baru yang dirilis selama periode ini. Dukungan teknis gratis dan tanpa batas diberikan baik kepada pengguna berlisensi maupun evaluasi.

{{% alert color="primary" %}}

Jika Anda ingin menguji **Aspose.PSD** tanpa batasan versi evaluasi, mintalah lisensi sementara 30 hari. Silakan lihat [Cara Mendapatkan Lisensi Sementara?](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx) untuk informasi lebih lanjut.

{{% /alert %}} 
### **Menetapkan Lisensi**
Lisensi adalah file XML teks biasa yang berisi detail seperti nama produk, jumlah pengembang yang dilisensikan, tanggal kadaluwarsa langganan, dan sebagainya. File ini ditandatangani digital, jadi jangan mengubah file tersebut; bahkan penambahan jeda baris tambahan secara tidak sengaja ke file akan membuatnya tidak valid.

Anda perlu menetapkan lisensi sebelum memanfaatkan **Aspose.PSD** jika Anda ingin menghindari batasan evaluasinya. Anda hanya perlu menetapkan lisensi sekali per aplikasi atau proses.

Lisensi dapat dimuat dari aliran atau file di lokasi berikut:

1. Jalur eksplisit.
1. Folder yang berisi Aspose.PSD.jar.

Gunakan metode [License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License).setLicense untuk melisensikan komponen. Seringkali cara termudah untuk menetapkan lisensi adalah dengan meletakkan file lisensi di folder yang sama dengan Aspose.PSD.jar dan menentukan hanya nama file tanpa jalur seperti yang ditunjukkan dalam contoh berikut:
#### **Contoh 1**
Dalam contoh ini, **Aspose.PSD** akan mencoba menemukan file lisensi di folder yang berisi JAR aplikasi Anda.

**Java**

{{< highlight csharp >}}

com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **Contoh 2**
Menginisialisasi lisensi dari suatu aliran.

**Java**

{{< highlight csharp >}}

com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **Validasi Lisensi**
Dimungkinkan untuk memvalidasi apakah lisensi telah diatur dengan benar atau tidak. Kelas Lisensi memiliki isLicensed field yang akan mengembalikan true jika lisensi telah diatur dengan benar.

**Java**

{{< highlight csharp >}}

License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("Lisensi diatur!");

}

{{< /highlight >}}
## **Tempat Menetapkan Lisensi dalam Aplikasi Anda**
Di mana Anda menerapkan lisensi tergantung pada jenis aplikasi yang Anda kembangkan. Ikuti aturan sederhana berikut:

- Lisensi hanya perlu diatur sekali per domain aplikasi. Memanggil License.setLicense beberapa kali tidak merugikan tapi membuang-buang waktu pemrosesan.
- Terapkan lisensi sebelum memanggil kelas-kelas Aspose.PSD apa pun.
- **Aplikasi Java**: panggil License.SetLicense dalam kode startup.
- **Pustaka kelas**: panggil License.setLicense dari konstruktor statis dari kelas yang menggunakan Aspose.PSD. Konstruktor statis dieksekusi sebelum sebuah instance kelas Anda dibuat, memastikan bahwa lisensi Aspose.PSD diatur dengan benar.
## **Menggunakan Beberapa Produk Aspose**
Jika Anda menggunakan lebih dari satu produk Aspose dalam aplikasi Anda, misalnya Aspose.PSD dan Aspose.Cells, berikut adalah beberapa tips berguna.

- **Terapkan lisensi untuk masing-masing produk Aspose secara terpisah**. Meskipun Anda memiliki file lisensi tunggal untuk semua komponen, misalnya 'Aspose.Total.lic', Anda masih perlu memanggil License.setLicense secara terpisah untuk setiap produk Aspose dalam aplikasi Anda.
- **Gunakan nama kelas lisensi yang lengkap**. Setiap produk Aspose memiliki kelas Lisensi di namespace-nya. Misalnya, Aspose.PSD memiliki com.aspose.psd.license.License dan Aspose.Cells memiliki com.aspose.cells.License. Menggunakan nama kelas yang lengkap menghindari kebingungan tentang lisensi mana yang diterapkan ke produk mana.

---
title: Cara membuat pembangkit gambar mini YouTube secara programatik di Java
type: docs
weight: 10
url: /id/java/cara-membuat-pembangkit-gambar-mini-youtube-secara-programatik-di-java/
---

## **Pengantar**
Tujuan dokumen ini adalah untuk menunjukkan penggunaan API dari beberapa perangkat gabungan [Aspose.PSD untuk Java](https://products.aspose.com/psd/java) pada contoh dunia nyata. Dalam artikel ini, **program Java sederhana yang menghasilkan gambar mini YouTube** untuk saluran [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q) akan ditulis dan dijelaskan. Saluran ini dipilih dari dunia nyata karena gambar mini-nya cukup standar, dan mereka mengilustrasikan penggunaan beberapa perangkat gabungan populer dari Aspose.PSD untuk Java (misalnya efek [bayangan](/psd/id/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), pengisian gradien radial, menggambar teks dan bentuk):

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **Bagaimana cara kerjanya secara ringkas**
Sebuah program Java sederhana mengambil dua argumen sebagai input: sebuah keterangan dan sebuah gambar. Sebuah **dokumen Photoshop (PSD) dalam memori dihasilkan** dari input tersebut menggunakan Aspose.PSD untuk Java. Setelah itu, program **mengonversi dokumen dari PSD ke format file PNG** untuk mendapatkan gambar mini YouTube dengan ukuran 1280x720 pixel. Gambar output terlihat mirip dengan gambar berikut:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **Persyaratan teknis**
Teknologi-teknologi berikut diperlukan untuk berhasil menjalankan kode dari artikel ini:

- Java 6+
- [Aspose.PSD untuk Java](/psd/id/java/installation/) (terbaru)

## **Memulai**
Seperti yang telah disebutkan sebelumnya, program menggunakan PSD dalam memori untuk menghasilkan gambar mini. Jadi, mari **membuat dokumen PSD**, untuk memulai:

PsdImage psdImage = new PsdImage(1280, 720);

Jika Anda melihat lebih dekat pada gambar mini YouTube di atas, Anda mungkin perhatikan bahwa **terdiri dari beberapa komponen**:

1. sebuah gambar latar belakang (mask tercetak)
1. gradien radial psd (menyoroti area di sudut kanan atas)
1. logotipe dengan efek bayangan
1. keterangan dan gambaran sederhana (persegi biru)

Mari kita mendalami untuk melihat bagaimana mengimplementasikan masing-masing komponen ini menggunakan Aspose.PSD untuk Java pada bagian-bagian selanjutnya.

## **1. Menambahkan gambar latar belakang**
Urutan lapisan penting. Oleh karena itu, sebuah gambar latar belakang harus ditambahkan terlebih dahulu agar tidak tumpang tindih dengan lapisan lain. Perhatikan bahwa hanya [format file raster yang didukung](/psd/id/java/supported-file-formats/) saat ini.
### **1.1. Menambahkan gambar latar belakang ke lapisan Photoshop**
Untuk **menambahkan gambar raster ke PSD**, aliran input harus dilewatkan sebagai argumen selama konstruksi lapisan (lihat lebih banyak [contoh pengisian gambar raster](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}
```


1.2. Sesuaikan gambar latar belakang ke kanvas

Dua tindakan berikut (pengubahan ukuran, penempatan) berguna untuk kasus-kasus di mana **ukuran gambar berbeda dari ukuran kanvas**, meskipun gambar dalam artikel ini memiliki ukuran yang sama dengan kanvas (asumsikan tidak selalu seperti itu).

Pastikan gambar yang dimuat **sesuai dengan ukuran kanvas** (lihat lebih banyak [contoh pengubahan ukuran](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}
```

Setelah mengubah ukuran, posisi gambar berubah. Oleh karena itu, untuk **mereset posisi gambar**, pindahkan gambar yang diubah ukurannya ke sudut kiri atas:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}
```

## **2. Menambahkan gradien radial**
Ada **dua cara untuk menambahkan gradien radial**, menggunakan:

- efek tumpahan gradien pada lapisan yang ada (efek gradien yang terikat pada lapisan sekarang dan berlaku pada isinya)
- lapisan gradien pengisian baru (lapisan terpisah yang menyimpan konfigurasi gradien mandiri)

Cukup menggunakan efek tumpahan gradien untuk contoh ini. Namun, untuk membuat artikel ini lebih menarik dan berguna **lapisan gradien pengisian digunakan** karena semua efek lapisan berlaku dengan cara yang sama dan efek lapisan lain akan digunakan pada bagian berikutnya.
### **2.1. Menambahkan lapisan gradien pengisian radial**
Proses menambahkan lapisan gradien pengisian baru terdiri dari 2 langkah berikut:

\1. Perlu **deklarasikan pengaturan gradien pengisian** karena tidak ada yang sebelumnya. Konfigurasi minimum yang diperlukan terlihat seperti berikut (berarti tipe gradien, skala, titik warna dan transparansi diperlukan):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}
```

Konfigurasi di atas mendeklarasikan gradien radial yang transparan di pinggiran dan biru tua di tengah. Posisi gradien berada di tengah kanvas secara default.

Untuk membalik gradien pengisian dan sedikit bergeser ke sudut kanan atas gunakan properti opsional yang sesuai:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}
```

\2. Ketika konfigurasi selesai, tambahkan lapisan gradien pengisian bersama dengan pengaturannya ke dalam PSD:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}
```

## **Menambahkan logotipe dengan bayangan**
**Bayangan jatuh** adalah efek yang memungkinkan untuk menambah bayangan kustom sepanjang kontur objek (gambar, teks, dll.).
### **3.1. Menambahkan logotipe ke lapisan Photoshop**
Pendekatan yang sama seperti pada bagian 1.1. dapat digunakan untuk **menambahkan logotipe ke PSD**:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
```

### **3.2. Posisikan logotipe**
Gambar yang dimuat erat melekat pada sudut kiri atas secara default. Namun, beberapa **margin perlu ditambahkan** agar terlihat seperti gambar mini YouTube asli di saluran. Oleh karena itu, posisi gambar harus bergeser dari tepi lapisan:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
```

### **3.3. Menambahkan efek bayangan jatuh ke logotipe**
Logotipe dapat menjadi tidak terlihat jika digunakan gambar latar belakang yang terang. Oleh karena itu, disarankan untuk **menambahkan efek bayangan jatuh** ke logotipe melalui properti opsi blending (lihat lebih banyak [contoh bayangan](/psd/id/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}
```

Efek bayangan jatuh tidak memiliki properti yang diperlukan karena konfigurasi default (terlihat seperti milik Photoshop). Namun, bayangan di atas dimodifikasi untuk terlihat seperti batas tembus yang kabur di pinggiran.

## **4. Menambahkan gambaran teks dan bentuk**
### **3.1. Membuat lapisan grafis**
Menggambar tidak didukung oleh lapisan biasa secara langsung. Oleh karena itu, mesin grafis digunakan di samping lapisan untuk **memberikan API untuk menggambar** (lihat lebih banyak [contoh penggambaran](/psd/id/java/drawing-images-using-graphics/)):

```java
Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
```

### **3.2. Menggambar teks multi-baris**
Seorang pembaca yang ahli mungkin bertanya: mengapa tidak menggunakan lapisan teks untuk menambahkan teks? Nah, ada beberapa alasan: pengeditan teks tidak diperlukan dalam kasus ini karena PSD dihasilkan dari awal setiap kali; kustomisasi font tidak didukung oleh [API teks](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) saat ini (v20.6 pada saat penulisan).

Mudah untuk **menggambar teks dengan font yang disesuaikan** cukup instansiasi font yang diinginkan dan panggil metode yang sesuai dari mesin grafis. Namun, untuk membuat sebuah persegi panjang (lihat detailnya di bagian berikut) yang mengubah tingginya secara otomatis berdasarkan jumlah baris teks sedikit lebih sulit. Tinggi pasti dari semua baris harus dihitung terlebih dahulu:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}
```

Di mana 1,15 adalah tinggi lini, 3 adalah padding teks.

### **3.3. Menggambar sebuah persegi panjang**
Sebuah persegi panjang juga mudah digambar bahkan dengan kuas gradien (hanya atur area untuk digambar dan rentang warna). Ketika tinggi teks diketahui, ukuran dan posisi persegi panjang dihitung. Untuk **menggambar persegi panjang terisi** **di psd** (bukan hanya bingkai), panggil metode yang sesuai dari mesin grafis dengan semuanya itu:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}
```

` `Di mana 40, 15, 25 adalah indent.

## **Hasil**
Jadi, pembentukan gambar mini telah selesai. Oleh karena itu, saatnya untuk **mengekspor gambar mini ke format file raster** (misalnya, PNG) untuk distribusi lebih lanjut:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}
```

## **Kesimpulan**
Dalam artikel ini, kita telah membuat pembangkit gambar mini YouTube untuk saluran DW Documentary dan menjelaskan bagaimana menggunakan beberapa perangkat gabungan paling populer seperti efek bayangan, pengisian gradien radial, menggambar teks, dan bentuk.

## **Contoh Lengkap**
Anda dapat [mengunduh SDK Aspose.PSD](https://products.aspose.com/psd/net)

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
```
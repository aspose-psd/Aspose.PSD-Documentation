---
title: Instalasi
type: dokumen
weight: 40
url: /id/java/installation/
---

## **Menginstal Aspose.PSD untuk Java dari Repositori Maven**
Aspose memuat semua API Java di [repositori Maven](https://releases.aspose.com/java/repo/com/aspose/). Anda dapat dengan mudah menggunakan [Aspose.PSD untuk Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API langsung di Proyek Maven Anda dengan konfigurasi yang sederhana.
### **Tentukan Konfigurasi Repositori Maven**
Pertama, Anda perlu menentukan konfigurasi/lokasi Repositori Maven Aspose dalam pom.xml Maven Anda sebagai berikut:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Tentukan Ketergantungan API Aspose.PSD untuk Java**
Kemudian tentukan ketergantungan API Aspose.PSD untuk Java dalam pom.xml Anda sebagai berikut:

{{< highlight java >}}

 <dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-psd</artifactId>
        <version>24.2</version>
        <classifier>jdk16</classifier>
    </dependency>
</dependencies>

{{< /highlight >}}

Setelah mengikuti langkah-langkah di atas, ketergantungan Aspose.PSD untuk Java akan akhirnya ditentukan dalam Proyek Maven Anda.
## **Platform yang Didukung**
Aspose.PSD untuk Java mendukung platform pengembangan dan implementasi yang paling populer.

|**Fitur**|**Deskripsi**|
| :- | :- |
|Aplikasi Desktop|Aspose.PSD untuk Java dapat digunakan untuk mengembangkan aplikasi Desktop di MS Windows.|
|Aplikasi Web Perusahaan|Aspose.PSD untuk Java sepenuhnya mendukung aplikasi Web.|
|Linux/Unix|Aspose.PSD untuk Java adalah API yang platform-independen dan dapat berfungsi dalam lingkungan Linux dan Unix.|
## **Versi Java yang Didukung**
- JDK 1.6 atau lebih tinggi

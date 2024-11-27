---
title: Peningkatan Kinerja Aspose.PSD dengan Penggunaan Cache yang Dapat Disesuaikan
type: docs
weight: 30
url: /id/java/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Meningkatkan Kinerja dengan Cache yang Dapat Disesuaikan**
Aspose.PSD menggunakan caching untuk penyimpanan data sementara. Mekanisme ini mudah digunakan, dapat disesuaikan, dan transparan. Ini memastikan tidak ada masalah kinerja selama pemrosesan gambar. Artikel ini menjelaskan bagaimana cara menyesuaikan cache dengan API Aspose.PSD untuk Java.
### **Menyesuaikan Cache**
Ketika suatu proses memerlukan penyimpanan data sementara, penyimpanan ini dialokasikan di dalam cache. Cache dapat berupa ruang di memori atau di disk dan diatur oleh pengguna. Ketika data sementara tidak lagi diperlukan, ruangnya akan dilepas. Statistik ruang yang dialokasikan dapat diperiksa kapan saja. Bagaimana Aspose.PSD mengalokasikan dan menggunakan cache dapat disesuaikan. Bagian ini menjelaskan berbagai pengaturan dan defaultnya, serta potongan kode di bawah ini menunjukkan bagaimana cara menggunakannya.
### **Menentukan Tempat Penyimpanan Cache**
Untuk menyesuaikan bagaimana ruang cache dialokasikan, atur properti CacheType. Secara default, cache dialokasikan di memori dan ketika tidak ada lagi ruang yang tersedia di memori, ruangnya dialokasikan di disk. Perilaku ini ditangkap oleh mode Auto. Mode Auto fleksibel dan memaksimalkan kinerja. Terdapat juga mode lainnya:

- mode CacheOnDiskOnly: dialokasikan hanya di disk.
- mode CacheInMemoryOnly: dialokasikan hanya di memori.

Memilih mode CacheOnDiskOnly mungkin mengakibatkan kinerja yang buruk.
### **Menentukan Ukuran Cache**
Atur ruang maksimum (dalam byte) yang dapat dialokasikan di disk atau memori dengan mengatur properti MaxDiskSpaceForCache dan MaxMemoryForCache secara berturut-turut. Secara default, kedua nilai tersebut diatur ke 0, yang berarti tidak ada batasan atasnya.
### **Mengendalikan Realokasi Cache**
Jika tidak cukup ruang yang tersedia di memori (seperti yang ditentukan oleh properti MaxMemoryForCache) saat cache baru dialokasikan, cache tersebut dialokasikan ke disk. Jika tidak cukup ruang di disk, maka akan dilemparkan sebuah pengecualian. Proses alokasi cache berpindah dari memori ke disk tetapi tidak sebaliknya. Properti ExactReallocateOnly digunakan untuk mengendalikan realokasi memori. Realokasi kemungkinan besar terjadi untuk cache yang sudah dialokasikan sebelumnya. Hal ini dapat terjadi ketika sistem menyadari bahwa ruang yang dialokasikan tidak akan mencukupi. Jika ExactReallocateOnly diatur ke nilai default, False, ruang tersebut dialokasikan kembali ke medium yang sama. Ketika diatur ke True, realokasi tidak dapat melebihi ruang maksimum yang ditentukan. Dalam hal ini, cache di dalam memori yang sudah dialokasikan (yang membutuhkan realokasi) akan dibebaskan dan ruang tambahan dialokasikan di disk.
### **Contoh Program**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}

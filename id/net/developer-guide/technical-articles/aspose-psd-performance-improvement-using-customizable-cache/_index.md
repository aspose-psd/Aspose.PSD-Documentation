---
title: Meningkatkan Kinerja Aspose.PSD dengan Cache yang Dapat Disesuaikan
type: docs
weight: 20
url: /id/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Meningkatkan Kinerja dengan Cache yang Dapat Disesuaikan**
[Aspose.PSD](https://products.aspose.com/psd/family) menggunakan caching untuk penyimpanan data sementara. Mekanisme ini mudah digunakan, dapat disesuaikan, dan transparan. Hal ini memastikan tidak ada masalah kinerja selama pemrosesan gambar. Artikel ini menjelaskan bagaimana menyesuaikan cache dengan Aspose.PSD API untuk .NET.
### **Menyesuaikan Cache**
Ketika sebuah proses memerlukan penyimpanan data sementara, penyimpanan ini dialokasikan dalam cache. Cache dapat berada di memori atau di disk dan diatur oleh pengguna. Ketika data sementara tidak lagi diperlukan, ruangnya dibebaskan. Statistik ruang yang dialokasikan dapat diperiksa kapan saja. Bagaimana Aspose.PSD mengalokasikan dan menggunakan cache dapat disesuaikan. Bagian ini menjelaskan berbagai pengaturan dan nilai defaultnya, dan potongan kode di bawah ini menunjukkan bagaimana cara menggunakannya.
### **Menentukan Lokasi Alokasi Cache**
Untuk menyesuaikan bagaimana ruang cache dialokasikan, atur properti [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Secara default, cache dialokasikan di memori dan ketika tidak ada lagi ruang yang tersedia di memori, dialokasikan ke disk. Perilaku ini ditangkap oleh mode Auto. Mode Auto fleksibel dan memaksimalkan kinerja. Ada juga mode lain:

- mode CacheOnDiskOnly: alokasi hanya ke disk.
- mode CacheInMemoryOnly: alokasi hanya ke memori.

Memilih mode CacheOnDiskOnly dapat mengakibatkan kinerja yang buruk.
### **Menentukan Ukuran Cache**
Atur ruang maksimum (dalam byte) yang dapat dialokasikan di disk atau memori dengan mengatur properti [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) dan [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache) secara berturut-turut. Secara default, kedua nilai tersebut diatur ke 0, yang berarti tidak ada batasan atas.
### **Mengontrol Penyalahgunaan Cache**
Jika tidak cukup ruang yang tersedia di memori (seperti yang ditentukan oleh properti MaxMemoryForCache) ketika cache baru dialokasikan, cache dialokasikan ke disk. Jika tidak ada cukup ruang di disk, akan muncul pengecualian. Proses alokasi cache berpindah dari memori ke disk tetapi tidak sebaliknya. Properti [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) digunakan untuk mengontrol realokasi memori. Realokasi kemungkinan besar terjadi untuk cache yang telah dialokasikan sebelumnya. Ini bisa terjadi saat sistem menemukan bahwa ruang yang dialokasikan tidak akan mencukupi. Jika ExactReallocateOnly diatur ke nilai default, False, ruang dialokasikan kembali ke media yang sama. Ketika diatur ke True, realokasi tidak dapat melebihi ruang maksimum yang ditentukan. Dalam kasus ini, cache yang telah dialokasikan di memori (yang memerlukan realokasi) dibebaskan dan ruang tambahan dialokasikan di disk.
### **Contoh Program**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}

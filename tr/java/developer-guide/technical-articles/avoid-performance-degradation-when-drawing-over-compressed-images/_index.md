---
title: Sıkıştırılmış Görüntüler Üzerine Çizim Yaparken Performans Bozulmasını Önleme
type: docs
weight: 40
url: /tr/java/sikistirilmis-goruntuler-uzerine-cizim-yaparken-performans-bozulmasini-onleme/
---

## **Sıkıştırılmış Görüntüler Üzerine Çizim Yaparken Performans Bozulmasını Önleme**
Zaman zaman sıkıştırılmış bir görüntü üzerinde son derece yoğun grafik işlemleri gerçekleştirmek isteyebilirsiniz. Aspose.PSD'nin görüntüleri canlı olarak sıkıştırmasını ve açmasını gerektiren durumlarda performans bozulması yaşanabilir. Sıkıştırılmış görüntüler üzerine çizim yapmak da performans cezası getirebilir.
### **Çözüm**
Performans bozulmasını önlemek için grafik işlemleri gerçekleştirmek öncesinde görüntüyü sıkıştırılmamış veya ham bir formata dönüştürmenizi öneririz.
### **Dosya Yolu Kullanma**
Aşağıdaki örnekte, bir PSD görüntüsü ham formata (sıkıştırma olmadan) dönüştürülür ve diske kaydedilir. Grafik işlemleri gerçekleştirilmeden önce sıkıştırılmamış görüntü daha sonra tekrar yüklenir. Aynı teknik BMP ve GIF dosyaları için de geçerlidir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **Akış Nesnesi Kullanma**
Aşağıdaki kod parçacığı, PSD görüntüsünün ham formata (sıkıştırma olmadan) dönüştürülerek ve diskte kaydedilerek Akış kullanılarak nasıl yapıldığını göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}

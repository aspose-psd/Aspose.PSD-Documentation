---
title: Sıkıştırılmış Görüntüler Üzerine Çizim Yaparken Performans Bozulmasını Önleme
type: docs
weight: 10
url: /tr/net/sikistirilmis-goruntuler-uzerine-cizim-yaparken-performans-bozulmasini-onleme/
---

## **Sıkıştırılmış Görüntüler Üzerine Çizim Yaparken Performans Bozulmasını Önleme**
Bir sıkıştırılmış görüntü üzerinde son derece yoğun grafik işlemleri gerçekleştirmek istediğiniz zamanlar olabilir. Aspose.PSD'nin görüntüleri sıkıştırıp açması gerekli olduğunda performans bozulması meydana gelebilir. Sıkıştırılmış görüntüler üzerine çizim yapmak da performans cezası getirebilir.
### **Çözüm**
Performans bozulmasını önlemek için, grafik işlemleri yapmadan önce görüntüyü sıkıştırılmamış, veya ham, formata dönüştürmenizi öneririz.
### **Dosya Yolu Kullanarak**
Aşağıdaki örnekte, bir PSD görüntüsü ham biçime (sıkıştırma olmadan) dönüştürülür ve diske kaydedilir. Grafik işlemleri yapmadan önce sıkıştırılmamış görüntü geri yüklenir. BMP ve GIF dosyaları için aynı teknik uygulanır.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **Akış Nesnesi Kullanarak**
Aşağıdaki kod parçası, bir PSD görüntüsünün ham biçime (sıkıştırma olmadan) dönüştürülüp MemoryStream kullanılarak diske kaydedildiğini gösterir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}


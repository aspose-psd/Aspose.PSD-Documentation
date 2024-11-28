---
title: Büyük Resim Desteği
type: docs
weight: 60
url: /tr/java/buyuk-resim-destegi/
---

## **Büyük Resim Desteği**
Standart Java kütüphanesinin işleyebileceği resim boyutlarına ilişkin bazı kısıtlamalar olduğundan büyük resim desteği için yeni bir mekanizma tanıttık. Yeni yaklaşım kısıtlamaları aşar ancak veri boyutu kısıtlamaları nedeniyle oluşturma ve yükleme için desteklenen maksimum boyutlar 2.147.483.647 x 2.147.483.647 pikseldir.
### **Büyük Resimlerle Çalışma**
Aspose.PSD performansı ve büyük resimler için destek iyileştirilmiştir. Yüzlerce megabayt boyutunda olan resimler artık bir sorun oluşturmuyor, böylece bu resimler üzerinde oluşturma, yükleme ve çizim yapabilirsiniz. Bununla birlikte, kısmi işleme ve OutOfMemoryException istisnanın ele alınması nedeniyle performans, çok büyük resimlerde çok düşük olabilir. Bu, Aspose.PSD'nin işlem yapmak için daha küçük bir veri miktarını yeniden tahsis etmeye çalışmasındandır ve her yeniden tahsis adımı çok maliyetlidir. Yeni mimarinin faydaları açıktır:

- Resim boyutu için herhangi bir sınırlama bulunmamaktadır.
- PC'nizde mevcut bellekle sınırlı olmazsınız.

Yavaş işlem yaşarsanız, tüm piksellerinizi belleğe sığdırmak için toplam RAM miktarını artırmanız önerilir. Sığdırmazsanız, işlem yapmak hala mümkündür ancak daha yavaş olacaktır. Yaklaşım şu şekildedir:

- Belirtilen dikdörtgenle yüklenen pikselleri almak için LoadPartialPixels yöntemini çağırın ve belirtilen pikselleri almak için bir delege belirtin.

Aspose.PSD, tüm dikdörtgeni yüklemeye çalışır.

- Tüm pikselleri sığdıracak kadar bellek varsa, tüm pikseller sadece çağrı sahibine geri döndürülür.
- Yeterli bellek yoksa, çağrı sahibi belirtilen dikdörtgenin içinden bir piksel alt kümesini alır. Bu pikseller işlendikten sonra, çağrı sahibi bir sonraki dikdörtgeni alır. İşlem, tüm dikdörtgen işlenene kadar devam eder.

Aspose.PSD, mümkün olduğunca çok satır çıkarmaya çalışır. Eğer bir satır pikseli sığdırmak için yeterli bellek yoksa, bir satır parçalara ayrılır ve yüksekliği 1 olan dikdörtgenlere uygun hale getirilir. Ayrıca büyük resimler üzerine çizebilirsiniz. Çizim süreci, istenen tüm dikdörtgene etki etmeye çalışır. Yeterli bellek yoksa, çizim tüm alan çizilecek şekline kadar kısmi dikdörtgenlerde gerçekleştirilir. Ayrıca, Aspose.PSD büyük resimleri kaydetme ve dışa aktarma işlemlerini destekler. Kaynak resmi diske kaydedin veya başka bir dosya biçimine dışa aktarın. Kaydetme veya dışa aktarma işlemi gerekirse kısmi dikdörtgenler kullanılarak gerçekleştirilir.
### **Desteklenen Görüntü Biçimleri**
Büyük resim işleme için desteklenen aşağıdaki biçimler:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

Yukarıdaki biçimler, resim boyutundan bağımsız olarak oluşturma, değiştirme, çizim işlemleri uygulama, diske kaydetme veya dışa aktarma yoluyla güvenli bir şekilde işlenebilir.

. 

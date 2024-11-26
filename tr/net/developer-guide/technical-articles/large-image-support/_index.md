---
title: Büyük Resim Desteği
type: docs
weight: 40
url: /tr/net/buyuk-resim-destegi/
---

## **Büyük Resim Desteği**
Standart .NET kütüphanesinin işleyebileceği resim boyutlarına yönelik bazı sınırlamalar bulunduğundan, büyük resimler için destek sağlamak amacıyla yeni bir mekanizma tanıttık. Yeni yaklaşım, sınırlamaları aşarken, veri boyutu sınırlamaları nedeniyle oluşturma ve yükleme için desteklenen maksimum boyutlar 2.147.483.647 x 2.147.483.647 pikseldir.
### **Büyük Resimlerle Çalışma**
Aspose.PSD, büyük resimler için performansı ve desteği artırmıştır. Yüzlerce megabayt boyutundaki resimler artık bir problem oluşturmamakta, böylece bu resimler üzerine oluşturma, yükleme ve çizim yapabilirsiniz. Ancak, kısmi işleme ve OutOfMemoryException istisnalarını işleme yeteneğinden dolayı, performans çok büyük resimlerde çok düşük olabilir. Bu, Aspose.PSD'nin işleme için daha küçük bir veri miktarını yeniden ayırmaya çalışmasından kaynaklanmaktadır ve her yeniden tahsis adımı çok maliyetlidir. Yeni mimarinin faydaları açıktır:

- Resim boyutu için herhangi bir kısıtlama bulunmamaktadır.
- PC'nizdeki mevcut bellekle sınırlı kalmazsınız.

Eğer yavaş işleme deneyimlerseniz, tüm piksellerinizi belleğe sığdırmak için toplam RAM miktarını arttırmanız önerilir. Eğer yapmazsanız, işlem yapmak hala mümkündür fakat daha yavaş olacaktır. Yaklaşım şöyledir:

- İstenen dikdörtgenle [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) yöntemini çağırın ve yüklenen belirtilen pikselleri almak için delegeyi belirleyin.

Aspose.PSD tüm dikdörtgeni yüklemeye çalışır.

- Eğer tüm pikselleri sığdıracak kadar belleğiniz varsa, tüm pikseller sadece çağıran kişiye geri döner.
- Eğer yeterli belleğiniz yoksa, çağrıyı yapan, belirtilen dikdörtgenin içinden piksellerin bir alt kümesini alır. Bu pikseller işlendikten sonra, çağrıyı yapan sonraki dikdörtgeni alır. İşlem, tüm dikdörtgen işlenene kadar devam eder.

Aspose.PSD, mümkün olduğunda mümkün olan kadar çok satırı çıkarmaya çalışır. Eğer tek bir satır pikseli sığdırmak için yeterli belleğiniz yoksa, bir satır, 1 yüksekliğe sahip dikdörtgenlere uyumlu şekilde bölünür. Ayrıca büyük resimlere çizim yapabilirsiniz. Çizim işlemi, tüm istenen dikdörtgeni etkilemeye çalışır. Eğer yeterli belleğiniz yoksa, çizim, tüm alan çizilene kadar kısmi dikdörtgenlerde gerçekleştirilir. Ek olarak, Aspose.PSD büyük resimlerin kaydedilmesini ve dışa aktarılmasını da destekler. Kaynak resmi diske kaydedin veya başka bir dosya biçimine dışa aktarın. Kaydetme veya dışa aktarma işlemi gerektiğinde kısmi dikdörtgenler kullanılarak gerçekleştirilir.
### **Desteklenen Resim Biçimleri**
Büyük resim işleme için aşağıdaki biçimler desteklenmektedir:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Yukarıdaki biçimler, resim boyutundan bağımsız olarak oluşturma, değiştirme, çizim işlemleri uygulama, diske kaydetme veya dışa aktarma işlemlerinden güvenle işlenebilir.

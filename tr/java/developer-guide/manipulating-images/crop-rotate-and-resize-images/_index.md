---
title: Görüntüleri Kırpma, Döndürme ve Yeniden Boyutlandırma
type: docs
weight: 40
url: /tr/java/goruntuleri-kirp-dondur-ve-yeniden-boyutlandir/
---

## **Görüntüleri Kırpma**
Görüntü kırpma genellikle bir görüntünün dış kısımlarının kaldırılması olarak tanımlanır ve çerçeveyi iyileştirmeye yardımcı olur. Ayrıca, belirli bir bölgeye odaklanmayı artırmak amacıyla görüntünün bir bölümünün kesilmesi için de kullanılabilir. Aspose.PSD API, görüntü kırpma için iki farklı yaklaşımı destekler: kaydırma ve dikdörtgen ile.
### **Kaydırarak Kırpma**
RasterImage sınıfı, sol, sağ, üst ve altı belirten 4 tamsayı değerini kabul eden Crop yönteminin aşırı yüklü bir sürümünü sağlar. Bu dört değere dayanarak, Crop yöntemi görüntü sınırlarını görüntü merkezine doğru taşırken dış kısmı atar. Aşağıdaki kod parçacığı, bir görüntüyü nasıl kaydırarak kırparı göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-CizimVeFormatlamaGoruntuler-KaydirmaylaKesme-KaydirmaylaKesme.java" >}}
### **Dikdörtgen ile Kırpma**
RasterImage sınıfı, dikdörtgen sınıfının bir örneğini kabul eden Crop yönteminin başka bir aşırı yüklü sürümünü sağlar. Dikdörtgen nesnesine istenen sınırları sağlayarak herhangi bir görüntü bölümünü kesebilirsiniz. Aşağıdaki kod parçacığı, bir görüntüyü Dikdörtgen ile nasıl kırparını göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-CizimVeFormatlamaGoruntuler-DikdortgenileKesme-DikdortgenileKesme.java" >}}
## **Görüntüyü Döndürme ve Yansıma**
Aspose.PSD for Java, basit işlemleri gerçekleştirmek için kullanımı kolay bir kütüphane olduğu için karmaşık operasyonlar yapmak için basit yöntemler sağlar. Örneğin, bir uygulamanın bir görüntüyü döndürmesi gerekiyorsa Aspose.PSD for Java, uygulamanın görüntüyü döndürmesini gerektiren RotateFlip yöntemini temel Image sınıfı için sağlamıştır. Görüntü formatından bağımsız olarak, kitaplık belirli bir Döndürme ve Yansıma prosedürünü gerçekleştirebilir.
### **Görüntüyü Döndürme**
Image.RotateFlip yöntemi görüntüyü 90/180/270 derece döndürmek ve yatay veya dikey olarak çevirmek için kullanılabilir. Image.RotateFlip yöntemi, görüntüye uygulanacak dönme ve yansıma türünü belirten RotateFlipType parametresini kabul eder. Döndürme ve Yansıma işlemlerini gerçekleştirmek için aşağıdaki adımlar kadar basittir,

1. Image sınıfı tarafından sağlanan Yükle fabrika yöntemini kullanarak bir görüntü yükleyin.
1. Uygun RotateFlipType belirtilerek Image.RotateFlip yöntemini çağırın.
1. Sonuçları kaydedin.

Aşağıdaki kod örneği, bir Görüntünün RotateFlip özelliğini ve RotateFlipType numaralandırmasını ayarlamanın nasıl yapıldığını göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-CizimVeFormatlamaGoruntuler-GoruntuyuDondurme-GoruntuyuDondurme.java" >}}
## **Belirli Bir Açıda Görüntü Döndürme**
Aspose.PSD for Java API, görüntüyü belirli bir açıda döndürmek isteyen kullanıcılarını kolaylaştırmak için RasterImage.Rotate yöntemini sunar. RasterImage.RotateFlip yönteminin aksine, RasterImage.Rotate yöntemi üç parametre kabul eder:

1. Döndürme açısı: Görüntünün döndürülmesi gereken açıyı belirten bir float tipi parametre. Pozitif bir değer görüntüyü saat yönünde, negatif bir değer ise saat yönünün tersine döndürür.
1. Orantılı yeniden boyutlandırma: Bir Boolean tipi parametre, görüntü boyutunun döndürülen dikdörtgenin (köşe noktaları) projeksiyonlarına göre değişip değişmeyeceğini belirtir. false olarak ayarlanırsa, görüntü boyutları dokunulmaz ve sadece iç görüntü içeriği döndürülür.
1. Arka plan rengi: Döndürülen görüntünün arka planına doldurulacak rengi belirten Bir Renk tipi parametre.

Aşağıdaki kod parçacığı, RasterImage.Rotate yönteminin kullanımını göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-CizimVeFormatlamaGoruntuler-BelirliBirAcidaGoruntuDondurme-BelirliBirAcidaGoruntuDondurme.java" >}}
## **Görüntüleri Yeniden Boyutlandırma**
Bu makale, bir görüntüde Yeniden Boyutlandırma işlemini gerçekleştirmek için Aspose.PSD for Java'nın kullanımını göstermektedir. Aspose.PSD API'leri, bu amaca ulaşmak için verimli ve kullanımı kolay yöntemler sunmuştur. Aspose.PSD for Java, mevcut görüntüleri dinamik olarak yeniden boyutlandırmak için Image sınıfı için Resize yöntemini sunmuştur. Uygulama gereksinimlerine uygun iki aşırı yüklemesi Resize yöntemi bulunmaktadır.
### **Basit Yeniden Boyutlandırma**
Yeniden Boyutlandırma işlemini gerçekleştirmek için aşağıdaki adımları izleyebilirsiniz:

1. Image sınıfı tarafından sağlanan Yükle fabrika yöntemini kullanarak bir görüntü yükleyin.
1. Yeni Yükseklik ve Genişlik belirterek Image.Resize yöntemini çağırın.
1. Sonuçları kaydedin.

Aşağıdaki kod örneği, bir görüntüyü nasıl Yeniden Boyutlandıracağınızı göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-CizimVeFormatlamaGoruntuler-BasitYenidenBoyutlandirma-BasitYenidenBoyutlandirma.java" >}}
### **ResizeType Numaralandırmasıyla Yeniden Boyutlandırma**
Aspose.PSD API, arzu edilen sonuçlara ulaşmak için Image.Resize ile kullanılabilecek ResizeType numaralandırmasını sunmuştur. Aşağıdaki kod parçacığı, ResizeType numaralandırmasının nasıl kullanıldığını göstermektedir, ResizeType numaralandırmasının üyelerinin ayrıntıları bu sayfanın altında bulunabilir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-CizimVeFormatlamaGoruntuler-ResizeTypeNumaralandirmasiylaYenidenBoyutlandirma-ResizeTypeNumaralandirmasiylaYenidenBoyutlandirma.java" >}}



Yeniden boyutlandırma uygulandığında kaliteli sonuç almak istiyorsanız, her zaman Kalite sonuçlarını çıkarmak için ResizeType.LanczosResample kullanmanızı öneririz, ancak ResizeType.NearestNeighbourResample'dan daha yavaş çalışabilir. Diğer yandan, ResizeType.NearestNeighbourResample algoritması özellikle hızlı yeniden boyutlandırma için kullanılırken görüntü kalitesinden ödün verilir. Bu yöntem, gerçek zamanlı küçük resim oluşturma veya performans gerektiren benzer işlemler için yararlı olabilir.
## **Görüntüyü Orantılı Olarak Yeniden Boyutlandırma**
Görüntüleri Yeniden Boyutlandırmak için yeni yükseklik ve genişlik değerlerini Image.Resize yöntemine parametre olarak geçerek yeniden boyutlandırabilirsiniz, ancak bu durumda en-boy oranını kendiniz hesaplamanız gerekir. Bu, bir görüntünün genişliği veya yüksekliği değiştirildiğinde, görüntünün yeni boyutunu doldurmak için ölçeklenmesine veya küçültülmesine neden olur. Bir görüntünün genişliği ve yüksekliği değişikliklere orantısız ise, bu gerilmiş ve bozulmuş sonuca yol açabilir. Bu makale, Aspose.PSD for Java API'sinin kullanımını göstererek görüntüleri yeniden boyutlandırmak için yeni yükseklik veya genişlik geçirilerek diğer oransal değeri otomatik olarak hesaplamasına olanak tanır.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-CizimVeFormatlamaGoruntuler-OrantiliOlarakYenidenBoyutlandirma-OrantiliOlarakYenidenBoyutlandirma.java" >}}
### **ResizeType Numaralandırması**
ResizeType, seçilen filtreye dayanarak görüntüde gerçekleştirilecek yeniden boyutlandırma türünü belirler.

ResizeType Numaralandırması Üyeleri

|**Üye Adı**|**Değer**|**Açıklama**|
| :- |  :- | :- |
|LeftTopToLeftTop|0|Yeni görüntünün sol üst noktası, orijinal görüntünün sol üst noktasıyla çakışacaktır. Gerekirse kırpılacaktır.|
|RightTopToRightTop|1|Yeni görüntünün sağ üst noktası, orijinal görüntünün sağ üst noktasıyla çakışacaktır. Gerekirse kırpılacaktır.|
|RightBottomToRightBottom|2|Yeni görüntünün sağ alt noktası, orijinal görüntünün sağ alt noktasıyla çakışacaktır. Gerekirse kırpılacaktır.|
|LeftBottomToLeftBottom|3|Yeni görüntünün sol alt noktası, orijinal görüntünün sol alt noktasıyla çakışacaktır. Gerekirse kırpılacaktır.|
|CenterToCenter|4|Yeni görüntünün ortası, orijinal görüntünün ortasıyla çakışacaktır. Gerekirse kırpılacaktır.|
|LanczosResample|5|7x7 maskesi kullanan Lanczos algoritması kullanarak yeniden örnekleyin.|
|NearestNeighbourResample|6|En yakın komşu algoritmasını kullanarak yeniden örnekleyin.|

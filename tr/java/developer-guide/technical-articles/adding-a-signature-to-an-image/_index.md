---
title: Bir Görüntüye İmza Ekleme
type: docs
weight: 10
url: /tr/java/bir-goruntuye-imza-ekleme/
---

## **İmza Ekleme**


Bir görüntüye imza eklemek bazen görüntülerin taklit edilmesini önlemek için dijital olarak imzalanmasını gerektirebilir. Başka bir düşünce ise görüntünün daha çok bir galeride gösteriliyormuş gibi işlenmesidir. Hangi sebep olursa olsun, Aspose.PSD API'leri, açıklanan en basit mekanizmayı kullanarak bir görüntüye imza ekleme özelliği sağlar. Lütfen dikkat edin, bu örnek, orijinal görüntünün üzerine imzalı başka bir görüntü çizmek için Graphics sınıfını kullanır. İşlemi göstermek için, bir PSD görüntüsünü diskin üzerinden yükleyeceğiz ve Graphics sınıfının DrawImage yöntemini kullanarak orijinal görüntünün üzerine imza olacak başka bir görüntü çizeceğiz. Sonucu PngOptions sınıfını kullanarak PNG formatında kaydedeceğiz. Aşağıdaki, bir görüntüye imza eklemenin nasıl yapıldığını gösteren bir kod örneği bulunmaktadır. Örnek kaynak kodu takip etmesi kolay olması için bölümlere ayrılmıştır. Adım adım, örnek aşağıdakileri nasıl yapılacağını gösterir:

- Birincil ve ikincil (imza) görüntüleri yükleme.
- Bir Grafik nesnesi oluşturma ve başlatma.
- Grafik sınıfının DrawImage yöntemini kullanarak görüntü çizme.
- Sonucu PNG formatında kaydetme.
### **Program Örnekleri**
#### **Görüntüleri Yükleme**
İlk olarak, Diskten örnek görüntüleri yüklemek için Image sınıfından örnekler oluşturun.
#### **Grafik Nesnesi Oluşturma ve Başlatma**
Görüntüleri yükledikten sonra, bir Grafik sınıfı nesnesi oluşturun ve başlatın, bu sırada birincil görüntünün nesnesini kullanın.
#### **İkincil Görüntüyü Birincil Görüntünün Üzerine Çizme**
Daha sonra, ikincil görüntüyü birincil görüntünün üzerine eklemek için Graphics sınıfının DrawImage yöntemini kullanın. DrawImage yönteminin bir Image nesnesini ilk parametre olarak kabul eden, diğer tüm parametrelerin görüntünün nerede çizileceğine karşılık geldiği çeşitli aşırı yüklemeleri vardır. Gösterim amaçlı olarak, aşağıdaki kod, DrawImage'ın bir Point nesnesini ikinci parametre olarak kabul eden aşırı yüklemesini kullanır ve imzayı birincil görüntünün sağ alt köşesine çizmeye çalışır.
#### **Görüntünün Kaydedilmesi**
Son olarak, PngOptions sınıfını kullanarak görüntüyü yerel diske PNG dosyası olarak kaydedin.
#### **Tam Kaynak**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-DrawingImages-GoruntuyeImzaEkleme-GoruntuyeImzaEkleme.java" >}}

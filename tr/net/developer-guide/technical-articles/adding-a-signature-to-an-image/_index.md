---
title: Bir Görüntüye İmza Ekleme
type: docs
weight: 70
url: /tr/net/bir-goruntuye-imza-ekleme/
---

## **İmza Ekleme**

Bir görüntüye imza eklemek bazen görüntülerin sahte üretimini önlemek amacıyla dijital olarak imzalanması gerekebilir. Başka bir düşünce ise, görüntünün bir galeride sergileniyormuş gibi daha özel bir hale getirilmesidir. Her ne sebep olursa olsun, Aspose.PSD API'leri, aşağıda açıklanan en basit mekanizmayı kullanarak bir görüntüye imza eklemeyi sağlar. Lütfen dikkat edin, bu örnek, orijinal görüntünün yüzeyine imza eklemek için [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfını kullanmaktadır. İşlemi göstermek için diskten bir PSD görüntü yükleyecek ve Graphics sınıfının [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) yöntemini kullanarak orijinal görüntünün yüzeyine imza olarak başka bir görüntü çizeceğiz. Sonuç görüntüyü [PngOptions](https://reference.aspose.com/psd/net/aspose.psd/imageoptions/pngoptions) sınıfını kullanarak PNG biçiminde kaydedeceğiz. Aşağıda, bir görüntüye imza eklemeyi gösteren bir kod örneği bulunmaktadır. Örnek kaynak kodu takip etmesi kolay olacak şekilde parçalara ayrılmıştır. Adım adım, örnek şunları nasıl gösterir:

- Birincil ve ikincil (imza) görüntüleri yükleme.
- Bir Grafik nesnesi oluşturma ve başlatma.
- Görüntüyü Graphics sınıfı DrawImage yöntemi kullanarak çizme.
- Sonucu PNG biçiminde kaydetme.

### **Program Örnekleri**
#### **Görüntüleri Yükleme**
Öncelikle, örnek görüntüleri diskten yüklemek için Image sınıfının örneklerini oluşturun.
#### **Grafik Nesnesi Oluşturma ve Başlatma**
Görüntüleri yükledikten sonra, bir Graphics sınıfı nesnesi oluşturun ve başlatın, bu sırada birincil görüntünün nesnesini kullanın.
#### **İkincil Görüntüyü Birincil Görüntüye Çizme**
Sonrasında, Graphics sınıfı DrawImage yöntemini kullanarak ikincil görüntüyü birincil görüntüye ekleyin. DrawImage yönteminin birincil parametre olarak bir Image nesnesini kabul eden ve diğer tüm parametrelerin nerede görüntülenmesi gerektiğiyle ilgili olduğu çeşitli aşırı yüklemeleri bulunmaktadır. Gösterim amaçlı olarak, aşağıdaki kod, bir resim nesnesini ikinci parametre olarak kabul eden DrawImage'in yüklemeli sürümünü kullanarak imzayı birincil görüntünün sağ alt köşesine çizmeye çalışmaktadır.
#### **Görüntüyü Kaydetme**
Son olarak, PngOptions sınıfını kullanarak görüntüyü PNG dosyası olarak yerel diske kaydedin.
#### **Tam Kaynak**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-CizimGoruntuleri-GoruntuyeImzaEkleme-GoruntuyeImzaEkleme.cs" >}}

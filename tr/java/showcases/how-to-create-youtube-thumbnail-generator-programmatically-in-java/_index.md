---
title: Java İle YouTube Önbellek Oluşturucu Oluşturma
type: docs
weight: 10
url: /tr/java/java-ile-youtube-onbellek-olusturucu-programatik-olarak-nasil-olusturulur/
---

## **Giriş**
Bu belgenin amacı, [Aspose.PSD for Java](https://products.aspose.com/psd/java) içindeki bazı bileşik araçların API kullanımını gerçek bir örnek üzerinde göstermektir. Bu makalede, [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q) kanalı için **YouTube on bellek oluşturan basit bir Java programı** yazılacak ve açıklanacaktır. Bu kanal, küçük tasarım örnekleri gösterdiği için seçilmiştir ve Aspose.PSD for Java'nın popüler bazı bileşik araçlarını kullanımını anlatmaktadır (örneğin, [gölge efekti](/psd/tr/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), radial gradyan doldurma, metin ve şekil çizme):

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **Basitçe Nasıl Çalışır**
Basit bir Java programı, bir açıklama ve bir görüntü olmak üzere iki argümanı girdi olarak alır. Bu girdiden Aspose.PSD for Java kullanılarak bir **bellek içinde Photoshop belgesi (PSD) oluşturulur**. Daha sonra, program belgeyi PSD'den PNG dosya biçimine çevirerek, 1280x720 piksel boyutunda bir YouTube ön izlemesi elde eder. Çıktı görüntüsü aşağıdakine benzer görünmektedir:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **Teknik Gereksinimler**
Bu makalenin kodunu çalıştırmak için aşağıdaki teknolojilere ihtiyaç duyulmaktadır:

- Java 6+
- [Aspose.PSD for Java](/psd/tr/java/installation/) (en güncel)

## **Başlangıç**
Üzerinde durulduğu gibi, program bir ön izleme oluşturmak için bellek içinde PSD kullanır. Bu nedenle, öncelikle **bir PSD belgesi oluşturalım**:

PsdImage psdImage = new PsdImage(1280, 720);

Yukarıdaki YouTube ön izlemesine daha yakından baktığınızda **birkaç bileşenden oluştuğunu görebilirsiniz**:

1. Bir arka plan görüntüsü (baskılı maske)
1. Bir radial psd gradyanı (sağ üst köşedeki alanı vurgular)
1. Bir gölge efekti ile logo
1. Bir açıklama ve basit bir çizim (mavi dikdörtgen)

Bu bileşenlerden her birini Aspose.PSD for Java kullanarak nasıl uygulayacağımızı görmek için bir sonraki bölümlere inelim.

## **1. Bir arka plan görüntüsü ekleyin**
Katmanların sırası önemlidir. Bu nedenle, diğer katmanları örtmemesi için bir arka plan görüntüsünü ilk eklemek önemlidir. Şu anda yalnızca [raster dosya biçimleri desteklenmektedir](/psd/tr/java/supported-file-formats/).
### **1.1. Bir arka plan görüntüsünü Photoshop katmanına ekleyin**
PSD'ye **raster görüntü eklemek** için, bir katmanın oluşturulması sırasında bir girdi akışının argüman olarak iletilmesi gerekmektedir (raster görüntülerin yüklenmesi hakkında daha fazla bilgi için [örnekleri inceleyin](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}



1.2. Arka plan görüntüsünü tuvale sığdırın

Yukarıdaki 2 eylem (yeniden boyutlandırma, konumlandırma), **görüntü boyutu tuval boyutundan farklı olduğunda** yararlıdır, ancak bu makaledeki görüntü, boyutu tuval boyutuna eşit olduğu için aynıdır (her zaman böyle olmayacağını varsayalım).

Yüklenen görüntünün, **tavşan çiftliği**ni **tuval boyutuna uydurduğundan** emin olun (daha fazla [yeniden boyutlandırma örneğini](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages) görün):



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}



Yeniden boyutlandırmadan sonra, görüntünün konumu değişir. Bu nedenle, görüntünün konumunu sıfırlamak için yeniden boyutlandırılmış görüntüyü sol üst köşeye taşıyın:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}



## **2. Bir radial gradyan ekleyin**
Bir radial gradyan eklemenin **iki yolu vardır**, bunlar kullanılarak:

- Var olan bir katmana [gradyan örtü efekti](/psd/tr/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) eklenerek (bu, mevcut katmana bağlanan ve içeriğine uygulanan bir gradyan efektidir)
- Yeni bir [gradyan doldurma katmanı](/psd/tr/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) eklenerek (ayrı bir katman, gradyanın bağımsız yapılandırmasını tutar)

Bu örnekte gradyan örtü efektini kullanmak yeterlidir. Ancak, bu makaleyi daha ilginç ve kullanışlı hale getirmek için **gradyan doldurma katmanı kullanılır**, çünkü tüm katman efektleri benzer şekilde uygulanır ve bir sonraki bölümde başka bir katman efekti kullanılacaktır.
### **2.1. Bir radial gradyan doldurma katmanı ekleyin**
Yeni bir gradyan doldurma katmanı eklemenin süreci aşağıdaki 2 adımdan oluşur:

\1. **Gradyan doldurma ayarlarını belirtmek** gereklidir çünkü önceden tanımlanmış ayarlar yoktur. En az gereken yapılandırma aşağıdaki gibi görünmektedir (gradyan türü, oranı, renk ve şeffaflık noktaları gerekli özellikler olarak kabul edilir):



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}



Yukarıdaki yapılandırma, kenarları transparan ve merkezde koyu mavi olan bir radial gradyanı belirtir. Gradyan pozisyonu varsayılan olarak tuvalin ortasındadır.

Gradyan doldurmayı tersine çevirip sağ üst köşeye hafifçe kaydırmak için ilgili isteğe bağlı özellikleri kullanın:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}


\2. Yapılandırma yapıldığında, gradyan doldurma katmanı ile ayarlarını birlikte PSD'ye ekleyin:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}


## **Gölge Efekti ile Bir Logo Ekleyin**
**Gölge efekti**, bir nesnenin (resim, metin vb.) çevresine özel bir gölge eklemeyi sağlayan bir efekttir.
### **3.1. Bir logoyu Photoshop katmanına ekleyin**
Bir logoyu PSD'ye eklemek için **1.1. bölümdeki** ile **aynı yaklaşımı** kullanabilirsiniz:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}



### **3.2. Logo konumlandırma**
Yüklenen görüntü varsayılan olarak sol üst köşeye sıkıca yapıştırılmıştır. Ancak, kanalda orijinal YouTube ön izlemesi gibi görünmesi için bazı **kenar boşlukları eklenmesi** gerekmektedir. Bu nedenle, görüntü konumu, katmanın kenarlarından uzaklaştırılması gereken yerlere taşınmalıdır:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}



### **3.3. Logoya Gölge Efekti Ekleme**
Bir hafif arka plan görüntüsü kullanıldığında logo görünmez olabilir. Bu nedenle, bir logoya **gölge efekti eklemek** arzu edilir ve gölgelendirme seçenekleri özelliği üzerinden bir logoya gölge efekti eklemek istenir (daha fazla gölgelendirme örneği için bkz. [gölgeleme örnekleri](/psd/tr/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)):



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}



Varsayılan yapılandırma nedeniyle düşen gölge efekte sahip değildir (Photoshop'un gölge efektine benzer görünmektedir). Ancak yukarıdaki gölge, kenarları bulanık bir yarı saydam sınır gibi görünmesi için değiştirilmiştir.        
## **4. Metin ve Şekil Çizimi Ekleme**
### **3.1. Grafik Katmanı Oluşturun**
Düz katman tarafından doğrudan desteklenmeyen çizim, bir katman yanında **çizim için bir API sağlamak** amacıyla grafik motorunu kullanır (çizim örnekleri için daha fazla bilgi için [çizim örneklerini görün](/psd/tr/java/drawing-images-using-graphics/)):

Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
### **3.2. Çok Satırlı Metin Çizin**
Bir bilgili okur neden bir metin katmanı kullanmıyor diye sorabilir: çünkü bu durumda metin düzenlemesi gerekmeksizin her seferinde sıfırdan bir PSD oluşturulduğundan. Yazı tipi özelleştirmesi henüz desteklenmediği için **özel bir yazı tipi ile metin çizmek** kolaydır, sadece istenilen yazı tipini oluşturun ve grafik motorundan ilgili yöntemi çağırın. Ancak, metnin satır sayısına bağlı olarak otomatik olarak yüksekliği değiştiren bir dikdörtgen yapmak (bir sonraki bölümde ayrıntıları görün) biraz daha zordur. Tüm satırların tam olarak yüksekliği önceden hesaplanmalıdır:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}



1.15 satır yüksekliği, 3 metin dolgusu anlamına gelir.
### **3.3. Bir Dikdörtgen Çizin**
Dikdörtgen çizmek de oldukça kolaydır, hatta bir gradyan fırça ile (çizmek için bir alan ve bir renk aralığı belirlenerek) bile. Metin yüksekliği bilindiğinde dikdörtgenin boyutu ve pozisyonu hesaplanır. **Doldurulmuş bir dikdörtgen çizmek** içi**n psd içinde** (yalnızca çerçeve değil) grafik motorundan ilgili yöntemi çağırın:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}



` `Burada 40, 15, 25 girintileridir.
## **Sonuç**
Böylece, ön izlemin şekillendirilmesi tamamlandı. Dolayısıyla, izlemeyi raster dosya biçimine (örneğin, PNG) **dışa aktarmak için** (daha sonra dağıtmak için) bir zaman geldi:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}


## **Sonuç**
Bu makalede, DW Documentary kanalı için YouTube önizleme oluşturucusu oluşturduk ve gölgeli efekt, radial gradyan doldurma, metin ve şekil çizme gibi en popüler bileşik araçların nasıl kullanılacağını açıkladık.
## **Tam Örnek**
Aspose.PSD SDK'yı [indirebilirsiniz](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
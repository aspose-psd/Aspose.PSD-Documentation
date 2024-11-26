---
title: Resim Çizme
type: docs
weight: 10
url: /tr/java/resim-cizme/
---

## **Çizgi Çizme**
Bu örnek, Çizim sınıfını kullanarak Resim yüzeyinde çizgi şekillerini çizmek için kullanır. İşlemi göstermek için örnek, yeni bir Resim oluşturur ve Çizim sınıfı tarafından maruz bırakılan DrawLine yöntemini kullanarak Resim yüzeyinde çizgiler çizer. İlk olarak, yüksekliği ve genişliği belirterek bir PsdResim oluşturacağız.

Resim oluşturulduktan sonra, arka plan rengini belirlemek için Çizim sınıfı tarafından maruz bırakılan Clear yöntemini kullanacağız. Çizim sınıfının DrawLine yöntemi, iki nokta yapısını birleştiren bir çizgi çizmek için kullanılır. Bu yöntem, nokta yapısı veya Point/PointF yapıları çiftleri ile kalem sınıfının örneğini ve koordinat çiftlerini kabul eden birkaç aşırı yüklüye sahiptir. Kalem Sınıfı, çizgi, eğri ve şekilleri çizmek için kullanılan bir nesneyi tanımlar. Kalem sınıfı, belirtilen renk, genişlik ve fırça ile çizgi çizmek için birkaç aşırı yüklemeli yapıcıya sahiptir. SolidBrush sınıfı belirli bir renkle sürekli çizim yapmak için kullanılır. Son olarak, resim BMP dosya formatına dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyinde çizgi şekillerini nasıl çizeceğinizi gösterir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}
## **Elips Çizme**
Elips çizme örneği, çizgi şekilleri serisindeki ikinci makaledir. Resim yüzeyinde elips şeklini çizmek için Çizim sınıfını kullanacağız. İşlemi göstermek için örnek, yeni bir Resim oluşturur ve elips şeklini Resim yüzeyine Çizim sınıfı tarafından maruz bırakılan DrawEllipse yöntemini kullanarak çizer. İlk olarak, yüksekliği ve genişliği belirterek bir PsdResim oluşturacağız.

Resim oluşturulduktan sonra, Resim yüzeyi üzerinde elips şekli çizmek için Çizim sınıfı nesnesini oluşturacak ve başlangıç ​​rengini belirleyeceğiz. Çizim sınıfının DrawEllipse yöntemi, belirli bir dikdörtgen yapısı tarafından belirtilen Resim yüzeyinde elips şekli çizmek için kullanılır. Bu yöntem, Kalem ve Rectangle/RectangleF sınıflarının örneklerini veya koordinat çiftlerini, bir yükseklik ve bir genişliği argüman olarak kabul eder. Kalem sınıfı, çizgi, eğri ve şekilleri çizmek için kullanılan bir nesneyi tanımlar. Kalem sınıfı, belirtilen renk, genişlik ve fırça ile çizgi çizmek için birkaç aşırı yüklemeli yapıcıya sahiptir. Rectangle sınıfı, bir dikdörtgenin konumunu ve boyutunu temsil eden dört tam sayı kümesini depolar. Rectangle sınıfı, belirtilen boyut ve konumla dikdörtgen yapısını çizmek için birkaç aşırı yüklemeli yapıcıya sahiptir. SolidBrush sınıfı belirli bir renkle sürekli çizim yapmak için kullanılır. Son olarak, resim BMP dosya formatına dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyinde elips şeklini nasıl çizeceğinizi gösterir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
## **Dikdörtgen Çizme**
Bu örnekte, Resim yüzeyinde dikdörtgen şeklini çizeceğiz. İşlemi göstermek için örnek, yeni bir Resim oluşturur ve Çizim sınıfı tarafından maruz bırakılan DrawRectangle yöntemini kullanarak Resim yüzeyine dikdörtgen şekli çizer. İlk olarak, yüksekliği ve genişliği belirterek bir PsdResim oluşturacağız. Ardından, Çizim sınıfının Clear yöntemini kullanarak Resim yüzeyinin arka plan rengini ayarlayacağız.

Çizim sınıfının DrawRectangle yöntemi, belirli bir dikdörtgen yapısı tarafından belirtilen Resim yüzeyinde dikdörtgen şekli çizmek için kullanılır. Bu yöntem, Kalem ve Rectangle/RectangleF sınıflarının örneklerini veya koordinat çiftlerini, bir genişlik ve bir yükseklik argümanı olarak kabul eder. Rectangle sınıfı, bir dikdörtgenin konumunu ve boyutunu temsil eden dört tam sayı kümesini depolar. Rectangle sınıfı, belirtilen boyut ve konumla dikdörtgen yapısını çizmek için birkaç aşırı yüklemeli yapıcıya sahiptir. Son olarak, resim BMP dosya formatına dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyinde dikdörtgen şeklini nasıl çizeceğinizi gösterir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}
## **Yay Çizme**
Bu çizgi şekli serisinin bu oturumunda, Resim yüzeyine Yay şeklini çizeceğiz. İşlemi BMP resmi üzerinde gerçekleştirmek için Graphics class'ın DrawArc yöntemini kullanacağız. İlk olarak, yüksekliği ve genişliği belirterek bir PsdResim oluşturacağız. Resim oluşturulduktan sonra, Resim yüzeyinin arka plan rengini belirlemek için Grafikler sınıfı tarafından maruz bırakılan Clear yöntemini kullanacağız.

Çizim sınıfının DrawArc yöntemi, Resim yüzeyinde Yay şeklini çizmek için kullanılır. DrawArc, dikdörtgen yapısı veya koordinat çifti tarafından belirtilen bir elipsin bir kısmını temsil eder. Bu yöntem, Kalem sınıflarının örneklerini ve Dikdörtgen/RectangleF yapısını veya koordinat çiftlerini, bir genişlik ve bir yükseklik argümanı olarak kabul eden birkaç aşırı yüklüye sahiptir. Son olarak, resim BMP dosya formatına dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyinde Yay şeklini nasıl çizeceğinizi gösterir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
## **Bezier Çizme**
Bu örnek, Çizim sınıfını kullanarak Resim yüzeyinde Bezier şeklini çizmek için kullanır. İşlemi göstermek için örnek, yeni bir Resim oluşturur ve Çizim sınıfı tarafından maruz bırakılan DrawBezier yöntemini kullanarak Resim yüzeyine Bezier şeklini çizer. İlk olarak, yüksekliği ve genişliği belirterek bir PsdResim oluşturacağız. Resim oluşturulduktan sonra, Çizim sınıfı tarafından maruz bırakılan Clear yöntemini kullanacağız ve arka plan rengini belirleyeceğiz.

Çizim sınıfının DrawBezier yöntemi, dört Nokta yapısı tarafından belirtilen Resim yüzeyinde Bezier spline şeklini çizmek için kullanılır. Bu yöntem, kalem sınıfının örneklerini ve dört sıralı koordinat çiftini veya dört Nokta/PointF yapılarını veya Nokta/PointF yapılarını kabul eden bir dizi yüklüye sahiptir. Kalem sınıfı, çizgi, eğri ve şekilleri çizmek için kullanılan bir nesneyi tanımlar. Kalem sınıfı, belirtilen renk, genişlik ve fırça ile çizgi çizmek için birkaç aşırı yüklü yapıcıya sahiptir. Son olarak, resim BMP dosya formatına dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyinde Bezier şeklini nasıl çizeceğinizi gösterir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
## **Çekirdek Fonksiyonellik Kullanarak Resim Çizimleri**
Aspose.PSD, birçok değerli özelliğin yanı sıra resimler oluşturma gibi birçok değerli özellik sunan bir kütüphanedir. Bir resmin piksel bilgilerini manipüle etme gibi çekirdek işlevleri kullanarak çizim yapın veya Grafikler ve Grafik Yolu gibi gelişmiş özellikleri ve farklı fırçalar ve kalemler kullanarak şekilleri resim yüzeyine çizin. Aspose.PSD'nin RasterImage sınıfını kullanarak, bir resim alanının piksel bilgilerini alıp manipüle edebilirsiniz. RasterImage sınıfı, tüm çekirdek çizim işlevselliğini içerir, pikselleri alma ve ayarlama ve resim manipülasyonu için diğer yöntemler gibi. Oluşturulan bir resmi, Oluşturma Dosyaları bölümünde açıklanan yöntemlerden herhangi birini kullanarak oluşturun ve bir RasterImage sınıf örneğine atayın. RasterImage sınıfının LoadPixels yöntemini kullanarak bir resmin bir bölümünün piksel bilgilerini alın. Bir piksel diziniz olduktan sonra, her pikselin rengini değiştirerek, örneğin, piksel bilgilerini işleyebilirsiniz. Piksel bilgilerini manipüle ettikten sonra, bunu RasterImage sınıfının SavePixels yöntemini kullanarak resimde istediğiniz alana geri kaydedin. Aşağıdaki kod parçası, çekirdek işlevselliği kullanarak resim çizme işlemini gösterir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}

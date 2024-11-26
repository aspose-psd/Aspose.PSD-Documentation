---
title: Resimleri Çizme
type: docs
weight: 10
url: /tr/net/resimleri-cizme/
---

## **Çizgi Çizme**
Bu örnek, Resim yüzeyindeki çizgi şekillerini çizmek için [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfını kullanır. İşlemi göstermek için örnek, yeni bir Resim oluşturur ve [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfı tarafından sağlanan DrawLine yöntemini kullanarak Resim yüzeyinde çizgiler çizer. İlk olarak, yüksekliği ve genişliği belirterek bir PsdImage oluşturacağız.

Resim oluşturulduktan sonra, Resmin arka plan rengini belirlemek için Graphics sınıfı tarafından sağlanan Clear yöntemini kullanacağız. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) yöntemi, iki nokta yapısını birleştiren bir çizgiyi çizmek için kullanılır. Bu yöntem, noktaların veya Point/PointF yapılarının çift koordinat çiftlerini ve Pen sınıfının örneğini kabul eden birkaç aşırı yüklü yapısı vardır. Pen Sınıfı, çizgiler, eğriler ve şekiller çizmek için kullanılan bir nesneyi tanımlar. Pen sınıfının, belirtilen renkte, genişlikte ve fırçayla çizilen çizgileri çizmek için birkaç aşırı yüklü yapısı vardır. SolidBrush sınıfı, belirli bir renkle sürekli çizim yapmak için kullanılır. Son olarak, resim bmp dosya biçimine dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyindeki çizgi şekillerini nasıl çizeceğinizi gösterir.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizme-CizgiCizme-CizgiCizme.cs" >}}
## **Elips Çizme**
Elips örneği, çizim şekilleri serisinin ikinci makalesidir. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfını kullanarak Resim yüzeyindeki elips şeklini çizmek için DrawEllipse yöntemini kullanacağız. İşlemi göstermek için örnek, yeni bir Resim oluşturur ve [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfı tarafından sağlanan DrawEllipse yöntemi kullanarak Resim yüzeyinde elips şeklini çizer. İlk olarak, yüksekliği ve genişliği belirterek bir PsdImage oluşturacağız.

Resim oluşturulduktan sonra, Graphics sınıfı nesnesini oluşturacak ve başlangıç değerlerini belirleyeceğiz ve Clear yöntemini kullanarak resim arka plan rengini ayarlayacağız. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının [DrawEllipse](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawellipse/index) yöntemi, belirtilen sınır dikdörtgen yapısının üzerinde elips şeklini çizmek için kullanılır. Bu yöntem, Pen ve Rectangle/RectangleF sınıflarının örneklerini veya bir çift koordinat, bir yükseklik ve bir genişlik olarak içeren aşırı yüklü yapılara sahiptir. Pen Sınıfı, çizgiler, eğriler ve şekiller çizmek için kullanılan bir nesneyi tanımlar. Pen sınıfının, belirtilen renkte, genişlikte ve fırçayla çizilen çizgileri çizmek için birkaç aşırı yüklü yapısı vardır. Rectangle sınıfı, bir dikdörtgenin konumunu ve boyutunu temsil eden dört tamsayıyı içeren bir küme saklar. Rectangle sınıfının, belirtilen boyut ve konumla dikdörtgen yapısını çizmek için birkaç aşırı yüklü kurucucu yapısı vardır. SolidBrush sınıfı, belirli bir renkle sürekli çizim yapmak için kullanılır. Son olarak, resim bmp dosya biçimine dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyindeki elips şeklini nasıl çizeceğinizi gösterir.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizme-ElipsCizme-ElipsCizme.cs" >}}
## **Dikdörtgen Çizme**
Bu örnekte, Resim yüzeyinde dikdörtgen şeklini çizeceğiz. İşlemi göstermek için örnek, yeni bir Resim oluşturur ve [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfı tarafından sağlanan DrawRectangle yöntemini kullanarak Resim yüzeyinde dikdörtgen şeklini çizer. İlk olarak, yüksekliği ve genişliği belirterek bir PsdImage oluşturacağız. Ardından, [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının Clear yöntemini kullanarak Resmin arka plan rengini ayarlayacağız.

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının [DrawRectangle](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawrectangle/index) yöntemi, belirtilen dikdörtgen yapısına sahip bir resim yüzeyinde dikdörtgen şeklini çizmek için kullanılır. Bu yöntem, Pen ve Rectangle/RectangleF sınıflarının örneklerini veya koordinat çiftini, bir genişlik ve bir yükseklik olarak içeren aşırı yüklü yapılara sahiptir. Rectangle sınıfı, bir dikdörtgenin konumunu ve boyutunu temsil eden dört tamsayıyı içeren bir küme saklar. Rectangle sınıfının, belirtilen boyut ve konumla dikdörtgen yapısını çizmek için birkaç aşırı yüklü kurucu yapısı vardır. Son olarak, resim bmp dosya biçimine dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyinde dikdörtgen şeklini nasıl çizeceğinizi gösterir.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizme-DikdortgenCizme-DikdortgenCizme.cs" >}}
## **Yay Çizme**
Bu çizim şekil serisindeki oturumda, Resim yüzeyinde Yay şeklini çizeceğiz. İşlemi göstermek için BMP resminde işlem yapmak için [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının DrawArc yöntemini kullanacağız. İlk olarak, yüksekliği ve genişliği belirterek bir PsdImage oluşturacağız. Resim oluşturulduktan sonra, [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfı tarafından sağlanan Clear yöntemini kullanarak arka plan rengini ayarlayacağız.

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının [DrawArc](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawarc/index) yöntemi, bir resim yüzeyinde Yay şeklini çizmek için kullanılır. DrawArc, bir dikdörtgen yapısı veya koordinat çifti tarafından belirtilen bir elipsin bir kısmını temsil eder. Bu yöntem, Pen sınıflarının ve Rectangle/RectangleF yapısının örneklerini veya koordinat çiftini, bir genişlik ve bir yükseklik olarak kabul eden aşırı yüklü yapıları içerir. Son olarak, resim bmp dosya biçimine dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyinde Yay şeklini nasıl çizeceğinizi gösterir.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizme-YayCizme-YayCizme.cs" >}}
## **Bezier Çizme**
Bu örnek, Resim yüzeyindeki Bezier şeklini çizmek için [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfını kullanır. İşlemi göstermek için örnek, yeni bir Resim oluşturur ve [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfı tarafından sağlanan DrawBezier yöntemini kullanarak Resim yüzeyinde Bezier şeklini çizer. İlk olarak, yüksekliği ve genişliği belirterek bir PsdImage oluşturacağız. Resim oluşturulduktan sonra, [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfı tarafından sağlanan Clear yöntemini kullanarak arka plan rengini ayarlayacağız.

[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının [DrawBezier](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawbezier/index) yöntemi, dört Nokta yapısına dayalı Bezier eğrisini bir resim yüzeyinde çizmek için kullanılır. Bu yöntem, Pen sınıflarının örneklerini ve dört sıralı koordinat çiftini veya dört Nokta/PointF yapısını veya Nokta/PointF yapılarının dizisini kabul eden aşırı yüklü yapıları içerir. Pen sınıfı, çizgiler, eğriler ve şekiller çizmek için kullanılan bir nesneyi tanımlar. Pen sınıfının, belirtilen renkte, genişlikte ve fırçayla çizilen çizgileri çizmek için birkaç aşırı yüklü yapısı vardır. Son olarak, resim bmp dosya biçimine dışa aktarılır. Aşağıdaki kod parçası, Resim yüzeyindeki Bezier şeklini nasıl çizeceğinizi gösterir.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizme-BezierCizme-BezierCizme.cs" >}}
## **Çekirdek Yetenekleri Kullanarak Resim Çizme**
Aspose.PSD, resimler oluşturmayı içeren birçok değerli özelliğin yanı sıra çizimler yapma gibi çekirdek yetenekleri sunan bir kütüphanedir. Bir Resim'nin bitmap bilgilerini yönlendirmek gibi çekirdek işlevleri kullanma veya [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) ve [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) gibi gelişmiş özellikleri kullanarak farklı fırçalar ve kalemlerle resim yüzeyine şekiller çizme gibi gelişmiş özellikleri kullanma gibi. Aspose.PSD'nin RasterImage sınıfını kullanarak bir resim alanının piksel bilgilerini alabilir ve manipüle edebilirsiniz. RasterImage sınıfı, pikselleri alma ve ayarlama gibi resmin tüm çekirdek çizim işlevlerini içerir. Yeni bir resim oluşturmak için Oluşturma Dosyaları adlı yöntemlerden herhangi birini kullanın ve bunu bir RasterImage sınıfının bir örneğine atayın. Bir resmin belirli bir alanının piksel bilgilerini almak için RasterImage sınıfının LoadPixels yöntemini kullanın. Pikseller dizisine sahip olduktan sonra, örneğin, her pikselin rengini değiştirerek manipüle edebilirsiniz. Piksel bilgilerini manipüle ettikten sonra, RasterImage sınıfının SavePixels yöntemini kullanarak istenen alana yeniden yerleştirin. Aşağıdaki kod parçası, çekirdek yetenekleri kullanarak resim çizme işlemini gösterir.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizme-CoreCizimOzellikleri-CoreCizimOzellikleri.cs" >}}

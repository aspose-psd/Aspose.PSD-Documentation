---
title: Drawing Images using GraphicsPath
type: docs
weight: 30
url: /tr/java/resim-cizimini-graphicspath-kullanarak/
---

## **Resim Çizimini GraphicsPath Kullanarak**
GraphicsPath sınıfı, bir grafik yolunu oluşturmak ve sürdürmekten sorumludur. GraphicsPath, bir resme referansı olmadığı için resmi kendisi değiştirmez; bunun yerine, Graphics sınıfının çizebileceği yolları tanımlayan metaveriyi içeren bir nesne olarak düşünülebilir. GraphicsPath sınıfı şekilleri kullanır; her şekil ya bir dizi bağlı çizgi ve eğri veya bir geometrik şekil ilkesinden oluşur. Her şekil şekil segmentlerine bölünebilir. Bir GraphicsPath nesnesinde farklı şekilleri veya şekilleri ekleyebilir, kaldırabilir ve değiştirebilirsiniz. GraphicsPath tamamen tanımlandığında, ilgili Graphics sınıfı yöntemlerini (DrawPath ve Fill Paths) kullanarak yolları çizmek veya doldurmak için kullanabilirsiniz. Graphics sınıfı, her şekil segmentini alır ve nihai resmi oluşturmak için çizer.
### **GraphicsPath Sınıfı Kullanarak Çizim**
Aşağıda, GraphicsPath sınıfının kullanımını gösteren bir örnek bulunmaktadır. Örnek kaynak kodu, basit ve takip etmesi kolay tutmak için birkaç bölüme ayrılmıştır. Adım adım, örnekler size şunları nasıl yapacağınızı gösterir:

- Bir resim oluşturun.
- Bir Graphics nesnesini başlatın.
- Yüzeyi temizleyin.
- GraphicsPath örneği oluşturun.
- Bir şekil oluşturun.
- Şekilleri şekle ekleyin.
- Bir Şekiller dizisi oluşturun.
- Yolları çizin.
- Yolları doldurun.

### **GraphicsPath Sınıfını Kullanarak Resim Çizimi: Program Örnekleri**
#### **GraphicsPath : Bir Resim Oluşturma**
Herhangi bir Resim Oluşturma Yöntemiyle bir resim oluşturarak başlayın.
#### **GraphicsPath : Bir Graphics Nesnesini Başlatma**
Graphics nesnesini başlatmak için, Image nesnesini oluşturucusuna geçirerek bir Graphics nesnesi oluşturun ve başlatın.
#### **GraphicsPath : Yüzeyi Temizleme**
Grafik yüzeyini temizleyin, Graphics sınıfı Clear yöntemini çağırarak ve bir Renk olarak bir parametre olarak geçirerek. Bu yöntem, argüman olarak geçirilen renk ile Grafik yüzeyini doldurur.
#### **GraphicsPath : GraphicsPath Örneği Oluşturma**
Varsayılan olarak GraphicsPath ayarlanmış bir GraphicsPath örneği oluşturun. Bu mod, kapalı bir şeklin içini nasıl dolduracağını belirler. Diğer olası GraphicsPath değeri Sarmalama'dır.
#### **GraphicsPath : Bir Şekil Oluşturma**
Bir Şekil sınıfı örneği oluşturun. Daha önce tartışıldığı gibi, Şekil, şekillere sahip olabilir ve şekiller Aspose.PSD.Shapes ad alanında bulunur.
#### **GraphicsPath : Şekillere Şekiller Eklemek**
Şekilleri Figür sınıfının sunduğu Ekle Şekiller yöntemi, şekliye şekil eklemenizi sağlar. Aşağıdaki kod örneklerinde, çeşitli şekiller bir Şekil nesnesine eklenir.
#### **GraphicsPath : Dizileri Bir Dizisine Eklemek**
Birden fazla şekil, GrafikleriPath sınıfının sunduğu AddFigures yöntemi kullanılarak bir GraphicsPath nesnesine eklenir. Bu yöntem bir dizi şekillerini parametre olarak kabul eder.
#### **GraphicsPath : Yolları Çizmek**
Graphics sınıfı tarafından sunulan DrawPath yöntemini kullanarak GraphicsPath'i çizin. Yöntem iki parametre alır. İlk parametre, yolun rengini, genişliğini ve stilini belirleyen Kalem sınıfının bir nesnesidir. İkinci parametre, yolun kendisini temsil eden GraphicsPath sınıfının nesnesidir.
#### **GraphicsPath : Yolları Doldurmak**


Graphics sınıfının sunmuş olduğu Fill Paths yöntemine bir GraphicsPath nesnesi geçirerek bir yol doldurabilirsiniz. Fill Paths yöntemi, yolun doldurma moduna (sırayla veya sarmalama) göre doldurur. Eğer yolun içinde açık şekiller varsa, yol, bu şekillerin kapalıymış gibi doldurulur.

Fill Paths yöntemi iki parametre alır. İlk parametre, Aspose.PSD.Brushes ad alanından herhangi bir fırça sınıfının bir nesnesidir. İkinci parametre ise yolun kendisidir. Bu örneğin gereği olarak, bir HatchBrush kullanın. HatchBrush, bir çizgi deseni, bir ön plan rengi ve bir arka plan rengi olan bir dikdörtgen fırçadır. HatchBrush nesnesini Fill Paths yöntemine geçirmeden önce özelliklerini ayarlayın.
### **GraphicsPath : Tam Kaynak Malzemeler**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



IDisposable arabirimini gerçekleştiren tüm sınıflar, doğru bir şekilde atılmalarını sağlamak için Using ifadesinde bir kullanımla başlatılır.

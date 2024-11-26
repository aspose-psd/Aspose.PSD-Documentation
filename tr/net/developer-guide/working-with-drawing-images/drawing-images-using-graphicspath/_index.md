---
title: Grafik Yolu Kullanarak Resim Çizme
type: docs
weight: 30
url: /tr/net/resim-cizme-grafik-yolu-kullanarak/
---

## **Grafik Yolu Kullanarak Resim Çizme**
[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) sınıfı, bir grafik yolunu oluşturmak ve sürdürmekten sorumludur. GraphicsPath, bir resme referans yapmaz ve resmi kendisi değiştirmez; bunun yerine, Graphics sınıfının çizebileceği yolları açıklayan metaveriyi içeren bir nesne olarak düşünülebilir. GraphicsPath sınıfı şekilleri kullanır; her şekil, birbirine bağlı çizgiler ve eğrilerin bir dizisi veya geometrik şekil öğesinden oluşabilir. Her şekil şekil segmentlerine ayrılabilir. GraphicsPath nesnesine farklı şekiller veya şekiller ekleyebilir, kaldırabilir ve değiştirebilirsiniz. GraphicsPath tam olarak açıklandıktan sonra, karşılık gelen Graphics sınıfı yöntemlerini (DrawPath ve FillPaths) kullanarak yolları çizmek veya doldurmak için kullanabilirsiniz. Graphics sınıfı her şekil segmentini alır ve nihai resmi üretmek için çizer.

### **GraphicsPath Sınıfını Kullanarak Çizim**
Aşağıda, [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) sınıfının kullanımını gösteren bir örnek bulunmaktadır. Örnek kaynak kodu, basit ve anlaşılır tutulması için birkaç bölüme ayrılmıştır. Adım adım, örnekler size nasıl yapılacağını gösterir:

- Bir resim oluşturun.
- Bir Graphics nesnesini başlatın.
- Yüzeyi temizleyin.
- [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) örneği oluşturun.
- Bir şekil oluşturun.
- Şekiller ekleyin.
- Bir Figürler dizisi oluşturun.
- Yolları çizin.
- Yolları doldurun.


### **Grafik Yolu Kullanarak Resim Çizme: Programlama Örnekleri**
#### **GraphicsPath : Bir Resim Oluşturun**
Herhangi bir Oluşturma Dosyaları bölümünde açıklanan yöntemlerden birini kullanarak bir resim oluşturmaya başlayın.
#### **GraphicsPath : Bir Grafik Nesnesini Başlatın**
Bir Grafik nesnesi oluşturun ve başlatın, Image nesnesini parametre olarak geçirerek.
#### **GraphicsPath : Yüzeyi Temizleme**
Grafik yüzeyini, Graphics sınıfı Clear yöntemini çağırarak ve bir renk olarak geçirerek temizleyin. Bu yöntem, argüman olarak geçirilen renkle Grafik yüzeyini doldurur.
#### **GraphicsPath : GraphicsPath Örneği Oluşturma**
GraphicsPath örneği oluşturun ve GraphicsPath varsayılan olarak Alternatif olarak ayarlı olduğunda. Bu mod, kapalı bir şeklin içini doldurmanın nasıl belirleneceğini belirler. Diğer olası GraphicsPath değeri Sarmalama'dır.
#### **GraphicsPath : Bir Şekil Oluşturma**
Figure sınıfının bir örneğini oluşturun.. Daha önce tartışıldığı gibi, Figürler Şekilleri içerebilir ve şekiller Aspose.PSD.Shapes ad alanında bulunur.
#### **GraphicsPath : Şekilleri Şekle Ekleme**
Figure sınıfı tarafından sunulan Ekle Şekiller yöntemi, şekilleri figüre eklemenizi sağlar. Aşağıdaki kod örneklerinde, bir Figür nesnesine birkaç şekil eklenmiştir.
#### **GraphicsPath : Şekilleri Dizisine Ekleme**
Birden fazla figürü bir GraphicsPath nesnesine EkleFigürler yöntemini kullanarak ekleyebilirsiniz. Bu yöntem bir figür dizisini parametre olarak alır.
#### **GraphicsPath : Yolları Çizin**
Graphics sınıfının çizimi kullanarak GraphicsPath'i çizin. Bu yöntem iki parametre alır. İlk parametre, yolun rengini, genişliğini ve stilini belirleyen bir Kalem sınıfı nesnesidir. İkinci parametre, yolun kendisini temsil eden GraphicsPath sınıfı nesnesidir.
#### **GraphicsPath : Yolları Doldurma**

Grafik yollarını, Graphics sınıfı tarafından sunulan FillPaths yöntemine bir GraphicsPath nesnesi geçirerek doldurabilirsiniz. FillPaths yöntemi, yol için mevcut dolgu moduna (alternatif veya büküm) göre yolu doldurur. Eğer yolun içinde açık figürler varsa, yol, bu figürlerin kapalıymış gibi doldurulur.

FillPaths yöntemi iki parametre alır. İlk parametre, Aspose.PSD.Brushes ad alanından herhangi bir fırça sınıfı nesnesidir. İkinci parametre yolun kendisidir. Bu örnek için, HatchBrush kullanın; bu, bir dama desen stiline, bir ön plan rengine ve bir arka plan renge sahip dikdörtgen bir fırçadır. HatchBrush nesnesini FillPaths yöntemine geçirmeden önce özelliklerini ayarlayın.
### **GraphicsPath : Tam Kaynak**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}

Tüm IDisposable uygulayan sınıflar, doğru bir şekilde atılması için Using ifadesinde başlatılır.

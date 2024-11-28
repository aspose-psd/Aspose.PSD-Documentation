---
title: Grafikler Kullanarak Resimler Çizme
type: belgeler
weight: 20
url: /tr/net/grafikler-kullanarak-resimler-cizme/
---

## **Grafikler Kullanarak Resimler Çizme**
Aspose.PSD kütüphanesi ile basit şekiller olan çizgiler, dikdörtgenler ve daireler gibi şekillerin yanı sıra çokgenler, eğriler, yaylar ve Bezier şekilleri gibi karmaşık şekiller de çizebilirsiniz. Aspose.PSD kütüphanesi, Aspose.PSD ad alanındaki [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfını kullanarak bu şekilleri oluşturur. Grafik nesneleri, bir resim üzerinde farklı çizim işlemlerini gerçekleştirmekten sorumludur ve bu sayede resmin yüzeyini değiştirir. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfı, şu şekilleri geliştirmek için çeşitli yardımcı nesneler kullanır:

- Çizim yapmak için kalemler.
- Alanların nasıl doldurulacağını tanımlamak için fırçalar.
- Metin karakterlerinin şeklini tanımlamak için yazı tipleri.
### **Graphics Sınıfı ile Çizim**
Aşağıda, [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının kullanımını gösteren bir kod örneği bulunmaktadır. Örnek kaynak kodu, basit ve takip etmesi kolay tutulması için birden fazla parçaya bölünmüştür. Adım adım, örnekler, nasıl yapılacağını göstermektedir:

1. Bir resim oluşturun.
1. Bir Graphics nesnesi oluşturun ve başlatın.
1. Yüzeyi temizleyin.
1. Bir elips çizin.
1. Doldurulmuş bir çokgen çizin ve resmi kaydedin.
### **Programlama Örnekleri**
#### **Bir Resim Oluşturma**
Herhangi Bir Dosya Oluşturma adımlarında açıklanan yöntemlerden birini kullanarak bir resim oluşturmaya başlayın.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Graphics Nesnesi Oluşturma ve Başlatma**
Daha sonra, bir Graphics nesnesi oluşturun ve başlatın ve bunun için Image nesnesini yapıcı fonksiyona ileterek bunu başlatın.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Yüzeyi Temizleme**
[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfı Clear metodu çağırılarak yüzey temizlenir ve parametre olarak renk geçirilir. Bu metot, argüman olarak geçirilen rengi kullanarak Grafik yüzeyini doldurur.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Bir Elips Çizin**
[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) sınıfının şekilleri çizmek ve doldurmak için birçok metodu olduğunu fark edebilirsiniz. Aspose.PSD for .NET API Referansında tüm metotların tam listesini bulacaksınız. Graphics sınıfı tarafından sunulan DrawEllipse yöntemine ekranın etrafındaki elipsin sınırlayıcı dikdörtgeni tanımlamak için bir Rectangle nesnesi kabul eden sürümlerinden birini kullanmak için istediğiniz rengi içeren Pen nesnesini kullandınız.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Doldurulmuş Bir Çokgen Çizin**
Ardından, LinearGradientBrush ve nokta dizisini kullanarak bir çokgen çizin. Graphics sınıfı, FillPolygon() yöntemini kabul eden bir dizi aşırı yüklü sürüm açığa çıkarmıştır. Bunların tümü dolgunun özelliklerini tanımlayan bir Brush nesnesini ilk argüman olarak alır ve ikinci argümanı bir nokta dizisi olarak alır. Lütfen, dizi içindeki her iki ardışık noktanın bir çokgenin bir kenarını belirttiğine dikkat edin.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Grafikler Kullanarak Resimler Çizme : Tam Kaynak**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Tüm işlemeyen ve yönetilmeyen kaynaklara erişen IDisposable arabirimini gerçekleyen tüm sınıflar, düzgün bir şekilde atıldığından emin olmak için Using deyimi içinde başlatılır.

---
title: Grafik Kullanarak Resimler Çizme
type: docs
weight: 20
url: /tr/java/drawing-images-using-graphics/
---

## **Grafik Kullanarak Resimler Çizme**

Aspose.PSD kütüphanesi ile çizgi, dikdörtgen, daire gibi basit şekillerin yanı sıra çokgenler, eğriler, yaylar ve Bezier şekilleri gibi karmaşık şekiller de çizebilirsiniz. Aspose.PSD kütüphanesi, bu şekilleri Aspose.PSD ad alanında bulunan Graphics sınıfını kullanarak oluşturur. Grafik nesneleri, bir resimde farklı çizim işlemlerini gerçekleştirmekten sorumludur ve bu şekilde resmin yüzeyini değiştirir. Graphics sınıfı, şekilleri geliştirmek için çeşitli yardımcı nesneleri kullanır:

- Kalemler, çizgileri çizmek, şekilleri çerçevelemek veya diğer geometrik temsilleri oluşturmak için.
- Fırçalar, alanların nasıl doldurulacağını tanımlamak için.
- Yazı tipleri, metnin karakter şeklini tanımlamak için.
### **Grafik Sınıfıyla Çizim Yapma**
Aşağıda, Grafik sınıfının kullanımını gösteren bir kod örneği bulunmaktadır. Örnek kaynak kodu, basit ve takip edilmesi kolay olacak şekilde parçalara ayrılmıştır. Adım adım, örnekler aşağıdakileri nasıl yapılacağını göstermektedir:

1. Bir resim oluşturma.
1. Bir Grafik nesnesi oluşturup başlatma.
1. Yüzeyi temizleme.
1. Bir elips çizme.
1. Dolu bir çokgen çizme ve resmi kaydetme.
### **Programlama Örnekleri**
#### **Bir Resim Oluşturma**
Herhangi bir Oluşturma Dosyaları bölümünde açıklanan yöntemlerden herhangi birini kullanarak bir resim oluşturmaya başlayın.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Bir Grafik Nesnesi Oluşturma ve Başlatma**
Daha sonra, bir Grafik nesnesi oluşturun ve başlatın, Image nesnesini oluşturucuya ileterek.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **Yüzeyi Temizleme**
Grafik yüzeyini, Clear yöntemini çağırarak ve bir renk olarak parametre olarak göndererek temizleyin. Bu yöntem, argüman olarak geçirilen renk ile Grafik yüzeyini doldurur.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **Bir Elips Çizme**
Grafik sınıfının çizim ve doldurma yöntemlerini birçoklarına açtığını fark edebilirsiniz. Aspose.PSD için Java API Referansında yöntemlerin tam listesini bulabilirsiniz. Grafik sınıfı tarafından açıklanan birden fazla aşırı yüklemeli çizElips yöntemine dikkatinizi çekerken. Tüm bu yöntemler, elipsin etrafındaki sınırlayıcı dikdörtgeni tanımlamak için ikinci bir parametre olarak bir Pen nesnesi kabul eder. Bu örneğin amacı için, istediğiniz rengi kullanarak bir elips çizmek için ikinci bir parametre olarak bir Rectangle nesnesini kabul eden sürümü kullanın.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **Dolu Bir Çokgen Çizme**
Sonra, bir dikdörtgen fırça ve bir nokta dizisi kullanarak bir çokgen çizin. Grafik sınıfı, FillPolygon yöntemine aşırı yüklemeli birkaç sürüm açıklamıştır. Tüm bu, bir doldurma özelliklerini tanımlayan bir Fırça nesnesi olarak ilk argümanı kabul eder. İkinci parametre bir nokta dizisidir. Lütfen dizideki her iki ardışık noktanın çokgenin bir kenarını belirlediğini unutmayın.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **Grafik Kullanarak Resimler Çizme: Tam Kaynak**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

Tüm IDisposable uygulayan sınıflar ve yönetilmeyen kaynaklara erişen sınıflar, düzgün bir şekilde atılmalarını sağlamak için bir Using deyimi içinde örneklenmektedir.


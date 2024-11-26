---
title: Resimleri Kırpma, Döndürme ve Yeniden Boyutlandırma
type: docs
weight: 40
url: /tr/net/crop-rotate-and-resize-images/
---

## **Resimleri Kırpma**
Resim kırpma genellikle bir resmin dış kısımlarının çıkarılması anlamına gelir ve çerçevenin iyileştirilmesine yardımcı olur. Kırpma ayrıca bir resmin belirli bir alanına odaklanmayı artırmak için bazı bölümlerin kesilmesi amacıyla da kullanılabilir. Aspose.PSD API'sı, resim kırpmanın iki farklı yaklaşımını destekler: kaydırma ve dikdörtgen.
### **Kaydırma ile Kırpma**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) sınıfı, dış kısımları atarak resmin sınırlarını resmin merkezine doğru taşıyan Kırpma yönteminin 4 tamsayı değerini kabul eden aşırı yüklenmiş bir Crop yöntemi sağlar. Bu dört değere göre, Crop yöntemi dış kısmı atarken resmin sınırlarını resmin merkezine doğru kaydırır. Aşağıdaki kod parçası, bir resmi kaydırmak için nasıl kodlanacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **Dikdörtgen ile Kırpma**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) sınıfı, Dikdörtgen sınıfının bir örneğini kabul eden Crop yönteminin başka bir aşırı yüklenmiş sürümünü sağlar. Dikdörtgen nesnesine istenen sınırları vererek, bir resmin herhangi bir bölümünü kesebilirsiniz. Aşağıdaki kod parçası, bir resmi Dikdörtgen ile kırpmak için nasıl kodlanacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **Resim Döndürme ve Çevirme**
Aspose.PSD for .NET, karmaşık işlemleri gerçekleştirmek için basit yöntemler sağladığından kullanımı kolay bir kütüphanedir. Örneğin, bir uygulamanın bir resmi döndürmesi gerektiğinde Aspose.PSD for .NET, temel sınıf Image için RotateFlip yöntemini sağlamıştır. Resim biçiminden bağımsız olarak, kütüphane resme özel Döndürme ve Çevirme işlemlerini gerçekleştirebilir.
### **Resmi Döndürme**
Image.RotateFlip yöntemi, resmi 90/180/270 derece döndürmek ve resmi yatay veya dikey olarak çevirmek için kullanılabilir. Image.RotateFlip yöntemi, resme uygulanacak döndürme ve çevirme türünü belirten RotateFlipType türünde bir parametreyi kabul eder. Döndürme ve Çevirme işlemlerini gerçekleştirmek için adımlar aşağıdaki gibidir:

1. Image sınıfı tarafından sağlanan Load fabrika yöntemi kullanılarak resim yüklenir.
1. Uygun RotateFlipType belirterek Image.RotateFlip yöntemi çağrılır.
1. Sonuçlar kaydedilir.

Aşağıdaki kod örneği, bir Image'ın RotateFlip özelliğini ve RotateFlipType numaralandırmasını belirleme şeklini göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **Belirli Bir Açıda Resmi Döndürme**
Aspose.PSD for .NET API, belirli bir açıda bir resmi döndürmek isteyen kullanıcılarına [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate yöntemini sunar. [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip yönteminin aksine, [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate yöntemi üç parametreyi kabul eder:

1. Döndürme açısı: Resmin döndürüleceği açıyı belirten float türünde bir parametre. Pozitif bir değer resmi saat yönünde döndürürken, negatif bir değer saat yönünün tersine bir dönüş gerçekleştirir.
1. Oransal olarak yeniden boyutlandır: Bir Boolean türünde bir parametre, resmin boyutunun döndürülmüş dikdörtgenin (köşe noktaları) projeksiyonlarına göre değişip değişmeyeceğini belirtir. false olarak ayarlandığında, resmin boyutları dokunulmamış olacak ve yalnızca iç resim içeriği döndürülecektir.
1. Arka plan rengi: Döndürülen resmin arka planına doldurulacak rengi belirten bir Color türünde bir parametre.

Aşağıdaki kod parçası, [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate yönteminin kullanımını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **Resimleri Yeniden Boyutlandırma**
Bu makale, Aspose.PSD for .NET'in bir resim üzerinde Yeniden Boyutlandırma işlemini gerçekleştirmek için nasıl kullanılacağını göstermektedir. Aspose.PSD API'ları, bu hedefe ulaşmak için verimli ve kullanımı kolay yöntemler sunmuştur. Aspose.PSD for .NET, Image sınıfı için kullanılabilecek, mevcut resimleri dinamik olarak yeniden boyutlandırabilmek için Resize yöntemini açığa çıkarmıştır. Uygulama ihtiyaçlarına uygun iki farklı aşırı yüklenmiş Resize yöntemi bulunmaktadır.
### **Basit Boyutlandırma**
Yeniden Boyutlandırma işlemi için adımlar aşağıdaki gibidir:

1. Image sınıfı tarafından sağlanan Load fabrika yöntemi kullanılarak resim yüklenir.
1. Yeni Yükseklik ve Genişlik belirterek Image.Resize yöntemi çağrılır.
1. Sonuçlar kaydedilir.

Aşağıdaki kod örneği, bir resmi nasıl yeniden boyutlandıracağınızı göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **ResizeType Numaralandırmasıyla Yeniden Boyutlandırma**
Aspose.PSD API'sı, Image.Resize ile kullanılabilecek ResizeType numaralandırmasını açığa çıkarmıştır. Aşağıda sağlanan kod parçası, ResizeType numaralandırmasının nasıl kullanılacağını gösterir, ResizeType numaralandırmasının üyelerinin ayrıntıları ise bu sayfanın altında bulunabilir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



Eğer yeniden boyutlandırma uygulandıktan sonra kaliteli sonuç almayı amaçlıyorsanız, her zaman ResizeType.LanczosResample kullanmanız önerilir çünkü yüksek kaliteli sonuçlar verecektir ancak ResizeType.NearestNeighbourResample'den daha yavaş çalışabilir. Diğer yandan, ResizeType.NearestNeighbourResample algoritması, hızlı yeniden boyutlandırma için özellikle kullanılırken görüntü kalitesinden ödün verir. Bu yöntem, canlı olarak küçük resim oluşturulması veya performans gerektiren benzer işlemler için kullanışlı olabilir.
## **Resmi Oransal Olarak Yeniden Boyutlandırma**
Resimleri Yeniden Boyutlandırmak için Image.Resize yöntemine yeni yükseklik ve genişlik değerlerini parametre olarak geçirerek resimleri yeniden boyutlandırabilirsiniz, ancak bu durumda en boy oranını kendiniz hesaplamanız gerekmektedir. Çünkü bir resmin genişliği veya yüksekliği değiştirildiğinde, resim yeni boyuta ulaşacak şekilde ölçeklenecektir veya küçültülecektir. Bir resmin genişlik ve yüksekliğindeki değişiklikler orantısız ise bu gerilmiş ve bozulmuş sonuca yol açabilir. Bu makale, Aspose.PSD for .NET API'sının resimleri yeniden boyutlandırmak için kullanımını ve diğer oransal değeri otomatik olarak hesaplamasına izin vererek yeni yükseklik veya genişlik parametrelerini geçirerek resimleri yeniden boyutlandırmasını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **ResizeType Numaralandırması**
ResizeType, seçilen filtreye dayalı olarak resimde gerçekleştirilecek yeniden boyutlandırma türünü belirler.

[ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype) Numaralandırmanın Üyeleri

|**Üye Adı**|**Değer**|**Açıklama**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Yeni resmin sol üst noktası, orijinal resmin sol üst noktasıyla örtüşecektir. Gerekirse Kırpma gerçekleşecektir.|
|RightTopToRightTop|1|Yeni resmin sağ üst noktası, orijinal resmin sağ üst noktasıyla örtüşecektir. Gerekirse Kırpma gerçekleşecektir.|
|RightBottomToRightBottom|2|Yeni resmin sağ alt noktası, orijinal resmin sağ alt noktasıyla örtüşecektir. Gerekirse Kırpma gerçekleşecektir.|
|LeftBottomToLeftBottom|3|Yeni resmin sol alt noktası, orijinal resmin sol alt noktasıyla örtüşecektir. Gerekirse Kırpma gerçekleşecektir.|
|CenterToCenter|4|Yeni resmin merkezi, orijinal resmin merkeziyle örtüşecektir. Gerekirse Kırpma gerçekleşecektir.|
|LanczosResample|5|7x7 maske kullanarak Lanczos algoritmasını kullanarak yeniden örnekleme yapın.|
|NearestNeighbourResample|6|Komşu algoritmayı kullanarak yeniden örnekleme yapın.|


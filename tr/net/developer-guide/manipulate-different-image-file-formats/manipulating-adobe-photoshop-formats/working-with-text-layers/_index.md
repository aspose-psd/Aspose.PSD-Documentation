---
title: Çalışma Metin Katmanları ile
type: docs
weight: 170
url: /tr/net/çalışma-metin-katmanları-ile/
---

## **Metin Katmanı Ekleme**
Aspose.PSD for .NET, bir PSD dosyasına metin katmanı eklemenize olanak tanır. Bir PSD dosyasına metin katmanı eklemek için aşağıdaki adımları uygulamanız yeterlidir:

- [Image sınıfı](https://reference.aspose.com/psd/net/aspose.psd/image) tarafından sağlanan fabrika yöntemi [**Yükle**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) kullanarak bir PSD dosyasını bir görüntü olarak yükleyin.
- Metin ve [**Dikdörtgen**](https://reference.aspose.com/psd/net/aspose.psd/rectangle) sınıfının bir örneğini kabul eden [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) yöntemini çağırın.
- Sonuçları kaydedin

Aşağıdaki kod örneği size bir PSD dosyasına metin katmanı ekleme işlemini nasıl gerçekleştireceğinizi gösterir

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **Metin Katmanı Konumunu Ayarlama**
Aspose.PSD for .NET, bir PSD dosyasında bir metin katmanı konumunu ayarlamanıza olanak tanır. PSD dosyasında metin katmanı konumunu ayarlamak için aşağıdaki adımları uygulamanız yeterlidir:

- [Image sınıfı](https://reference.aspose.com/psd/net/aspose.psd/image) tarafından sağlanan fabrika yöntemi Yükle kullanarak bir PSD dosyasını bir görüntü olarak yükleyin.
- Sol ve üst pozisyonları belirterek AddTextLayer yöntemini çağırın.
- Sonuçları kaydedin

Aşağıdaki kod örneği size bir PSD dosyasında metin katmanı konumunu nasıl ayarlayacağınızı gösterir

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}

## **Metin Katmanından Metin Özelliklerini Alın**
Aspose.PSD for .NET kullanarak, PSD metin katmanında bulunan metnin farklı bölümlerinin metin özelliklerini alabilir ve güncelleyebilirsiniz. Bu makale, metin katmanının Paragraflarını, Stillerini ve Metin özelliklerini nasıl alabileceğinizi ve güncelleyebileceğinizi göstermektedir.

Aşağıdaki kod parçacığı, bu gereksinimi nasıl yerine getireceğinizi göstermektedir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


İşte [Aspose.PSD for .NET](https://products.aspose.com/psd/net) kullanarak [TextLayer'dan](https://reference.aspose.com/net/psd/aspose.psd/fileformats/psd/layers/textlayer) farklı metin bölümlerinin metin biçimlendirme özelliklerini nasıl alabileceğinizi gösteren başka bir örnek.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}

## **PSD Dosyasındaki Metin Katmanını Güncelleme**
Aspose.PSD for .NET, bir PSD dosyasının metin katmanındaki metni değiştirmenize olanak tanır. Bir PSD dosyasını güncellemek için Aspose.PSD.FileFormats.Psd.Layers.TextLayer sınıfını kullanın. Aşağıdaki kod parçacığı, bir PSD dosyasını yükler, metin katmanına erişir, metni günceller ve PSD dosyasını [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer/methods/updatetext/index) yöntemini kullanarak yeni bir adla kaydeder.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **Çalışma Zamanında Metin Katmanı Desteği**
Bu makale, PSD görüntüleri için çalışma zamanında metin katmanları eklemenin nasıl yapıldığını göstermektedir. Aşağıdaki kod parçacığı sağlanmıştır.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}

---
title: Dolgu Katmanlarının Desteği
type: docs
weight: 90
url: /tr/net/support-of-fill-layers/
---


## **Desen Dolgusu ile Dolgu Katmanları**
Bu makale, [PSD ](https://wiki.fileformat.com/image/psd/)katmanını Desen dolgusu ile doldurmanın nasıl yapıldığını göstermektedir. Bir Desen* * bir resmi, rengi, gölgeyi veya çizgiyi bir resmin alanını doldurmada kullanılan bir ögedir. Lütfen Aspose.PSD. FileFormats.Psd.Layers.FillLayer'ı kullanarak PSD katmanına Desen eklemek için [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) özelliklerini ayarlayın.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



İşte [Aspose.PSD](https://products.aspose.com/psd/net)nin [FillLayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)ve [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings) kullanarak deseni nasıl renderlediğini gösteren başka bir örnek.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Gradyan Dolgusu ile Dolgu Katmanları**
Bu makale, PSD katmanını doldurmak için Gradyan dolgusunun kullanımını göstermektedir. Aspose.PSD API'leri, bu hedefe ulaşmak için verimli ve kullanımı kolay yöntemler sunmuştur. Aspose.PSD, bir katmana Gradyan efekti eklemek için [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) ve [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) sınıflarını açıklamıştır.

`PSD katmanını Gradyan dolgusuyla doldurmanın adımları aşağıdaki kadar basittir:

- [Yükle](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) yöntemi ile bir görüntü olarak PSD dosyasını yükleyin. [Image](https://reference.aspose.com/net/psd/aspose.psd/image) sınıfı tarafından sağlanan fabrika yöntemi ile.
- [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) nesnesinin ayarlar özelliklerini ayarlayın.
- Gerekli renkler ve renk pozisyonlarını içeren bir [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) listesi oluşturun.
- Gerekli opaklık ve şeffaflık noktası pozisyonlarını içeren bir şeffaflık noktaları listesi oluşturun.
- [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update) yöntemini çağırın
- Sonuçları kaydedin.



Aşağıdaki kod parçası, PSD katmanına Gradyan doldurmayı nasıl ekleyeceğinizi gösterir.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**Aspose.PSD'nin PSD katmanını Gradyan dolgusu kullanarak doldurmak için [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** özelliğini kullanan başka bir örnek. Aspose.PSD, GradientType numaralaması aracılığıyla aşağıdaki gradiyan türlerini destekler:

- **GradientType.Linear:**       Doğrusal gradiyanda, renk başlangıç renginden son renge doğru düz bir çizgide geçiş yapar. 
- **GradientType.Radial:**       Yarıçaplı gradiyanda, renkler başlangıç noktasından dairesel bir desende yayılır.
- **GradientType.Angle:**        Açılı gradiyanda, renk başlangıç noktasının çevresinde saat yönünün tersine doğru döner.
- **GradientType.Reflected:** Yansımalı gradiyanda, renk başlangıç noktasının her iki tarafında yansıtılır.
- **GradientType.Diamond:**   Elmas gradiyan, başlangıç noktasından elmas şeklinde bir desen oluşturur.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Gradyan Dolgu Katmanı için Ölçek Özelliği Desteği**
Bu makale, Aspose.PSD ile .NET için Gradyan dolgulu FillLayer'ı ölçeklendirmenin nasıl yapıldığını göstermektedir. Bu amaçla, [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings) içinde yeni bir [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) özelliği eklenmiştir. 

Aşağıdaki kod, **Scale** özelliğinin nasıl kullanılacağını gösteren bir örnek sunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Renk Dolgusu ile Dolgu Katmanları**
Bu makale, PSD katmanını Renk ile doldurmanın nasıl yapıldığını göstermektedir. Lütfen [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) sınıfını PSD katmanına Renk eklemek için kullanın. Aşağıdaki kod parçası bir PSD dosyası yükler, Fill katman sınıfına erişir ve rengi [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings) özelliğini kullanarak ayarlar.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}



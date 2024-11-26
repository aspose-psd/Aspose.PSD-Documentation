---
title: Katmanlarla Çalışma
type: docs
weight: 150
url: /tr/net/working-with-layers/
---

## **Bir Katman Grubu Oluşturma**
Bir katman grubu, bir veya daha fazla katmandan oluşur ve benzer veya ilgili katmanları düzenlemeye yardımcı olur. Aspose.PSD for .NET kullanarak bir katman grubu oluşturabilirsiniz. Bu amaçla, bir yeni yöntem olan [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) bir [PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage) sınıfına katman grubunu eklemek için eklenmiştir.

Katman gruplarını oluşturmanın adımları aşağıdaki gibidir:
- Belirtilen genişlik, yükseklik ve görüntü seçenekleriyle PsdImage sınıfı kullanarak bir görüntü örneği oluşturun.
- Belirtilen grup adı ve dizinle bir [LayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/layers/layergroup) oluşturun.
- Layer sınıfının bir örneğini oluşturun ve PSD görüntüsünü atayın.
- Oluşturulan katmanı LayerGroup sınıfı tarafından sunulan AddLayer yöntemiyle katman grubuna ekleyin.
- Sonuçları kaydedin.

Aşağıdaki kod örneği, bir katman grubu nasıl oluşturulacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Bir Katmanın Adını Değiştirme**
İstediğiniz herhangi bir adı kullanabilirsiniz, ancak tipik uygulama o katmanda bulunan nesne veya öğenin genel bir tanımını kullanmaktır. Bu makale, Aspose.PSD for .NET'i kullanarak bir katmanın adını değiştirmeyi göstermektedir. Bu amaçla, Layer sınıfına katman adını düzgün bir şekilde görüntülemek için [DisplayName](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/layer/properties/displayname) adında yeni bir özellik eklenmiştir. Görülmüştür ki Photoshop, bir katman adını [Name](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/layer/properties/name) özelliğini kullanarak kaydettiğinde, Kore karakterleri ASCII'de bayt 63'?' olarak depolanır. Bu nedenle bir katman adını düzgün bir şekilde görüntülemek istiyorsanız **DisplayName** özelliğini kullanın çünkü **Name** özelliği Kore karakterlerini desteklemez.

Aşağıdaki kod örneği, bir katmanın adını nasıl değiştirebileceğinizi gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **Bağlantılı Katmanların Desteklenmesi**
Katmanları bağlamak, katmanları gruplamaya benzerdir. İki veya daha fazla katmanı bağlarsanız, bağlı katmanların her ikisine de belirli değişiklikler yapmanıza olanak tanır. Örneğin, bir katmana dönüşümler uygularsanız, tüm diğer bağlantılı katmanlara da uygulanacaktır. Bu makale, [Aspose.PSD](https://products.aspose.com/psd) kullanarak bağlantılı katmanları nasıl alabileceğinizi ve bağlantılı katmanları nasıl bağlayabileceğinizi göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}

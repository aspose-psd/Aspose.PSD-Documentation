---
title: PSD Dosyasında API Aracılığıyla Raster Katman Maskelerini Düzenleme
type: docs
weight: 20
url: /tr/net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **Genel Bakış**
**PSD formatını otomatikleştirmek ve Adobe® Photoshop® kullanmadan PSD dosyasını değiştirmek için aşağıdaki Aspose.PSD API'sini kullanabilirsiniz. PSD dosyalarını değiştirmenize yardımcı olabilecek C# ve .NET kod parçaları bulunmaktadır.**

PSD Katman ve Vektör Maskeleri kullanarak katman piksellerini kalıcı olarak silmeden gizleyebilir ve gösterebiliriz. Raster maskeleri aynı zamanda bir katman maskesi veya kullanıcı maskesi olarak da adlandırılır. Aspose.PSD'de hem raster hem de vektör maskelerine [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) katman özelliğinden erişim sağlanır, bu özellik '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' ve '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' sınıfları olabilir. Bu sınıflar soyut 'LayerMaskData' sınıfının çocuk sınıflarıdır. Bir katman hem raster hem de vektör maskelere sahipse, [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)nelimi verilir. Bir katman sadece raster veya vektör maskesine sahipse, [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)nelimi verilir. Eğer LayerMaskData özelliği null ise, katmanda maskeler yoktur veya sadece devre dışı bırakılmış bir vektör maskesi vardır.

|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Bir raster maske ve devre dışı bırakılmış bir vektör maske LayerMaskDataShort</p><p>Bir devre dışı bırakılmış raster maske  LayerMaskDataShort</p><p>Bir raster maske ve bir vektör maske  LayerMaskDataFull</p><p>Bir raster maske  LayerMaskDataShort</p><p>Bir vektör maske  LayerMaskDataShort</p><p>Bir devre dışı bırakılmış vektör maske yok (Ancak vektör kaynağı mevcut)</p>|
| :- | :- |

## **PSD dosyasında bir katman raster maskesini nasıl alabiliriz?**
Öncelikle, bir katmanda hem vektör hem de katman maskesinin olup olmadığını bulmalıyız:

Aşağıdaki örnek kod, bir katman raster maskesini nasıl alacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

Aksi takdirde, LayerMaskData katman özelliğinin türü LayerMaskDataShort olacaktır. Bu durumda, katmanın sadece bir raster maskesi olup olmadığını Flags özelliğini kontrol ederek kontrol edelim. Maskenin [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags)ı içermemesi gerekmektedir.**UserMaskFromRenderingOtherData** bayrağı, aksi takdirde maske bir vektör maske önbelleği**tir**.

Maske kod parçacığı alımı:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Eğer ihtiyaç duyarsanız **bir raster maske çıkarma** işlemi için LayerMaskDataShort olarak (daha fazla işlem yapmak için) her iki maske varken bile LayerMaskDataFull alınmalı ve LayerMaskDataShort'a dönüştürülmelidir. Aşağıdaki kod her iki durumda da kullanılabilir:

PSD'den bir raster maske çıkarma

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **PSD dosyasında bir katmanda raster maske olup olmadığını nasıl kontrol edebiliriz?**
Aşağıdaki C# kodu, bir katmanda raster maskesinin olup olmadığını kontrol etmenize yardımcı olabilir:

Raster maske uygulanıp uygulanmadığını nasıl öğreniriz? [PSD Katmanı](/psd/tr/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **PSD dosyasında bir katman raster maskesini kaldırma / ekleme / güncelleme işlemi**
Sadece LayerMaskData'ı kaldırmak / eklemek / güncellemek yeterli olmaz, çünkü kanallar güncellenmez; ancak doğru saydam olabilir. Bu, maske kanallarını değiştirmez:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Kaldırmak / eklemek / güncellemek için katmanın AddLayerMask yöntemini kullanmalıyız.

Bu hem maskenin hem de kanalların eklenmesini / güncellemeyi sağlar:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Bu hem maskenin hem de kanalların silinmesini sağlar:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **PSD görüntüsünde bir katman raster maskesini kaldırma**
Öncelikle, maske kısa biçimindeyse ve vektör değilse sadece raster maskesini silmek için AddLayerMask yöntemini çağırabiliriz. Ancak tam biçimindeyse, bu durumda onu kısa biçime dönüştürmeli ve vektör maskesini yalnız bırakmalıdır. Bir katman maskesini kaldırmak için aşağıdaki C# .NET kod parçacığı kullanılabilir:

PSD Dosyasından Katman Maskesini Kaldırma kod parçası.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **PSD görüntüsünde bir katman raster maskesini güncelleme**
Bu basit bir işlemdir: kısa biçimdeki maskenin ImageData ve MaskRectangle'ı gerekiyorsa değiştirmemiz gerekir, aksi takdirde [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)ve [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)değiştirilmelidir. Aşağıdaki C# .NET kod parçacığı, bir katman maskesini güncellemede kullanılabilir:

C# ile PSD Katman Maskesini Güncelleme

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

İşte bir katman kullanıcı maskesini ters çeviren olası eylemlerden bir örnek:

C# ile PSD Katman Maskesini Güncelleme

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **PSD dosyasında bir katmanda raster maske varken bir vektör maskesini nasıl güncelleriz?**
Kullanıcı zaten bir vektör yol kaynağını değiştirmiştir varsayılır. Ardından, vektör maskesini [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask) katman yöntemini çağırarak güncelleyebilir:

[PSD Katmanı Vektör Maskesini ](/psd/tr/net/layer-vector-mask/) C# ile Güncelleme

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **PSD dosyasında bir katmanda raster maske eklemek**
Eğer bir katmanda maske yoksa, verilen raster maskesini AddLayerMask katman yöntemini çağırarak kolayca ekleyebiliriz.

Eğer maskenin [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags) bayrağı yoksa zaten bir raster maskesi vardır ve yukarıda açıklandığı gibi güncellememiz gerekir. Aksi takdirde, eğer bu maske kısa bir formatta ise onu tam biçime dönüştürürüz. Değilse olduğu gibi kullanırız. Daha sonra UserMaskData, UserMaskRectangle ve verilen maske özellikleri diğer özelliklerle güncellenir. Bir (güncelleme) katman maskesi eklemek için aşağıdaki C# .NET kod parçacığı kullanılabilir:

PSD'ye Yeni Katman Maske Ekleme

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Bir katman maskesinin etkin olup olmadığını nasıl kontrol ederiz?**
Katman raster maskesinin etkin olma durumunu bulmak için, LayerMaskDataShort için Flags özelliğinde veya LayerMaskDataFull için RealFlags özelliklerinde [LayerMaskFlags.Disabled](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags) bayrağı durumunu kontrol edebiliriz. Bir katman maskesinin etkin durumunu almak için aşağıdaki C# .NET kod parçacığı kullanılabilir:

Bir maskenin etkin olup olmadığını kontrol edin:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}
## **Bir raster katman maskesini etkinleştirmek veya devre dışı bırakmak için**
Bir katman raster maskesini etkinleştirmek veya devre dışı bırakmak için, LayerMaskDataShort için Flags özelliğinde veya LayerMaskDataFull için RealFlags özelliğinde [LayerMaskFlags.Disabled](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags) bayrağı durumunu değiştirebiliriz. Bir katman maskesinin etkin durumunu değiştirmek için aşağıdaki C# .NET kod parçacığı kullanılabilir:

Raster Katman Maskesini Etkinleştir veya Devre Dışı Bırak:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}

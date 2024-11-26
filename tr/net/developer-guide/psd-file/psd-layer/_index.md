---
title: PSD Katmanı
type: docs
weight: 70
url: /tr/net/psd-katmani/
---

## **Genel Bakış**
Adobe® Photoshop® PSD Katmanı, grafik işlemede en iyi kavramlardan biridir. Katmanlar pikseller hakkında bilgi içerir, farklı sayıda kanala sahip olabilirler.

Photoshop Belgesindeki Katmanın en önemli parçalarından biri Katman Kaynaklarıdır. PSD'deki desteklenen [Katman Kaynakları](/tr/psd/net/psd-katman-kaynaklarının-listesi/)yla ilgili tüm bilgilere belgelerimizden ulaşabilirsiniz.

Katmanı manipüle etmek için UI, aşağıdaki ekran görüntüsünde bulunabilir:

![todo:image_alt_text](psd-katmani_1.png)

Ancak Aspose.PSD, PSD Katmanlarının programatik olarak manipüle edilmesine odaklanmıştır [C# ](/tr/psd/net/home/)ve [Java](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home).

Ek belgelere şu makalede ulaşabilirsiniz: [Görüntüleri Manipüle Etme](/tr/psd/net/goruntuleri-manipule-etme-html/). Tüm manipülasyonlar, PSD Önizlemesi ve Katmanına işlenebilir, daha fazla bilgiyi [Aspose.PSD Raster Görüntü API Referansında](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) bulabilirsiniz.

## **Uygun PSD Katmanı API'si**
- Katman Efektleri
- Katmanlar genel özellikleri
- Katman Metadata

## **C# ile Katman Düzenleme Örnekleri**
### **Yeni Katman Ekleme**
Eğer açık [PSD Dosyasına](/tr/psd/net/psd-dosyasi/) boş bir Katman eklemek isterseniz, aşağıdaki kodu kullanabilirsiniz.

API kullanarak PSD Dosyasına yeni Katman ekleme

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}

### **Jpeg, Png, Gif, Ai, Tiff, Bmp dosyalarından Yeni Katman Ekleme**
Herhangi bir [desteklenen formatın ](/tr/psd/net/desteklenen-dosya-formatları/)dosyaları görüntünüze yeni bir katman olarak eklenebilir. Ancak onu doğrudan yükleyemezsiniz.

Herhangi desteklenen formattaki bir dosyadan yeni PSD Katmanı eklemek için aşağıdaki kodu kullanabilirsiniz.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

### **Tüm katmanları veya katman gruplarını düzleştirme**
Kullanıcılara düzenlenebilir bir PSD dosyası vermek istemiyorsanız yararlı olabilir. Aynı zamanda, dosyanın düzleştirilip düzleştirilmediğini API aracılığıyla tespit edebilirsiniz.

PSD Dosyasının Katman Düzleştirmesi:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}

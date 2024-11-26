---
title: Ham Veri İşleme
type: docs
weight: 50
url: /tr/net/ham-veri-isleme/
---

## **Ham Veri İşleme**
Aspose.PSD API'sinin performansını artırmak için sürüm 2.4.0 ile ham veri işleme yöntemini tanıttık. Ham veri işlemesi şu anda dahili olarak kullanılıyor ve dış API'ye sahip, böylece kütüphanenin dışından kullanılarak genel performans iyileştirilebiliyor. İşleme bazen biraz karmaşık olabilir ve bazı açıklamalara ihtiyaç duyabilir. Şu anda ham veri işlemesi yalnızca BMP formatı için mevcuttur.

Geliştiricilere en iyi performansı elde etmelerine yardımcı olmak amacıyla Aspose.PSD API'si, özelleştirme için dış API'ye sahip bir ham veri işleme sistemi sunar. Geliştiriciler, ham veri işlemini kullanmak için [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) ve [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) method ailesini çağırır. Bu yöntemler ayrıca istenen ham veri formatının [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings) sınıfını kullanarak ayarlanmasını gerektirir. RawDataSettings sınıfı, geliştiricilerin herhangi bir ham veri formatını belirtmelerine olanak tanır. Ancak en iyi performansı elde etmek için verinin depolandığı ham veri formatının kullanılması gerekmektedir. RasterImage sınıfında tanımlanan RawDataSettings, resmin ham [veri formatını](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat) belirlemeye yardımcı olur. RawDataSettings örneğini LoadRawData yöntemine geçirirken, veri herhangi bir dönüşüm uygulanmadan doğrudan döner ve performansı artırabilir. Aksi takdirde, bazen biraz karmaşık olabilen tüm olası ham veri formatları düzenine dikkat etmeniz gerekebilir.

İşlemi basitleştirmek için, bazen performansta bazı kayıplara neden olurken, istenen RawDataSettings'i ayarlayarak sınıfı örnekleyerek ve başlangıçta istenen ham veri ayarlarıyla başlatarak belirleyebilirsiniz. Bazı durumlarda belirtilen formatta ham verinin döndürülmesi mümkün olmayabilir (örneğin CMYK renk uzayından RGB'ye dönüşüm sürüm 2.4.0'da mevcut değildir). Ayrıca, bir resim formatı için ham veri işleminin hiç bulunmadığı senaryolar olabilir. LoadRawData ve SaveRawData method ailesini kullanıp kullanamayacağınızı belirlemek için [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable) özelliğini sorgulamanız gerekir.
### **Görüş**
RGB [piksel veri formatı](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) için dizinlenmiş (palet tabanlı) ve RGB tabanlı ham veri formatları mevcuttur. Dizinlenmiş ham veri formatları, 0..(2^bis sayısı – 1) aralığında palette giriş dizinlerini içerir. Dizinlenmiş ham veri formatları 1, 2, 4 ve 8 bit piksel başına değer içerir. Geri kalanı RGB tabanlı ham veri formatlarıdır. Ham veri yüklerken, verinin yüklenmesi için yeterli baytların mevcut olmasına dikkat edin, aksi takdirde uygun bir hata fırlatılır. Bayt dizisi boyutunu basitçe satır boyutunu gereken satırlarla çarparak tahmin edebilirsiniz. Satır boyutu değişebilir ve ham veri depolama formatına bağlıdır.

Her zaman en iyi performansı elde etmek için [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize) özelliğinin değerine eşit bir ham veri satır boyutunu kullanın. Ancak, bazen ham veri satırlarına ekstra dolgu eklemeniz veya azaltmanız gerekebilir, bu durumda farklı bir satır boyutu kullanılabilir. Bir görüntünün sınırlayıcı bir dikdörtgen alt kümesi gerekiyorsa, dizinlenmiş RGB piksel formatları için meydana gelebilecek bit kaymalarını dikkate alın. Örneğin, 100x100 piksellik boyutları olan ve 1 bit piksel başına ham veri formatına sahip bir görüntüyü düşünelim. (7,0) konumundan başlayarak (2,1) boyutlarında bir ham veri dikdörtgenini yüklemek istiyorsunuz, veya başka bir deyişle, x=7 ve y=0'dan başlayarak 2 piksel gerekiyor. Bu durumda aşağıdaki veri düzenini almalısınız:



![todo:image_alt_text](raw-data-processing_1.png)

Bu, 2 byte alacağınız ve ilk byte'ın 7 istenmeyen pikseli, sonra 1 istenilen pikseli içerdiği ve ikinci byte'ın 1 istenilen pikseli ve ardından 7 istenmeyeni içerdiği anlamına gelir.  Neden veri kaydırma yapmadık ve bu 2 pikseli tek bir bayta yerleştirme? Cevap basittir: performansı yüksek tutmak. Tüm dahili işlemler genellikle verinin ilk pikselden başlayıp mevcut son piksele kadar devam etmesiyle gerçekleştirilir. Piksel alt kümesinin gerektiğinden daha az olduğu nadir durumlar vardır. Ayrıca, bu piksellerin sonradan nasıl işleneceğini bilmediğimiz için kaydırma, performansı düşürür ve kodu gereksiz yere karmaşık hale getirir. İstenen piksellerin başlayacağı doğru biti hesaplamak için basit bir formül kullanılabilir: (rect.Sol * bitsSayısı) % 8.
### **Dizinlenmiş RGB Renk Dönüşümü**
Mümkün olan en yüksek performansı elde etmek için her zaman aynı kaynak ve hedef ham veri ayarlarını, piksel biçimlerini ve satır boyutlarını kullanın. Ancak, bazen veri dönüşümü yapmanız gerekebilir. Örneğin, 1 bit piksel başına RGB görüntü yükleyebilir ve 2 bit piksel başına kaydedebilirsiniz, veya 4 bit RGB görüntü yükleyebilir ve rengi 2 bit piksel başına düşürebilirsiniz. Her iki durumda da bir renk dönüşümü uygulanmalıdır. Dizinlenmiş RGB görüntülerin dönüşümü bazen karmaşık olabilir ve bazı ayarlar uygulanmadan gerçekleştirilemeyebilir. Kaynak renk aralığının hedef renk uzayına nasıl eşleştirildiğini belirlememiz gerekmektedir. Bu görevi yerine getirmek için farklı [modlar](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods) vardır:

- Palet eşleme (DitheringMethods.PaletteConversion)
- Ham veri eşleme (DitheringMethods.PaletteIgnore)
- Özel dönüşüm (DitheringMethods.CustomConverter)

Palet dönüşümü kullanıldığında, kaynak renk uzayı hedef renk uzayına mümkün olduğunca yakın bir şekilde eşleştirilmeye çalışır. Örneğin, aşağıdaki renklere sahip 4 bit bir görüntüye sahip olduğumuzu varsayalım:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

Kaynak görüntü şu şekildedir:



![todo:image_alt_text](raw-data-processing_2.png)

Ve 4 bitlik görüntüyü aşağıdaki palette renkleri tanımlandı şekilde 1 bitlik bir görüntüye dönüştürüyoruz:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Palet dönüşümü modunda, dönüştürücü kaynak rengi okur ve hedef paletin [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) yöntemini kullanarak hedef indeksi belirler. Paletin GetNearestColorIndex yöntemi, paletin dışında bir indeks verirse, [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) özellik değeri kullanılır. Bu, kaynak renkleri yoğunluk değerleri açısından en yakın hedef renklere dönüştürür. Hedef görüntü, kaynak görüntüyle mümkün olduğunca eşleşir. Aşağıdaki sonuçları görebilirsiniz:


![todo:image_alt_text](raw-data-processing_3.png)

Ham veri eşleme modunda farklı bir senaryo kullanılır. Kaynak ve hedef renk paletleri basitçe yok sayılır ve kaynak indeksler hedef indekslere eşlenir. (Bit sayısını düşürdüğünüzde hedef aralığa içine sığmayan bir değer bulunduğunda) o zaman RasterImage.RawFallbackIndex özelliği değeri kullanılır. Bu değer varsayılan olarak 0'dır ve hedef paletin ilk rengine eşleştirilir. Bu özellik değeri hedef aralığın dışında ise, uygun bir hata fırlatılır. Bu, tahmin edilebilir olmayan sonuçlara yol açabilir ve aşağıdaki gibi görselleştirilebilir:


![todo:image_alt_text](raw-data-processing_4.png)

Palet dönüşümü modu, renk eşleme sorunu için daha doğru bir çözüm olmasına rağmen, doğru renk eşlemesini tahmin etmek için hesaplamaların yapılması gerektiği için biraz daha fazla zaman alır. (İki yöntem arasında genellikle çok az performans farkı vardır.) Öte yandan, ham eşleme modu biraz daha hızlı çalışır ve kesin renk eşlemesi çok önemli değilken daha kabataslak renk dönüşümü için kullanılabilir. Örneğin, kaynak renk paletinin kırpıldığı ve ekstra bitlerin zaten kullanılmadığı durumlarda, fazla bitler kullanılmadığından daha az bit sayısına güvenle dönüştürülebilir.

Bu yaklaşımlardan herhangi birini kullanmak için, RasterImage sınıfı RawDitheringMethod özelliğini kullanın. Varsayılan olarak, en iyi görünüm sonuçlarını elde etmek için palet dönüşüm yöntemi olarak ayarlanmıştır. Bu özelliği herhangi bir dönüşüm gerçekleşmeden önce (örneğin resmi akışa kaydetme sırasında) değiştirebilirsiniz. Lütfen unutmayın ki, eğer bir görüntü yüklemiş ve orijinal piksel verilerinden bazılarını yeniden yazmış iseniz, yeni veriler önbelleğe girer ve önbellek verileri mevcut format 32ARGB'ye (sürüm 2.4.0 olarak, değişebilir) depolar. Bu format, yüklenen ve kaydedilen görüntüler için olası farklı renk aralıkları sorunlarını aşmak için kullanılır. Ayrıca, görüntü RGB modunda yüklenmiş ve dizinlenmiş mode dönüştürülmüşse veya tam tersi ise, paleti yok sayma ve palet dönüşümü takımları yok sayılacaktır.
### **Özel Renk Dönüştürücüler**
Bazen renk dönüşümü için standart yaklaşımların yetersiz olduğu durumlar olabilir. Renk dönüşüm rutinlerini kullanırken tam özgürlüğü elde etmek için özel bir algoritma kullanmak isteyebilirsiniz. Kaynak ve hedef görüntülerin piksel biçimleri her ikisi de dizinlenmiş RGB formatındaysa daha basit bir arabirim olan [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter) kullanılabilir. RasterImage.RawIndexedColorConverter özelliğini bir IIndexedColorConverter arabirimi örneğine ayarlayın ve RawDitheringMethod özelliği değer olarak [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter'ı kullanın. Bu kombinasyon kullanıldığında, tüm dizinlenmiş renk dönüşümleri belirtilen IIndexedColorConverter örneği üzerinden gerçekleştirilir. Özel dizinlenmiş renk dönüştürücüsünün aşağıdaki metodu tanımlanmıştır:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



FillIndexedtoIndexedMap metodu, dizinlenmiş RGB görüntüden dizinlenmiş RGB görüntü formatına dönüşüm gerektiğinde çağrılır (her biri birbirine dönüştürülen 1,2,4 veya 8 bit sayısından herhangi biri). Harita dizisi, tüm olası kaynak format girişlerinin sayısına sahiptir. Bu diziyi, kaynak renk palet girdisinden hedef renk palet girdisine eşleme yapmak için doldurmanız gerekir. Dikkat edin ki, hedef indeks değeri 0..(bit sayısı - 1) aralığında olmalıdır, aksi takdirde uygun bir hata fırlatılır.

Daha özel bir renk dönüşüm senaryosu gerçekleştirmek gerekiyorsa, o zaman [RasterImage.RawCustomColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawcustomcolorconverter) özelliği bir [IColorConverter](https://reference.aspose.com/psd/net/aspose.psd/icolorconverter) arabirimi örneğine ayarlanmalıdır. Her iki özell
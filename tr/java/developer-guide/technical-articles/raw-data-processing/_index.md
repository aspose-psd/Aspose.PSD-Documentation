---
title: Ham Veri İşleme
type: docs
weight: 70
url: /tr/java/ham-veri-isleme/
---

## **Ham Veri İşleme**
Aspose.PSD API'sının performansını artırmak için 2.4.0 sürümü ile ham veri işleme yöntemini tanıttık. Ham veri işlemesi şu anda dahili olarak kullanılır ve dış API'ye sahiptir, bu nedenle genel performansı artırmak için kütüphanenin dışından kullanılabilir. İşleme bazen biraz karmaşık olabilir ve açıklamalarını gerektirebilir. Ham veri işlemesi şu anda sadece BMP formatı için mevcuttur.

Geliştiricilere en iyi performansı sağlamak için Aspose.PSD API, özelleştirme için dış API'ye sahip bir ham veri işleme sistemi sunmaktadır. Geliştiriciler, ham veri işlemini kullanmak için LoadRawData ve SaveRawData method ailesini çağırır. Bu yöntemler ayrıca istenen ham veri formatının RawDataSettings sınıfı kullanılarak ayarlanmasını gerektirir. RawDataSettings sınıfı, geliştiricilere herhangi bir ham veri formatını belirtme olanağı sağlar. Ancak, en iyi performansı elde etmek için verinin depolandığı ham veri formatını kullanmanız gerekmektedir. RasterImage sınıfında tanımlanan RawDataSettings, görüntünün ham veri formatını belirlemeye yardımcı olur. RawDataSettings örneğini LoadRawData methoduna iletirken veri doğrudan dönüştürülmeden ve uygulanmadan döndürülür, bu da performansı artırabilir. Öte yandan, bazen biraz karmaşık olan tüm muhtemel ham veri formatları yerleşimi ile ilgilenmeniz gerekir.

İşleme sürecini basitleştirmek için, performans cezası karşılığında, istenen RawDataSettings'i özelleştirme ile belirterek sınıfı örnekleyerek ve başlatarak belirtebilirsiniz. Örneğin, CMYK renk uzayından RGB'ye dönüşümün 2.4.0 sürümünde mümkün olmadığı durumlar vardır. Dahası, bazen bir görüntü formatı için hiç ham veri işlemesi kullanılamayabilir. LoadRawData ve SaveRawData method ailesini kullanıp kullanamayacağınızı belirlemek için IsRawDataAvailable özelliğini sorgulamanız gerekir.
### **İçgörü**
RGB piksel veri formatı için endeksli (palet tabanlı) ve RGB tabanlı ham veri formatları mevcuttur. Endeksli ham veri formatları, 0..(2^bit sayısı - 1) aralığında palet giriş indekslerini içerir. Endeksli ham veri formatları 1, 2, 4 ve 8 bit piksel başına olabilir. Geri kalanları RGB tabanlı ham veri formatlarıdır. Ham verileri yüklerken, veriyi yüklemek için yeterli baytların olduğundan emin olun, aksi takdirde uygun bir hata fırlatılacaktır. Veriyi yüklemek için gereken byte dizisi boyutunu, satır başına çarpım yaparak basitçe tahmin edebilirsiniz. Satır boyutu değişebilir ve ham veri depolama formatına bağlıdır.

En iyi performansı elde etmek için her zaman RasterImage.RawLineSize özelliği değerine eşit bir ham veri satır boyutu kullanın. Ancak bazen ham veri satırlarına ek padding eklemeniz veya azaltmanız gerekebilir ve bu durumda farklı bir satır boyutu kullanılabilir. Bir görüntünün sınırlı bir dikdörtgen alt kümesi gerekiyorsa, o zaman endeksli RGB piksel formatları için oluşabilecek bit kaydırmalarını dikkate almalısınız. Örneğin, 100x100 piksel boyutunda 1 bit piksel ham veri formatına sahip bir görüntü olduğunu varsayalım. Konum (7,0) ve boyutlar (2,1) olan bir ham veri dikdörtgeni yüklemek istiyorsunuz, veya diğer bir deyişle x=7 ve y=0 konumlarından başlayarak 2 piksel gerekiyor. Bu durumda aşağıdaki veri düzenini almalısınız:



![todo:image_alt_text](raw-data-processing_1.png)

Bu, 2 bayt alacağınız anlamına gelir, ilk bayt 7 istenmeyen piksel içerir, ardından 1 istenilen piksel vardır ve ikinci bayt 1 istenilen piksel içerir ve ardından 7 istenmeyen piksel bulunur. Neden veri kaydırma yapmadık ve bu 2 pikseli tek bir bayta yerleştirme? Cevap basittir: performansı yüksek tutmak için. Tüm dahili işlem, tipik olarak ilk piksellerden başlayıp son kullanılabilir pikselle sona eren tüm verilerle gerçekleştirilir. Piksel alt kümesinin gerekliliği nadiren karşılaşılan durumlardır. Ayrıca, bu piksellerin sonradan nasıl işleneceğini bilmediğimizden dolayı kaydırma performansı düşürecek ve kodu gereksiz yere karmaşık hale getirecektir. Teklif edilen piksellerin başlayacağı doğru biti tahmin etmek için doğru formül kullanılabilir: (dikdörtgen.Sol * bit sayısı) % 8.
### **Endeksli RGB Renk Dönüşümü**
Mümkün olan en yüksek performansı elde etmek için her zaman aynı kaynak ve hedef ham veri ayarlarını, piksel formatlarını ve satır boyutlarını kullanın. Ancak bazen veri dönüşümü yapmanız gerekebilir. Örneğin 1 bit piksel başına RGB görüntü yükleyebilir ve 2 bit piksel başına kaydedebilirsiniz veya 4 bit RGB görüntü yükleyebilir ve rengi 2 bit piksel başına indirgeyebilirsiniz. Her iki durumda da bir renk dönüşümü uygulanmalıdır. Endeksli RGB görüntülerin dönüştürülmesi bazen zor olabilir ve bazı ayarlar uygulanmadan gerçekleştirilemeyebilir. Kaynak renk aralığının hedef renk uzayına nasıl eşlenmesi gerektiğini belirlememiz gerekmektedir. Bu görevi gerçekleştirmek için farklı modlarımız vardır:

- Palet eşleme (DitheringMethods.PaletteConversion)
- Ham veri eşleme (DitheringMethods.PaletteIgnore)
- Özel dönüştürücü (DitheringMethods.CustomConverter)

Palet dönüşümü kullanıldığında, kaynak renk alanı, hedef renk alanına mümkün olduğunca yakın olacak şekilde eşleştirilmeye çalışır. Örneğin, aşağıdaki renklere sahip 4 bitlik bir görüntümüz olduğunu varsayalım:
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

Kaynak görüntü şu şekilde görünüyor:



![todo:image_alt_text](raw-data-processing_2.png)

Ve 4 bitlik görüntüyü 1 bitlik görüntüye aşağıdaki palet renkleri tanımlanmış olarak dönüştürdüğümüzü varsayalım:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Palet dönüşümü modunda, dönüştürücü kaynak rengi okur ve hedef paletin GetNearestColorIndex metodunu kullanarak hedef indeksi belirler. Paletin GetNearestColorIndex metodu, hedef paletinin dışında bir indeks verirse, RasterImage.RawFallbackIndex özniteliği değeri kullanılır. Bu, kaynak renkleri parlaklık değerleri açısından hedef renklere en yakın şekilde dönüştürür. Hedef görüntü, kaynak görüntüye mümkün olduğunca yakın olacaktır. Aşağıdaki sonucu görebilirsiniz:



![todo:image_alt_text](raw-data-processing_3.png)

Ham veri eşleme modunda farklı bir senaryo kullanılır. Kaynak ve hedef renk paletleri basitçe yoksayılır ve kaynak indeksler hedef indekslere eşlenir. Değerlerin belli bir yelpazeye eşlenemeyeceği durumlarda (bit sayısını azaltırken) RasterImage.RawFallbackIndex özelliği kullanılır. Varsayılan olarak, değeri 0'dır ve hedef paletin ilk rengine eşlenir. Bu özellik değeri, hedef aralığın dışında kalırsa, uygun bir hata fırlatılır. Bu, daha öngörülemez sonuçlara ve aşağıdaki resimde gösterilebilecek sonuçlara yol açar:



![todo:image_alt_text](raw-data-processing_4.png)

Palet dönüşüm modu, renk eşleme sorunu için daha doğru bir çözümdür ancak hesaplama yapmak için biraz daha fazla zamana ihtiyaç duyar. (Genellikle iki yöntem arasında çok küçük bir performans farkı vardır.) Diğer yandan, ham eşleme modu biraz daha hızlı çalışır ve renk eşlenmesi tam olarak önemli olmadığında daha ham renk dönüşümleri için kullanılabilir. Örneğin, kaynak renk paleti kırpılmış ve ekstra bitler zaten kullanılmamışsa güvenli bir şekilde daha düşük bit sayılarına dönüştürülebilir.

Bu yaklaşımlardan herhangi birini kullanmak için RasterImage sınıfı RawDitheringMethod özelliğini kullanın. Varsayılan olarak, en iyi görünümlü sonuçları elde etmek için palet dönüşüm yöntemi olarak ayarlanmıştır. Bu özelliği, herhangi bir dönüşüm gerçekleşmeden önce (örneğin, resmi bir akışa kaydetme) değiştirebilirsiniz. Lütfen unutmayın ki paleti yok sayma ve palet dönüşümü sürtünmeleri, yüklenmiş bir görüntü varsa ve orijinal piksel verisinin bazılarını yeniden yazarsanız (2.4.0 sürümüne göre olduğu gibi, değişebilir), olası farklı renk aralıklarıyla ilgili sorunları aşmak için kullanışlıdır. Ayrıca, sinek dışlama ve palet dönüşümü sürütme yöntemleri, bir görüntü RGB modunda yüklenirken ve endeksli moda dönüştürülürken veya tam tersi durumlarda yüklenirse dikkate alınmaz.
### **Özel Renk Dönüştürücüler**
Bazen renk dönüşümü için standart yaklaşım yeterli olmayabilir. Renk dönüşümü rutinlerini kullanırken tam özgürlük sağlamak için özel bir algoritma kullanmak isteyebilirsiniz. Kaynak ve hedef görüntü piksel formatları her ikisi de endeksli RGB formatları ise daha basit bir arayüz olan IIndexedColorConverter kullanılabilir. RasterImage.RawIndexedColorConverter özelliği, bir IIndexedColorConverter arabirimi örneğine ayarlanmalı ve RawDitheringMethod özelliği değeri olarak DitheringMethods.CustomConverter kullanılmalıdır. Bu kombinasyon uygulanırken, herhangi bir endeksli renk dönüşümü belirtilen IIndexedColorConverter örneği üzerinden gerçekleşir. Özel endeksli renk dönüştürücü, aşağıdaki yönteme sahiptir:



{{< highlight java >}}

void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



FillIndexedtoIndexedMap yöntemi, endeksli RGB görüntüden endeksli RGB görüntü formatına dönüşüm gerektiğinde çağrılır (1,2,4 veya 8 bit sayısından herhangi biri diğerine dönüştürüldüğünde). Harita dizisi, tüm olası kaynak format giriş sayısı uzunluğundadır. Bu diziyi doldurarak kaynak renk palet girişinden hedef palet girişine eşleme yapmanız gerekir. Hedef indeks değerinin 0..(bit sayısı - 1) aralığında olduğundan emin olun, aksi takdirde uygun bir hata fırlatılır.

Eğer daha özel bir renk dönüşüm senaryosu yapılması gerekiyorsa, o zaman RasterImage.RawCustomColorConverter özelliği bir IColorConverter arabirim örneğine ayarlanmalıdır. RawCustomColorConverter özelliği, hem RawIndexedColorConverter özelliğini hem de IColorConverter arabirimini ayarlayarak, her ikisi de ayarlanmışsa bir endeksli renk dönüştürücü kullanılmayacaktır. IColorConverter'ın tek bir metoduna sahiptir:



{{< highlight java >}}

int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}



Convert yöntemi, her renk dönüşümü gerektiğinde çağrılır. Metod, kaynak ham veriyi kaynak formatta alır ve dönüştürülen rengi almak için bir çıktı önbelleğine sahiptir. Hedef önbellek, dönüştürülen verileri almak için yeterli olmalıdır (Eğer This section has been removed since it contained code, which should not be translated.exeral olarak Aspose.PSD kitaplığı tarafından çağrı yapılarak bu arabirim çağrıldığında, önbellek dönüştürülen ham veriyi içermesi gereken ve yöntem dönüş yapılınca dönüşen ham veriyi içermelidir. Convert yöntemi, tüm kaynak veri kapsanana kadar birkaç kez çağrılabilir.

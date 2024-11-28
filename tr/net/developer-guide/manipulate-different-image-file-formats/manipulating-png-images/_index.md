---
title: PNG Görüntülerini Manipüle Etmek
type: docs
weight: 40
url: /tr/net/png-goruntulerini-manipule-etmek/
---

## **PNG Görüntüleri İçin Şeffaflık Belirtme**
Görüntüleri PNG formatında kaydetmenin avantajlarından biri, PNG'nin şeffaf arka plana sahip olabilme özelliğidir. Aspose.PSD .NET için, aşağıdaki bölümde gösterildiği gibi PNG Görüntüleri & Raster görüntüleri için şeffaflığı belirtme özelliği sağlar. Aspose.PSD .NET API, yeni PNG görüntüler oluştururken veya mevcut görüntüleri PNG formatına dönüştürürken herhangi bir rengi şeffaf olarak belirtmek için kullanılabilir. Bu amaçlar için, Aspose.PSD .NET API, şeffaf olarak belirlenecek herhangi bir rengi belirlemek için [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) özelliği ve [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) numaralandırmasını sunmuştur. Aşağıda verilen kod parçası, mevcut bir PSD görüntüsünü istenilen rengi şeffaf olarak belirterek PNG görüntüsüne dönüştürmenin nasıl yapıldığını göstermektedir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Goruntuleri-DuzenlemeVeDondurmePNG-SeffafligiBelirtme-SeffafligiBelirtme.cs" >}}
## **PNG Görüntüleri İçin Çözünürlüğü Ayarlama**
Aspose.PSD .NET, PNG de dahil olmak üzere tüm görüntü formatları için çözünürlüğü ayarlamak için kullanılabilen ResolutionSetting sınıfını açıklar. Bu makale, Aspose.PSD .NET API'nin yatay ve dikey çözünürlük parametrelerini PNG görüntü biçimi için nasıl belirleyeceğini göstermektedir. Aşağıdaki kod parçası, mevcut bir PSD görüntü yükler ve aynı zamanda çözünürlüğü değiştirerek PNG formatına dönüştürür.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Goruntuleri-DuzenlemeVeDondurmePNG-CozunurluguAyarla-CozunurluguAyarla.cs" >}}
## **PNG Dosyalarını Sıkıştırma**
Taşınabilir Ağ Grafik (PNG), bir bit eşlemesini ağlar üzerinden iletmek için kayıpsız bir sıkıştırma formatıdır. Herhangi bir programda bir görüntüyü PNG dosyası olarak kaydederken, bir sıkıştırma seviyesi seçmeniz istenebilir, bu seviye 0 ile herhangi bir maksimum seviye arasında olabilir. Bu değeri ayarlamak aslında dosya boyutunu sıkıştırır ve görüntü kalitesini azaltmaz. Bu makale, Aspose.PSD API'lerinin PNG dosya boyutunu kontrol etmenize izin verdiğini açıklar. Aspose.PSD API'leri, PNG dosya biçimi için sıkıştırma düzeylerini belirlemek için int türünde [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) özelliğine sahip olan PngOptions sınıfını kullanabilir. Bu özellik, 0 ila 9 arasında bir değer kabul eder, 9 maksimum sıkıştırmadır. Aşağıda verilen kod parçası, Aspose.PSD .NET API'sini kullanarak Sıkıştırma Düzeylerini nasıl ayarlayacağınızı göstermektedir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Goruntuleri-DuzenlemeVeDondurmePNG-SikistirmaDosyalari-SikistirmaDosyalari.cs" >}}
## **PNG Görüntüleri İçin Bit Derinliği Belirtme**
Görüntüleme'de bit derinliği, bir bit eşlemeli bir görüntüde tek bir pikselin rengini belirtmek için kullanılan bit sayısıdır. Diğer tüm bit eşlemeli formatlar gibi, PNG renk derinliği de 1-bit (2 renk), 2-bit (4 renk), 4-bit (16 renk) ve 8-bit (256 renk) gibi bit olarak temsil edilir. Aspose.PSD .NET API, PngOptions sınıfı tarafından sunulan [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) özelliğini kullanarak PNG görüntüleri için bit derinliği belirlemek için kullanılabilir. Şu anda, BitDepth özelliği 1, 2, 4 veya 8 bitler için gri tonlama ve dizinli renk türleri için ayarlanabilir. Tüm diğer renk türleri için yalnızca 8 bit desteklenir. Aşağıda verilen kod parçası, bir PNG görüntüsü için Bit Derinliğini nasıl ayarlayacağınızı göstermektedir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Goruntuleri-DuzenlemeVeDondurmePNG-BitDerinligiBelirtme-BitDerinligiBelirtme.cs" >}}
## **PNG Görüntülerinde Filtre Yöntemlerinin Uygulanması**
Görüntülemede bit derinliği, bir bit eşlemeli bir görüntüde tek bir pikselin rengini belirtmek için kullanılan bit sayısıdır. Diğer tüm bit eşlemeli formatlar gibi, PNG renk derinliği de 1-bit (2 renk), 2-bit (4 renk), 4-bit (16 renk) ve 8-bit (256 renk) gibi bit olarak temsil edilir. Aspose.PSD .NET API, PngOptions sınıfı tarafından sunulan BitDepth özelliğini kullanarak PNG görüntüleri için bit derinliği belirlemek için kullanılabilir. Şu anda, BitDepth özelliği 1, 2, 4 veya 8 bitler için gri tonlama ve dizinli renk türleri için ayarlanabilir. Tüm diğer renk türleri için yalnızca 8 bit desteklenir. Aşağıda verilen kod parçası, bir PNG görüntüsü için Bit Derinliğini ayarlamanın nasıl yapıldığını göstermektedir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Goruntuleri-DuzenlemeVeDondurmePNG-FiltreUygulamaYontemi-FiltreUygulamaYontemi.cs" >}}
## **Şeffaf Bir PNG Görüntüsünün Arka Plan Rengini Değiştirme**
PNG formatındaki görüntülerin şeffaf arka plana sahip olabilme özelliği vardır. Aspose.PSD .NET, şeffaf arka plana sahip bir PNG görüntüsünün arka plan rengini değiştirme özelliğini sağlar. Aspose.PSD .NET API, şeffaf bir PNG görüntüsünün rengini ayarlamak/değiştirmek için kullanılabilir. Aşağıda verilen kod parçası, şeffaf bir PNG görüntüsünün arka plan rengini nasıl ayarlayacağınızı göstermektedir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Goruntuleri-DuzenlemeVeDondurmePNG-ArkaPlanRenginiDegistirme-ArkaPlanRenginiDegistirme.cs" >}}

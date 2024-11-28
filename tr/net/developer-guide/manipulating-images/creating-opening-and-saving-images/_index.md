---
title: Resim Oluşturma, Açma ve Kaydetme
type: docs
weight: 30
url: /tr/net/resim-olusturma-acma-ve-kaydetme/
---

## **Resim Dosyaları Oluşturma**
Aspose.PSD for .NET, geliştiricilere kendi resimlerini oluşturma imkanı sunar. Yeni resimler oluşturmak için Image sınıfı tarafından sağlanan statik Create yöntemini kullanın. Yalnızca istenen çıkış resim formatı için ImageOptions alanından bir sınıfın uygun nesnesini sağlamanız yeterlidir. Bir resim dosyası oluşturmak için öncelikle ImageOptions alanından bir sınıfın örneğini oluşturun. Bu sınıflar çıkış resim formatını belirler. Aşağıda ImageOptions alanından bazı sınıflar bulunmaktadır (şu anda yalnızca PSD dosya format ailesi oluşturma için desteklenmektedir):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions), PSD dosyası oluşturmak için seçenekleri belirler. Resim dosyaları, bir çıkış yolunu ayarlayarak veya bir akışı ayarlayarak oluşturulabilir.
### **Yol Ayarıyla Oluşturma**
[ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) alanından PsdOptions oluşturun ve çeşitli özellikleri ayarlayın. Ayarlanması gereken en önemli özellik Kaynak özelliğidir. Bu özellik, resim verilerinin ne yerde bulunduğunu belirler (bir dosyada veya bir akışta). Aşağıdaki örnekte, kaynak bir dosyadır. Özellikleri ayarladıktan sonra, nesneyi bir genişlik ve yükseklik parametresi ile birlikte statik [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) yöntemlerinden birine geçirin. Genişlik ve yükseklik piksellerle belirlenir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Akış Kullanarak Oluşturma**
Bir akışı kullanarak bir resim oluşturma süreci, bir yol kullanarak oluşturmaya benzer. Tek fark, [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) örneği oluşturmanız ve Kaynak özelliğine bir Stream nesnesini geçirerek atamanız gerektiğidir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Resim Dosyalarını Açma**
Geliştiriciler, mevcut PSD resim dosyalarını farklı amaçlarla açmak için Aspose.PSD for .NET API'yı kullanabilirler, örneğin resme efektler eklemek veya mevcut bir dosyayı başka bir formata dönüştürmek. Amacınız ne olursa olsun, Aspose.PSD, mevcut dosyaları açmak için iki standart yol sağlar: dosyadan veya akıştan.
### **Diskten Açma**
Image sınıfının eklediği Load yöntemine yol ve dosya adını parametre olarak geçirerek bir resim dosyasını açın.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Akış Kullanarak Açma**
Açmamız gereken resmin bazen bir akış olarak saklandığı durumlar olabilir. Bu durumlarda, Load yönteminin aşırı yüklü versiyonunu kullanın. Bu, resmi açmak için bir Stream nesnesini bir argüman olarak kabul eder.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Katman Olarak Resmi Yükleme**
Bu makale, bir resmi bir katman olarak yükleme işlemini Aspose.PSD'nin kullanımını göstermektedir. Aspose.PSD API'leri, bu hedefe ulaşmak için etkili ve kolay kullanımlı yöntemler sunmuştur. Aspose.PSD, bir resmi PSD dosyasına bir katman olarak eklemek için PsdImage sınıfının AddLayer yöntemini açığa çıkarmıştır.

Bir resmi PSD olarak bir katman olarak yükleme adımları aşağıdaki gibi basittir:

- Belirli bir genişlik ve yüksekliğe sahip bir PsdImage sınıfı kullanarak bir resim örneği oluşturun.
- Image sınıfı tarafından sağlanan Load fabrika yöntemi kullanarak bir PSD dosyasını bir resim olarak yükleyin.
- Bir Katman sınıfı örneği oluşturun ve PSD resim katmanını buna atayın.
- Yaratılan katmanı PsdImage sınıfı tarafından açığa çıkarılan AddLayer yöntemi kullanarak ekleyin.
- Sonuçları kaydedin.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Akıştan Bir Katman Olarak Resmi Yükleme**
Bu makale, bir resmi bir akıştan bir katman olarak yükleme işlemini Aspose.PSD'nin kullanımını göstermektedir. Bir görüntüyü bir akıştan yüklemek için basitçe, bir resmi içeren bir akış nesnesini Layer sınıfı yapıcısına geçirin. Oluşturulan katmanı PsdImage sınıfı tarafından açığa çıkarılan AddLayer yöntemi kullanarak ekleyin ve sonuçları kaydedin.


İşte örnek kod.

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Resim Dosyalarını Kaydetme**
Aspose.PSD, sıfırdan resim dosyaları oluşturmanıza olanak tanır. Varolan resim dosyalarını düzenlemek için de imkanlar sağlar. Resim oluşturulduğunda veya düzenlendiğinde, genellikle dosya diske kaydedilir. Aspose.PSD, resimleri bir yola belirterek veya bir Akış nesnesi kullanarak diske kaydetmek için yöntemler sağlar.
### **Diske Kaydetme**
Image sınıfı, bir resim nesnesini temsil ettiğinden, bu sınıf, bir resim dosyası oluşturmak, yüklemek ve kaydetmek için gereken tüm araçları sağlar. Resimleri kaydetmek için Image sınıfı Save yöntemini kullanın. Save yönteminin aşırı yüklü versiyonlarından biri, dosya konumunu bir dize olarak kabul eder.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Akışa Kaydetme**
Başka bir Save yönteminin aşırı yüklü versiyonu Stream nesnesini bir argüman olarak kabul eder ve resmi akışa kaydeder.

Eğer bir resim, Image sınıfının Oluştur işleminde CreateOptions'ları belirterek oluşturulmuşsa, resim, Image sınıfının başlatılması sırasında sağlanan yol veya akışa otomatik olarak kaydedilir. Bu, herhangi bir parametre kabul etmeyen Save yöntemini çağırarak yapılır.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Eksik Yazı Tiplerini Değiştirme Ayarı**
Geliştiriciler, Aspose.PSD for .NET API'yı, örneğin PSD belgelerini raster bir resim olarak (PNG, JPG ve BMP formatlarına) kaydederken eksik yazı türü adını ayarlamak için kullanabilirler. Bu varsayılan yazı tipi, tüm eksik yazı tipleri için (mevcut İşletim Sisteminda bulunmayan yazı tipleri) bir yer tutucu olarak kullanılmalıdır. Resim düzenlendikten sonra, dosya diske kaydedilecektir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}

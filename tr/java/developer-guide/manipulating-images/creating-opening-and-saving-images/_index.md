---
title: Resimler Oluşturma, Açma ve Kaydetme
type: docs
weight: 30
url: /tr/java/resimler-olusturma-acma-ve-kaydetme/
---

## **Resim Dosyaları Oluşturma**
Aspose.PSD for Java, geliştiricilere kendi resimlerini oluşturma imkanı sağlar. Yeni resimler oluşturmak için Image sınıfı tarafından sunulan statik Create yöntemini kullanın. Yapmanız gereken tek şey istenen çıkış resim formatı için ImageOptions isim alanındaki sınıflardan uygun bir nesneyi sağlamaktır. Bir resim dosyası oluşturmak için öncelikle ImageOptions isim alanından bir sınıfın örneğini oluşturun. Bu sınıflar çıkış resim formatını belirler. Aşağıda ImageOptions isim alanından bazı sınıflar bulunmaktadır (şu an sadece PSD dosya format ailesi oluşturmayı desteklemektedir):

PsdOptions, bir PSD dosyası oluşturmak için seçenekleri ayarlar. Resim dosyaları, bir çıkış yolunu ayarlayarak veya bir akış ayarlayarak oluşturulabilir.

### **Yol Ayarlayarak Oluşturma**
ImageOptions isim alanından PsdOptions oluşturun ve çeşitli özellikleri ayarlayın. Ayarlanması gereken en önemli özellik Source özelliğidir. Bu özellik, resim verilerinin nerede bulunduğunu (bir dosyada veya bir akışta) belirtir. Aşağıdaki örnekte, kaynak bir dosyadır. Özellikleri ayarladıktan sonra, nesneyi static Create yöntemlerinden birine genişlik ve yükseklik parametreleriyle birlikte geçirin. Genişlik ve yükseklik pikseller cinsindendir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}

### **Akış Kullanarak Oluşturma**
Bir akışı kullanarak bir resim oluşturma işlemi, bir yol kullanarak oluşturmaktan farklı değildir. Tek fark, bir Akış nesnesini oluşturup yapılandırarak onu Source özelliğine atamaktır.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}

## **Resim Dosyalarını Açma**
Geliştiriciler, Aspose.PSD for Java API'sini farklı amaçlar için var olan PSD resim dosyalarını açmak için kullanabilirler, örneğin resme efektler eklemek veya mevcut bir dosyayı başka bir formata dönüştürmek. Amacınız ne olursa olsun, Aspose.PSD, var olan dosyaları açmak için iki standart yol sağlar: dosyadan veya bir akıştan.
### **Diskten Açma**
Bir resim dosyasını Image sınıfı tarafından sağlanan Load statik yöntemine parametre olarak yol ve dosya adını geçirerek açın.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}

### **Akış Kullanarak Açma**
Bazen açmamız gereken resim bir akış olarak depolanmış olabilir. Bu tür durumlarda, Load yönteminin aşırı yüklü sürümünü kullanın. Bu, resmi açmak için bir Akış nesnesini argüman olarak kabul eder.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}

### **Katman Olarak Resmi Yükleme**
Bu makale, bir resmi bir katman olarak yükleme işlemini Aspose.PSD'nin kullanımını göstermektedir. Aspose.PSD API'leri, bu hedefe ulaşmak için verimli ve kullanımı kolay yöntemler sunmaktadır. Aspose.PSD, bir resmi bir PSD dosyasına katman olarak eklemek için PsdImage sınıfının AddLayer yöntemini açığa çıkarmıştır.

Bir resmi PSD içine katman olarak yükleme adımları aşağıda belirtilmiştir:

- Belirtilen genişlik ve yükseklikle PsdImage sınıfını kullanarak bir resim örneği oluşturun.
- Image sınıfı tarafından sağlanan Load fabrika yöntemi ile bir resmi bir PSD dosyası olarak yükleyin.
- Bir Layer sınıfının örneğini oluşturun ve PSD resim katmanını ona atayın.
- Oluşturulan katmanı PsdImage sınıfı tarafından sunulan AddLayer yöntemi kullanarak ekleyin.
- Sonuçları kaydedin.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}

## **Resim Dosyalarını Kaydetme**
Aspose.PSD, resim dosyalarını sıfırdan oluşturmanızı sağlar. Ayrıca mevcut resim dosyalarını düzenlemenin yollarını da sağlar. Resim oluşturulduğunda veya değiştirildiğinde genellikle dosya diske kaydedilir. Aspose.PSD, resimleri diske bir yol belirterek veya bir Akış nesnesi kullanarak kaydetme yöntemleri sağlar.
### **Diske Kaydetme**
Image sınıfı bir resim nesnesini temsil eder, bu nedenle bu sınıf, bir resim dosyası oluşturmak, yüklemek ve kaydetmek için gereken tüm araçları sağlar. Resimleri kaydetmek için Image sınıfının Save yöntemini kullanın. Save yönteminin aşırı yüklenmiş bir versiyonu dosya konumunu bir dize olarak kabul eder.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}

### **Akışa Kaydetme**
Save yönteminin başka bir aşırı yüklenmiş versiyonu, Akış nesnesini bir argüman olarak kabul eder ve resim dosyasını akışa kaydeder.

Eğer resim, Image sınıfının başlatılması sırasında herhangi bir CreateOptions belirtilerek oluşturulursa, resim, Image sınıfının başlatılması sırasında sağlanan yol veya akışa otomatik olarak kaydedilir ve parametre kabul etmeyen Save yöntemi çağrılarak diske kaydedilir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}

### **Eksik Fontları Değiştirmek İçin Ayarlar**
Geliştiriciler, mevcut PSD resim dosyalarını yüklemek için Aspose.PSD for Java API'sini kullanabilirler; örneğin, PSD belgelerini raster resme (PNG, JPG ve BMP formatlarında) dönüştürürken varsayılan font adını ayarlamak. Bu varsayılan font, mevcut İşletim Sisteminden bulunamayan tüm eksik fontlar için bir değiştirme olarak kullanılmalıdır. Resim değiştirildiğinde, dosya diske kaydedilir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}

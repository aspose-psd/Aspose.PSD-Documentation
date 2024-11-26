---
title: PSD Dosyalarını Oluşturma, Açma ve Kaydetme
type: docs
weight: 10
url: /tr/java/psd-dosyalarini-olusturma-acma-ve-kaydetme/
---

## **Görüntüyü PSD'ye Aktarma**
PSD, PhotoShop belgesi, Adobe PhotoShop'un görüntülerle çalışmak için kullandığı varsayılan dosya biçimidir. Aspose.PSD, dosyaları PSD biçimine yükleme, düzenleme ve kaydetme olanağı sağlar; böylece dosyalar PhotoShop'ta açılıp düzenlenebilir. Bu makalede, Aspose.PSD ile bir dosyayı PSD biçimine kaydetmenin nasıl yapılacağı ve bu formata kaydedilirken kullanılabilecek bazı ayarlar ele alınmaktadır. PsdOptions, görüntüleri PSD biçimine dışa aktarmak için kullanılan ImageOptions isim alanında uzmanlaşmış bir sınıftır. PSD'ye aktarmak için bir Image sınıfının örneğini oluşturun, var olan bir görüntü dosyasından yüklendiğinden (örneğin küçük resimler) veya sıfırdan oluşturulduğundan emin olun. Bu makale, bu durumu açıklar. Aşağıdaki örneklerde bir görüntü sıfırdan oluşturulmaktadır. Oluşturulduktan ve piksel verisi doldurulduktan sonra, görüntüyü Image sınıfı Save yöntemini kullanarak kaydedin ve ikinci argüman olarak bir PsdOptions nesnesini sağlayın. PsdOptions sınıfının birkaç özelliği ileri düzey dönüşüm için ayarlanabilir. Bazı özellikler, ColorMode, CompressionMethod ve Version'dır. Aspose.PSD, CompressionMethod numaralandırması aracılığıyla aşağıdaki sıkıştırma yöntemlerini destekler:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Aşağıdaki renk modları, ColorModes numaralandırması aracılığıyla desteklenmektedir:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



PSD v4.0, v5.0 ve üstü için küçük resim kaynakları veya PSD v4.0 ve üstü için ızgara ve kılavuz kaynakları gibi ek kaynaklar ekleyebilirsiniz. Aşağıdaki kod, sıfırdan bir BMP dosyası oluşturur, pikselleri doldurur ve bu dosyayı RLE sıkıştırma ve gri renk moduna sahip bir PSD dosyasına kaydeder. Aşağıdaki kod parçacığı, Görüntüyü PSD'ye Dışa Aktarma işlemini nasıl yapacağınızı gösterir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuleriDegistirmeVeCevirme-PSD-GoruntuyuPSDyeDısarıAktar-GoruntuyuPSDyeDısarıAktar.java" >}}
## **PSD Katmanına Görüntü İthal etme**
Bu makale, Aspose.PSD kullanarak bir görüntüyü PSD katmanına eklemeyi veya içe aktarmayı göstermektedir. Aspose.PSD API'ları, bu amaca ulaşmak için verimli ve kolay kullanımı olan yöntemler sunmaktadır. Aspose.PSD, bir görüntüyü PSD dosyasına eklemek veya içe aktarmak için Layer sınıfının DrawImage yöntemini ortaya çıkarmıştır. DrawImage yöntemi, bir görüntüyü PSD dosyasına eklemek veya içe aktarmak için konum ve görüntü değerlerini gerektirir. Görüntüyü PSD katmanına içe aktarma adımları aşağıda basitçe belirtilmiştir:

- Image sınıfı tarafından sunulan Load fabrika yöntemiyle bir PSD dosyasını bir görüntü olarak yükleyin.
- Bir Layer sınıfı örneği oluşturun ve PSD görüntü katmanını ona atayın.
- Eklenmesi gereken görüntüyü yükleyin veya sıfırdan bir tane oluşturun.
- Location ve görüntü örneğini belirterek Layer.DrawImage yöntemini çağırın.
- Sonuçları kaydedin.



Aşağıdaki kod parçacığı, bir görüntüyü PSD katmanına nasıl içe aktaracağını gösterir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuleriDegistirmeVeCevirme-PSD-PsdKatmanınaGoruntuIthalEt-PsdKatmanınaGoruntuIthalEt.java" >}}


## **PSD Dosyalarından Küçük Resimler Oluşturma**
PSD, Adobe'nin Photoshop uygulamasının yerli belge biçimidir. Adobe Photoshop (5.0 sürümü ve sonrası), görüntülerin önizleme görüntülemesi için küçük resim bilgilerini bir görüntü kaynak bloğunda depolar; bu blok, başlangıçta 28 bayt başlık ve ardından RGB (kırmızı, yeşil, mavi) sırasında JFIF küçük resimini içerir. Aspose.PSD API'si, PSD dosyasının kaynaklarına erişmek için kullanımı kolay bir mekanizma sağlar. Bu kaynaklar, uygulama gereksinimlerine göre alınabilir ve diske kaydedilebilir küçük resim kaynağı da içerir. Aşağıdaki kod parçacığı, PSD Dosyalarından Küçük Resimler Oluşturmanın nasıl yapılacağını gösterir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuleriDegistirmeVeCevirme-PSD-PsdDosyalarındanKucukResimlerOlusturma-PsdDosyalarındanKucukResimlerOlusturma.java" >}}


## **İndeksli PSD Dosyaları Oluşturma**
Aspose.PSD for Java API, sıfırdan İndeksli PSD dosyaları oluşturabilir. Bu makale, PsdOptions ve PsdImage sınıflarının kullanımını göstererek Çizilen şekilleri yeni oluşturulan tuval üzerine çizmek için İndeksli bir PSD oluşturmayı göstermektedir. İndeksli PSD dosyası oluşturmak için aşağıdaki basit adımlar gerekmektedir:

- PsdOptions örneği oluşturun ve kaynak belirleyin.
- PsdOptions'ın ColorMode özelliğini ColorModes.Indexed olarak ayarlayın.
- RGB uzayından renk paleti oluşturun ve PsdOptions'ın Palette özelliği olarak ayarlayın.
- Gereken sıkıştırma algoritmasını CompressionMethod özelliğine ayarlayın.
- PsdImage.Create yöntemini çağırarak yeni bir PSD görüntüsü oluşturun.
- Grafik çizin veya gereksinimlere göre diğer işlemleri gerçekleştirin.
- Tüm değişiklikleri kaydetmek için PsdImage.Save yöntemini çağırın.



Aşağıdaki kod parçacığı, indeksli PSD dosyaları oluşturmanın nasıl yapılacağını gösterir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuleriDegistirmeVeCevirme-PSD-CreateIndexedPSDDosyaları-CreateIndexedPSDDosyaları.java" >}}
## **PSD Katmanını Raster Görüntüye Aktarma**
Aspose.PSD for Java, bir PSD dosyasındaki katmanları raster görüntülere aktarmanıza olanak tanır. Lütfen katmanı görüntüye aktarmak için Aspose.PSD.FileFormats.Psd.Layers.Layer.Save yöntemini kullanın. Aşağıdaki örnek kod, bir PSD dosyasını yükler ve her bir katmanını Aspose.PSD.FileFormats.Psd.Layers.Layer.Save kullanarak PNG görüntüsüne dışa aktarır. Tüm katmanlar PNG görüntülerine aktarıldıktan sonra, bunları favori görüntü görüntüleyicinizle açabilirsiniz. Aşağıdaki kod parçacığı, PSD katmanını raster görüntüye nasıl aktaracağınızı gösterir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuleriDegistirmeVeCevirme-PSD-ExportPSDKatmanınıRasterGoruntuye-PSDKatmanınıRasterGoruntuyeExport.java" >}}

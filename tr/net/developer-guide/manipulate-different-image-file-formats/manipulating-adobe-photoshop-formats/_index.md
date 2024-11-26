---
title: Adobe Photoshop Biçimlerini Manipüle Etmek
type: docs
weight: 20
url: /tr/net/manipulating-adobe-photoshop-formats/
---

## **PSD Katmanlarını Diğer Katmanlara Birleştirme**

## **Resmi PSD Olarak Dışa Aktarma**
PSD, Adobe Photoshop'un görüntülerle çalışmak için kullandığı varsayılan dosya biçimidir. Aspose.PSD, dosyaları PSD olarak yüklemenize, düzenlemenize ve kaydetmenize olanak tanır, böylece bunlar Photoshop'ta açılıp düzenlenebilir. Bu makale, Aspose.PSD ile bir dosyayı PSD olarak nasıl kaydedeceğinizi gösterir ve bu formata kaydederken kullanılabilecek bazı ayarları tartışır. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions), PSD'ye resimleri dışa aktarmak için kullanılan [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) ad alanındaki uzmanlaşmış bir sınıftır. PSD'ye dışa aktarmak için bir Image sınıfı örneği oluşturun, mevcut bir resim dosyasından yüklenen bir resim (örneğin küçük resimler) veya baştan oluşturulan. Bu makale bu işlemi açıklar. Aşağıdaki örneklerde, bir resim baştan oluşturulur. Oluşturulduktan ve piksel verileri doldurulduktan sonra, resmi Image sınıfı Büyütmek yöntemini kullanarak kaydedin ve ikinci bağımsız değişken olarak bir PsdOptions nesnesi sağlayın. PsdOptions sınıfına ait birkaç özellik gelişmiş dönüşüm için ayarlanabilir. Bazı özellikler ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) ve Version'dur. Aspose.PSD, CompressionMethod numaralandırması aracılığıyla aşağıdaki sıkıştırma yöntemlerini destekler:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Aşağıdaki renk modları, [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes) numaralandırmasıyla desteklenir:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


PSD v4.0, v5.0 ve daha yüksek için küçük resim kaynakları veya PSD v4.0 ve daha yüksek için ızgara ve rehber kaynakları gibi ek kaynaklar eklenmelidir. Aşağıdaki kod, bir Resim dosyası baştan oluşturur, pikselleri doldurur ve RLE sıkıştırması ve gri tonlama renk moduyla PSD olarak kaydeder. Aşağıdaki kod parçası Resmi PSD'ye nasıl dışa aktaracağınızı gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Örnekler-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}

## **Resmi PSD Katmanına İçe Aktarma**
Bu makale, bir resmi PSD katmanına eklemenin veya içe aktarmanın Aspose.PSD kullanımını göstermektedir. Aspose.PSD API'leri bu hedefe ulaşmak için etkili ve kolay kullanımlı yöntemler sunmuştur. Aspose.PSD, bir resmi PSD dosyasına bir resim eklemek veya içe aktarmak için Katman sınıfının [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) yöntemini açığa çıkarmıştır. DrawImage yöntemi, bir resmi PSD dosyasına eklemek veya içe aktarmak için konum ve resim değerlerine ihtiyaç duyar. Bir resmi PSD katmanına bir resim eklemenin adımları aşağıdaki gibi basittir:

- Image sınıfı tarafından sağlanan Load fabrika yöntemi kullanılarak bir resim olarak bir PSD dosyasını yükle.
- Bir Layer sınıfının bir örneğini bir Png, Jpeg, Tiff, Gif, Bmp, Psd veya j2k dosyasından oluştur. 
- Layer sınıfını AddLayer yöntemini kullanarak Psd'ye ekleyin.
- Sonuçları kaydedin.

Aşağıdaki kod parçası, resmi PSD katmanına nasıl içe aktaracağınızı gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Örnekler-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

## **PSD Katmanlarındaki Renk Değiştirme**
Bu makale, Aspose.PSD'nin bir PSD katmanına resim eklemenin veya içe aktarmanın kullanımını göstermektedir. Aspose.PSD API'lerinin bu hedefe ulaşmak için etkili ve kolay kullanımlı yöntemler sunduğunu belirtmek önemlidir. Aspose.PSD, PSD dosyasına resim eklemek veya içe aktarmak için Katman sınıfının DrawImage yöntemini açığa çıkarmıştır. DrawImage yöntemi, bir resmi PSD dosyasına eklemek veya içe aktarmak için konum ve resim değerlerine ihtiyaç duyar. Bir resmi PSD katmanına bir resim eklemenin adımları aşağıdaki gibi basittir:


- Image sınıfı tarafından sağlanan Load fabrika yöntemi kullanılarak bir resmi PSD dosyasını yükle.
- Layer sınıfının bir örneğini oluşturun ve PSD görüntü katmanını buna atayın.
- Eklenmesi veya baştan bir resim oluşturulması gereken resmi yükleyin.
- Konumu ve resim örneğini belirterek Layer.DrawImage yöntemini çağırın.
- Sonuçları kaydedin.


Aşağıdaki kod parçası, resmi PSD katmanına nasıl içe aktaracağınızı gösterir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Örnekler-CSharp-Aspose-ResimleriDüzenlemeVeDönüştürme-PSD-RenkDeğiştirme-PSD-RenkDeğiştirme.cs" >}}

## **PSD Dosyalarından Küçük Resimler Oluşturma**
PSD, Adobe Photoshop uygulamasının yerel belge biçimidir. Adobe Photoshop (5.0 sürümü ve sonrası) bir resmin önizleme görüntüsü için önizleme görüntüsü için thumbnail bilgilerini içeren bir resim kaynak bloğunda JFIF küçük resmi içeren başlangıçta 28 bayt başlık ve ardından RGB (kırmızı, yeşil, mavi) sırasında a JFIF küçük resmi saklar. Aspose.PSD API, PSD dosyasının kaynaklarına erişmek için kolay kullanımlı bir mekanizma sağlar. Bu kaynaklar ayrıca uygulama ihtiyaçlarına göre alınabilir ve disc'e kaydedilebilir. Aşağıdaki kod parçası, PSD dosyalarından küçük resimler oluşturmanın nasıl yapılacağını gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Örnekler-CSharp-Aspose-ResimleriDüzenlemeVeDönüştürme-PSD-PsdDosyalarındanKüçükResimlerOluşturma-PsdDosyalarındanKüçükResimlerOluşturma.cs" >}}

## **İndeksli PSD Dosyaları Oluşturma**
Aspose.PSD for .NET API, baştan İndeksli PSD dosyaları oluşturabilir. Bu makale, PsdOptions ve [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) sınıflarını kullanarak İndeksli PSD oluşturmanın nasıl yapılacağını göstermektedir. İndeksli bir PSD dosyası oluşturmak için aşağıdaki basit adımlar gereklidir:

- Bir PsdOptions örneği oluşturun ve kaynağını ayarlayın.
- PsdOptions'un ColorMode özelliğini ColorModes.Indexed olarak ayarlayın.
- RGB alanından yeni bir renk paleti oluşturun ve bu paleti PsdOptions'un Palette özelliğine ayarlayın.
- CompressionMethod özelliğini gerekli sıkıştırma algoritmasına ayarlayın.
- PsdImage'in [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) yöntemini çağırarak yeni PSD resmi oluşturun.
- Görüntüler çizin veya diğer işlemleri gerçekleştirin.
- Tüm değişiklikleri kaydetmek için PsdImage.Save yöntemini çağırın.

Aşağıdaki kod parçası, nasıl İndeksli PSD dosyaları oluşturulacağını gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Örnekler-CSharp-Aspose-ResimleriDüzenlemeVeDönüştürme-PSD-IndeksliPSDDosyalarıOluşturma-IndeksliPSDDosyalarıOluşturma.cs" >}}

## **PSD Katmanını Raster (Yayıcı) Görüntüye Aktarma**
Aspose.PSD for .NET, PSD dosyasındaki katmanları raster (yayıcı) görüntülere dışa aktarmanıza olanak tanır. Lütfen, katmanı görüntüye dışa aktarmak için [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) yöntemini kullanın. Aşağıdaki örnek kod, bir PSD dosyası yükler ve her bir katmanını, Aspose.PSD.FileFormats.Psd.Layers.Layer.Save kullanarak PNG görüntüsüne dışa aktarır. Tüm katmanlar PNG görüntülerine dışa aktarıldıktan sonra, bunları favori görüntü görüntüleyicinizle açabilirsiniz. Aşağıdaki kod parçası, bir PSD katmanını raster (yayıcı) bir görüntüye dışa aktarmanın nasıl yapıldığını gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Örnekler-CSharp-Aspose-ResimleriDüzenlemeVeDönüştürme-PSD-PSDKatmanınıRasterGörüntüyeAktarma-PSDKatmanınıRasterGörüntüyeAktarma.cs" >}}

## **PSD Dosyasındaki Metin Katmanını Güncelleme**
Aspose.PSD for .NET, bir PSD dosyasındaki metni manipüle etmenize olanak tanır. Lütfen, metni PSD katmanındaki metni güncellemek için [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) sınıfını kullanın. Aşağıdaki kod parçası, bir PSD dosyasını yükler, metin katmanına erişir, metni günceller ve [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index) yöntemini kullanarak yeni bir adla PSD dosyasını kaydeder.

{{< gist "aspose-com-gists" "8a4d34ce856c7c0ce974175" "Örnekler-CSharp-Aspose-ResimleriDüzenlemeVeDönüştürme-PSD-MetinKatmanınıGüncelleme-PSD-MetinKatmanınıGüncelleme.cs" >}}

## **Yassalı PSD Algılama**
Aspose.PSD for .NET, belirli bir PSD dosyasının yassalaştırılıp yassallaştırılmadığını belirlemenize olanak tanır. Bu işlevselliği elde etmek için Aspose.PSD.FileFormats.Psd.PsdImage sınıfındaki IsFlatten özelliği tanıtılmıştır. Aşağıdaki kod parçası, bir PSD dosyasını yükler ve [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten) özelliğine erişir.

{{< gist "aspose-com-gists" "8a4d34ce856c7c0ce974175" "Örnekler-CSharp-Aspose-ResimleriDüzenlemeVeDönüştürme-PSD-YassalaştırılanPSDAAlgılama-YassalaştırılanPSDAAlgılama.cs" >}}

## **PSD Katmanlarını Birleştirme**
Bu makale, Aspose.PSD ile bir PSD dosyasındaki katmanları birleştirmenin yolunu gösterirken, bir PSD dosyasını JPG formatına dönüştürür. Aşağıdaki örnekte, var olan bir PSD dosyası, dosya yolu Image sınıfının statik Load yöntemi aracılığıyla geçirilerek yüklenir. Yüklendikten sonra, resmi PsdImage biçimine dönüştürür/dönüştürür. Bir JpegOptions sınıfının bir örneği oluşturulur ve farklı özellikleri ayarlanır. Şimdi PsdImage örneğinin Save yöntemini çağırabilirsiniz. Aşağıdaki kod parçası, PSD katmanlarını nasıl birleştireceğinizi gösterir.

{{< gist "aspose-com-gists" "8a4d34ce856c7c0ce974175" "Örnekler-CSharp-Aspose-ResimleriDüzenlemeVeDönüştürme-PSD-PSDKatmanlarınıBirleştirme-PSDKatmanlarınıBirleştirme.cs" >}}

## **RGB İle Alfa İçeren Gri Tonlama Desteği İçin PSD**
Bu makale, Aspose.PSD ile bir PSD dosyasını PNG formatına dönüştürürken, PSD dosyasında RGB ile alfa için gri tonlama desteğini nasıl uygulayacağınızı gösterir. Aşağıdaki örnekte, var olan bir PSD dosyası, dosya yolu Image sınıfının statik Load yöntemi aracılığıyla geçirilerek yüklenir. Yüklendikten sonra, resmi PsdImage biçimine dönüştürür/dönüştürür. Bir PngOptions sınıfının bir örneği oluşturulur ve farklı özellikleri ayarlanır. [ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) özelliğini TruecolorWithAlpha olarak ayarlayın. Şimdi PngOptions örneğinin Save yöntemini çağırabilirsiniz. Aşağıdaki kod parçası, gri tonlama ve alfa ile PNG'ye nasıl dönüştürüleceğini gösterir.

{{< gist "aspose-com-gists" "8a4d34ce856c7c0ce974175" "Örnekler-CSharp-Aspose-ResimleriDüzenlemeVeDönüştürme-PSD-RenkDeğiştirme-PSD-RenkDeğiştirme.cs" >}}
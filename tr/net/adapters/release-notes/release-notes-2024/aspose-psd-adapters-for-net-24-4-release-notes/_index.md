---
title: Aspose.PSD Adaptörler için .NET 24.4 - Sürüm Notları
type: docs
weight: 100
url: /tr/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD Adaptörler için .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/) sürümü için sürüm notlarını içerir

{{% /alert %}}

| **Anahtar** | **Özet**                                                             | **Kategori** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Aspose.PSD.Adapters.Imaging'in Nuget'e yayınlanması                   | Geliştirme   |


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- Hiçbiri

# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**

Lütfen [Aspose.PSD.Adaptörler belgelendirme sayfasına](/tr/psd/net/adapters) bakın

**PSDNET-1985. Aspose.PSD.Adaptörlerin kullanımının en kapsamlı örneği**

{{< highlight csharp >}}
// Adaptörleri başlatma yapılandırmanıza ekleyin
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// Ek olarak, Dışa Aktarıcıları etkinleştirin
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Adaptörlerle çalışabilmek için hem Aspose.PSD hem de adapte Lisanslara ihtiyacınız vardır
// İşte Aspose.PSD Lisansını nasıl uygulayacağınız
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// İşte Aspose.Imaging için adapte Lisansının nasıl uygulanacağına dair bir örnek
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Daha sonra, herhangi bir adaptör veya PSD veya Imaging kütüphanesi kodunu çalıştırabilirsiniz

// Bundan sonra, bu dosyaların Aspose.PSD ile ek bir kod olmadan açılabilir, sadece şunu kullanın
using (var img = Aspose.PSD.Image.Load("BazıDosya.Webp")) 
{
    // Bu kodun çalıştırılmasından sonra, WEBP'den oluşturulan PSD Dosyasını alacak ve Aspose.PSD Filtreleri, Katmanları ve Warp Dönüşümü de dahil olmak üzere herhangi bir Aspose.PSD Filtresini, Katmanı ve Düzenlemesini uygulayabilirsiniz
}

// Ek olarak, Dışa Aktarıcıların görüntülerini PSD Formatına dönüştürebilirsiniz
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Imaging özgü özelliklerle WEBP dosyasını düzenlemek için Aspose.Imaging API'sini kullanın
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Ardından, sadece ToPsdImage() yöntemini kullanın ve PSD gibi dosyaları Photoshop benzeri özelliklerle düzenleyin
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Bazı metin", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Aspose.PSD kullanarak nihai PSD dosyasını kaydedin
        psdImage.Save("çıktı.psd");
    }
}

// Adaptörler tarafından sağlanan Yükleyicileri veya Dışa Aktarıcıları kullanmanıza gerek yoksa bunları devre dışı bırakın
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}

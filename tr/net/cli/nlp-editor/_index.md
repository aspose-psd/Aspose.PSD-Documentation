---
title: Aspose.PSD CLI NLP Editör Uygulaması için .NET
type: docs
weight: 10
url: /tr/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Aracı NLP Doğal Dil İşleme PSD Konsol C# Kütüphane PSD API
description: Aspose.PSD tabanlı NLP Editör CLI uygulaması, PSD, PSB ve AI Dosya Biçimleri için. Kod Yok CI/CD Otomasyonu. PSD dosyalarını düzenlemek için doğal dil işleme destekler. Çeşitli işlemleri yapmak için doğal dilde isteğinizi yazmanız yeterli, dönüştürme, ayarlama, yeniden boyutlandırma vb. Adobe Photoshop veya Adobe Illustrator kurulu olmasını gerektirmez ve ek kod olmadan konsoldan çalıştırılabilir.
---

**![Aspose.PSD for .NET Ürün Logosu](home_1.png)**

**.NET için Aspose.PSD NLP Editör CLI Uygulamasına Hoş Geldiniz**

Aspose.PSD CLI NLP Editör Uygulaması, doğal dil komutlarını kullanarak PSD dosyalarını düzenlemek için hafif bir konsol yardımcı programıdır. CI/CD Akışlarına kolay entegrasyon.

**Sorumluluk Reddi** 

Bu deneysel bir uygulamadır. Lütfen deneyin ve geribildirimde bulunun. Her türlü geribildirim çok değerlidir. Kod Yok uygulamayı bir üst seviyeye taşımak istiyoruz. Herhangi bir yapı sürecine veya iş sürecine kolay entegrasyon hedefimizdir.

**.NET için Aspose.PSD NLP Editör CLI Uygulamasının Temel İşlevselliği**

1. Doğal dil komutlarını kullanarak PSD, PSB, AI dosyalarında işlemler gerçekleştirme.
2. Dönüştürme, ayarlama, yeniden boyutlandırma vb. gibi çeşitli işlemleri destekler.
3. Kod yok CI/CD otomasyonu.
4. PSD dosyalarını düzenlemek için doğal dile istek yazmayı destekler.

## **Komut Satırından Kullanım:**

{{% alert color="primary" %}}
İlk olarak bu dotnet aracını yükleyin:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

İlk kullanımdan önce aşağıdaki komutu çalıştırmanızı öneririz:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Bu komuttan sonra bu uygulamayı Aspose.PSD.CLI.NLP.Editor yerine kısa adı nlp.cli ile çalıştırabileceksiniz. Kendi kısa adınızı belirtebilirsiniz.
{{% /alert %}}

**Aspose.PSD.CLI.Crop Uygulaması İçin Kullanılabilir Parametreler** 

| **Argüman**   | **Açıklama**                             |
|:-------------|:----------------------------------------   |
| herhangi metin  | Gerekli. PSD veya PSB Dosyasını güncellemek için doğal dil komutunuz                             |
| lisans         | Lisans dosyasının yolu.                               |
| detaylı          | Belirli bir komut hakkında daha fazla bilgi görüntüler.                             |
| kurulum        | Hızlı çağrı için araçlar klasörüne bat dosyası oluşturur. Örnek: --setup psd.nlp. Sonrasında aracı psd.nlp komutuyla çağırabilirsiniz.                     |

**Kullanım Örnekleri**

1. Bu komut, mevcut klasördeki ilk bulunan dosyayı (Aspose.PSD ile açılabilen) png formatına şeffaflıkla kaydedecektir. Ayrıca lisans kurulumu yapılacaktır. Lisansı yalnızca bir kez belirtmeniz gerekmektedir. Sonraki çalışmalarda lisans belirtilen yol üzerinde kullanılacaktır. Bu komut, mevcut olduğunda NLP işlemi ayrıntılı günlüğünü gösterecektir.
{{< highlight bash >}}
  nlp.cli Bu klasörden png formatına alpha ile dönüştür ve lisans "C:\Aspose\LisansDosyası.lic --detaylı "
{{< /highlight >}}

2. Bu komut, "smth.psd" ile en benzer adıma sahip dosyayı bulacaktır. Ardından kontrastı ayarlayacak ve en iyi kalitede jpeg olarak kaydedecektir. Çıktı dosyasının adı yazdırılacaktır. Bu smth.jpg olacaktır.
{{< highlight bash >}}
Kontrastı 10 ayarlama ve smth.psd dosyasındaki elliğin adında bir katmanı bul ve bunu en iyi kalitede output.jpg olarak kaydet
{{< /highlight >}}

3. Bu komut, belirtilen yolundaki dosyayı bulacak, boyutunu %25'e indirecek ve çıktı dosyasını yazdıracaktır. Dosya konsolun mevcut klasöründe kaydedilecektir.
{{< highlight bash >}}
C:\Kullanıcılar\bazı_kullanıcı\Masaüstü\input.psd dosyasını %25 oranında boyutlandır
{{< /highlight >}}

4. Bu komut, C:\Kullanıcılar\bazı_kullanıcı\Masaüstü\ içindeki input.psd dosyasını bulacaktır. Ardından indeksi 3 olan katmanı bulacak ve genişliği 50px, yüksekliği 100px olacak şekilde boyutlandıracaktır. Daha sonra bu katman, C:\Kullanıcılar\bazı_kullanıcı\Masaüstü\output.pdf olarak PDF olarak kaydedilecektir.
{{< highlight bash >}}
3 indeksli katmanı boyutlandır, genişliği 50 ve yüksekliği 100 olan C:\Kullanıcılar\bazı_kullanıcı\Masaüstü\input.psd dosyası ve C:\Kullanıcılar\bazı_kullanıcı\Masaüstü\output.pdf olarak kaydet
{{< /highlight >}}

5. Bu komut, mevcut klasördeki smth.psd dosyasını açacak ancak tüm efektler devre dışı bırakılacaktır. Daha sonra bu dosyayı BMP formatına çevirecek ve output.bmp olarak mevcut klasöre kaydedecektir.
{{< highlight bash >}}
Efektler olmadan smth.psd dosyasını aç ve output.bmp olarak kaydet
{{< /highlight >}}

**Lütfen iş akışınıza PSD, PSB ve AI Biçimleri desteği eklemeniz gerekiyorsa, diğer [Aspose.PSD CLI Uygulamalarını](https://docs.aspose.com/psd/net/cli) kontrol edin** 

1. [Aspose.PSD CLI Dönüştür](/psd/tr/net/cli/donustur)
2. [Aspose.PSD CLI Kırpma](/psd/tr/net/cli/krpma)
3. [Aspose.PSD CLI Boyutlandırma](/psd/tr/net/cli/boyutlandirma)
4. [Aspose.PSD CLI Dışa Aktar](/psd/tr/net/cli/dışa-aktar)
5. [Aspose.PSD CLI NLP Editör](/psd/tr/net/cli/nlp-editor)

**Lütfen Aspose.PSD for .NET veya [diğer platformları](https://releases.aspose.com/psd) kontrol edin** 

Aspose.PSD CLI Uygulamaları, popüler işlemler için kullanıma hazır bir çözümdür. Esnek bir çözüm gerekiyorsa, lütfen Aspose.PSD'nin tam sürümünü kontrol edin.

1. [Aspose.PSD for .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD for Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD for Python via .NET](https://releases.aspose.com/psd/python-net/)

## **.NET İçin Aspose.PSD Kaynakları**

Aşağıdaki bağlantılar, görevlerinizi başarıyla tamamlamanız için ihtiyacınız olan bazı faydalı kaynaklara yönlendirme yapar.

- [.NET için Aspose.PSD CLI Uygulamaları Çevrimiçi Belgeleri](/psd/tr/net/cli/dönüştürme)
- [.NET için Aspose.PSD CLI Uygulamaları Yayın Notları](/psd/tr/net/cli/dönüştürme/yayın-notları/)
- [.NET için Aspose.PSD CLI Uygulamaları Ürün Sayfası](https://products.aspose.com/psd/net/cli)
- [.NET için Aspose.PSD API Referans Kılavuzu](https://reference.aspose.com/net/psd)
- [GitHub Deposundan Örnekleri İndirin](https://github.com/aspose-psd/CLI-Applications)
- [.NET için Aspose.PSD Ücretsiz Destek Forumu](https://forum.aspose.com/c/psd)
- [.NET için Aspose.PSD Ücretli Destek Yardımı](https://helpdesk.aspose.com/)


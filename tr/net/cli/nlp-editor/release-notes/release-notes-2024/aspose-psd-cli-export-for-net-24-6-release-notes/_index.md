---
title: Aspose.PSD CLI NLP Düzenleyicisi için .NET 24.6 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD CLI NLP Düzenleyicisi için .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/) sürümü için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                                                      | **Kategori**  |
|:------------|:----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI Uygulamalarının İlk Sürümü: Aspose.PSD.CLI.Export ve Aspose.PSD.CLI.NLP.Düzenleyici | Geliştirme    |


## **Kullanım örnekleri:**

**PSDNET-2110. Aspose.PSD CLI NLP Düzenleyici Uygulamasının İlk Sürümü**

## **Komut satırından kullanım:**

{{% alert color="primary" %}}
Öncelikle bu dotnet aracını yükleyin:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

İlk kullanımdan önce aşağıdaki komutu çalıştırmanızı öneririz:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Bu komuttan sonra bu uygulamayı kısa adı olan nlp.cli adıyla çalıştırabilirsiniz. Kendi kısa adınızı belirleyebilirsiniz.
{{% /alert %}}

**Kullanım Örnekleri**

1. Bu komut, mevcut klasörde bulunan ilk dosyayı (aspose.psd ile açılabilen) alacak ve onu şeffaflıkla png formatına dönüştürecek. Ayrıca lisans kurulacak. Lisansı sadece bir kez belirtmeniz gerekmektedir. Sonraki çalışmalarda lisans belirtilen yoldan kullanılacaktır. Bu komut, NLP işleminin ayrıntılı günlüğünü, varsa, gösterecektir.
{{< highlight bash >}}nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. Bu komut, "smth.psd" adına en benzer isme sahip dosyayı bulacak. Bu dosyanın karşıtlığını ayarlayacak ve en iyi kalitede jpeg olarak kaydedecek. Çıkış dosyasının adı yazdırılacak. Bu smth.jpg olacak 
{{< highlight bash >}}Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality{{< /highlight >}}

3. Bu komut ise belirtilen yol üzerindeki dosyayı eğecek ve boyutunu %25 oranında azaltacak. Çıkış dosyası yazdırılacak. Bu, konsolun mevcut klasörüne kaydedilecektir.
{{< highlight bash >}}Resize file C:\Users\someuser\Desktop\input.psd to 25%{{< /highlight >}}

4. Bu komut, C:\Users\someuser\Desktop\ içindeki input.psd dosyasını bulacak. Ardından, 3 numaralı dizindeki katmanı bulacak ve genişliğini 50 piksel, yüksekliğini 100 piksel olarak değiştirecek. Daha sonra bu katman, C:\Users\someuser\Desktop\output.pdf içine PDF olarak kaydedilecektir.
{{< highlight bash >}}Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

 5. Bu komut, mevcut klasördeki smth.psd dosyasını açacak, ancak tüm efektler devre dışı bırakılacaktır. Daha sonra bu dosya BMP formatına dönüştürülecek ve output.bmp olarak mevcut klasöre kaydedilecektir.
 {{< highlight bash >}}Open smth.psd without effects and save it to output.bmp{{< /highlight >}}

**Not**

Bu deneysel bir uygulamadır. Lütfen deneyin ve geribildirim bırakın. Her türlü geribildirim çok değerlidir. NO-Kod uygulamasını bir sonraki seviyeye taşımak istiyoruz. Kolay entegrasyon, herhangi bir yapı boru hattına veya iş sürecine hedefimizdir.

---
title: Aspose.PSD for .NET 21.6 - Sürüm Notları
type: docs
weight: 70
url: /tr/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-546|Grup için kırpma maskesinin doğru şekilde oluşturulmaması|Hata|
|PSDNET-547|Bir katman grubu için normal veya vektör maskenin görmezden gelinmesi|Hata|
|PSDNET-647|Devre dışı bırakılmış vektör katman maskelerine sahip PSD resminin kaydedilmesi ile vektör maskelerin etkinleştirilmesi|Hata|
|PSDNET-786|255 karakterden uzun metin içeren bir TextLayer oluşturulurken hata alınması|Hata|
|PSDNET-900|Text katmanının metni Linux üzerinde görüntülenememesi|Geliştirme|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- Yok

# **Kaldırılan API'lar:**
- Yok

## **Kullanım örnekleri:**

**PSDNET-546. Grup için kırpma maskesinin doğru şekilde oluşturulmaması**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Bir katman grubu için normal veya vektör maskenin görmezden gelinmesi**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. Devre dışı bırakılmış vektör katman maskelerine sahip PSD resminin kaydedilmesi ile vektör maskelerin etkinleştirilmesi**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. 255 karakterden uzun metin içeren bir TextLayer oluşturulurken hata alınması**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}

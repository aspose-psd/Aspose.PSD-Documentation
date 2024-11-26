---
title: Aspose.PSD for Java 21.6 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) için sürüm notlarını içerir. {{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-351|Bir grup için kırpmalı maske doğru şekilde oluşturulmaz|Hata|
|PSDJAVA-352|Bir katman grubu için düzenli veya vektör maskesi oluşturulmadığında göz ardı edilir|Hata|
|PSDJAVA-353|Vektör katman maskeleri devre dışı bırakılmış PSD görüntüsü vektör maskeleri etkinleştirmekte|Hata|
|PSDJAVA-354|255 karakterden uzun metin içeren bir TextLayer oluşturulurken istisna oluşur|Hata|

# **Genel API Değişiklikleri**
# **Yeni Eklenen API'ler:**
- Yok

# **Kaldırılan API'ler:**
- Yok

# **Kullanım örnekleri:**

**PSDJAVA-351. Bir grup için kırpmalı maske doğru şekilde oluşturulmaz**

{{< highlight java >}}
        String kaynakDosyaAdi = "AppleClip.psd";
        String ciktiDosyaAdi = "sonuc.png";

        PsdImage görüntü = (PsdImage) Image.load(kaynakDosyaAdi);
        try
        {
            görüntü.save(ciktiDosyaAdi, new PngOptions());
        }finally {
            görüntü.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Bir katman grubu için düzenli veya vektör maskesi oluşturulmadığında göz ardı edilir**

{{< highlight java >}}
        String kaynakDosyaAdi = "Stripes3Mask.psd";
        String ciktiDosyaAdi = "CıktıStripes3Mask.png";

        PsdImage görüntü = (PsdImage)Image.load(kaynakDosyaAdi);
        try
        {
            görüntü.save(ciktiDosyaAdi, new PngOptions());
        }finally {
            görüntü.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. Vektör katman maskeleri devre dışı bırakılmış PSD görüntüsü vektör maskeleri etkinleştirmekte**

{{< highlight java >}}
        String kaynakDosyaAdi = "FourWithMasksVd.psd";
        String ciktiDosyaAdi = "FourWithMasksVdCıktı.psd";

        PsdImage görüntü = (PsdImage) Image.load(kaynakDosyaAdi);
        try
        {
            görüntü.save(ciktiDosyaAdi);
        }finally {
            görüntü.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. 255 karakterden uzun metin içeren bir TextLayer oluşturulurken istisna oluşur**

{{< highlight java >}}
        String cikti = "çıktı.psd";

        PsdImage görüntü = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String metin = new String(chars);
            görüntü.addTextLayer(metin, Rectangle.getEmpty());

            görüntü.save(cikti);
        }finally {
            görüntü.dispose();
        }
{{< /highlight >}}

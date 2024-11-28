---
title: Aspose.PSD for Java 23.8 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-23-8-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) için sürüm notlarını içerir. {{% /alert %}}

| **Anahtar**  | **Özet**                                                                                                                                     | **Kategori** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Yeni bir eğim türü ekleyin (Bayrak)                                                                                                          | Özellik      |
| PSDJAVA-519 | Yeni eğim türleri eklendi: yukarı yay, aşağı yay, küre                                                                                      | Özellik      |
| PSDJAVA-520 | Yeni Posterize katmanı eklemek için PsdImage.AddPosterizeAdjustmentLayer yöntemini uygulayın                                               | Özellik     |
| PSDJAVA-521 | Sadece açma ve kaydetme işlemi sırasında PSD bilgileri kayboldu                                                                             | Hata         |
| PSDJAVA-522 | Görüntü yüklenemedi                                                                                                                        | Hata         |
| PSDJAVA-523 | Görüntü yüklenemedi: Tanınmayan tipteki bir nesneyi Tanımlayıcı Yapı türüne dönüştürememe                                         | Hata         |
| PSDJAVA-524 | 3. taraf kütüphanesinde değişiklik yapılması PSD dosyasını bozuyor ancak Photoshop'ta açılabilir                               | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **Kaldırılan API'ler:**

- Hiçbiri

## **Kullanım örnekleri:**

**PSDJAVA-518. Yeni bir eğim türü ekleyin (Bayrak)**

{{< highlight java >}}
    String kaynakDosya = "src/main/resources/flag_warp.psd";
    String çıktıDosyası = "src/main/resources/flag_export.png";

    PsdLoadOptions psdYüklemeSeçenekleri = new PsdLoadOptions();
    psdYüklemeSeçenekleri.setAllowWarpRepaint(true);
    psdYüklemeSeçenekleri.setLoadEffectsResource(true);
    try (PsdImage psdİmaj = (PsdImage) Image.load(kaynakDosya, psdYüklemeSeçenekleri)) {
        PngOptions pngSeçenekleri = new PngOptions();
        pngSeçenekleri.setColorType(PngColorType.TruecolorWithAlpha);

        psdİmaj.save(çıktıDosyası, pngSeçenekleri);
    }
{{< /highlight >}}

**PSDJAVA-519. Yeni eğim türleri eklendi: yukarı yay, aşağı yay, küre**

{{< highlight java >}}
    String kaynakDosyaYayYukarı = "src/main/resources/arc_upper_warp.psd";
    String kaynakDosyaYayAşağı = "src/main/resources/arc_lower_warp.psd";
    String kaynakDosyaÇıkıntı = "src/main/resources/bulge_warp.psd";

    String çıktıDosyaYayYukarı = "src/main/resources/ArcUpper_export.png";
    String çıktıDosyaYayAşağı = "src/main/resources/ArcLower_export.png";
    String çıktıDosyaÇıkıntı = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdYüklemeSeçenekleri = new PsdLoadOptions();
    psdYüklemeSeçenekleri.setAllowWarpRepaint(true);
    psdYüklemeSeçenekleri.setLoadEffectsResource(true);

    PngOptions pngSeçenekleri = new PngOptions();
    pngSeçenekleri.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdİmaj = (PsdImage) Image.load(kaynakDosyaYayYukarı, psdYüklemeSeçenekleri)) {
        psdİmaj.save(çıktıDosyaYayYukarı, pngSeçenekleri);
    }

    try (PsdImage psdİmaj = (PsdImage) Image.load(kaynakDosyaYayAşağı, psdYüklemeSeçenekleri)) {
        psdİmaj.save(çıktıDosyaYayAşağı, pngSeçenekleri);
    }

    try (PsdImage psdİmaj = (PsdImage) Image.load(kaynakDosyaÇıkıntı, psdYüklemeSeçenekleri)) {
        psdİmaj.save(çıktıDosyaÇıkıntı, pngSeçenekleri);
    }
{{< /highlight >}}

**PSDJAVA-520. Yeni bir Posterize katmanı eklemek için PsdImage.AddPosterizeAdjustmentLayer yöntemini uygulayın**

{{< highlight java >}}
public static void main(String[] args) {
    String srcDosya = "src/main/resources/zendeya.psd";
    String çıktıDosyası = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage psdİmaj = (PsdImage) Image.load(srcDosya)) {
        psdİmaj.addPosterizeAdjustmentLayer();
        psdİmaj.save(çıktıDosyası);
    }

    PsdLoadOptions psdYüklemeSeçenekleri = new PsdLoadOptions();
    psdYüklemeSeçenekleri.setLoadEffectsResource(true);

    // Kaydedilen değişiklikleri kontrol et
    try (PsdImage imaj = (PsdImage) Image.load(çıktıDosyası, psdYüklemeSeçenekleri)) {
        assertAreEqual(2, imaj.getLayers().length);

        PosterizeLayer posterizeKatmanı = (PosterizeLayer) imaj.getLayers()[1];

        assertAreEqual(true, posterizeKatmanı instanceof PosterizeLayer);
    }
}

static void assertAreEqual(Object beklenen, Object gerçek) {
    assertAreEqual(beklenen, gerçek, "Nesneler eşit değil.");
}

static void assertAreEqual(Object beklenen, Object gerçek, String mesaj) {
    if (!beklenen.equals(gerçek)) {
        throw new IllegalArgumentException(mesaj);
    }
}
{{< /highlight >}}

**PSDJAVA-521. Sadece açma ve kaydetme işlemi sırasında PSD bilgileri kayboldu**

{{< highlight java >}}
    String kaynak = "src/main/resources/Orjinal dosya.psd";
    String çıktıPsd = "src/main/resources/out_Orjinal dosya.psd";
    String çıktıPng = "src/main/resources/out_Orjinal dosya.png";

    try (PsdImage psdİmaj = (PsdImage) Image.load(kaynak)) {
        PngOptions pngSeçenekleri = new PngOptions();
        pngSeçenekleri.setColorType(PngColorType.TruecolorWithAlpha);

        psdİmaj.save(çıktıPsd);
        psdİmaj.save(çıktıPng, pngSeçenekleri);
    }
{{< /highlight >}}

**PSDJAVA-522. Görüntü yüklenemedi**

{{< highlight java >}}
    String dosya1 = "src/main/resources/test_text.psd";
    String dosya2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdİmaj = (PsdImage) Image.load(dosya1)) {
    }

    try (PsdImage psdİmaj = (PsdImage) Image.load(dosya2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Görüntü yüklenemedi: Tanınmayan tipteki bir nesneyi Tanımlayıcı Yapı türüne dönüştürememe**

{{< highlight java >}}
   try (PsdImage yeniPsd = new PsdImage(10, 10)) {
        yeniPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream bellekAkışı = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            yeniPsd.save(bellekAkışı.toOutputStream());

            bellekAkışı.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            bellekAkışı.write(new byte[1], 0, 0);
            bellekAkışı.setPosition(0);

            try (PsdImage psdİmaj = (PsdImage) Image.load(bellekAkışı.toInputStream())) {
                // Doğru bir şekilde yüklenmelidir
            }
        } finally {
            bellekAkışı.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. 3. taraf kütüphanesinde yapılan değişiklikler PSD dosyasını bozuyor ancak Photoshop'ta açılabilir**

{{< highlight java >}}
    String kaynakDosya = "src/main/resources/output.psd";
    String çıktıDosyası = "src/main/resources/export.png";

    PsdLoadOptions psdYüklemeSeçenekleri = new PsdLoadOptions();
    psdYüklemeSeçenekleri.setLoadEffectsResource(true);

    try (PsdImage resim = (PsdImage) Image.load(kaynakDosya, psdYüklemeSeçenekleri)) {
        PngOptions pngSeçenekleri = new PngOptions();
        pngSeçenekleri.setCompressionLevel(9);
        pngSeçenekleri.setColorType(PngColorType.TruecolorWithAlpha);

        resim.save(çıktıDosyası, pngSeçenekleri);
    }
{{< /highlight >}}

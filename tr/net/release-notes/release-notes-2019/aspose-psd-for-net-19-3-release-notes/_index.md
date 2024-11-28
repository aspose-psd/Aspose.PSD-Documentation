---
title: Aspose.PSD için .NET 19.3 - Sürüm Notları
type: docs
weight: 100
url: /tr/net/aspose-psd-for-net-19-3-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, Aspose.PSD için .NET 19.3'e ilişkin sürüm notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-104|Dönüşüm Matrisi tarafından döndürülen Metin Katmanlarının Oluşturulması|Özellik|
|PSDNET-96|Dışa aktarma için Renk Dolgulu Vuruş efektinin uygulanması|Özellik|
|PSDNET-112|InnerData Dönüştürücüler, bazı vektör maskeleri içeren katmanları bozar|Hata|
|PSDNET-113|Photoshop'ta açıldığında PSD görüntüsü için metin katmanını güncelleştirme hatası verir|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- Yok
# **Kaldırılan API'lar:**
- Yok

## **Kullanım örnekleri:**
**PSDNET-104. Dönüşüm Matrisi tarafından döndürülen Metin Katmanlarının Oluşturulması**

{{< highlight java >}}

 string kaynakDosyaAdı = "DönüştürülmüşMetin.psd";

string dışaAktarmaYolu = "DönüştürülmüşMetinDışaAktarma.psd";

string dışaAktarmaPngYolu = "DönüştürülmüşMetinDışaAktarma.png";

var im = (PsdImage) Image.Load(kaynakDosyaAdı);

using(im) {

 im.Save(dışaAktarmaYolu);

 im.Save(dışaAktarmaPngYolu, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

}      

{{< /highlight >}}

**PSDNET-96. Dışa aktarma için Renk Dolgulu Vuruş efektinin uygulanması**

{{< highlight java >}}

  // Dışa aktarma için Renk Dolgulu Vuruş efektinin uygulanması

 string kaynakDosyaAdı = "VuruşKarmaşık.psd";

 string dışaAktarmaYolu = "VuruşKarmaşıkOluşturma.psd";

 string dışaAktarmaPngYolu = "VuruşKarmaşıkOluşturma.png";

 var yüklemeSeçenekleri = new PsdLoadOptions() {

  LoadEffectsResource = true

 };

 using(var im = (PsdImage) Image.Load(kaynakDosyaAdı, yüklemeSeçenekleri)) {

  for (int i = 0; i < im.Layers.Length; i++) {

   var efekt = (StrokeEffect) im.Layers[i].BlendingOptions.Effects[0];

   var ayarlar = (ColorFillSettings) efekt.FillSettings;

   ayarlar.Color = Color.DeepPink;

  }

  // Psd kaydet

  im.Save(dışaAktarmaYolu, new PsdOptions());

  // Png kaydet

  im.Save(dışaAktarmaPngYolu, new PngOptions() {

   ColorType = PngColorType.TruecolorWithAlpha

  });

 }         

{{< /highlight >}}

**PSDNET-112. InnerData Dönüştürücüleri, bazı vektör maskeleri içeren katmanları bozar**

{{< highlight java >}}

 // InnerData Dönüştürücüleri, bazı vektör maskeleri içeren katmanları bozar

var kaynakDosya = "1.psd";

var pngYolu = "DöndürDevirTest2617.png";

var psdYolu = "DöndürDevirTest2617.psd";

var döndürmeTürü = RotateFlipType.Rotate270FlipXY;

using(var im = (PsdImage)(Image.Load(kaynakDosya))) {

 im.RotateFlip(döndürmeTürü);

 im.Save(pngYolu, new PngOptions() {

  ColorType = PngColorType.TruecolorWithAlpha

 });

 im.Save(psdYolu);

}

{{< /highlight >}}

**PSDNET-113. Photoshop'ta açıldığında PSD görüntüsü için metin katmanını güncelleştirme hatası verir**

{{< highlight java >}}

 string kaynakDosyaAdı = "Test.psd";

string dışaAktarmaYolu = "Sonuç.psd";

using(Image görüntü = Image.Load(kaynakDosyaAdı)) {

 if (!(görüntü is PsdImage)) {

  return;

 }

 PsdImage psdGörüntü = (PsdImage) görüntü;

 Layer[] katmanlar = psdGörüntü.Layers;

 for (int indeks = katmanlar.Length - 1; indeks >= 0; indeks--) {

  Layer katman = katmanlar[indeks];

  if (!(katman is TextLayer)) {

   continue;

  }

  TextLayer metinKatmanı = (TextLayer) katman;

  metinKatmanı.UpdateText("\\()");

 }

 PsdOptions görüntüSeçenekleri = new PsdOptions(psdGörüntü);

 psdGörüntü.Save(dışaAktarmaYolu, görüntüSeçenekleri);

}

// Dosya, istisnasız olarak açılmalı ve Photoshop için okunabilir olmalıdır

using(Image görüntü = Image.Load(dışaAktarmaYolu)) {}

{{< /highlight >}}

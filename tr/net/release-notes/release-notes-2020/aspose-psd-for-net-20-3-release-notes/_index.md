---
title: Aspose.PSD for .NET 20.3 - Sürüm Notları
type: docs
weight: 100
url: /tr/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa [Aspose.PSD for .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-188|.Net Core Desteği|Özellik|
|PSDNET-523|Adobe Illustrator dosyalarını PDF'e dönüştürme|Özellik|
|PSDNET-212|Tek metin katmanında farklı stilleri renderlama yeteneği ekleme|Özellik|
|PSDNET-144|Siyah ve Beyaz Ayarlama Katmanı Desteği|Özellik|
|PSDNET-233|AI formatını (Sürüm 8) diğer formatlara dönüştürme desteği ekleme|Özellik|
|PSDNET-540|PassThrough Karıştırma Modu işleme desteği (Yalnızca Katman Grubu için kullanılır)|Özellik|
|PSDNET-539|Boş Unicode Alpha Adı Kaynaklı görüntü yüklemesinde hata: Görüntü yüklemesi başarısız|Hata|
|PSDNET-541|Bir Katman Grubunun görünürlüğünü değiştirdikten sonra yanlış çıktı|Hata|
|PSDNET-516|PSD görüntüsü yüklerken hata: Renk bölümü (DropShadow Kaynağı) RGB için 3 renk bileşeni veya CMYK için 4 renk bileşeni içermelidir|Hata|
|PSDNET-536|Yeni oluşturulan katmana çizim yapmaya çalışıldığında hata oluşması durumu: Constructor'ın basit sürümü kullanılırsa hata oluşabilir|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Yok
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Üstsimge
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Altsimge
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.Yok
- F:Aspose.PSD.FileFormats.Psd.FontCaps.KüçükHarf
- F:Aspose.PSD.FileFormats.Psd.FontCaps.TümBüyükHarf
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Yok
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ÖzDeğişken
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Özİtalik
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Altçizgi
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Üstçizgi
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.YazıtipiTabançizgisi
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.TabanSatırKayması
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.YazıtipiHarfBüyüklüğü
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ParçalarÜret(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **Kaldırılan API'ler:**
- Yok

## **Kullanım örnekleri:**
**PSDNET-523. Adobe Illustrator dosyalarını PDF'e dönüştürme**

{{< highlight java >}}

 string kaynakDosya = "rect2_color.ai";

using (var aiGörüntüsü = (AiImage)Image.Load(kaynakDosya))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Bir metin katmanında farklı stilleri renderlama yeteneği ekleme**

{{< highlight java >}}

 string kaynakDosya = "text212.psd";

string etalonDosya = "Ethalon_text212.psd";

string çıktıDosyası = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(kaynakDosya))

{

    TextLayer metinKatmanı = (TextLayer)img.Layers[1];

    IText metinVerisi = metinKatmanı.TextData;

    ITextStyle varsayılanStil = metinVerisi.ParçaÜret().Stil;

    ITextParagraph varsayılanParagraf = metinVerisi.ParçaÜret().Paragraf;

    varsayılanStil.RenkDoldur = Renk.KoyuGri;

    varsayılanStil.YazıBoyutu = 51;

    metinVerisi.Öğeler[1].Stil.Üstçizgi = true;

    ITextPortion[] yeniParçalar = metinVerisi.ParçalarÜret(new string[] { "E=mc",  "2\r",  "Kalın",  "İtalik\r",  "Küçükharf" }, varsayılanStil, varsayılanParagraf);

    yeniParçalar[0].Stil.Altçizgi = true; // yazı stili "E=mc" güncelle

    yeniParçalar[1].Stil.YazıtipiTabançizgisi = FontBaseline.Üstsimge; // yazı stili "2\r" güncelle

    yeniParçalar[2].Stil.ÖzDeğişken = true; // yazı stili "Kalın" güncelle

    yeniParçalar[3].Stil.Özİtalik = true; // yazı stili "İtalik\r" güncelle

    yeniParçalar[3].Stil.TabanSatırKayması = -25; // yazı stili "İtalik\r" güncelle

    yeniParçalar[4].Stil.YazıtipiHarfBüyüklüğü = FontCaps.KüçükHarf; // yazı stili "Küçükharf" güncelle

    foreach (var yeniParça in yeniParçalar)

    {

        metinVerisi.ParçaEkle(yeniParça);

    }

    metinData.GüncelleKatmanVerisi();

    img.Save(çıktıDosyası);

}

{{< /highlight >}}

**PSDNET-233. AI formatını (Sürüm 8) diğer formatlara dönüştürme desteği ekleme**

{{< highlight java >}}

 // AI dosyasının PSD ve PNG formatına dönüştürülmesi örneği

string kaynakDosyaAdı = "form_8.ai";

string çıktıDosyaAdı = "form_8_export";

using (AiImage image = (AiImage)Image.Load(kaynakDosyaAdı))

{

    image.Save(çıktıDosyaAdı + ".psd", new PsdOptions());

    image.Save(çıktıDosyaAdı + ".png", new PngOptions() { RenkTipi = PngRenkTipi.GerçekrenkAlfaile });

}

{{< /highlight >}}

**PSDNET-540. PassThrough Karıştırma Modu işleme desteği (Yalnızca Katman Grubu için kullanılır)**

{{< highlight java >}}

 void DoğruMu(bool koşul, string mesaj)

{

    if (!koşul)

    {

        throw new FormatException(mesaj);

    }

}

string kaynakDosyaAdı = "Apple.psd";

string çıktıDosyaAdı = "Çıktı" + kaynakDosyaAdı;

using (PsdImage image = (PsdImage)Image.Load(kaynakDosyaAdı))

{

    DoğruMu(image.Katmanlar.Uzunluk >= 23, "23. katman bulunamadı.");

    var katman = image.Katmanlar[23] as LayerGroup;

    DoğruMu(katman != null, "23. katman bir katman grubu değil.");

    DoğruMu(katman.Adı == "AyarGrubu", "23. katman adı 'AyarGrubu' değil.");

    DoğruMu(katman.KarıştırmaModuAnahtarı == KarıştırmaModu.PassThrough, "AyarGrubu katmanı 'geçiş' karıştırma moduna sahip olmalıdır.");

    image.Save(çıktıDosyaAdı, new PsdOptions());

    image.Save("ÇıktıApple.png", new PngOptions() { RenkTipi = PngRenkTipi.GerçekrenkAlfaile });

    katman.KarıştırmaModuAnahtarı = KarıştırmaModu.Normal;

    image.Save("Normal" + çıktıDosyaAdı, new PsdOptions());

    image.Save("NormalÇıktıApple.png", new PngOptions() { RenkTipi = PngRenkTipi.GerçekrenkAlfaile });

}

{{< /highlight >}}

**SPSDNET-180. Metin katmanı metnini güncelleme özel durumu**

{{< highlight java >}}

 // Metin katmanı metnini güncellemek özel durumu

string dosyaYolu = "FlipDikey.psd";

string çıktıYolu = "FlipDikey_değiştirilmiş.psd";

var yeniMetin = "Test";

using (var görüntü = Image.Load(dosyaYolu))

{

    var psdGörüntüsü = görüntü as PsdImage;

    if (image == null)

    {

        return;

    }

    var katmanlar = psdGörüntüsü.Katmanlar;

    for (var indeks = katmanlar.Uzunluk - 1; indeks >= 0; indeks--)

    {

        var katman = katmanlar[indeks] as TextLayer;

        if (katman == null)

        {

            continue;

        }

        katman.MetniGüncelle(yeniMetin);

    }

    var görüntüSeçenekleri = new PsdOptions(psdGörüntü);

    psdGörüntüsü.Kaydet(çıktıYolu, görüntüSeçenekleri);

}

{{< /highlight >}}

**PSDNET-182. Döndürme ve Yansıtma işleminden sonra PSD görüntüsünü kaydetmek, açılamayan bozuk bir dosyayı oluşturur.**

{{< highlight java >}}

 string kaynakDosyaAdı = "1.psd";

RotateFlipType yansıtmaTürü = RotateFlipType.Rotate270FlipXY;

string çıkışDosyaAdıPsd = "DöndürYansıtTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(kaynakDosyaAdı))

{

    image.RotateFlip(yansıtmaTürü);

    image.Save(çıkışDosyaAdıPsd);

}

// Herhangi bir hata olmadan çalıştırılmalı

using (PsdImage image = (PsdImage)Image.Load(çıkışDosyaAdıPsd)) 

{

    // Hiçbir şey yapılmamalı

}

{{< /highlight >}}

**PSDNET-539. Boş Unicode Alpha Adı Kaynaklı görüntü yüklemesinde hata**

{{< highlight java >}}

 string kaynakDizin = "apple.psd";

using (var psdGörüntüsü = (PsdImage)Image.Load(kaynakDizin)) // Burada hiçbir hata almamalıyız

{

    // hiçbir şey yapma

}

{{< /highlight >}}

**PSDNET-541. Bir Katman Grubunun görünürlüğünü değiştirdikten sonra yanlış çıktı**

{{< highlight java >}}

 string kaynakDosya = "giriş.psd";

string çıktıDosyası = "çıktı.psd";

// Katman isimlerinde değişiklik yap ve kaydet

using (var görüntü = (PsdImage)Image.Load(kaynakDosya))

{

    for (int i = 0; i < görüntü.Katmanlar.Uzunluk; i++)

    {

        var katman = görüntü.Katmanlar[i];

        // Grup içindeki her şeyi kapat

        if (katman is LayerGroup)

        {

            katman.Görünür = false;

        }

    }

    görüntü.Kaydet(çıktıDosyası);

}

{{< /highlight >}}

**PSDNET-516. PSD görüntüsü yüklerken hata: Renk bölümü (DropShadow Kaynağı) RGB için 3 renk bileşeni veya CMYK için 4 renk bileşeni içermelidir**

{{< highlight java >}}

 string kaynakDosya = "sss0136=GUID-SSS0136=1=ar-sa=Düşük.psd";

using (var img = (PsdImage)Image.Load(kaynakDosya)) // Burada hiçbir hata almamalıyız

{

    // hiçbir şey yapma

}

{{< /highlight >}}

**PSDNET-536. Basit Sürümünü Kullanırken Yeni Oluşturulan Katmana Çizim Yapmaya Çalışırsanız Hata Alırsınız**

{{< highlight java >}}

 string çıktıDosyası = "çıktı.psd";

int genişlik = 100;

int yükseklik = 100;

using (var görüntü = new PsdImage(genişlik, yükseklik))

{

    var katman = new Katman();

    katman.Alta = yükseklik;

    katman.Sağa = genişlik;

    görüntü.KatmanEkle(katman);

    Grafik grafik = new Grafik(katman);

    grafik.Temizle(Renk.Sarı);

    // Kalem aracı ile bir dikdörtgen çiz

    grafik.DikdörtgenÇiz(new Kalem(Renk.Kırmızı), new Rectangle(30, 10, 40, 80));

    // Mavi renkte Solid Brush ile başka bir dikdörtgen çiz

    grafik.DikdörtgenÇiz(new Kalem(new SabitFırça(Renk.Mavi)), new Rectangle(10, 30, 80, 40));

    görüntü.Kaydet(çıktıDosyası);

}

{{< /highlight >}}


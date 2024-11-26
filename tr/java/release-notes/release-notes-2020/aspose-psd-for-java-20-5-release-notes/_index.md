---
title: Aspose.PSD for Java 20.5 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-20-5-sürüm-notları/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) için sürüm notlarını içermektedir. {{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-188|Belge dönüşüm ilerlemesine destek|Özellik|
|PSDJAVA-197|Kanal başına 16 bit ile Grayscale Renk Modu PSD görüntü kaydetme desteği|Özellik|
|PSDJAVA-198|Nvrt Kaynağının (Ters Ayar Katmanı Kaynağı) desteği|Özellik|
|PSDJAVA-200|Katman Grupları için Katman Maskelerini destekle|Özellik|
|PSDJAVA-195|16 bit kanala sahip Grayscale Renk Modlu PSD görüntüsünü 16 bit kanala sahip RGB PSD formatına kaydetme hatası düzeltildi|Hata|
|PSDJAVA-196|16 bit kanala sahip Grayscale Renk Modlu PSD görüntüsünü 8 bit kanala sahip Grayscale PSD formatına kaydetme hatası düzeltildi|Hata|
|PSDJAVA-199|Sağdan sola diller için ITextParçacığı ile Metin Hizalamanın çalışmaması. Çıktı dosyası hasarlıdır.|Hata|
|PSDJAVA-201|Lab Renkli ve 8 bit/kanalı olan belirli Psd dosyasını açmaya çalışırken oluşan istisna|Hata|
# **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- Yok
## **Kaldırılan API'lar:**
- Yok
# **Kullanım örnekleri:**

**PSDJAVA-188. Belge dönüşüm ilerlemesine destek**

{{< highlight java >}}

 // Yükleme ve kaydetme işlemleri için ilerleme işleyicisinin kullanımına ilişkin bir örnek.

// Program, ilerleme olaylarını tetiklemek için farklı kaydetme seçenekleri kullanmaktadır.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// İlerleme bilgilerini konsola yazan bir ilerleme işleyicisi oluştur

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s out of %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Apple.psd Yükleme ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Yükleme ilerlemesini göstermek için ilerleme işleyicisini bağla

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Belirli yükleme seçeneklerini kullanarak PSD yükle

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Apple.psd'yi PNG formatına kaydetme ----------");

    PngOptions pngOptions = new PngOptions();

    // Çıktı görüntüsünü renkli ve saydam olmayacak şekilde yap

    pngOptions.setColorType(PngColorType.Truecolor);

    // Kaydetme ilerlemesini göstermek için ilerleme işleyicisini bağla

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Belirli özelliklere sahip PSD dosyasını PNG'ye dönüştür

    image.save(outputStream, pngOptions);

    System.out.println("---------- Apple.psd'yi PSD formatına kaydetme ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Çıktıyı renkli yap

    psdOptions.setColorMode(ColorModes.Rgb);

    // Her renk için (kırmızı, yeşil ve mavi) bir kanal ve bir bileşik kanal ayarla

    psdOptions.setChannelsCount((short)4);

    // Kaydetme ilerlemesini göstermek için ilerleme işleyicisini bağla

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Belirli özelliklere sahip bir PSD kopyasını kaydet

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Kanal başına 16 bit ile Grayscale Renk Modu PSD görüntü kaydetme desteği**

{{< highlight java >}}

 // Belirli katmanlar için farklı renk modları, kanal başına bit sayıları, kanal

// sayıları ve sıkıştırmaların uygulama örneği.

// Bir yöntemi yerel kapsamdan erişilebilir yap.

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String dosya,

            short renkModu,

            short kanalBitSayısı,

            short kanalSayısı,

            short sıkıştırma,

            int katmanNumarası)

    {

        String dosyaYolu = dosya + ".psd";

        String ek = Enum.getName(ColorModes.class, renkModu) + kanalBitSayısı + "_" +

                kanalSayısı + "_" + Enum.getName(CompressionMethod.class, sıkıştırma);

        String dışaAktarmaYolu = dosya + ek + ".psd";

        String pngDışaAktarmaYolu = dosya + ek + ".png";

        // Tanımlı 16-bit Grayscale PSD'yi yükle

        PsdImage image = (PsdImage)Image.load(dosyaYolu);

        try

        {

            RasterCachedImage raster = katmanNumarası >= 0 ? image.getLayers()[katmanNumarası] : image;

            // Katmanın çevresinde gri bir iç kenar çizen

            Graphics graphics = new Graphics(raster);

            int genişlik = raster.getWidth();

            int yükseklik = raster.getHeight();

            Rectangle rect = new Rectangle(

                    genişlik / 3,

                    yükseklik / 3,

                    genişlik - (2 * (genişlik / 3)) - 1,

                    yükseklik - (2 * (yükseklik / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Renk modu değiştirilmiş PSD'nin bir kopyasını kaydet

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(renkModu);

            psdOptions.setChannelBitsCount(kanalBitSayısı);

            psdOptions.setChannelsCount(kanalSayısı);

            psdOptions.setCompressionMethod(sıkıştırma);

            image.save(dışaAktarmaYolu, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // Kaydedilmiş PSD'yi yükle

        PsdImage image1 = (PsdImage)Image.load(dışaAktarmaYolu);

        try

        {

            // Kaydedilmiş PSD'yi bir Grayscale PNG görüntüsüne dönüştür

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngDışaAktarmaYolu, pngOptions); // burada istisna olmamalı

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Nvrt Kaynağının (Ters Ayar Katmanı Kaynağı) desteği**

{{< highlight java >}}

 // Bir ters ayar katmanının Nvrt Kaynağını bulma örneği.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// İçeren bir ters ayar katmanı bulunduran önceden tanımlanmış bir PSD'yi yükle

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Ters ayar katmanının kaynağını bulmaya çalış

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Nvrt Kaynağı bulundu

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Katman Grupları için Katman Maskelerini destekle**

{{< highlight java >}}

 // Katman grupları için katman maskelerini destekleme örneği. Program, PSD'yi yükler ve kaydeder

// farklı çıktı biçimlerine, istisnanın atılmamasını sağlar.

String kaynakDosya = "psdnet595.psd";

String cıktıPng = "cıktı.png";

String cıktıPsd = "cıktı.psd";

// Katman grupları için katman maskeleri içeren tanımlı bir PSD'yi yükle

PsdImage giriş = (PsdImage)Image.load(kaynakDosya);

try

{

    // Yüklenen PSD'yi PNG'ye dönüştür

    giriş.save(cıktıPng, new PngOptions());

    // PSD'nin bir kopyasını kaydet

    giriş.save(cıktıPsd);

}

finally

{

    giriş.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. 16 bit kanala sahip Grayscale Renk Modlu PSD görüntüsünü 16 bit kanala sahip RGB PSD formatına kaydetme hatası düzeltildi**

{{< highlight java >}}

 // 16-bit Grayscale bir PSD'yi 16-bit RGB'ye dönüştürme ve

// ardından 16-bit Grayscale ancak bir raster görüntüye geri dönme örneği.

String kaynakDosyaYolu = "grayscale5x5.psd";

String dışaAktarDosyaYolu = "rgb16bit5x5_cıktı.psd";

String pngDışaAktarYolu = "rgb16bit5x5_cıktı.png";

// Tanımlı 16-bit Grayscale PSD'yi yükle

PsdImage image = (PsdImage)Image.load(kaynakDosyaYolu);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Katmanın çevresinde gri bir iç kenar çizen

    Graphics graphics = new Graphics(raster);

    int genişlik = raster.getWidth();

    int yükseklik = raster.getHeight();

    Rectangle rect = new Rectangle(genişlik / 3, yükseklik / 3, genişlik - (2 * (genişlik / 3)) - 1, yükseklik - (2 * (yükseklik / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Renk modu RBG olarak değiştirilmiş PSD'nin bir kopyasını kaydet

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(dışaAktarDosyaYolu, psdOptions);

}

finally

{

    image.dispose();

}

// Kaydedilen PSD'yi yükle

PsdImage image1 = (PsdImage)Image.load(dışaAktarDosyaYolu);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Kaydedilen PSD'yi bir Grayscale PNG görüntüsüne dönüştür

    image1.save(pngDışaAktarYolu, pngOptions); // burada istisna olmamalı

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. 16 bit kanala sahip Grayscale Renk Modlu PSD görüntüsünü 8 bit kanala sahip Grayscale PSD formatına kaydetme hatası düzeltildi**

{{< highlight java >}}

 // 16-bit Grayscale bir PSD'yi 8-bit Grayscale'e dönüştürme ve

// ardından 8-bit Grayscale bir raster görüntüye geri dönme örneği.

String kaynakDosyaYolu = "grayscale16bit.psd";

String dışaAktarDosyaYolu = "grayscale16bit_cıktı.psd";

String pngDışaAktarYolu = "grayscale16bit_cıktı.png";

// Tanımlı 16-bit Grayscale PSD'yi yükle

PsdImage image = (PsdImage)Image.load(kaynakDosyaYolu);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Katmanın çevresinde gri bir iç kenar çizen

    Graphics graphics = new Graphics(raster);

    int genişlik = raster.getWidth();

    int yükseklik = raster.getHeight();

    Rectangle rect = new Rectangle(genişlik / 3, yükseklik / 3, genişlik - (2 * (genişlik / 3)) - 1, yükseklik - (2 * (yükseklik / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Kanal sayısı 8-bit yapılmış PSD'nin bir kopyasını kaydet

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(dışaAktarDosyaYolu, psdOptions);

}

finally

{

    image.dispose();

}

// Kaydedilen PSD'yi yükle

PsdImage image1 = (PsdImage)Image.load(dışaAktarDosyaYolu);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Kaydedilen PSD'yi bir Grayscale PNG görüntüsüne dönüştür

    image1.save(pngDışaAktarYolu, pngOptions); // burada istisna olmamalı

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Sağdan sola diller için ITextParçacığı ile Metin Hizalamanın çalışmaması. Çıktı dosyası hasarlıdır.**

{{< highlight java >}}

 // ITextParçacığı ile sağdan sola metin hizalama örneği. Program, yüklenmiş PSD'deki

// mevcut bir sağdan sola metin katmanını değiştirir ve değiştirilmiş belgenin bir kopyasını kaydeder.

String kaynakDosyaAdı = "bidi.psd";

String cıktıDosyaAdı = "bidiOutput.psd";

// Sağdan sola metin katmanı içeren bir PSD yükleyin

PsdImage image = (PsdImage
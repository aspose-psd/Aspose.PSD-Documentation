---
title: Aspose.PSD for Java 20.3 - Sürüm Notları
type: docs
weight: 10
url: /tr/java/aspose-psd-for-java-20-3-release-notes/
---

{{% alert color="primary" %}} Bu sayfa [Aspose.PSD for Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) için sürüm notlarını içermektedir. {{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-133|Adobe Illustrator dosyalarını PDF'lere dönüştürme|Özellik|
|PSDJAVA-134|Tek metin katmanında farklı stilleri oluşturma yeteneği ekleme|Özellik|
|PSDJAVA-135|Siyah ve Beyaz Ayarlama Katmanı desteği|Özellik|
|PSDJAVA-137|AI formatını diğer formatlara (Versiyon 8) dönüştürme desteği ekleme|Özellik|
|PSDJAVA-138|PassThrough Karıştırma Modu işleme desteği (Yalnızca Katman Grubu İçin Kullanılır).|Özellik|
|PSDJAVA-136|Boş Unicode Alfabe Adları Kaynağı ile görüntünün yüklenmesi başarısız oldu istisnası|Hata|
|PSDJAVA-139|Bir Katman Grubunun görünürlüğünü değiştikten sonra yanlış çıkış|Hata|
|PSDJAVA-140|PSD görüntüsü yüklenirken istisna: Renk bölümü (Gölge Kaynağı) RGB için 3 renk bileşeni veya CMYK için 4 renk bileşeni içermelidir|Hata|
|PSDJAVA-141|Basit Versiyon Kullanılırsa yeni oluşturulan katmana çizmeye çalışıldığında istisna oluşur|Hata|
# **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Aksayan
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **Kaldırılan API'lar:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)
# **Kullanım örnekleri:**
**PSDJAVA-133. Adobe Illustrator dosyalarını PDF'lere dönüştürme**

{{< highlight java >}}

 String inFile = "rect2_color.ai";

String outFile = "rect2_color.ai_output.pdf";

AiImage aiImage = (AiImage)Image.load(inFile);

try

{

    aiImage.save(outFile, new PdfOptions());

}

finally

{

    aiImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-134. Tek metin katmanında farklı stilleri oluşturma yeteneği ekleme**

{{< highlight java >}}

 String inFilePath = "text212.psd";

String outFilePath = "Output_text212.psd";

PsdImage image = (PsdImage)Image.load(inFilePath);

try

{

    TextLayer textLayer = (TextLayer)image.getLayers()[1];

    IText textData = textLayer.getTextData();

    ITextStyle defaultStyle = textData.producePortion().getStyle();

    ITextParagraph defaultParagraph = textData.producePortion().getParagraph();

    defaultStyle.setFillColor(Color.getDimGray());

    defaultStyle.setFontSize(51);

    textData.getItems()[1].getStyle().setStrikethrough(true);

    ITextPortion[] newPortions = textData.producePortions(new String[] { "E=mc",  "2\r",  "Koyu",  "Eğik\r",  "Küçükharfli metin" }, defaultStyle, defaultParagraph);

    newPortions[0].getStyle().setUnderline(true); // metni "E=mc" olarak düzenle

    newPortions[1].getStyle().setFontBaseline(FontBaseline.Süperskript); // metni "2\r" olarak düzenle

    newPortions[2].getStyle().setFauxBold(true); // metni "Koyu" olarak düzenle

    newPortions[3].getStyle().setFauxItalic(true); // metni "Eğik\r" olarak düzenle

    newPortions[3].getStyle().setBaselineShift(-25); // metni "Eğik\r" olarak düzenle

    newPortions[4].getStyle().setFontCaps(FontCaps.KüçükHarfler); // metni "Küçükharfli metin" olarak düzenle

    for (ITextPortion newPortion : newPortions)

    {

        textData.addPortion(newPortion);

    }

    textData.updateLayerData();

    image.save(outFilePath);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-135. Siyah ve Beyaz Ayarlama Katmanı desteği**

{{< highlight java >}}

 // Çalışma zamanında siyah beyaz ayarlama katmanı ekleme örneği

String inFileName = "Stripes.psd";

String outFileName = "Çıktı" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer newLayer = image.addBlackWhiteAdjustmentLayer();

    newLayer.setName("SiyahBeyazAyarlamaKatmanı");

    newLayer.setReds(22);

    newLayer.setYellows(92);

    newLayer.setGreens(70);

    newLayer.setCyans(79);

    newLayer.setBlues(7);

    newLayer.setMagentas(28);

    image.save(outFileName, new PsdOptions());

}

finally

{

    image.dispose();

}

// Siyah beyaz ayarlama katmanı desteği örneği

inFileName = "SiyaBeyazAyarlamaKatmanıStripesMask.psd";

outFileName = "Çıktı" + inFileName;

PsdImage image1 = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer blwhLayer = (BlackWhiteAdjustmentLayer)image1.getLayers()[1];

    blwhLayer.setReds(15);

    blwhLayer.setYellows(25);

    blwhLayer.setGreens(35);

    blwhLayer.setCyans(10);

    blwhLayer.setBlues(50);

    blwhLayer.setMagentas(105);

    blwhLayer.setUseTint(true);

    blwhLayer.setBwPresetKind(4);

    blwhLayer.setBlackAndWhitePresetFileName("bwPresetFileName");

    blwhLayer.setTintColorRed(60);

    blwhLayer.setTintColorGreen(80);

    blwhLayer.setTintColorBlue(200);

    image1.save(outFileName, new PsdOptions());

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-137. AI formatını diğer formatlara (Versiyon 8) dönüştürme desteği ekleme**

{{< highlight java >}}

 // AI dosyasını PSD ve PNG formatına dışa aktarma örneği

String inFileName = "form_8.ai";

String outFileNamePrefix = "form_8_dışa_aktarma";

AiImage image = (AiImage)Image.load(inFileName);

try

{

    image.save(outFileNamePrefix + ".psd", new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save(outFileNamePrefix + ".png", pngOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-138. PassThrough Karıştırma Modu işleme desteği (Yalnızca Katman Grubu İçin Kullanılır).**

{{< highlight java >}}

 class LocalScope

{

    void assertIsTrue(boolean condition, String message)

    {

        if (!condition)

        {

            throw new FormatException(message);

        }

    }

}

LocalScope localScope = new LocalScope();

String inFileName = "Apple.psd";

String outFileName = "Çıktı" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    localScope.assertIsTrue(image.getLayers().length >= 23, "23. katman yok.");

    LayerGroup layer = (LayerGroup)image.getLayers()[23];

    localScope.assertIsTrue(layer != null, "23. katman bir katman grubu değil.");

    localScope.assertIsTrue(layer.getName().equals("AyarGrubu"), "23. katmanın adı 'AyarGrubu' değil.");

    localScope.assertIsTrue(layer.getBlendModeKey() == BlendMode.PassThrough, "AyarGrubu katmanında 'pass through (aktar)' karıştırma modu olmalıdır.");

    image.save(outFileName, new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("ÇıktıApple.png", pngOptions);

    layer.setBlendModeKey(BlendMode.Normal);

    image.save("Normal" + outFileName, new PsdOptions());

    PngOptions pngOptions1 = new PngOptions();

    pngOptions1.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("NormalÇıktıApple.png", pngOptions1);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-136. Boş Unicode Alfabe Adları Kaynağı ile görüntünün yüklenmesi başarısız oldu istisnası**

{{< highlight java >}}

 String inFilePath = "elma.psd";

PsdImage psdImage = null;

try

{

    // Burada herhangi bir istisna olmamalı

    psdImage = (PsdImage)Image.load(inFilePath);

}

finally

{

    if (psdImage != null) psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-139. Bir Katman Grubunun görünürlüğünü değiştikten sonra yanlış çıkış**

{{< highlight java >}}

 String inFileName = "giriş.psd";

String outFileName = "çıktı.psd";

// Katman adlarında değişiklik yap ve kaydet

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    for (int i = 0; i < image.getLayers().length; i++)

    {

        Layer layer = image.getLayers()[i];

        // Bir grup içindeki her şeyi kapat

        if (layer instanceof LayerGroup)

        {

            layer.setVisible(false);

        }

    }

    image.save(outFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-140. PSD görüntüsü yüklenirken istisna: Renk bölümü (Gölge Kaynağı) RGB için 3 renk bileşeni veya CMYK için 4 renk bileşeni içermelidir**

{{< highlight java >}}

 String inFilePath = "sss0136=GUID-SSS0136=1=ar-sa=Düşük.psd";

PsdImage image = null;

try

{

    image = (PsdImage)PsdImage.load(inFilePath);

}

finally

{

    if (image != null) image.dispose();

}       

{{< /highlight >}}

**PSDJAVA-141. Basit Versiyon Kullanılırsa yeni oluşturulan katmana çizmeye çalışıldığında istisna oluşur**

{{< highlight java >}}

 String outputFile = "çıktı.psd";

int genişlik = 100;

int yükseklik = 100;

PsdImage image = new PsdImage(genişlik, yükseklik);

try

{

    Layer katman = new Layer();

    katman.setBottom(yükseklik);

    katman.setRight(genişlik);

    image.addLayer(katman);

    Graphics grafik = new Graphics(katman);

    graphic.clear(Color.getYellow());

    // Kalem aracıyla bir dikdörtgen çiz

    grafik.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

    // Mavi renkte Solid Fırça ile başka bir dikdörtgen çiz

    grafik.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));

    image.save(outputFile);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

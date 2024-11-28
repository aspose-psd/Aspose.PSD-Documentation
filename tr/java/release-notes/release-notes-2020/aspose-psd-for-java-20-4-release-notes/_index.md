---
title: Aspose.PSD for Java 20.4 - Sürüm Notları
type: docs
weight: 30
url: /tr/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) için sürüm notlarını içerir. {{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-156|'Vektör Köken Verileri' kaynağının desteklenmesi|Özellik|
|PSDJAVA-171|lclrResource (Sayfa rengi ayarı) desteği|Özellik|
|PSDJAVA-157|Uzunluk Kayıt verilerinden özelliklerin desteklenmesi. (Yol işlemleri (mantıksal işlemler), katman içinde şeklin dizini, Bezier düğüm kayıtlarının sayısı)|Özellik|
|PSDJAVA-158|Resim Bölümü Kaynak #1010 Arka plan renginin desteklenmesi|Özellik|
|PSDJAVA-161|Çalışma zamanında Doldurma Katmanlarının eklenmesi|Özellik|
|PSDJAVA-168|Resim Bölümü Kaynak #1009 Kenar bilgisinin desteklenmesi|Özellik|
|PSDJAVA-169|AI Format Dosyalarında Katmanların Desteklenmesi|Özellik|
|PSDJAVA-163|Gradyan Örtü Efekti'nin Okunması ve Düzenlenmesinin Desteklenmesi|Özellik|
|PSDJAVA-164|Gradyan Örtü Efekti'nin Oluşturulması|Özellik|
|PSDJAVA-149|Metin katmanının textData.items özelliğini alırken Aspose.PSD for java hatası|Hata|
|PSDJAVA-166|Grayscale ColorMode'a ve kanal başına 16 bit'e sahip PSD resminin grayscale PSD formatına kaydedilmesinin düzeltilmesi|Hata|
|PSDJAVA-167|Grayscale ColorMode'a ve kanal başına 16 bit'e sahip PSD resminin PNG formatına kaydedilmesinin düzeltilmesi|Hata|
|PSDJAVA-159|GradientOverlayEffect.BlendMode özelliği değişikliklerinin Photoshop'ta gösterilmemesi|Hata|
# **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
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
## **Kaldırılan API'ler:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **Kullanım Örnekleri:**

**PSDJAVA-156. 'Vektör Köken Verileri' kaynağının desteklenmesi**

{{< highlight java >}}

 /*

Bir Vektör Köken Veri kaynağını okuma ve değiştirme örneği.

*/

// Basitlik için metodları yerel kapsamda tut

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("VogkResource bulunamadı.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Önceden tanımlanmış VOGK kaynağı içeren PSD dosyasını yükle

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Tanımlanan katman kaynaklarında ilk VogkResource'u bul

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Önceden tanımlı kaynak özelliklerini doğrula

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource yanlış okundu.");

    }

    // Bazı VogkResource özelliklerini değiştir

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Yüklenen PSD dosyasının değiştirilmiş bir kopyasını belirtilen yola kaydet

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. lclrResource (Sayfa rengi ayarı) desteği**

{{< highlight java >}}

 /*

Katman Sayfa Rengini kullanarak katmanları görsel olarak vurgulama örneği. Örneğin, PSD'deki bazı katmanları güncelleyebilir ve ardından dikkat çekmek istediğiniz katmanı renkle vurgulayabilirsiniz.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // lcrl kaynağı her zaman psd dosyası kaynak listesinde mevcuttur.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("Sayfa Rengi yanlış okundu");

                }

                // Stil sayfa renklerinin tersine çevrilmesi. Dikkat çekmek istediğiniz katmana renk vurgusu yapın.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// Dosyada katman vurgulamasının renkleri bu sırayla

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Red,

        SheetColorHighlightEnum.Orange,

        SheetColorHighlightEnum.Yellow,

        SheetColorHighlightEnum.Green,

        SheetColorHighlightEnum.Blue,

        SheetColorHighlightEnum.Violet,

        SheetColorHighlightEnum.Gray,

        SheetColorHighlightEnum.NoColor

};

// Önceden tanımlanmış bir LclrResource içeren PSD dosyasını yükle

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Yalnızca kaydedilen PSD dosyasını yükle

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Renkleri tersine çevir

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Uzunluk Kayıt verilerinden özelliklerin desteklenmesi. (Yol işlemleri (mantıksal işlemler), katman içinde şeklin dizini, Bezier düğüm kayıtlarının sayısı)**

{{< highlight java >}}

 /*

Şekillerle çalışırken yol işlemlerini değiştirmenin bir örneği. Program, önceden tanımlanmış vektör yol kayıtlarını (LengthRecord) okur

ve yol işlemlerini değiştirir, ardından modifiye edilmiş belgenin yeni bir PSD dosyası olarak kaydedilir.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Uzun sürekli şekil kaynağı içeren bir PSD dosyasını yükle

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Önceden tanımlı katmanın kaynaklarında ilk VsmsResource'u bul

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // Şekillerin nasıl birleştirildiğini değiştir

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Yüklenen PSD dosyasının modifiye edilmiş bir kopyasını belirtilen yola kaydet

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Resim Bölümü Kaynak #1010 Arka plan renginin desteklenmesi**

{{< highlight java >}}

 /*

Arka plan rengi kaynağını okuma ve değiştirme örneği.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Önceden tanımlı bir arka plan rengi kaynağı içeren bir PSD dosyasını yükle

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("BackgroundColorResource bulunamadı");

    }

    // Arka plan rengi kaynağının rengini güncelle

    backgroundColorResource.setColor(Color.getDarkRed());

    // Yüklenen PSD dosyasının modifiye edilmiş bir kopyasını belirtilen yola kaydet

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Çalışma zamanında Doldurma Katmanlarının eklenmesi**

{{< highlight java >}}

 /*

Farklı türde doldurma katmanlarını bir Photoshop belgesine eklemenin örneği.

*/

String outPsdFilePath = "output.psd";

// Boş bir tuval ile bir Photoshop belgesi oluştur

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // PSD'ye farklı türde doldurma katmanları ekle

    FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);

    colorFillLayer.setDisplayName("Renk Doldurma Katmanı");

    psdImage.addLayer(colorFillLayer);

    FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);

    gradientFillLayer.setDisplayName("Gradyan Doldurma Katmanı");

    psdImage.addLayer(gradientFillLayer);

    FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);

    patternFillLayer.setDisplayName("Desen Doldurma Katmanı");

    patternFillLayer.setOpacity((byte)50);

    psdImage.addLayer(patternFillLayer);

    // Yüklenen PSD dosyasının modifiye edilmiş bir kopyasını belirtilen yola kaydet

   
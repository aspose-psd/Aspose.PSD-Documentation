---
title: Aspose.PSD for Java 20.7 - Sürüm Notları
type: docs
weight: 50
url: /tr/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) için sürüm notlarını içerir. {{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-231|Çalışma zamanında Stroke Etkisi eklemenin desteklenmesi|Özellik|
|PSDJAVA-249|lnk2 / lnk3 Kaynakları (Akıllı Nesne Katmanı Kaynakları) Desteği|Özellik|
|PSDJAVA-247|Desteklenmeyen formatlarda bir görüntüyü açmaya çalışırken hata mesajı değişikliği|Geliştirme|
|PSDJAVA-235|Yeni Katman Grubu oluşturulduktan sonra PSD dosyasını kaydettiğimizde Photoshop uyarısı alıyoruz.|Hata|
|PSDJAVA-236|Katman Maskesini Kaydetme Başarısızlığı|Hata|
|PSDJAVA-237|Klasöre Uygulanan Kırpma Maskesi|Hata|
|PSDJAVA-238|Aspose.PSD for Java ile dosya açılamıyor|Hata|
|PSDJAVA-239|PSD'yi PDF'ye dönüştürürken görsel kaydetme hatası|Hata|
|PSDJAVA-240|Kırpma işlemi PSD görüntüsündeki Kırpma Yolunu geçersiz kılar|Hata|
|PSDJAVA-241|Belirli bir PSD dosyasını gölge efektiyle kaydetmeye çalışırken oluşan NullReference istisnası|Hata|
|PSDJAVA-243|Aspose.PSD, Image.CanLoad(pdfStream) metodunda true döndürür|Hata|
|PSDJAVA-244|Oluşturulan PNG'de katmanlar düzgün bir şekilde oluşturulamıyor|Hata|
|PSDJAVA-245|Metin Verilerine erişim sırasında istisna oluşumu|Hata|
|PSDJAVA-246|PSD'yi kaydetmeye çalışırken ImageSaveException oluşumu|Hata|

# **Genel API Değişiklikleri**

# **Eklenen API'ler:**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData
- T:com.aspose.psd.fileformats.psd.resources.WorkingPathResource

## **Kaldırılan API'ler**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])

# **Kullanım Örnekleri:**

**PSDJAVA-231. Çalışma zamanında Stroke Etkisi ekleme desteği**
{{< highlight java >}}
// Bu örnek, Java'da mevcut PSD dosyalarının katmanlarına bir vurgu efekti (sınır) eklemeyi nasıl gösterir.
// Sınır, renk, gradyan ve desen olmak üzere üç tür vardır. Her tür, sınırın
// iç, merkez ve dışında render edildiği üç şekilde bulunur.
// Bu örnek, tüm bu durumların kullanımını göstermektedir.

String srcPsdPath = "StrokeEffectsSource.psd";
String dstPngPath = "output.png";

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath, psdLoadOptions);
try
{
    StrokeEffect strokeEffect;
    IColorFillSettings colorFillSettings;
    IGradientFillSettings gradientFillSettings;
    IPatternFillSettings patternFillSettings;

    // 1. Renk doldurmayı, İç kısımda ekler
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 2. Renk doldurmayı, Dış kısımda ekler
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 3. Renk doldurmayı, Merkez kısımda ekler
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 4. Gradyan doldurmayı, İç kısımda ekler
    strokeEffect = psdImage.getLayers()[4].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(false);
    gradientFillSettings.setAngle(90);

    // 5. Gradyan doldurmayı, Dış kısımda ekler
    strokeEffect = psdImage.getLayers()[5].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Outside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(90);

    // 6. Gradyan doldurmayı, Merkez kısımda ekler
    strokeEffect = psdImage.getLayers()[6].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Center);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(0);

    // 7. Desen doldurmayı, İç kısımda ekler
    strokeEffect = psdImage.getLayers()[7].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(200);

    // 8. Desen doldurmayı, Dış kısımda ekler
    strokeEffect = psdImage.getLayers()[8].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Outside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(100);

    // 9. Desen doldurmayı, Merkez kısımda ekler
    strokeEffect = psdImage.getLayers()[9].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Center);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(75);

    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-249. lnk2 / lnk3 Kaynakları (Akıllı Nesne Katmanı Kaynakları) Desteği**
{{< highlight java >}}
// Bu örnek, akıllı nesne kaynakları (temelde Lnk2Resource) ile nasıl çalışılacağını gösterir.
// Program çeşitli Photoshop belgelerini yükler ve akıllı nesnelerini raster dosya formatlarına dışa aktarır.
// Ayrıca kod, Lnk2Resource'un genel yöntemlerinin kullanımını gösterir.

class LocalScopeExtension
{
    void assertAreEqual(Object expected, Object actual)
    {
        if (!actual.equals(expected))
        {
            throw new FormatException(String.format("Gerçek değer %s beklenen %s ile eşleşmiyor.", actual, expected));
        }
    }

    // Akıllı nesnenin verilerini PSD dosyasına kaydeder
    void saveSmartObjectData(String filePath, byte[] data)
    {
        FileStreamContainer container = FileStreamContainer.createFileStream(filePath, false);
        try
        {
            container.write(data);
        }
        finally
        {
            container.dispose();
        }
    }

    // Bir dosyadan akıllı nesne için yeni verileri yükler
    byte[] loadNewData(String filePath)
    {
        FileStreamContainer container = FileStreamContainer.openFileStream(filePath);
        try
        {
            return container.toBytes();
        }
        finally
        {
            container.dispose();
        }
    }

    // PSD görüntüsündeki Lnk2 / Lnk3 Kaynağı ve liFD veri kaynaklarının özelliklerini alır ve ayarlar
    void exampleOfLnk2ResourceSupport(
        String fileName,
        int dataSourceCount,
        int length,
        int newLength,
        Object[] dataSourceExpectedValues)
    {
        String srcPsdPath = fileName;
        String dstPsdPath = "out_" + fileName;

        PsdImage image = (PsdImage)Image.load(srcPsdPath);
        try
        {
            // Lnk2Resource ara
            Lnk2Resource lnk2Resource = null;
            for (LayerResource resource : image.getGlobalLayerResources())
            {
                if (resource instanceof Lnk2Resource)
                {
                    lnk2Resource = (Lnk2Resource)resource;

                    // Lnk2Resource özelliklerini doğrula
                    assertAreEqual(lnk2Resource.getDataSourceCount(), dataSourceCount);
                    assertAreEqual(lnk2Resource.getLength(), length);
                    assertAreEqual(lnk2Resource.isEmpty(), false);

                    for (int i = 0; i < lnk2Resource.getDataSourceCount(); i++)
                    {
                        // LiFdDataSource özelliklerini doğrula ve değiştir
                        LiFdDataSource lifdSource = lnk2Resource.get_Item(i);
                        Object[] expected = (Object[])dataSourceExpectedValues[i];
                        assertAreEqual(LinkDataSourceType.liFD, lifdSource.getType());
                        assertAreEqual(expected[0], lifdSource.getUniqueId().toString());
                        assertAreEqual(expected[1], lifdSource.getOriginalFileName());
                        assertAreEqual(expected[2], lifdSource.getFileType().trim());
                        assertAreEqual(expected[3], lifdSource.getFileCreator().trim());
                        assertAreEqual(expected[4], lifdSource.getData().length);
                        assertAreEqual(expected[5], lifdSource.getAssetModTime());
                        assertAreEqual(expected[6], lifdSource.getChildDocId());
                        assertAreEqual(expected[7], lifdSource.getVersion());
                        assertAreEqual(expected[8], lifdSource.hasFileOpenDescriptor());
                        assertAreEqual(expected[9], lifdSource.getLength());

                        if (lifdSource.hasFileOpenDescriptor())
                        {
                            assertAreEqual(-1, lifdSource.getCompId());
                            assertAreEqual(-1, lifdSource.getOriginalCompId());
                            lifdSource.setCompId(Integer.MAX_VALUE);
                        }

                        saveSmartObjectData(
                            fileName + "_" + lifdSource.getOriginalFileName(),
                            lifdSource.getData());
                        lifdSource.setData(loadNewData("new_" + lifdSource.getOriginalFileName()));
                        assertAreEqual(expected[10], lifdSource.getLength());

                        lifdSource.setChildDocId(UUID.randomUUID().toString());
                        lifdSource.setAssetModTime(Double.MAX_VALUE);
                        lifdSource.setFileType("test");
                        lifdSource.setFileCreator("me");
                    }

                    assertAreEqual(newLength, lnk2Resource.getLength());
                    break;
                }
            }

            // Lnk2Resource'un bulunduğundan emin ol
            assertAreEqual(true, lnk2Resource != null);

            // Yüklü PSD'nin bir kopyasını yap
            if (image.getBitsPerChannel() < 32) // 32 bitlik kanal için henüz kaydetme desteklenmiyor
            {
                image.save(dstPsdPath, new PsdOptions(image)); 
            }
        }
        finally
        {
            image.dispose();
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();


Object[] Lnk2ResourceSupportCases = new Object[]
  {
    new Object[]
    {
      "00af34a0-a90b-674d-a821-73ee508c5479",
      "rgb8_2x2.png",
      "png",
      "",
      0x53,
      0d,
      "",
      7,
      true,
      0x124L,
      0x74cL
    }
  };

Object[] LayeredLnk2ResourceSupportCases = new Object[]
  {
    new Object[]
    {
      "69ac1c0d-1b74-fd49-9c7e-34a7aa6299ef",
      "huset.jpg",
      "JPEG",
      "",
      0x9d46,
      0d,
      "xmp.did:0F94B342065B11E395B1FD506DED6B07",
      7,
      true,
      0x9E60L,
      0xc60cL
    },
    new Object[]
    {
      "5a7d1965-0eae-b24e-a82f-98c7646424c2",
      "panama-papers.jpg",
      "JPEG",
      "",
      0xF56B,
      0d,
      "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
      7,
      true,
      0xF694L,
      0x10dd4L
    },
  };

Object[] LayeredLnk3ResourceSupportCases = new Object[]
  {
    new Object[]
    {
      "2fd7ba52-0221-de4c-bdc4-1210580c6caa",
      "panama-papers.jpg",
      "JPEG",
      "",
      0xF56B,
      0d,
      "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
      7,
      true,
      0xF694l,
      0x10dd4L
    },
    new Object[]
    {
      "372d52eb-5825-8743-81a7-b6f32d51323d",
      "huset.jpg",
      "JPEG",
      "",
      0x9d46,
      0d,
      "xmp.did:0F94B342065B11E395B1FD506DED6B07",
      7,
      true,
      0x9E60L,
      0xc60cL
    },
  };

// Bu örnek, PSD Lnk2 Kaynağının ve liFD veri kaynaklarının özelliklerini nasıl alıp ayarlayacağını gösterir.
$.exampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);

// Bu örnek, PSD Lnk3 Kaynağının ve liFD veri kaynaklarının özelliklerini nasıl alıp ayarlayacağını gösterir.
$.exampleOfLnk2ResourceSupport("Katmanlı PSD dosyası akıllı nesneler.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);

// Bu örnek, PSD Lnk2 Kaynağının ve liFD veri kaynaklarının özelliklerini nasıl alıp ayarlayacağını gösterir.
$.exampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}
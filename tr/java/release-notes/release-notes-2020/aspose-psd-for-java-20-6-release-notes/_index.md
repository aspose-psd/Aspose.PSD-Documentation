---
title: Aspose.PSD for Java 20.6 - Sürüm Notları
type: docs
weight: 50
url: /tr/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} Bu sayfa [Aspose.PSD for Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) için sürüm notlarını içerir. {{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-216|LnkEResource'un (Akıllı Nesne Katmanı Kaynağı) Desteklenmesi|Özellik|
|PSDJAVA-219|britResource'un (Tutuluk/Aydınlatma Ayar Katmanı Kaynağı) Desteklenmesi|Özellik|
|PSDJAVA-222|DefaultReplacementFont ayarının ImageOptionsBase sınıfına taşınması|Geliştirme|
|PSDJAVA-217|Maskesi olan ayarlama katmanında PSD dosyalarının yeniden boyutlandırılması yanlış çalışır|Hata|
|PSDJAVA-218|RGB modunda 16 bit/kanal olan Psd Resmi yalnızca ön izlemelerde güncellenir|Hata|
|PSDJAVA-220|PSD Katman Maskelerinde yapılan değişiklikler kaydedilmez|Hata|
|PSDJAVA-221|Boş Katman Grubuna Katman Grubu ekledikten sonra Yanlış Katman Sırası|Hata|
|PSDJAVA-223|AdobeStockLicenseState özelliği olan bileşik LnkE Kaynağı olan belirli PSD dosyasının yüklenmesi sırasında Olay|Hata|
|PSDJAVA-224|AI Dosyasının Jpeg2000 Biçimine Kaydedilmesi Çalışmaz|Hata|
|PSDJAVA-225|Geçiş Yöntemi Olmayan Karışık Karışım Kipi Katman Grubu Rendelenmiyor|Hata|
|PSDJAVA-226|Belirli Psd dosyasını görüntüye dönüştürmeye çalışırken NullReference İstisnası|Hata|
|PSDJAVA-227|Belirli Psd dosyasını açmaya çalışırken OverflowException|Hata|
# **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **Kaldırılan API'ler:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **Kullanım örnekleri:**

**PSDJAVA-216: LnkEResource'un Desteklenmesi (Akıllı Nesne Katmanı Kaynağı)**

{{< highlight java >}}

 // PSD'ye farklı tiplerde varlıkların (raster görüntüler, CC kitaplıkları) bağlanmasının bir örneği.

// Ayrıca LnkeResource API'si ele alınmıştır.

// Yerel kapsamdaki metodları içeren bir sınıf

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport yanlış çalışıyor.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Bu örnek, dış bağlantılı bir dosya hakkında bilgi içeren Photoshop Psd LnkE

    // Kaynağı üzerindeki özelliklerin nasıl alınıp ayarlanacağını gösterir.

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,

            int length3,

            int length4,

            String fullPath,

            String date,

            double assetModTime,

            String childDocId,

            boolean locked,

            String uid,

            String name,

            String originalFileName,

            String fileType,

            long size)

    {

        String outputPath = "out_" + fileName;

        // Önceden tanımlanmış bir PSD'yi yükle

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Genel kaynaklar arasında LnkeResource'yi ara

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // LnkeResource özelliklerinin doğru olduğundan emin ol

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), size);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.liFE);

                    // LnkeResource özelliklerini güncelle

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), length2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), length3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), length4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    break;

                }

            }

            // LnkeResource'nin desteklendiğinden emin ol

            assertIsTrue(lnkeResource != null);

            // Yüklenmiş PSD'nin kopyasını kaydet

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // Kaydedilen kopyayı yükle

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // PSD'yi PNG dosya biçimine dönüştür (alfa kanalı ile şeffaflık için)

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            image1.save(Path.changeExtension(outputPath, "png"), pngOptions);

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Bu örnek, dış bağlantılı JPEG dosyası hakkında bilgi içeren Psd LnkE Kaynağı olan

// Photoshop Psd'nin dış bir JPEG dosyası hakkında bilgi içeren LnkE Kaynağı olan

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "05/09/2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// Bu örnek, dış bağlantılı PNG dosyası hakkında bilgi içeren Photoshop Psd'nin LnkE Kaynağı olan

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "14/04/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Bu örnek, dış bağlantılı CC Kitaplıkları Varlığı hakkında bilgi içeren Photoshop Psd LnkE Kaynağı olan

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Varlık “rgb8_2x2_linked/rgb8_2x2” (Özellik sadece Photoshop CC 2015'te mevcuttur)",

        "01/01/0001 00:00:00",

        1588890915488.0d,

        "",

        false,

        "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

        "rgb8_2x2_linked",

        "rgb8_2x2.png",

        "png",

        0);


{{< /highlight >}}

**PSDJAVA-219: britResource'un Desteklenmesi (Tutuluk/Aydınlatma Ayar Katmanı Kaynağı)**

{{< highlight java >}}

 // Bu Örnek, PSD Görüntüsü Parlaklık/Kontrast Katmanı Kaynağı - BritResource üzerinde programatik olarak değişiklik yapabileceğinizi gösterir. Bu Düşük Seviye Aspose.PSD API'sini kullanabilirsiniz.

// Parlaklık/Kontrast Katmanını API'si üzerinden kullanarak, PSD dosyası içeriği üzerinde daha fazla kontrol elde edebilirsiniz.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Parlaklık / Kontrast ayarllık Katmanı içeren bir Photoshop belgesini yükler

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // BritResource'u ara

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Kaynak özelliklerini doğrula

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource yanlış okundu");

                    }

                    // Kaynak özelliklerini güncelle

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Güncellenmiş PSD'nin kopyasını kaydet

                    psdImage.save(dstPath, new PsdOptions());

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

**PSDJAVA-217: Ayarlama katmanında maskesi olan PSD dosyalarının yeniden boyutlandırılması yanlış çalışır**

{{< highlight java >}}

 // Boş sınırlara sahip ayarlama katmanındaki bir maskeye sahip bir görüntünün yeniden boyutlandırılmasına ilişkin bir örnektir.

// Program, herhangi bir istisna olup olmadığını kontrol etmek için önceden tanımlanmış bir PSD yükler.

final int scale = 2; // keyfi bir katsayı

String[] names = {

        "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

        "LevelsLayerWithLayerMaskRgb",

        "LevelsLayerWithLayerMaskCmyk",

};

for (String name : names)

{

    String srcFilePath = name + ".psd";

    String dstFilePath = "output_" + srcFilePath;

    String dstPngFilePath = "output_" + name + ".png";

    // Boş sınırlara sahip bir ayarlama katmanı olan önceden tanımlanmış bir PSD yükleyin

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, psdLoadOptions);

    try

    {

        // Görüntüyü yeniden boyutlandır

        image.resize(image.getWidth() * scale, image.getHeight() * scale);

        // Yüklü PSD'nin kopyasını kaydet

        image.save(dstFilePath, new PsdOptions());

        // PSD'yi PNG dosya biçimine dönüştür (alfa kanalı ile şeffaflık için)

        PngOptions pngOptions = new PngOptions();

        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        image.save(dstPngFilePath, pngOptions);

    }

    finally

    {

        image.dispose();

    }

}

{{< /highlight >}}

**PSDJAVA-218: RGB modunda 16 bit/kanal olan Psd Resmi yalnızca ön izlemelerde güncellenir**

{{< highlight java >}}

 // 16 bit RGB görüntü için düzenli katmanların güncellenmesi hakkında bir örnektir. Program herhangi bir katmanın doğru bir şekilde güncellendiğinden emin olmak için her katmanda bir şeyler çizer.

String kaynakDosyaYolu = "in.psd";

String ciktiDosyaYolu = "output.psd";

// 16 bit RGB modunda belirli bir PSD dosyasını yükleyin

PsdImage image = (PsdImage)Image.load(kaynakDosyaYolu);

try

{

    for (Layer layer : image.getLayers())

    {

        // Düzenli bir katman için katman adını ve iç çerçeveyi çizer

        if (!(layer instanceof LayerGroup) && !(layer instanceof AdjustmentLayer) &&

                (layer.getWidth() > 100) && (layer.getHeight() > 100))

        {

            Graphics graphics = new Graphics(layer);

            graphics.drawString(layer.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            graphics.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // Yüklü PSD'nin kopyasını kaydet

    image.save(ciktiDosyaYolu, new PsdOptions(image));

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-220: PSD Katman Maskelerinde yapılan değişiklikler kaydedilmez**

{{< highlight java >}}

 // Yerel kapsamdaki metodları içeren bir sınıf

class LocalScopeExtension

{

    void assertAreEqual(Object actual, Object expected)

    {

        if (!(actual != null && actual.equals(expected)))

        {

            throw new FormatException("Örnek yanlış çalışıyor.");

        }

    }

    // Byte'ın büyük uçta sıralanması

    byte[] getBigEndianBytesInt32(int value)

    {

        byte[] bytes = new byte[4];

        bytes[0] = (byte)((value >> 24) & 0x000000FF);

        bytes[1] = (byte)((value >> 16) & 0x000000FF);

        bytes[2] = (byte)((value >> 8) & 0x000000FF);

        bytes[3] = (byte)value;

        return bytes;

    }

    // Dizi içindeki büyük uçtan Int32'ye dönüştürülen değeri alır

    int fromBigEndianToInt32(byte[] bytes, int index)

    {

        if (bytes == null)

        {

            throw new ArgumentNullException("bytes");

        }

        if (index < 0 || index + 4 > bytes.length)

        {

            throw new ArgumentOutOfRangeException("index", "İndeks, bayt dizisi dışında düşmektedir.");

        }

        return ((bytes[index] & 0xff) << 24) | ((bytes[index + 1] & 0xff) << 16) |

                ((bytes[index + 2] & 0xff) << 8) | (bytes[index + 3] & 0xff);

    }

    // Psd görüntüsünden bir raster maske alır ve dosyaya kaydeder

    void saveRasterMask(String maskFilePath, Layer layer)

    {

        LayerMaskDataShort maskData = (LayerMaskDataShort)layer.getLayerMaskData();

        FileStreamContainer container = FileStreamContainer.createFileStream(maskFilePath, false);

        try

        {

            container.write(getBigEndianBytesInt32(maskData.getTop()));

            container.write(getBigEndianBytesInt32(maskData.getLeft()));

            container.write(getBigEndianBytesInt32(maskData.getBottom()));

            container.write(getBigEndianBytesInt32(maskData.getRight()));

            container.writeByte(maskData.getDefaultColor());

            container.writeByte((byte)maskData.getFlags());

            container.write(getBigEndianBytesInt32(maskData.getImageData().length));

            container.write(maskData.getImageData(), 0, maskData.getImageData().length);

        }

        finally

        {

            container.dispose();

        }

    }

    // Bir dosyadan katmana raster bir maskel ekler ve psd biçimli görüntüyü kaydeder

    void addRasterMask(Layer layer, String maskSourcePath)

    {

        LayerMaskDataShort maskData = new LayerMaskDataShort();

        FileStreamContainer container = FileStreamContainer.openFileStream(maskSourcePath);

        try

        {

            byte[] bytes = new byte[22];

            assertAreEqual(container.read(bytes), 22);

            maskData.setTop(fromBigEndianToInt32(bytes, 0));

            maskData.setLeft(fromBigEndianToInt32(bytes, 4));

            maskData.setBottom(fromBigEndianToInt32(bytes, 8));

            maskData.setRight(fromBigEndianToInt32(bytes, 12));

            maskData.setDefaultColor(bytes[16]);

            maskData.setFlags(bytes[17]);

            int imageDataLength = fromBigEndianToInt32(bytes, 18);

            byte[] data = new byte[imageDataLength];

            assertAreEqual(maskData.getMaskRectangle().getWidth() *

                    maskData.getMaskRectangle().getHeight(), imageDataLength);

            assertAreEqual(container.read(data), imageDataLength);

            maskData.setImageData(data);

        }

        finally

        {

            container.dispose();

        }

        // Yalnızca katman Maske Verisini eklemek, kanalların güncellenmesi için yeterli değildir;

        // layer.setLayerMaskData(mask); // Bu, maske kanalını eklemiyor

        // Maskı ekle (veya güncelle)

        layer.addLayerMask(maskData); // Ancak bu hem maskeleri hem de kanalları ekler/günceller!

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Bu örnek, dış bir JPEG dosyası hakkında bir Psd dosyasının LnkE Kaynağını bilgi içerecek şekilde

$.addRasterMask(layer, "raster.msk");

image.save("FourWithMasksAdded2.png", pngOptions);

image.save("FourWithMasksAdded2.psd");

}

finally

{

image.dispose();

}

{{< /highlight >}}

**PSDJAVA-221: Boş Katman Grubuna Katman Grubu ekledikten sonra Yanlış Katman Sırası**

{{< highlight java >}}

 // Bu örnek, programatik olarak bir PSD'ye iç içe bir katman grubu ekleme işlemini gösterir.

String dstPsdYolu = "output.psd";

// Çalışılacak bir görüntü oluştur

PsdImage psdImage = new PsdImage(1, 1);

try

{

    // Bir üst katman grubu ekleyin ("true", grup katmanını başlangıçta açması anlamına gelir)

    LayerGroup group1 = psdImage.addLayerGroup("Grup 1", 0, true);

    // İç içe bir katman grubu ekleyin

    LayerGroup group2 = group1.addLayerGroup("Grup 2", 0);

    if (group1.getLayers().length != 2)

    {

        throw new RuntimeException("Grup 1, Grup 2'nin iki katmanını içermelidir.");

    }

    // Yalnızca yeni oluşturulan katman gruplarını kaydetmeye çalışarak hiçbir istisna olmadığını doğrulayın

    psdImage.save(dstPsdYolu);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-223: AdobeStockLicenseState özelliği olan bileşik LnkE Kaynağı olan belirli PSD dosyasının yüklenmesi sırasında Olay**

{{< highlight java >}}

 // Bu örnek, Adobe® Photoshop® harici bağlantı kaynağını (LnkeResource) programatik olarak okuyup değiştirmenizi gösterir.

// Yerel kapsamdaki metodları içeren bir sınıf

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("Örnek yanlış çalışıyor.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    void exampleOfComplexLnkEResourceSupport(String srcPsdPath, int length, int length2, Object[] dataSourceExpectedValues)

    {

        // Birden çok veri kaynağı okuyan LayerResource içeren önceden tanımlanmış bir PSD'yi yükler

        PsdImage image = (PsdImage)Image.load(srcPsdPath);

        try

        {

            // LnkeResource ara

            LnkeResource
---
title: Notatki wydania Aspose.PSD dla Java 20.6
type: docs
weight: 50
url: /pl/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} Ta strona zawiera notatki wydania dla [Aspose.PSD dla Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDJAVA-216|Wsparcie dla LnkEResource (Zasób warstwy Smart Object)|Funkcja|
|PSDJAVA-219|Wsparcie dla britResource (Zasób warstwy regulacji jasności/kontrastu)|Funkcja|
|PSDJAVA-222|Przeniesienie ustawienia DefaultReplacementFont do klasy ImageOptionsBase|Usprawnienie|
|PSDJAVA-217|Zmiana rozmiaru plików PSD działa nieprawidłowo, jeśli w warstwie korekcji jest maska, która ma puste granice|Błąd|
|PSDJAVA-218|Obraz PSD w trybie RGB 16 bit/na kanał aktualizuje warstwy tylko podglądu|Błąd|
|PSDJAVA-220|Zmiany maski warstwy PSD są odrzucane podczas zapisywania|Błąd|
|PSDJAVA-221|Niepoprawna kolejność warstw po dodaniu grupy warstw do pustej grupy warstw|Błąd|
|PSDJAVA-223|Wyjątek podczas wczytywania określonego pliku PSD ze złożonym zasobem LnkE i adobeStockLicenseState|Błąd|
|PSDJAVA-224|Zapisywanie pliku AI w formacie Jpeg2000 nie działa|Błąd|
|PSDJAVA-225|Grupa warstw z trybem mieszania innych niż Przejście nie jest renderowana|Błąd|
|PSDJAVA-226|Wyjątek NullReference podczas próby konwertowania określonego pliku Psd na obraz|Błąd|
|PSDJAVA-227|OverflowException podczas próby otwarcia określonego pliku Psd|Błąd|

# **Zmiany w API publicznym**
## **Dodane API:**
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
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **Usunięte API:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)

# **Przykłady użycia:**

**PSDJAVA-216: Wsparcie dla LnkEResource (Zasób warstwy Smart Object)**

{{< highlight java >}}
  
 // Przykład łączenia różnych typów zasobów (obrazy rastrowe, biblioteki CC) z plikiem PSD.

// Rozważana jest również API klasy LnkeResource.

// Klasa przechowująca metody w lokalnym zakresie

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport działa nieprawidłowo.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Ten przykład demonstruje, jak uzyskać i ustawić właściwości zasobu Photoshop Psd LnkE

    // Resource, który zawiera informacje o zewnętrznym pliku połączonym.

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

        // Wczytaj predefiniowany PSD

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Szukaj LnkeResource wśród zasobów warstw globalnych

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Sprawdź właściwości zasobu LnkeResource

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

                    // Zaktualizuj właściwości zasobu LnkeResource

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

                    break;

                }

            }

            // Upewnij się, że LnkeResource jest obsługiwane

            assertIsTrue(lnkeResource != null);

            // Zapisz kopię wczytanego PSD

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // Wczytaj zapisaną kopię

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // Konwertuj PSD na format pliku PNG (z kanałem alfa dla przeźroczystości)

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

// Ten przykład pokazuje, jak uzyskać i ustawić właściwości zasobu Psd LnkE, który

// zawiera informacje o zewnętrznie połączonym pliku JPEG.

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

// Ten przykład pokazuje, jak uzyskać i ustawić właściwości zasobu PSD LnkE, który

// zawiera informacje o zewnętrznie połączonym pliku PNG.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "04/14/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Ten przykład pokazuje, jak uzyskać i ustawić właściwości zasobu Psd LnkE, który

// zawiera informacje o zewnętrznie połączonym zasobie bibliotek CC.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Funkcja dostępna w Photoshop CC 2015)",

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

**PSDJAVA-219: Wsparcie dla britResource (Zasób warstwy regulacji jasności/kontrastu)**

{{< highlight java >}}
  
 // Ten przykład demonstruje, jak programistycznie zmienić zasób warstwy jasności/kontrastu PSD. Jest to niskopoziomowe API Aspose.PSD.

// Możesz korzystać z warstwy jasności/kontrastu za pomocą jej API, co będzie o wiele łatwiejsze,

// ale bezpośrednia edycja zasobów programu PhotoShop daje większą kontrolę nad zawartością pliku PSD---

PSDJAVA-219: Support of britResource (Resource of Brightness/Contrast Adjustment Layer)

{{< highlight java >}}

 // This Example demonstrates how you can programmatically change the PSD Image

// Brightness/Contrast Layer Resource - BritResource. This is a Low-Level Aspose.PSD API.

// You can use Brightness/Contrast Layer through its API, which will be much easier,

// but direct PhotoShop resource editing gives you more control over the PSD file content.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Load a Photoshop document containing a Brightness / Contrast adjustment layer

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Search for BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Verify resource properties

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource was read wrong");

                    }

                    // Update resource properties

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Save a copy of the updated PSD

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

{{< /highlight >}}

PSDJAVA-217: Resizing PSD files works incorrect if there is a mask in the adjustment layer that has empty bounds

{{< highlight java >}}

 // An example of resizing an image that contains an adjustment layer mask with empty bounds.

// The program loads a predefined PSD just to check whether there are no exceptions.

final int scale = 2; // arbitrary coefficient

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

    // Load a predefined PSD containing an adjustment layer mask that has empty bounds

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, psdLoadOptions);

    try

    {

        // Resize the image

        image.resize(image.getWidth() * scale, image.getHeight() * scale);

        // Save a copy of the loaded PSD

        image.save(dstFilePath, new PsdOptions());

        // Export PSD to PNG file format (with alpha channel for transparency)

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

PSDJAVA-218: Psd Image with RGB mode 16 bit/channel updates layers only on preview

{{< highlight java >}}

 // An example of updating regular layers for a 16-bit RGB image. The program draws something

// on each layer just to make sure that the whole layer updates properly.

String sourceFilePath = "in.psd";

String outputFilePath = "output.psd";

// Load a predefined PSD in 16-bit RGB mode

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    for (Layer layer : image.getLayers())

    {

        // Draw the layer name and an inner border for the regular layer

        if (!(layer instanceof LayerGroup) && !(layer instanceof AdjustmentLayer) &&

                (layer.getWidth() > 100) && (layer.getHeight() > 100))

        {

            Graphics graphics = new Graphics(layer);

            graphics.drawString(layer.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            graphics.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // Save a copy of the loaded PSD

    image.save(outputFilePath, new PsdOptions(image));

}

finally

{

    image.dispose();

}

{{< /highlight >}}

PSDJAVA-220: PSD Layer Mask changes are discarded on save

{{< highlight java >}}

 // A class that keeps methods in the local scope

class LocalScopeExtension

{

    void assertAreEqual(Object actual, Object expected)

    {

        if (!(actual != null && actual.equals(expected)))

        {

            throw new FormatException("Example works incorrectly.");

        }

    }

    // Gets the int value converted to big-endian bytes order.

    byte[] getBigEndianBytesInt32(int value)

    {

        byte[] bytes = new byte[4];

        bytes[0] = (byte)((value >> 24) & 0x000000FF);

        bytes[1] = (byte)((value >> 16) & 0x000000FF);

        bytes[2] = (byte)((value >> 8) & 0x000000FF);

        bytes[3] = (byte)value;

        return bytes;

    }

    // Gets the value converted from the big endian to Int32.

    int fromBigEndianToInt32(byte[] bytes, int index)

    {

        if (bytes == null)

        {

            throw new ArgumentNullException("bytes");

        }

        if (index < 0 || index + 4 > bytes.length)

        {

            throw new ArgumentOutOfRangeException("index", "The index falls outside the bytes array.");

        }

        return ((bytes[index] & 0xff) << 24) | ((bytes[index + 1] & 0xff) << 16) |

                ((bytes[index + 2] & 0xff) << 8) | (bytes[index + 3] & 0xff);

    }

    // Gets a raster mask from the layer of a PSD image and saves it to a file

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

    // Adds a raster mask from the file to the layer and saves it the PSD format image

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

        // Just adding LayerMaskData is not enough for correct saving because channels are not updated;

        // layer.setLayerMaskData(mask); // This does not add the mask channel

        // Add (or update) the mask

        layer.addLayerMask(maskData); // But this adds / updates both the mask and channels!

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// This example shows how to get, update, remove and add raster layer masks in the Adobe® Photoshop® file programmatically.

PngOptions pngOptions = new PngOptions();

pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

String sourceFilePath = "FourWithMasks.psd";

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    Layer layer = image.getLayers()[2];

    // Get a raster mask from the layer and save it to a file

    $.saveRasterMask("FourWithMasks2.msk", layer);

    // Change the layer mask (invert) and save the image

    LayerMaskData mask = layer.getLayerMaskData();

    byte[] maskData = mask.getImageData();

    for (int i = 0; i < maskData.length; i++)

    {

        maskData[i] = (byte)~maskData[i];

    }

    // Just changing LayerMaskData is enough to effect rendering

    image.save("FourWithMasksUpdated2.png", pngOptions);

    // But just changing LayerMaskData is not enough for correct saving because channels are not updated;

    layer.setLayerMaskData(mask); // This does not work either

    layer.addLayerMask(mask); // But this updates both the mask and channels!

    image.save("FourWithMasksUpdated2.psd");

    // Remove a raster mask from the layer and save the image

    layer.setLayerMaskData(null); // Just removing LayerMaskData is enough to effect rendering but not for saving to PSD format

    image.save("FourWithMasksRemoved2.png", pngOptions);

    layer.addLayerMask(null); // But this removes both the mask and the mask channel!

    image.save("FourWithMasksRemoved2.psd");

    // Add a raster mask from the file to the layer and save the image

    $.addRasterMask(layer, "raster.msk");

    image.save("FourWithMasksAdded2.png", pngOptions);

    image.save("FourWithMasksAdded2.psd");

}

finally

{
    image.dispose();
}

{{< /highlight >}}

PSDJAVA-221: Incorrect Layer Order after you add Layer Group to empty Layer Group

{{< highlight java >}}

 // This example demonstrates how to add a nested layer group to PSD programmatically.

String dstPsdPath = "output.psd";

// Create an image with the size of 1x1 pixels to work with

PsdImage psdImage = new PsdImage(1, 1);

try

{

    // Add a parent layer group ("true" means to open the layer group on start)

    LayerGroup group1 = psdImage.addLayerGroup("Group 1", 0, true);

    // Add a nested layer group

    LayerGroup group2 = group1.addLayerGroup("Group 2", 0);

    if (group1.getLayers().length != 2)

    {

        throw new RuntimeException("Group 1 must contain two layers of Group 2.");

    }

    // Verify that there are no exceptions on saving just created layer groups

    psdImage.save(dstPsdPath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}
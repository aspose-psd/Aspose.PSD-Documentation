---
title: Aspose.PSD für Java 20.6 - Versionshinweise
type: docs
weight: 50
url: /de/java/aspose-psd-fur-java-20-6-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-216|Unterstützung von LnkEResource (Ressource der Smart-Objekt-Ebene)|Feature|
|PSDJAVA-219|Unterstützung von britResource (Ressource der Helligkeit/Kontrast-Anpassungsebene)|Feature|
|PSDJAVA-222|Verschieben der Einstellung DefaultReplacementFont in die Klasse ImageOptionsBase|Verbesserung|
|PSDJAVA-217|Das Skalieren von PSD-Dateien funktioniert nicht korrekt, wenn in der Anpassungsebene eine Maske mit leeren Grenzen vorhanden ist|Fehler|
|PSDJAVA-218|Psd-Bild im RGB-Modus mit 16 Bit/Kanal aktualisiert Ebenen nur in der Vorschau|Fehler|
|PSDJAVA-220|Änderungen an PSD-Ebenenmasken gehen beim Speichern verloren|Fehler|
|PSDJAVA-221|Falsche Ebenenreihenfolge, nachdem Sie eine leere Ebenengruppe zu einer anderen leeren Ebenengruppe hinzugefügt haben|Fehler|
|PSDJAVA-223|Ausnahme beim Laden einer bestimmten PSD-Datei mit der zusammengesetzten LnkE-Ressource und der Eigenschaft adobeStockLicenseState|Fehler|
|PSDJAVA-224|Das Speichern einer AI-Datei im Jpeg2000-Format funktioniert nicht|Fehler|
|PSDJAVA-225|Ebenengruppe mit nicht durchschreibendem Überblendungsmodus wird nicht gerendert|Fehler|
|PSDJAVA-226|NullReference-Ausnahme beim Versuch, eine bestimmte PSD-Datei in ein Bild umzuwandeln|Fehler|
|PSDJAVA-227|OverflowException beim Versuch, eine bestimmte PSD-Datei zu öffnen|Fehler|

# **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
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
## **Entfernte APIs:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **Beispiele:**

**PSDJAVA-216: Unterstützung von LnkEResource (Ressource der Smart-Objekt-Ebene)**

{{< highlight java >}}

 // Ein Beispiel zur Verknüpfung verschiedener Arten von Assets (Rasterbilder, CC-Bibliotheken) mit PSD.

// Auch API der LnkeResource wird berücksichtigt.

// Eine Klasse, die Methoden im lokalen Bereich hält

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport funktioniert nicht korrekt.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Dieses Beispiel zeigt, wie Eigenschaften der Photoshop Psd LnkE-Ressource erhalten und festgelegt werden.

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

        // Laden einer vordefinierten PSD

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Suche LnkeResource unter globalen Ressourcen

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Überprüfe LnkeResource-Eigenschaften

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

                    // Aktualisiere LnkeResource-Eigenschaften

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

            // Stelle sicher, dass LnkeResource unterstützt wird

            assertIsTrue(lnkeResource != null);

            // Speichern einer Kopie der geladenen PSD

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // Die gespeicherte Kopie laden

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // Konvertieren Sie PSD in das PNG-Dateiformat (mit Alphakanal für Transparenz)

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

// Dieses Beispiel zeigt, wie Eigenschaften der Psd LnkE-Ressource erhalten und festgelegt werden.

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

// Dieses Beispiel zeigt, wie Eigenschaften der Psd Lnke-Ressource erhalten und festgelegt werden.

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

// Dieses Beispiel zeigt, wie Eigenschaften der Photoshop Psd LnkE-Ressource erhalten und festgelegt werden.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Feature ist in Photoshop CC 2015 verfügbar)",

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

**PSDJAVA-219: Unterstützung von britResource (Ressource der Helligkeit/Kontrast-Anpassungsebene)**

{{< highlight java >}}

 // Dieses Beispiel zeigt, wie Sie programmgesteuert die PSD-Bild-Helligkeits/Kontrast-Ebene-Ressource (BritResource) ändern können. Dies ist ein Low-Level-Aspose.PSD-API.

// Sie können die Helligkeits/Kontrast-Ebene über ihre API verwenden, was jedoch einfacher ist,

// aber das direkte Bearbeiten von Photoshop-Ressourcen bietet Ihnen mehr Kontrolle über den PSD-Dateiinhalt.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Laden eines Photoshop-Dokuments, das eine Helligkeit/Kontrast-Anpassungsebene enthält

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Suchen nach BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Überprüfen von Ressourceneigenschaften

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource wurde falsch gelesen");

                    }

                    // Aktualisierenvon Ressourceneigenschaften

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource wurde falsch gelesen");

                    }

                    // Aktualisieren von Ressourceneigenschaften

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Speichern einer Kopie der aktualisierten PSD

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

**PSDJAVA-217: Das Skalieren von PSD-Dateien funktioniert nicht korrekt, wenn in der Anpassungsebene eine Maske mit leeren Grenzen vorhanden ist**

{{< highlight java >}}

 // Ein Beispiel für das Skalieren eines Bildes, das eine Anpassungsebenenmaske mit leeren Grenzen enthält.

// Das Programm lädt eine vordefinierte PSD nur, um zu überprüfen, ob keine Ausnahmen auftreten.

final int skalierung = 2; // beliebiger Koeffizient

String[] namen = {

        "EineReguläreUndEineAnpassungMitVektorUndEbenenmaske",

        "EbenenmaskeMitEbenenmaskeRgb",

        "EbenenmaskeMitEbenenmaskeCmyk",

};

for (String name : namen)

{

    String srcDateipfad = name + ".psd";

    String dstDateipfad = "output_" + srcDateipfad;

    String dstPngDateipfad = "output_" + name + ".png";

    // Laden einer vordefinierten PSD, die eine Anpassungsebenenmaske mit leeren Grenzen enthält

    PsdLoadOptions psdLoadOptionen = new PsdLoadOptions();

    psdLoadOptionen.setLoadEffectsResource(true);

    PsdImage bild = (PsdImage)Image.load(srcDateipfad, psdLoadOptionen);

    try

    {

        // Das Bild skalieren

        bild.resize(bild.getWidth() * skalierung, bild.getHeight() * skalierung);

        // Speichern einer Kopie der geladenen PSD

        bild.save(dstDateipfad, new PsdOptions());

        // PSD in PNG-Dateiformat exportieren (mit Alphakanal für Transparenz)

        PngOptions pngOptionen = new PngOptions();

        pngOptionen.setColorType(PngColorType.TruecolorWithAlpha);

        bild.save(dstPngDateipfad, pngOptionen);

    }

    finally

    {

        bild.dispose();

    }

}

{{< /highlight >}}

**PSDJAVA-218: Das Psd-Bild im RGB-Modus mit 16 Bit/Kanal aktualisiert Ebenen nur auf der Vorschau**

{{< highlight java >}}

 // Ein Beispiel für das Aktualisieren regulärer Ebenen für ein 16-Bit-RGB-Bild. Das Programm zeichnet etwas

// auf jede Ebene, um sicherzustellen, dass die gesamte Ebene ordnungsgemäß aktualisiert wird.

String quelleDateipfad = "ein.psd";

String ausgabeDateipfad = "ausgabe.psd";

// Laden einer vordefinierten PSD im 16-Bit-RGB-Modus

PsdImage bild = (PsdImage)Image.load(quelleDateipfad);

try

{

    for (Layer ebene : bild.getLayers())

    {

        // Zeichnen des Ebenennamens und eines inneren Rahmens für die reguläre Ebene

        if (!(ebene instanceof LayerGroup) && !(ebene instanceof AdjustmentLayer) &&

                (ebene.getWidth() > 100) && (ebene.getHeight() > 100))

        {

            Graphics grafiken = new Graphics(ebene);

            grafiken.drawString(ebene.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            grafiken.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // Speichern einer Kopie der geladenen PSD

    bild.save(ausgabeDateipfad, new PsdOptions(bild));

}

finally

{

    bild.dispose();

}

{{< /highlight >}}

**PSDJAVA-220: Änderungen an PSD-Ebenenmasken gehen beim Speichern verloren**

{{< highlight java >}}

 // Eine Klasse, die Methoden im lokalen Bereich hält

class LocalScopeExtension

{

    void assertAreEqual(Object actual, Object expected)

    {

        if (!(actual != null && actual.equals(expected)))

        {

            throw new FormatException("Das Beispiel funktioniert nicht richtig.");

        }

    }

    // Erhalten des int-Werts, der in groß-endianischen Bytes-Aufzeichnungen umgewandelt ist.

    byte[] getBigEndianBytesInt32(int value)

    {

        byte[] bytes = new byte[4];

        bytes[0] = (byte)((value >> 24) & 0x000000FF);

        bytes[1] = (byte)((value >> 16) & 0x000000FF);

        bytes[2] = (byte)((value >> 8) & 0x000000FF);

        bytes[3] = (byte)value;

        return bytes;

    }

    // Erhalten des Werts, der von groß-endianisch in Int32 konvertiert ist.

    int fromBigEndianToInt32(byte[] bytes, int index)

    {

        if (bytes == null)

        {

            throw new ArgumentNullException("bytes");

        }

        if (index < 0 || index + 4 > bytes.length)

        {

            throw new ArgumentOutOfRangeException("index", "Der Index liegt außerhalb des Bytes-Arrays.");

        }

        return ((bytes[index] & 0xff) << 24) | ((bytes[index + 1] & 0xff) << 16) |

                ((bytes[index + 2] & 0xff) << 8) | (bytes[index + 3] & 0xff);

    }

    // Eine Rastermaske von der Ebene eines PSD-Bildes erhalten und in einer Datei speichern

    void saveRasterMask(String maskenDateipfad, Layer ebene)

    {

        LayerMaskDataShort maskenDaten = (LayerMaskDataShort)ebene.getLayerMaskData();

        FileStreamContainer container = FileStreamContainer.createFileStream(maskenDateipfad, false);

        try

        {

            container.write(getBigEndianBytesInt32(maskenDaten.getTop()));

            container.write(getBigEndianBytesInt32(maskenDaten.getLeft()));

            container.write(getBigEndianBytesInt32(maskenDaten.getBottom()));

            container.write(getBigEndianBytesInt32(maskenDaten.getRight()));

            container.writeByte(maskenDaten.getDefaultColor());

            container.writeByte((byte)maskenDaten.getFlags());

            container.write(getBigEndianBytesInt32(maskenDaten.getImageData().length));

            container.write(maskenDaten.getImageData(), 0, maskenDaten.getImageData().length);

        }

        finally

        {

            container.dispose();

        }

    }

    // Eine Rastermaske aus der Datei auf die Ebene hinzufügen und das PSD-Formatbild speichern

    void addRasterMask(Layer ebene, String maskenQuellpfad)

    {

        LayerMaskDataShort maskenDaten = new LayerMaskDataShort();

        FileStreamContainer container = FileStreamContainer.openFileStream(maskenQuellpfad);

        try

        {

            byte[] bytes = new byte[22];

            assertAreEqual(container.read(bytes), 22);

            maskenDaten.setTop(fromBigEndianToInt32(bytes, 0));

            maskenDaten.setLeft(fromBigEndianToInt32(bytes, 4));

            maskenDaten.setBottom(fromBigEndianToInt32(bytes, 8));

            maskenDaten.setRight(fromBigEndianToInt32(bytes, 12));

            maskenDaten.setDefaultColor(bytes[16]);

            maskenDaten.setFlags(bytes[17]);

            int imageDataLength = fromBigEndianToInt32(bytes, 18);

            byte[] data = new byte[imageDataLength];

            assertAreEqual(maskenDaten.getMaskRectangle().getWidth() *

                    maskenDaten.getMaskRectangle().getHeight(), imageDataLength);

            assertAreEqual(container.read(data), imageDataLength);

            maskenDaten.setImageData(data);

        }

        finally

        {

            container.dispose();

        }

        // Das Hinzufügen von LayerMaskData reicht nicht aus, um das Channel korrekt zu speichern, da die Kanäle nicht aktualisiert sind;

        // ebene.setLayerMaskData(mask); // Dies fügt den Maskenkanal nicht hinzu

        // Die Maske hinzufügen (oder aktualisieren)

        ebene.addLayerMask(maskenDaten); // Aber das fügt/aktualisiert sowohl die Maske als auch die Kanäle hinzu!

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Dieses Beispiel zeigt, wie Sie raster Ebene Masken in der Adobe® Photoshop®-Datei programmgesteuert erhalten, aktualisieren, entfernen und hinzufügen können.

PngOptions pngOptionen = new PngOptions();

pngOptionen.setColorType(PngColorType.TruecolorWithAlpha);

String quelleDateipfad = "VierMitMasken.psd";

PsdImage bild = (PsdImage)Image.load(quelleDateipfad);

try

{

    Layer ebene = bild.getLayers()[2];

    // Erhalt einer Rastermaske von der Ebene und Speichern in einer Datei

    $.saveRasterMask("VierMitMasken2.msk", ebene);

    // Ändern der Ebenenmaske (invertieren) und Speichern des Bildes

    LayerMaskData maske = ebene.getLayerMaskData();

    byte[] maskenDaten = maske.getImageData();

    for (int i = 0; i < maskenDaten.length; i++)

    {

        maskenDaten[i] = (byte)~maskenDaten[i];

    }

    // Nur das Ändern von LayerMaskData ist ausreichend, um das Rendering zu beeinflussen

    bild.save("VierMitMaskenAktualisiert2.png", pngOptionen);

    // Aber nur das Ändern von LayerMaskData reicht nicht aus, um korrekt zu speichern, da die Kanäle nicht aktualisiert werden;

    ebene.setLayerMaskData(maske); // Das funktioniert auch nicht

    ebene.addLayerMask(maske); // Aber das aktualisiert sowohl die Maske als auch die Kanäle!

    bild.save("VierMitMaskenAktualisiert2.psd");

    // Entfernen einer Rastermaske von der Ebene und Speichern des Bildes

    ebene.setLayerMaskData(null); // Nur das Entfernen von LayerMaskData reicht aus, um das Rendering zu beeinflussen, aber nicht für das Speichern im PSD-Format

    bild.save("VierMitMaskenEntfernt2.png", pngOptionen);

    ebene.addLayerMask(null); // Aber das entfernt sowohl die Maske als auch den Maskenkanal!

    bild.save("VierMitMaskenEntfernt2.psd");

    // Hinzufügen einer Rastermaske aus der Datei auf die Ebene und Speichern des Bildes

    $.addRasterMask(ebene, "raster.msk");

    bild.save("VierMitMaskenHinzugefügt2.png", pngOptionen);

    bild.save("VierMitMaskenHinzugefügt2.psd");

}

finally

{

    bild.dispose();

}

{{< /highlight >}}
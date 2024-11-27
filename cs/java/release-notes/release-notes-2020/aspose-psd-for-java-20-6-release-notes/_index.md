---
title: Aspose.PSD pro Java 20.6 - Poznámky k vydání
type: docs
weight: 50
url: /cs/java/aspose-psd-pro-java-20-6-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-216|Podpora LnkEResource (Zdroj vrstvy chytrého objektu)|Funkce|
|PSDJAVA-219|Podpora britResource (Zdroj jasu/kontrastu vrstvy úpravy)|Funkce|
|PSDJAVA-222|Přesun nastavení DefaultReplacementFont do třídy ImageOptionsBase|Vylepšení|
|PSDJAVA-217|Změna velikosti souborů PSD nefunguje správně pokud je v vrstvě úpravy maska s prázdnými hranami|Chyba|
|PSDJAVA-218|Snímek PSD s režimem RGB 16 bitů/kanál aktualizuje vrstvy pouze v náhledu|Chyba|
|PSDJAVA-220|Změny masky vrstvy PSD jsou zahozeny při uložení|Chyba|
|PSDJAVA-221|Nesprávné pořadí vrstev po přidání vrstvy skupiny do prázdné vrstvy skupiny|Chyba|
|PSDJAVA-223|Výjimka při načítání konkrétního souboru PSD se složeným LnkE zdrojem a vlastností adobeStockLicenseState|Chyba|
|PSDJAVA-224|Ukládání souboru AI do formátu Jpeg2000 nefunguje|Chyba|
|PSDJAVA-225|Vrstva skupiny s režimem míchání jiným než Procházet není vykreslena|Chyba|
|PSDJAVA-226|Výjimka NullReference při pokusu o převedení konkrétního souboru Psd na obrázek|Chyba|
|PSDJAVA-227|Přetečení výjimky při pokusu o otevření konkrétního souboru Psd|Chyba|

# **Změny ve veřejném API**
# **Přidaná API:**
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

## **Odebraná API:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)

# **Příklady použití:**

**PSDJAVA-216: Podpora LnkEResource (Zdroj vrstvy chytrého objektu)**

{{< highlight java >}}

 // Příklad propojení různých typů aktiv souborů (rastr, knihovny CC) do souboru PSD.

// Též se zde uplatňuje API LnkeResource.

// Třída, která udržuje metody v lokálním rozsahu

class LocalScopeExtension

{

    void assertIsTrue(boolean podmínka)

    {

        if (!podmínka)

        {

            throw new FormatException("PříkladLnkEResourceSupport nefunguje správně.");

        }

    }

    void assertAreEqual(Object skutečný, Object očekávaný)

    {

        assertIsTrue(skutečný != null && skutečný.equals(očekávaný));

    }

    // Tento příklad ukazuje, jak získat a nastavit vlastnosti Photoshop Psd LnkE

    // Resource, který obsahuje informace o externím propojeném souboru.

    void exampleOfLnkEResourceSupport(

            String názevSouboru,

            int délka,

            int délka2,

            int délka3,

            int délka4,

            String cesta,

            String datum,

            double časAktualizace,

            String childDocId,

            boolean uzamčeno,

            String uid,

            String jméno,

            String originálníJméno,

            String typSouboru,

            long velikost)

    {

        String výstupníCesta = "out_" + názevSouboru;

        // Načtení předdefinovaného souboru PSD

        PsdImage obrázek = (PsdImage)Image.load(názevSouboru);

        try

        {

            // Hledání LnkeResource mezi globálními zdroji

            LnkeResource lnkeResource = null;

            for (LayerResource zdroj : obrázek.getGlobalLayerResources())

            {

                if (zdroj instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)zdroj;

                    // Ověření vlastností LnkeResource

                    assertAreEqual(lnkeResource.getLength(), délka);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), cesta);

                    assertAreEqual(new SimpleDateFormat("dd.MM.yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), datum);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), časAktualizace);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), uzamčeno);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), jméno);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), velikost);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), typSouboru);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originálníJméno);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.liFE);

                    // Aktualizace vlastností LnkeResource

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), délka2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), délka3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), délka4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    break;

                }

            }

            // Ujistění, že LnkeResource je podporován

            assertIsTrue(lnkeResource != null);

            // Uložení kopie načteného PSD

            obrázek.save(výstupníCesta, new PsdOptions(obrázek));

        }

        finally

        {

            obrázek.dispose();

        }

        // Načtení uložené kopie

        PsdImage obrázek1 = (PsdImage)Image.load(výstupníCesta);

        try

        {

            // Konverze PSD na formát souboru PNG (s alfa kanálem pro průhlednost)

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            obrázek1.save(Path.changeExtension(výstupníCesta, "png"), pngOptions);

        }

        finally

        {

            obrázek1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Tento příklad ukazuje, jak získat a nastavit vlastnosti Psd LnkE Resource,

// který obsahuje informace o externí propojeném souboru JPEG.

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "09.05.2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// Tento příklad ukazuje, jak získat a nastavit vlastnosti Psd LnkE Resource,

// který obsahuje informace o externálním propojeném PNG souboru.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "14.04.2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Tento příklad ukazuje, jak získat a nastavit vlastnosti Photoshop Psd LnkE Resource

// který obsahuje informace o externálním propojeném aktivu z knihoven CC.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Funkce je dostupná v Photoshop CC 2015)",

        "01.01.0001 00:00:00",

        1588890915488.0d,

        "",

        false,

        "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

        "rgb8_2x2_linked",

        "rgb8_2x2.png",

        "png",

        0);


{{< /highlight >}}

**PSDJAVA-219: Podpora britResource (Zdroj jasu/kontrastu vrstvy úpravy)**

{{< highlight java >}}

 // Tento Příklad ukazuje, jak programaticky měnit zdroj vrstvy jasu/kontrastu Psd obrázku. Jedná se o nízkoúrovňové API Aspose.PSD. Můžete také použít vrstvu jasu/kontrastu přes jeho API, které bude mnohem jednodušší, ale přímá úprava zdrojů PhotoShop vám dává větší kontrolu nad obsahemobrázku PSD.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Načtěte dokument Photoshopu obsahující vrstvu úpravy jasu/kontrastu

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Hledání BritResource

    for (Layer vrstva : psdImage.getLayers())

    {

        if (vrstva instanceof BrightnessContrastLayer)

        {

            for (LayerResource zdrojVrstvy : vrstva.getResources())

            {

                if (zdrojVrstvy instanceof BritResource)

                {

                    BritResource zdroj = (BritResource)zdrojVrstvy;

                    // Ověření vlastností zdroje

                    if (zdroj.getBrightness() != -40 ||

                            zdroj.getContrast() != 10 ||

                            zdroj.getLabColor() ||

                            zdroj.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource byla špatně přečtena");

                    }

                    // Aktualizace vlastností zdroje

                    zdroj.setBrightness((short)25);

                    zdroj.setContrast((short)-14);

                    zdroj.setLabColor(true);

                    zdroj.setMeanValueForBrightnessAndContrast((short)200);

                    // Uložení kopie aktualizovaného PSD

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

**PSDJAVA-217: Změna velikosti souborů PSD nefunguje správně pokud je v vrstvě úpravy maska s prázdnými hranami**

{{< highlight java >}}

 // Příklad změny velikosti obrázku obsahující masku vrstvy úpravy s prázdnými hranami.

// Program načte předdefinovaný soubor PSD pouze k ověření, zda nejsou vyvolány výjimky.

final int měřítko = 2; // libovolný koeficient

String[] názvy = {

        "JednaNormálníAVrstvaÚpravySVektorovouAVrstvovouMaskou",

        "VrstvaSÚpravamiÚrovníSMaskouRgb",

        "VrstvaSÚpravamiÚrovníSCmykMaskou",

};

for (String název : názvy)

{

    String srcSouborPsds = název + ".psd";

    String dstSouborPsds = "output_" + srcSouborPsds;

    String dstPngSoubor = "output_" + název + ".png";

    // Načtěte předdefinovaný soubor PSD obsahující masku vrstvy úpravy s prázdnými hranami

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage obrázek = (PsdImage)Image.load(srcSouborPsds, psdLoadOptions);

    try

    {

        // Změna velikosti obrázku

        obrázek.resize(obrázek.getWidth() * měřítko, obrázek.getHeight() * měřítko);

        // Uložení kopie načteného PSD

        obrázek.save(dstSouborPsds, new PsdOptions());

        // Exportování PSD do formátu PNG (s alfa kanálem pro průhlednost)

        PngOptions pngOptions = new PngOptions();

        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        obrázek.save(dstPngSoubor, pngOptions);

    }

    finally

    {

        obrázek.dispose();

    }

}

{{< /highlight >}}

**PSDJAVA-218: Snímek PSD s režimem RGB 16 bitů/kanál aktualizuje vrstvy pouze v náhledu**

{{< highlight java >}}

 // Příklad aktualizace běžných vrstev pro obrázek s 16bitovým RGB režimem. Program vykresluje něco na každé vrstvě pouhým tím, že zajistí, aby byla celá vrstva aktualizována správně.

String zdrojováCesta = "in.psd";

String výstupníCesta = "output.psd";

// Načtení předdefinovaného PSD v 16bitovém režimu RGB

PsdImage obrázek = (PsdImage)Image.load(zdrojováCesta);

try

{

    for (Layer vrstva : obrázek.getLayers())

    {

        // Vykreslení názvu vrstvy a vnitřního rámečku pro běžnou vrstvu

        if (!(vrstva instanceof LayerGroup) && !(vrstva instanceof AdjustmentLayer) &&

                (vrstva.getWidth() > 100) && (vrstva.getHeight() > 100))

        {

            Graphics grafika = new Graphics(vrstva);

            grafika.drawString(vrstva.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            grafika.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // Uložení kopie načteného PSD

    obrázek.save(výstupníCesta, new PsdOptions(obrázek));

}

finally

{

    obrázek.dispose();

}

{{< /highlight >}}
---
title: Převádění obrázků
type: docs
weight: 20
url: /cs/net/prevadani-obrazku/
---

## **Převádění obrázků na černobílou a stupně šedi**
Někdy může být potřeba převést barevné obrázky na černobílou nebo stupně šedi pro tisk nebo archivaci. Tento článek ukazuje, jak pomocí Aspose.PSD prohodit obrázky pomocí dvou metod, jak je uvedeno níže.

- Binární
- Stupně šedi

### **Binární**
Pro pochopení konceptu binarizace je důležité definovat binární obraz; digitální obraz, který může mít pouze dvě možné hodnoty pro každý pixel. Obvykle jsou pro binární obraz použity dvě barvy, černá a bílá, ačkoli lze použít kteroukoli dvojici barev. Binární je proces převádění obrazu na dvouúrovňový, což znamená, že každý pixel je uložen jako jeden bit (0 nebo 1), kde 0 znamená absenci barvy a 1 značí přítomnost barvy. Aspose.PSD pro .NET API v současné době podporuje dvě metody binarizace.
#### **Binární s pevným prahem**
Následující ukázka kódu ukazuje, jak lze na obraz použít binarizaci s pevným prahem.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binární s Otsuovým prahem**
Následující ukázka kódu ukazuje, jak lze na obrázek aplikovat binarizaci s Otsuovým prahem.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Stupně šedi**
Stupně šedi jsou procesem převodu obrazu s plynulými odstíny šedi na obraz s útržkovitými odstíny šedé. Následující ukázka kódu ukazuje, jak použít stupně šedi.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **Převést vrstvy obrazu GIF na obraz TIFF**
Někdy je potřeba extrahovat a převést vrstvy obrázku PSD do jiného rastrového formátu obrázku z důvodu splnění potřeby aplikace. Aspose.PSD API podporuje funkci extrakce a převodu vrstev obrázku PSD do jiného rastrového formátu obrázku. Nejprve vytvoříme instanci obrázku a načteme obrázek PSD z lokálního disku, poté iterujeme každou vrstvu v vlastnosti Layer. Poté provedeme konverzi bloku na obrázek TIFF. Následující ukázka kódu ukazuje, jak převést vrstvy obrázku PSD na obrázky TIFF.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **Převádění CMYK PSD na CMYK TIFF**
Pomocí Aspose.PSD pro .NET mohou vývojáři převádět soubor CMYK PSD na formát tiff v režimu CMYK. Tento článek ukazuje, jak exportovat/převést soubor CMYK PSD na formát tiff s Aspose.PSD. S Aspose.PSD pro .NET můžete načítat obrázky PSD a nastavovat různé vlastnosti pomocí [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) třídy a ukládat nebo exportovat obrázek. Následující ukázka kódu ukazuje, jak tohoto dosáhnout.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **Exportování obrázků**
Kromě bohatého souboru rutin pro zpracování obrázků poskytuje Aspose.PSD specializované třídy pro převod formátů souborů PSD na jiné formáty. Použitím této knihovny je velmi jednoduché a intuitivní převádět obrázky PSD na jiné formáty. Níže jsou některé specializované třídy pro tento účel ve jmenném prostoru [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions).

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

S Aspose.PSD pro .NET API je snadné exportovat obrázky PSD. Stačí vám objekt příslušné třídy z jmenného prostoru [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions). Použitím těchto tříd můžete snadno exportovat libovolný obrázek vytvořený, upravený nebo jednoduše načtený s Aspose.PSD pro .NET do jakéhokoli podporovaného formátu.
## **Kombinace obrázků**
Tento příklad používá třídu Graphics a ukazuje, jak kombinovat dva nebo více obrázků do jednoho kompletního obrázku. Pro demonstraci operace vytvoří příklad nový PsdImage a vykreslí obrázky na plochu plátna pomocí metody Draw Image exposed. Pomocí třídy Graphics mohou být dva nebo více obrázků spojeny tak, že výsledný obrázek bude vypadat jako kompletní obrázek bez mezery mezi částmi obrázku a bez stránek. Velikost plátna musí být rovna velikosti výsledného obrázku. Níže je ukázka kódu, která ukazuje, jak používat [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) metodu [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) třídy kombinovat obrázky do jednoho obrázku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **Rozšíření a ořezání obrázků**
Aspose.PSD API vám umožňuje během procesu konverze obrázku rozšířit nebo oříznout obrázek. Vývojář musí vytvořit obdélník s X a Y souřadnicemi a určit šířku a výšku obdélníkového pole. X, Y a šířka, výška obdélníku budou zobrazovat rozšíření nebo ořezání načteného obrázku. Pokud má být obrázek během konverze rozšířen nebo oříznut, proveďte následující kroky:

1. Vytvořte instanci třídy [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) a načtěte existující obrázek.
1. Vytvořte instanci třídy ImageOption.
1. Vytvořte instanci třídy [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) a inicializujte X, Y a šířku, výšku obdélníku.
1. Zavolejte metodu [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) třídy RasterImage s předáním názvu výstupního souboru, možností obrázku a objektem obdélníku jako parametry.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **Čtení a zápis dat XMP do obrázků**
XMP (Extensible Metadata Platform) je standard ISO. XMP standardizuje datový model, formát serializace a základní vlastnosti pro definici a zpracování rozšiřitelných metadat. Poskytuje také pokyny pro vložení informací XMP do populárních obrázků, jako je JPEG, aniž by porušoval jejich čitelnost aplikacemi, které nepodporují XMP. Pomocí Aspose.PSD pro .NET API mohou vývojáři číst nebo zapisovat XMP metadata do obrázků. Tento článek ukazuje, jak lze číst XMP metadata z obrázku a zapisovat XMP metadata do obrázků.
### **Vytvořte XMP Metadata, Zapište jej a přečtěte z souboru**
S pomocí jmenného prostoru Xmp může vývojář vytvořit objekt XMP metadata a zapsat ho do obrázku. Následující ukázka kódu ukazuje, jak používat Balík XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage a DublinCorePackage obsažené v [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp) jmenném prostoru.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **Exportování obrázků v prostředí s více vlákny**
Aspose.PSD pro .NET nyní podporuje převádění obrázků v prostředí s více vlákny. Aspose.PSD pro .NET zajistí optimalizovaný výkon operací během provádění kódu v prostředí s více vlákny. Všechny [třídy možností obrazu](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) (např. BmpOptions, TiffOptions, JpegOptions atd.) v Aspose.PSD pro .NET implementují rozhraní IDisposable. Proto je nutné, aby vývojář správně zrušil objekt třídy možností obrázku v případě nastavení vlastnosti Source. Následující ukázka kódu ukazuje tuto funkcionalitu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD nyní podporuje vlastnost SyncRoot při práci v prostředí s více vlákny. Vývojář může tuto vlastnost použít k synchronizaci přístupu k zdrojovému proudu. Následující ukázka kódu ukazuje, jak může být vlastnost SyncRoot použita.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}

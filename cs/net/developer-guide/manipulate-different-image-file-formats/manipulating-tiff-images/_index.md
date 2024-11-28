---
title: Manipulace s soubory TIFF
type: docs
weight: 50
url: /cs/net/manipulace-soubory-tiff/
---

## **Přidání rámečků s různými nastaveními**
TIFF je velmi flexibilní formát a umožňuje přidat různé rámečky s různými rozměry, kompresí a dalšími nastaveními. API Aspose.PSD vám umožní přidat libovolný rámec TIFF libovolné velikosti, což pomáhá vytvářet složité dokumenty. Pokud je potřeba upravit rámečky během procesu přidání tak, aby byly všechny stejné, proveďte následující kroky:

- Vytvořte nový prázdný rámec s požadovanými volbami nebo zkopírujte zdrojový rámec se specifikovanými výstupními možnostmi pomocí metody CreateFrameFrom.
- Změňte velikost zdrojového rámce/obrazu na požadované rozměry pomocí metody Resize.
- Přidejte pixely zdrojového rámce/obrazu do nového rámečku.
- Přidejte nový rámec do výstupního obrazu TIFF.
## **Exportování vrstev obrazu PSD do formátu souboru Multi Page Tiff**
Někdy je potřeba exportovat vrstvy obrazu PSD do formátu souboru Multi-page TIFF. Tento článek ukáže, jak toho můžeme dosáhnout pomocí API Aspose.PSD pro .NET. Nejprve načteme obraz PSD z disku. Poté projdeme vrstvy obrazu PSD a vytvoříme objekt TiffFrame odpovídající vrstvám. Nakonec uložíme výsledný obrázek TIFF do jednoho souboru na disku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **Konfigurace TiffOptions**
Vývojáři mohou upravit různé vlastnosti třídy [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) pro získání požadovaných výsledků. V této dokumentaci se zaměříme na 4 hlavní vlastnosti, které ovlivňují vlastnosti výsledného obrazu.

Tyto vlastnosti jsou uvedeny níže.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Při inicializaci prázdné struktury TiffOptions jsou všechny volby nastaveny na výchozí hodnotu, například komprese je nastavena na None, BitsPerSample je nastaveno na 1 a Photometric jako MinIsWhite. Uložení do tohoto formátu způsobí, že výsledný obrázek bude černobílý, a to je očekávané chování pro tuto kombinaci voleb. K získání barevných výsledků musíte nastavit všechny výše uvedené vlastnosti na hodnoty, které odpovídají požadovanému barevnému prostoru, nebo můžete inicializovat strukturu TiffOptions s předdefinovanými nastaveními, jak je popsáno později v tomto článku. Níže je uvedena tabulka popisující očekávané hodnoty parametrů, které můžete nastavit pro dosažení požadovaných výsledků. Pamatujte, že všechny 4 sloupce by měly být nastaveny skrz TiffOptions, aby se uložil jakýkoli načtený/vytvořený obrázek ve formátu TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Paleta|LZW/Nezkomprimováno|1/4/8/16 (paleta, barevný režim) pouze jediný kanál|None|
|MinIsWhite/MinIsBlack|LZW/Nezkomprimováno|1/4/8/16 (šedotónový režim) pouze jediný kanál|None|
|Paleta|LZW/Nezkomprimováno|8 (paleta, barevný režim) pouze jediný kanál|Horizontální (větší komprese dosaženo u LZW stejné vzory)|
|MinIsWhite/MinIsBlack|LZW/Nezkomprimováno|8 (šedotónový režim) pouze jediný kanál|Horizontální (větší komprese dosaženo u LZW stejné vzory)|
|RGB|LZW/Nezkomprimováno|[8,8,8] (3 RGB kanály)|None/Horizontální|
|RGB|LZW/Nezkomprimováno|[8,8,8,8] (3 RGB kanály a další alfa kanál může být nastaven skrz TiffOptions.AlphaStorage) Ve skutečnosti je podporováno libovolné množství dalších kanálů, ale každý kanál musí mít velikost 8 bitů jako [8,8,8,8,8,8]|None/Horizontální|
Všechny 4 vlastnosti by měly být nastaveny skrz TiffOptions, aby se uložil jakýkoli formát obrazu do formátu Tiff. Při použití různých kombinací mohou některé prohlížeče (včetně prohlížeče Windows Photo Viewer) odmítnout zobrazit výsledný obrázek kvůli omezené podpoře, kterou nabízejí. V takovém případě si vyberte jiný prohlížeč pro vaše testování.
### **Předdefinovaná nastavení pro třídu TiffOptions**
Aby se uživatelům usnadnilo a zabránilo se chybné konfiguraci instance TiffOptions, API Aspose.PSD pro .NET poskytuje další konstruktor, který přijímá parametr typu [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Na základě vybrané hodnoty z výčtu TiffExpectedFormat API automaticky nastaví všechny povinné vlastnosti instance TiffOptions tak, aby byly dosaženy požadované výsledky. Předtím, než se přesuneme k ukázkovému kódu, zde je seznam polí TiffExpectedFormat a jejich podrobnosti pro lepší pochopení použití.


- TiffExpectedFormat.Default: Nastavení pole na Výchozí jedná se podobně jako výchozí konstruktor třídy TiffOptions s žádnou nastavenou kompresí a BitsPerPixel nastaveno na 1 kvůli vytvoření černobílého výsledku. Doporučuje se používat toto pole, pokud mají být jiné specifické vlastnosti formátu nastaveny ručně podle požadovaných výsledků.
- TiffExpectedFormat.TiffCcitRle: Specifické pro RLE kódování při ukládání výsledku ve formátu 1 BitsPerPixel (černobílý) TIFF.
- TiffExpectedFormat.TiffCcittFax3: Specifické pro kodování CCITT Fax3 při ukládání výsledku ve formátu 1 BitsPerPixel (černobílý) TIFF.
- TiffExpectedFormat.TiffCcittFax4: Specifické pro kodování CCITT Fax4 při ukládání výsledku ve formátu 1 BitsPerPixel (černobílý) TIFF.
- TiffExpectedFormat.TiffDeflateBW: Specifické pro kompresi Deflate při ukládání výsledku ve formátu 1 BitsPerPixel (černobílý) TIFF.
- TiffExpectedFormat.TiffDeflateRGB: Specifické pro kompresi Deflate při ukládání výsledku ve formátu RGB (barevný) TIFF.
- TiffExpectedFormat.TiffJpegRGB: Specifické pro kompresi Jpeg při ukládání výsledku ve formátu RGB (barevný) TIFF.
- TiffExpectedFormat.TiffJpegYCBCR: Specifické pro kompresi Jpeg při ukládání výsledku ve formátu YCBCR (barevný) TIFF.
- TiffExpectedFormat.TiffLzwBW: Specifické pro kompresi LZW při ukládání výsledku ve formátu 1 BitsPerPixel (černobílý) TIFF.
- TiffExpectedFormat.TiffLzwRGB: Specifické pro kompresi LZW při ukládání výsledku ve formátu RGB (barevný) TIFF.
- TiffExpectedFormat.TiffLzwRGBA: Specifické pro kompresi LZW při ukládání výsledku ve formátu RGBA (barevný s průhledností) TIFF.
- TiffExpectedFormat.TiffNoCompressionBW: Specifické pro nekomprimovaný formát TIFF při ukládání výsledku ve formátu 1 BitsPerPixel (černobílý).
- TiffExpectedFormat.TiffNoCompressionRGB: Specifické pro nekomprimovaný formát TIFF při ukládání výsledku ve formátu RGB (barevný).
- TiffExpectedFormat.TiffNoCompressionRGBA: Specifické pro nekomprimovaný formát TIFF při ukládání výsledku ve formátu RGBA (barevný s průhledností).



Následující ukázka kódu objasňuje použití polí TiffExpectedFormat při vytváření instance třídy TiffOptions.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **Podpora pro kompresi Deflate a Adobe Deflate**
Souborový formát TIFF (Tagged Image File Format) podporuje různé typy komprese, kde typ komprese je uložen jako značka (celé číslo) v souboru. Jednou z těchto metod komprese je Adobe Deflate (dříve známý jako Deflate). API Aspose.PSD pro .NET podporuje tuto metodu komprese pro exportování a vytváření obrazů TIFF.
### **Uložení obrázku do TIFF s kompresí Deflate**
Převod načtených obrázků do formátu TIFF s kompresí Deflate/Adobe Deflate je snadný následovně.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Vytvoření TiffImage s kompresí Adobe Deflate**
Níže uvedená ukázka demonstruje použití API Aspose.PSD pro .NET k vytvoření obrázku od začátku s použitím metody komprese Adobe Deflate.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **Komprese obrázků TIFF**
API Aspose.PSD pro .NET lze použít k převodu obrázků PSD do formátu obrázku TIFF a dokonce ke změně komprese výsledného obrázku TIFF. API lze také použít k ukládání různých obrázků jako rámečky v obrázku TIFF pro účely archivace při komprimování obrázků na nejnižší datovou velikost. Kompresi obrázků by měla být vždy prováděna snižováním velikosti zdrojových dat bez ohledu na použitý kompresní algoritmus. Pro dosažení nejlepšího kompresního poměru můžeme použít indexované barevné prostory. Níže uvedený kód zajišťuje nejlepší kompresi pomocí 16 indexovaných barev a algoritmu komprese LZW, i když jsou zdrojové barvy mírně rušeny.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}

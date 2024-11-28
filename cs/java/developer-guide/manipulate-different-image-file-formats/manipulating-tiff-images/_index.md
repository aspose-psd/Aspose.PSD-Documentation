---
title: Manipulace s obrázky TIFF
type: docs
weight: 40
url: /cs/java/manipulace-s-obrazky-tiff/
---

## **Přidání rámečků s různým nastavením**
TIFF je velmi flexibilní formát a umožňuje přidávání různých rámečků s různými rozměry, kompresí a dalším nastavením. API Aspose.PSD vám umožňuje přidat libovolný rámec TIFF o libovolné velikosti, což pomáhá vytvářet složité dokumenty. Pokud je požadavek na upravení rámečků během procesu přidání, aby byly všechny stejné, proveďte následující kroky:

- Vytvořte nový prázdný rámec s požadovanými možnostmi nebo kopírujte zdrojový rámec s určenými výstupními možnostmi pomocí metody CreateFrameFrom.
- Změňte rozměry zdrojového rámečku/obrázku na požadované rozměry pomocí metody Resize.
- Přidejte pixely zdrojového rámečku/obrázku do nového rámečku.
- Přidejte nový rámec do výstupního obrázku TIFF.
## **Exportování vrstev obrázku PSD do formátu souboru Multi-Stránkový TIFF**
Občas je zapotřebí exportovat vrstvy obrázku PSD do formátu souboru Multi-stránkový TIFF. Tento článek ukáže, jak lze tento úkol provést pomocí Aspose.PSD pro Java API. Nejprve načteme obrázek PSD z disku. Poté projdeme vrstvy obrázku PSD a vytvoříme TiffFrame z odpovídajících vrstev. Nakonec uložíme výsledný obrázek TIFF do jednoho souboru na disku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **Konfigurace TiffOptions**


Vývojáři mohou upravit různé vlastnosti třídy Tiffoptions pro získání požadovaných výsledků. V tomto dokumentu se zaměříme na 4 hlavní vlastnosti, které ovlivňují atributy výsledného obrázku.

Tyto vlastnosti jsou uvedeny níže.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Pokud inicializujeme prázdnou strukturu Tiffoptions, každá možnost je nastavena na svou výchozí hodnotu. Například komprese je nastavena na None, BitsPerSample je nastaveno na 1 a Photometric na MinIsWhite. Uložení do tohoto formátu způsobí, že finální obrázek bude černobílý, což je očekávané chování pro tyto kombinace možností. Abychom dosáhli barevných výsledků, musíme nastavit všechny výše uvedené vlastnosti na hodnoty odpovídající požadovanému barevnému prostoru nebo můžeme inicializovat strukturu Tiffoptions s předdefinovanými nastaveními, jak je diskutováno později v tomto článku. Níže je uvedena tabulka popisující očekávané hodnoty parametrů, které můžete nastavit pro dosažení požadovaných výsledků. Všimněte si, že každý ze 4 sloupců musí být nastaven skrz TiffOptions, abyste mohli uložit jakýkoli načtený/vytvořený obrázek do formátu souboru TIFF.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Paleta|LZW/Nezkomprimováno|1/4/8/16 (paleta, režim barev) pouze jeden kanál|None|
|MinIsWhite/MinIsBlack|LZW/Nezkomprimováno|1/4/8/16 (stupně šedi) pouze jeden kanál|None|
|Paleta|LZW/Nezkomprimováno|8 (paleta, režim barev) pouze jeden kanál|Horizontální (větší komprese dosažena pro LZW pro stejné vzory)|
|MinIsWhite/MinIsBlack|LZW/Nezkomprimováno|8 (režim odstínů šedi) pouze jeden kanál|Horizontální (větší komprese dosažena pro LZW pro stejné vzory)|
|RGB|LZW/Nezkomprimováno|[8,8,8] (3 RGB kanály)|None/Horizontal|
|RGB|LZW/Nezkomprimováno|[8,8,8,8] (3 RGB kanály a další alfa kanál může být nastaven pomocí TiffOptions.AlphaStorage) Vlastně je podporován libovolný počet dalších kanálů, ale každý kanál musí mít velikost 8 bitů, jako například [8,8,8,8,8,8]|None/Horizontal|
Všechny 4 vlastnosti by měly být nastaveny skrz TiffOptions, abyste mohli uložit jakýkoli formát obrázku do formátu Tiff. Při použití různých kombinací někteří prohlížeče (včetně Prohlížeče fotografií ve Windows) mohou odmítnout renderovat výsledný obrázek kvůli omezené podpoře, kterou nabízejí. V takovém případě si prosím vyberte jiného prohlížeče pro vaše testování.
### **Předdefinovaná nastavení pro třídu TiffOptions**
Aby se uživatelům usnadnilo a zabránilo se nesprávné konfiguraci instance Tiffoptions, Aspose.PSD pro Java API vystavilo další konstruktor, který přijímá parametr typu TiffExpectedFormat. Na základě vybrané hodnoty z enumerace TiffExpectedFormat se API automaticky konfiguruje všechny povinné vlastnosti instance Tiffoptions pro dosažení požadovaných výsledků. Předtím, než se dostaneme k ukázkovému kódu, zde je seznam položek TiffExpectedFormat a jejich podrobnosti pro lepší porozumění použití.



- TiffExpectedFormat.Default: Nastavení pole na Výchozí se chová podobně jako výchozí konstruktor třídy Tiffoptions s nekomprimovaným nastavením a BitsPerPixel nastaveno na 1, aby vytvořilo černobílý výsledek. Doporučuje se použít toto pole, když jsou jiné formátové vlastnosti nastaveny ručně dle požadovaných výsledků.
- TiffExpectedFormat.TiffCcitRle: Specifické pro RLE kódování při ukládání výsledku do formátu TIFF s 1 BitsPerPixel (černobílý) formatem.
- TiffExpectedFormat.TiffCcittFax3: Specifické pro CCITT Fax3 kódování při ukládání výsledku do formátu TIFF s 1 BitsPerPixel (černobílý) formát.
- TiffExpectedFormat.TiffCcittFax4: Specifické pro CCITT Fax4 kódování při ukládání výsledku do formátu TIFF s 1 BitsPerPixel (černobílý) formát.
- TiffExpectedFormat.TiffDeflateBW: Specifické pro Deflate kompresi při ukládání výsledku do formátu TIFF s 1 BitsPerPixel (černobílý) formát.
- TiffExpectedFormat.TiffDeflateRGB: Specifické pro Deflate kompresi při ukládání výsledku do formátu TIFF s RGB (barevný) formát.
- TiffExpectedFormat.TiffJpegRGB: Specifické pro Jpeg kompresi při ukládání výsledku do formátu TIFF s RGB (barevný) formát.
- TiffExpectedFormat.TiffJpegYCBCR: Specifické pro Deflate kompresi při ukládání výsledku do formátu TIFF s YCBCR (barevný) formát.
- TiffExpectedFormat.TiffLzwBW: Specifické pro LZW kompresi při ukládání výsledku do formátu TIFF s 1 BitsPerPixel (černobílý) formát.
- TiffExpectedFormat.TiffLzwRGB: Specifické pro LZW kompresi při ukládání výsledku do formátu TIFF s RGB (barevný) formát.
- TiffExpectedFormat.TiffLzwRGBA: Specifické pro LZW kompresi při ukládání výsledku do formátu TIFF s RGBA (barevný s průhledností) formát.
- TiffExpectedFormat.TiffNoCompressionBW: Specifické pro nekomprimovaný formát TIFF při ukládání výsledku s 1 BitsPerPixel (černobílý).
- TiffExpectedFormat.TiffNoCompressionRGB: Specifické pro nekomprimovaný formát TIFF při ukládání výsledku s RGB (barevný).
- TiffExpectedFormat.TiffNoCompressionRGBA: Specifické pro nekomprimovaný formát TIFF při ukládání výsledku s RGBA (barevný s průhledností).



Následující kódový výřez objasňuje použití položek TiffExpectedFormat při vytváření instance třídy Tiffoptions.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **Podpora pro kompresi Deflate a kompresi Adobe Deflate**
Formát souboru TIFF (Tagged Image File Format) podporuje různé typy komprese, přičemž typ komprese je uložen jako značka (celé číslo) v souboru. Jedna z těchto metod komprese je Adobe Deflate (dříve známá jako Deflate). Aspose.PSD pro Java API podporuje tento typ komprese při exportu a vytváření obrazů TIFF.
### **Uložení obrázku do TIFF s kompresí Deflate**
Převádění načtených obrázků do formátu TIFF s kompresí Deflate/Adobe Deflate je snadné následovně.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Vytváření TiffImage s kompresí Adobe Deflate**
Níže poskytnutá ukázka demonstruje použití Aspose.PSD pro Java API k vytvoření obrázku od začátku s použitím metody Adobe Deflate komprese.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **Kompresní obrázky TIFF**
Aspose.PSD pro Java API lze použít k převodu obrázků PSD do formátu obrázku TIFF a dokonce změnit kompresi výsledného obrázku TIFF. API lze také použít k ukládání různých obrázků jako rámce v obrázku TIFF pro účely archivace a zároveň komprimovat obrázky na co nejmenší datovou velikost. Kompresní algoritmus by měl být v každém případě prováděn snižováním velikosti zdrojových dat bez ohledu na použitý kompresní algoritmus. Abyste dosáhli nejlepšího kompresního poměru, můžeme použít indexované barevné prostory. Níže uvedený kódový výřez provádí nejlepší kompresi použitím pouze 16 indexovaných barev a algoritmu komprese LZW, avšak zdrojové barvy jsou mírně ditherované.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}

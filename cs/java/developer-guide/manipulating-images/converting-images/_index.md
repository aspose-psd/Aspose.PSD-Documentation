---
title: Konverze obrázků
type: docs
weight: 20
url: /cs/java/konverze-obrazku/
---

## **Konverze obrázků na černobílé a stupně šedi**
Někdy může být potřeba konvertovat barevné obrázky na černobílé nebo stupně šedi pro účely tisku nebo archivace. Tento článek ukazuje použití Aspose.PSD pro Java API k dosažení tohoto pomocí dvou metod, jak je uvedeno níže.

- Binarizace
- Převod na stupně šedi
### **Binarizace**
Abychom porozuměli konceptu binarizace, je důležité definovat binární obraz; jedná se o digitální obraz, který může mít pro každý pixel pouze dvě možné hodnoty. Obvykle se pro binární obraz používají dvě barvy - černá a bílá, i když mohou být použity jakékoliv dvě barvy. Binarizace je proces převodu obrázku na binární, což znamená, že každý pixel je uložen jako jediný bit (0 nebo 1), kde 0 znamená absenci barvy a 1 znamená přítomnost barvy. Aspose.PSD pro Java API v současné době podporuje dvě metody binarizace.
#### **Binarizace s pevným prahem**
Následující kódová ukázka vám ukazuje, jak aplikovat binarizaci s pevným prahem na obrázek.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Binarizace s Otsu prahem**
Následující kódová ukázka vám ukazuje, jak aplikovat binarizaci s Otsu prahem na obrázek.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Převod na stupně šedi**
Šedé škálování je proces převodu obrázku s nepřetržitými tóny na obrázek s přerušenými stupni šedi. Následující kódová ukázka vám ukazuje, jak použít šedé škálování.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Převést vrstvy obrázku GIF na obrázek TIFF**
Někdy je potřeba extrahovat a převést vrstvy obrázku PSD do jiného rastrového formátu obrázku pro splnění potřeby aplikace. API Aspose.PSD podporuje funkci extrahování a převodu vrstev obrázku PSD do jiného rastrového formátu obrázku. Nejprve vytvoříme instanci obrázku a načteme obrázek PSD z lokálního disku, poté budeme iterovat každou vrstvu v vlastnosti Layer. Poté převedeme blok na obrázek TIFF. Následující kódová ukázka vám ukazuje, jak převést vrstvy obrázku PSD na obrázky TIFF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **Převod CMYK PSD na CMYK TIFF**
Pomocí Aspose.PSD pro Java mohou vývojáři převádět soubor CMYK PSD na formát tiff CMYK. Tento článek ukazuje, jak exportovat / převést soubor CMYK PSD na formát tiff CMYK s pomocí Aspose.PSD. Pomocí Aspose.PSD pro Java můžete načítat obrázky PSD a poté můžete nastavit různé vlastnosti pomocí třídy TiffOptions a uložit nebo exportovat obrázek. Následující kódová ukázka vám ukazuje, jak dosáhnout této funkce.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Export obrázků**
Kromě bohatého souboru zpracovávacích rutin Aspose.PSD poskytuje specializované třídy pro konverzi formátů souborů PSD na jiné formáty. Použití této knihovny je velmi jednoduché a intuitivní. Zde jsou některé specializované třídy v namespace ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

S Aspose.PSD pro Java API je snadné exportovat obrázky PSD. Vše, co potřebujete, je objekt příslušné třídy z namespace ImageOptions. Použitím těchto tříd můžete snadno exportovat libovolný obrázek vytvořený, upravený nebo jednoduše načtený pomocí Aspose.PSD pro Java do libovolného podporovaného formátu.
## **Kombinace obrázků**
Tento příklad používá třídu Graphics a ukazuje, jak kombinovat dva nebo více obrázků do jednoho kompletního obrázku. K demonstrování operace příklad vytvoří nový PsdImage a nakreslí obrazy na plochu plátna pomocí metody Draw Image vystavené třídou Graphics. Pomocí třídy Graphics lze kombinovat dva nebo více obrázků tak, že výsledný obrázek bude vypadat jako kompletní obraz s žádným prostorem mezi částmi obrázku a žádnými stránkami. Velikost plátna musí být rovna velikosti výsledného obrázku. Následuje kódová ukázka, která ukazuje, jak použít metodu Draw Image třídy Graphics pro kombinaci obrázků do jednoho obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Roztažení a ořezání obrázků**
API Aspose.PSD vám umožňuje rozšířit nebo oříznout obrázek během procesu konverze obrázku. Vývojář musí vytvořit obdélník s X a Y souřadnicemi a určit šířku a výšku obdélníkové krabice. X, Y a šířka, výška obdélníka budou znázorňovat rozšíření nebo ořezání načteného obrázku. Pokud je během konverze obrázku nutné rozšířit nebo oříznout obrázek, proveďte následující kroky:

1. Vytvořte instanci třídy RasterImage a načtěte existující obrázek.
1. Vytvořte instanci třídy ImageOption.
1. Vytvořte instanci třídy Rectangle a inicializujte X, Y a šířku, výšku obdélníka.
1. Zavolejte metodu Save třídy RasterImage a předejte název výstupního souboru, možnosti obrázku a objekt obdélníku jako parametry.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Čtení a zápis dat XMP do obrázků**
XMP (Extensible Metadata Platform) je ISO standard. XMP standardizuje datový model, formát serializace a základní vlastnosti pro definici a zpracování rozšiřitelných metadat. Poskytuje také pokyny pro vložení informací XMP do populárních obrázků, jako je JPEG, aniž by narušily jejich čitelnost aplikacemi, které XMP nepodporují. S využitím Aspose.PSD pro Java API mohou vývojáři číst nebo zapisovat XMP metadata do obrázků. Tento článek ukazuje, jak mohou být metadata XMP přečtena z obrázku a jak mohou být XMP metadata zapsána do obrázků.
### **Vytvořit XMP Metadata, Zapsat a Číst Ze Souboru**
S pomocí prostoru názvů XMP může vývojář vytvořit objekt metadat XMP a zapsat ho do obrázku. Následující kódová ukázka vám ukazuje, jak používat balíčky XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage a DublinCorePackage obsažené v prostoru názvů XMP.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Export obrázků v prostředí vícevláknového prostředí**
Aspose.PSD pro Java nyní podporuje konverzi obrázků v prostředí vícevláknového prostředí. Aspose.PSD pro Java zajistí optimalizovaný výkon operací během provádění kódu v vícevláknovém prostředí. Všechny třídy možností obrázků (např. BmpOptions, TiffOptions, JpegOptions atd.) v Aspose.PSD pro Java implementují rozhraní IDisposable. Proto je důležité, aby vývojář správně uvolnil objekt třídy možností obrázku v případě, že je nastavena vlastnost Source. Následující kódová ukázka ukazuje uvedenou funkcionalitu.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



Aspose.PSD nyní podporuje vlastnost SyncRoot při práci v vícevláknovém prostředí. Vývojář může tuto vlastnost použít k synchronizaci přístupu k zdrojovému proudu. Následující kódová ukázka ukazuje, jak může být vlastnost SyncRoot použita.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

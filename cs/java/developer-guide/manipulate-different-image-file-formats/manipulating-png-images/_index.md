---
title: Manipulace s PNG obrázky
type: docs
weight: 30
url: /cs/java/manipulace-s-png-obrazky/
---

## **Specifikace průhlednosti pro PNG obrázky**
Jednou z výhod ukládání obrázků ve formátu PNG je možnost mít průhledné pozadí. Aspose.PSD pro Jav využívá funkci pro specifikaci průhlednosti pro třídy PngImage & RasterImage, jak je ukázáno v následující sekci. API Aspose.PSD pro Jav může být použito k nastavení libovolné barvy jako průhledné při vytváření nových PNG obrázků nebo převádění existujících obrázků do formátu PNG. Pro tyto účely API Aspose.PSD pro Jav poskytuje vlastnost TransparentColor a výčet PngColorType, který lze nastavit pro specifikaci jakékoliv barvy, která bude vykreslena jako průhledná v PNG obrázku. Následující kódový úryvek ukazuje, jak převést existující obrázek PSD na obrázek PNG pomocí přetíženého konstruktoru PngImage a specifikovat požadovanou barvu jako průhlednou.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Nastavení rozlišení pro PNG obrázky**
Aspose.PSD pro Jav poskytuje třídu ResolutionSetting, která může být použita k nastavení rozlišení pro všechny formáty obrázků včetně PNG. Tento článek demonstruje použití API Aspose.PSD pro Jav k nastavení parametrů horizontálního a vertikálního rozlišení pro formát obrázku PNG. Následující kódový úryvek načítá existující obrázek PSD a konvertuje jej do formátu PNG, změňuje také rozlišení.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **Komprimace souborů PNG**
Formát Portable Network Graphic (PNG) je ztrátově komprimovaný formát pro přenos bitmapy po sítích. Když uložíte obrázek jako soubor PNG v jakémkoli programu, může se vás požádat, abyste vybrali úroveň komprese v rozmezí od 0 do jakékoli maximální úrovně. Nastavení této hodnoty ve skutečnosti komprimuje velikost souboru a doopravdy neovlivňuje kvalitu obrázku. Tento článek popisuje, jak API Aspose.PSD umožňuje kontrolovat velikost souboru PNG. API Aspose.PSD může být použito k nastavení kompresní úrovně pro formát souboru PNG pomocí třídy PngOptions, která má vlastnost CompressionLevel typu int. Tato vlastnost přijímá hodnotu od 0 do 9, kde 9 je maximální komprese. Následující kódový úryvek ukazuje, jak nastavit kompresní úrovně pomocí API Aspose.PSD pro Jav.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Specifikace barevné hloubky pro PNG obrázky**
Barevná hloubka v obrazové technice je počet bitů použitých k indikaci barvy jednoho pixelu v mapě bitů. Stejně jako u všech ostatních bitmapových formátů je barva PNG také vyjádřena v bitech, například 1 bit (2 barvy), 2 bity (4 barvy), 4 bity (16 barev) a 8 bitů (256 barev). API Aspose.PSD pro Jav může být použito k nastavení barevné hloubky pro PNG obrázky pomocí vlastnosti BitDepth, kterou má třída PngOptions. V současné době lze vlastnost BitDepth nastavit na 1, 2, 4 nebo 8 bitů pro stupně šedi a indexované barevné typy. Pro všechny ostatní typy barev jsou podporovány pouze 8 bitů. Následující kódový úryvek ukazuje, jak nastavit barevnou hloubku pro PNG obrázek.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Použití metody filtru na obrázky PNG**
Aspose.PSD pro Jav poskytuje výčet PngFilterType, který může být použit k nastavení typu filtru pro obrázek PNG. Následující kódový úryvek ukazuje, jak aplikovat filtr na existující soubor PSD na obrázek PNG pomocí PngFilterType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Změna barvy pozadí průhledného obrázku PNG**
Obrázky ve formátu PNG mohou mít průhledné pozadí. Aspose.PSD pro Jav poskytuje možnost změnit barvu pozadí pro PNG obrázek s průhledným pozadím. API Aspose.PSD pro Jav může být použito k nastavení/změně barvy průhledného PNG obrázku. Následující kódový úryvek ukazuje, jak nastavit/změnit barvu pozadí průhledného PNG obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}

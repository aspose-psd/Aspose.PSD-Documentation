---
title: Použití mediánového a Wienerova filtru
type: docs
weight: 10
url: /cs/pouziti-medianoveho-a-wienerova-filtru/
---

## **Použití mediánového a Wienerova filtru**
Mediánový filtr je nelineární digitální filtrační technika, často používaná k odstranění šumu. Takové snížení šumu je typickým krokem předzpracování pro zlepšení výsledků pozdějšího zpracování. Wienerův filtr je optimální stacionární lineární filtr MSE (střední čtvercová chyba) pro obrázky poškozené aditivním šumem a rozmazáním. Vývojáři API Aspose.PSD pro jazyk Java mohou aplikovat mediánový filtr k odšumování obrazu a mohou aplikovat Gaussův Wienerův filtr na obrázky. Tento článek ukazuje, jak mohou být mediánový filtr a Gaussův Wienerův filtr aplikovány na obrázky.
### **Použití mediánového filtru**
Aspose.PSD poskytuje třídu MedianFilterOptions pro aplikaci filtru na RasterImage. Následující ukázkový kód ukazuje, jak aplikovat mediánový filtr na rastrový obrázek.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Použití Gauss Wienerova filtru**
Aspose.PSD poskytuje třídu GaussWienerFilterOptions pro aplikaci filtru na RasterImage. Následující ukázkový kód ukazuje, jak aplikovat Gaussův Wienerův filtr na rastrový obrázek.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Použití Gauss Wienerova filtru pro barevný obrázek**
Aspose.PSD poskytuje třídy GaussWienerFilterOptions i pro barevné obrázky. Následující ukázkový kód ukazuje, jak aplikovat Gaussův Wienerův filtr na barevný obrázek.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Použití Motion Wienerova filtru**
Aspose.PSD poskytuje třídu MotionWienerFilterOptions pro aplikaci filtru na RasterImage. Následující ukázkový kód ukazuje, jak aplikovat filtr pohybu Wiener na rastrový obrázek.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Aplikace korekčního filtru na obrázek**
Tento článek ukazuje použití Aspose.PSD pro jazyk Java k provádění korekčních filtrů na obrázku. API Aspose.PSD nabízí efektivní a snadno použitelné metody pro dosažení tohoto cíle. Aspose.PSD pro jazyk Java vystavil třídy BilateralSmoothingFilterOptions a SharpenFilterOptions pro filtrace. Třída BilateralSmoothingFilterOptions potřebuje jako velikost celé číslo. Postup pro provedení změny velikosti je jednoduchý jak následuje:


1. Načtěte obrázek pomocí metody Factory Load, kterou exponuje třída Image.
1. Převeďte obrázek na RasterImage.
1. Vytvořte instance tříd BilateralSmoothingFilterOptions a SharpenFilterOptions.
1. Zavolejte metodu RasterImage.Filter s určením obdélníku jako hranice obrázku a instance třídy BilateralSmoothingFilterOptions.
1. Zavolejte metodu RasterImage.Filter s určením obdélníku jako hranice obrázku a instance třídy SharpenFilterOptions.
1. Upravte kontrast.
1. Nastavte jas.
1. Uložte výsledky.

Následující kódový úryvek vám ukazuje, jak aplikovat korekční filtr.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Použití Bradleyho algoritmu prahování**
Prahování obrázků se používá v grafických aplikacích. Cílem prahování obrázku je klasifikovat pixely jako "tmavé" nebo "světlé". Aspose.PSD API vám umožňuje používat Bradleyho prahování při převodu obrázků. Následující kódový úryvek vám ukazuje, jak definovat hodnotu prahu a poté spustit Bradleyho algoritmus prahování.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}

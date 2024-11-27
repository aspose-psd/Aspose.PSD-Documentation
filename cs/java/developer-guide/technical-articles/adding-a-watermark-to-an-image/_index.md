---
title: Přidání vodoznaku k obrázku
type: docs
weight: 20
url: /cs/přidání-vodoznaku-k-obrázku/
---

## **Přidání vodoznaku k obrázku**
Tento dokument vysvětluje, jak přidat vodoznak k obrázku pomocí Aspose.PSD. Přidání vodoznaku k obrázku je běžný požadavek pro aplikace zpracovávající obrázky. Tento příklad používá třídu Graphics k vykreslení řetězce na povrch obrázku.
### **Přidání vodoznaku**
K demonstraci operace načteme obrázek BMP z disku a pomocí metody DrawString třídy Graphics vykreslíme řetězec jako vodoznak na povrchu obrázku. Obrázek uložíme ve formátu PNG pomocí třídy PngOptions. Níže je ukázkový kód, který demonstruje, jak přidat vodoznak k obrázku. Zdrojový kód příkladu byl rozdělen do částí, aby byl snadno sledovatelný. Postupně příklady ukazují, jak:

1. Načíst obrázek.
1. Vytvořit a inicializovat objekt Graphics.
1. Vytvořit a inicializovat objekty Font a SolidBrush.
1. Vykreslit řetězec jako vodoznak pomocí metody DrawString třídy Graphics.
1. Uložit obrázek ve formátu PNG.

Následující ukázka kódu vám ukazuje, jak přidat vodoznak k obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Přidání diagonálního vodoznaku**
Přidání diagonálního vodoznaku k obrázku je podobné přidání vodorovného vodoznaku, jak bylo diskutováno výše, s několika rozdíly. K demonstraci operace načteme obrázek JPG z disku, přidáme transformace pomocí objektu třídy Matrix a vykreslíme řetězec jako vodoznak na povrchu obrázku pomocí metody DrawString třídy Graphics. Níže je ukázkový kód, který demonstruje, jak přidat diagonální vodoznak k obrázku. Zdrojový kód příkladu byl rozdělen do částí, aby byl snadno sledovatelný. Postupně příklady ukazují, jak:

1. Načíst obrázek.
1. Vytvořit a inicializovat objekt Graphics.
1. Vytvořit a inicializovat objekty Font a SolidBrush.
1. Získat velikost obrázku v objektu SizeF.
1. Vytvořit instanci třídy Matrix a provést složenou transformaci.
1. Přiřadit transformaci objektu Graphics.
1. Vytvořit a inicializovat objekt třídy StringFormat.
1. Vykreslit řetězec jako vodoznak pomocí metody DrawString třídy Graphics.
1. Uložit výsledný obrázek.

Následující ukázka kódu vám ukazuje, jak přidat diagonální vodoznak.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}

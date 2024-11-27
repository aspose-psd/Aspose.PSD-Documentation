---
title: Přidání vodoznaku do obrázku
type: docs
weight: 30
url: /cs/net/přidání-vodoznaku-do-obrázku/
---

## **Přidání vodoznaku do obrázku**
Tento dokument vysvětluje, jak přidat vodoznak do obrázku pomocí Aspose.PSD. Přidání vodoznaku do obrázku je běžným požadavkem pro aplikace zpracování obrazu. Tento příklad používá třídu Graphics k nakreslení řetězce na povrch obrázku.
### **Přidání vodoznaku**
Pro demonstraci operace načteme obrázek BMP z disku a nakreslíme řetězec jako vodoznak na povrch obrázku pomocí metody DrawString třídy Graphics. Obrázek uložíme do formátu PNG pomocí třídy PngOptions. Níže je ukázkový kód, který demonstruje, jak přidat vodoznak do obrázku. Ukázkový zdrojový kód byl rozdělen na části, aby bylo snadné jej sledovat. Postupně ukázky ukazují, jak:

1. [Načíst](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) obrázek.
1. Vytvořit a inicializovat objekt [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. Vytvořit a inicializovat objekty Font a [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. Nakreslit řetězec jako vodoznak pomocí metody [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) třídy Graphics.
1. Uložit obrázek do PNG.

Následující ukázkový kód vám ukazuje, jak přidat vodoznak do obrázku.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Přidání diagonálního vodoznaku**
Přidání diagonálního vodoznaku do obrázku je podobné přidání vodorovného vodoznaku, jak bylo diskutováno výše, s několika rozdíly. Pro demonstraci operace načteme obrázek JPG z disku, přidáme transformace pomocí objektu třídy [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) a nakreslíme řetězec jako vodoznak na povrch obrázku pomocí metody DrawString třídy Graphics. Níže je ukázkový kód, který demonstruje, jak přidat diagonální vodoznak do obrázku. Ukázkový zdrojový kód byl rozdělen na části, aby bylo snadné jej sledovat. Postupně ukázky ukazují, jak:

1. Načíst obrázek.
1. Vytvořit a inicializovat objekt Graphics.
1. Vytvořit a inicializovat objekty [Font](https://reference.aspose.com/psd/net/aspose.psd/font) a SolidBrush.
1. Získat velikost obrázku ve [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. Vytvořit instanci třídy Matrix a provést složenou transformaci.
1. Přiřadit transformaci objektu Graphics.
1. Vytvořit a inicializovat objekt [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. Nakreslit řetězec jako vodoznak pomocí metody DrawString třídy Graphics.
1. Uložit výsledný obrázek.

Následující ukázkový kód vám ukazuje, jak přidat diagonální vodoznak.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}

---
title: Přidání podpisu k obrázku
type: docs
weight: 10
url: /cs/pridani-podpisu-k-obrazku/
---

## **Přidání podpisu**


Přidání podpisu k obrázku je někdy nezbytné pro digitální podepisování obrázků, aby se předešlo padělání. Další možností může být zacházení s obrázkem tak, jako by byl vystavován v galerii. Bez ohledu na důvod, API Aspose.PSD poskytují funkci přidání podpisu k obrázku pomocí nejjednoduššího mechanismu, jak je vysvětleno níže. Všimněte si, že toto ukázka využívá třídu Graphics k nakreslení dalšího obrázku s podpisem na původní povrch obrázku. Pro demonstrování operace načteme obrázek PSD z disku a nakreslíme další obrázek s podpisem na původní plochu obrázku pomocí metody DrawImage třídy Graphics. Výsledný obrázek uložíme ve formátu PNG pomocí třídy PngOptions. Níže je příklad kódu, který demonstruje, jak přidat podpis k obrázku. Zdrojový kód je rozdělen do částí, aby bylo snadné ho sledovat. Krok za krokem příklad ukazuje, jak:

- Načíst primární a sekundární (podpisové) obrázky.
- Vytvořit a inicializovat objekt Graphics.
- Nakreslit obrázek pomocí metody DrawImage třídy Graphics.
- Uložit výsledek ve formátu PNG.
### **Příklady programů**
#### **Načítání obrázků**
Nejprve vytvořte instance třídy Image pro načtení ukázkových obrázků z disku.
#### **Vytvoření a inicializace grafického objektu**
Po načtení obrázků vytvořte a inicializujte objekt třídy Graphics pomocí objektu primárního obrázku.
#### **Nakreslení sekundárního obrázku na primární obrázek**
Pak pomocí metody DrawImage třídy Graphics přidejte sekundární obrázek na primární obrázek. Metoda DrawImage má několik verzí, které přijímají objekt Image jako první parametr, zatímco všechny ostatní parametry odpovídají místu, kam má být obrázek nakreslen. Pro účely demonstrace následující kód používá přetíženou verzi DrawImage, která přijímá objekt Point jako druhý parametr a snaží se podpis nakreslit do pravé dolní části primárního obrázku.
#### **Uložení obrázku**
Nakonec uložte obrázek zpět na lokální disk jako soubor PNG pomocí třídy PngOptions.
#### **Kompletní zdrojový kód**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}

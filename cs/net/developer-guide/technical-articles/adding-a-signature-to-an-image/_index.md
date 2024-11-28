---
title: Přidání podpisu k obrázku
type: docs
weight: 70
url: /cs/přidání-podpisu-k-obrázku/
---

## **Přidání podpisu**

Přidání podpisu k obrázku je někdy vyžadováno k digitálnímu podepisování obrázků a zabránění padělání. Dalším záměrem může být zacházení s obrázkem, jako by byl představen v galerii. Bez ohledu na důvod, rozhraní API Aspose.PSD poskytuje funkci pro přidání podpisu k obrázku pomocí nejjednoduššího mechanismu, jak je vysvětleno níže. Všimněte si, že tento příklad využívá třídu [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) pro nakreslení dalšího obrazu s podpisem na původní povrch obrázku. Pro demonstraci operace budeme načítat obrázek PSD ze serveru a nakreslíme další obraz jako podpis na povrch původního obrázku pomocí metody [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) třídy Graphics. Výsledný obrázek uložíme ve formátu PNG pomocí třídy [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions). Níže je uveden příklad kódu, který ukazuje, jak přidat podpis k obrázku. Příklad zdrojového kódu byl rozdělen do částí, aby bylo snazší ho sledovat. Krok za krokem příklad ukazuje, jak:

- Načíst primární a sekundární (podpisové) obrázky.
- Vytvořit a inicializovat objekt Graphics.
- Nakreslit obrázek pomocí metody DrawImage třídy Graphics.
- Uložit výsledek ve formátu PNG.
### **Programové vzorky**
#### **Načítání obrázků**
Nejprve vytvořte instance třídy Image pro načtení vzorových obrázků ze serveru.
#### **Vytváření a inicializace objektu Graphic**
Po načtení obrázků vytvořte a inicializujte objekt třídy Graphics při použití objektu primárního obrázku.
#### **Nakreslení sekundárního obrazu na primární obrázek**
Poté pomocí metody DrawImage třídy Graphics přidejte sekundární obrázek na primární obrázek. Existuje několik verzí metody DrawImage, které přijímají objekt obrázku jako první parametr, zatímco všechny ostatní parametry odpovídají místu, kam má být obrázek nakreslen. Pro účely demonstrace následující kód používá verzi přetížení DrawImage, která přijímá objekt typu Point jako druhý parametr, a snaží se nakreslit podpis v pravém dolním rohu primárního obrázku.
#### **Ukládání obrázku**
Nakonec uložte obrázek zpět na lokální server jako soubor PNG pomocí třídy PngOptions.
#### **Kompletní zdrojový kód**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}

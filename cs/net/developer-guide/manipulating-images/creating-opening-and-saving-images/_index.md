---
title: Vytváření, Otevírání a Ukládání Obrázků
type: docs
weight: 30
url: /cs/net/vytvareni-otevirani-a-ukladani-obrazku/
---

## **Vytváření Souborů s Obrázky**
Aspose.PSD pro .NET umožňuje vývojářům vytvářet vlastní obrázky. K vytvoření nových obrázků použijte statickou metodu Create, kterou nabízí třída Image. Vše, co musíte udělat, je poskytnout vhodný objekt jedné z tříd z prostoru názvů ImageOptions pro požadovaný výstupní formát obrázku. Pro vytvoření obrázkového souboru nejprve vytvořte instanci jedné z tříd z prostoru názvů ImageOptions. Tyto třídy určují formát výstupního obrázku. Níže jsou uvedeny některé třídy z prostoru názvů ImageOptions (poznamenejte, že jsou v současné době podporovány pouze rodiny formátů souborů PSD pro vytváření):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) nastavuje možnosti pro vytváření souboru PSD. Obrázkové soubory lze vytvořit nastavením výstupní cesty nebo nastavením proudu.
### **Vytváření Nastavením Cesty**
Vytvořte PsdOptions z prostoru názvů ImageOptions a nastavte různé vlastnosti. Nejdůležitější vlastností k nastavení je vlastnost Source. Tato vlastnost určuje, kde jsou uložena data obrázku (v souboru nebo v proudu). V příkladu níže je zdrojem soubor. Po nastavení vlastností předejte objekt jedné z statických metod [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) spolu s parametrem šířky a výšky. Šířka a výška jsou definovány v pixelech.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Vytváření Pomocí Proudu**
Postup pro vytvoření obrázku pomocí proudu je stejný jako u využití cesty. Jediný rozdíl spočívá v tom, že musíte vytvořit instanci třídy [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) tím, že Stream objekt předáte jeho konstruktoru a přiřadíte ho vlastnosti Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Otevírání Obrázkových Souborů**
Vývojáři mohou pomocí API Aspose.PSD pro .NET otevřít existující obrázkové soubory PSD pro různé účely, například přidávání efektů na obrázek nebo konverzi existujícího souboru do jiného formátu. Bez ohledu na účel, Aspose.PSD poskytuje dvě standardní způsoby otevírání existujících souborů: ze souboru nebo z proudu.
### **Otevírání z Disku**
Otevřete obrázkový soubor předáním cesty a názvu souboru jako parametru statické metody Load, kterou nabízí třída Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Otevírání pomocí Proudu**
Někdy je obrázek, který potřebujeme otevřít, uložen jako proud. V takových případech použijte přetíženou verzi metody Load. Tato metoda přijímá objekt Stream jako argument k otevření obrázku.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Načtení Obrázku jako Vrstvy**
Tento článek demonstruje použití Aspose.PSD k načtení obrázku jako vrstvy. API Aspose.PSD nabízí efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD vystavil metodu AddLayer třídy PsdImage k přidání obrázku do souboru PSD jako vrstvy.

Kroky k načtení obrázku do PSD jako vrstvy jsou velmi jednoduché:

- Vytvořte instanci obrázku pomocí třídy PsdImage s určenou šířkou a výškou.
- Načtěte soubor PSD jako obrázek pomocí tovární metody Load vystavené třídou Image.
- Vytvořte instanci třídy Layer a přiřaďte do ní vrstvu obrázku PSD.
- Přidejte vytvořenou vrstvu pomocí metody AddLayer vystavené třídou PsdImage
- Uložte výsledky.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Načtení Obrázku jako Vrstvy z Proudu**
Tento článek demonstruje použití Aspose.PSD k načtení obrázku jako vrstvy z proudu. Pro načtení obrázku z proudu jednoduše předejte objekt proudu, který obsahuje obrázek, konstruktoru třídy Layer. Přidejte vytvořenou vrstvu pomocí metody AddLayer vystavené třídou PsdImage a uložte výsledky.


Zde je ukázkový kód.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Ukládání Obrázkových Souborů**
Aspose.PSD vám umožňuje vytvářet obrázkové soubory od základů. Také poskytuje možnosti upravovat existující obrázkové soubory. Jakmile je obrázek vytvořen nebo upraven, soubor je obvykle uložen na disk. Aspose.PSD vám poskytuje metody pro ukládání obrázků na disk tím, že specifikujete cestu nebo použitím objektu Stream.
### **Ukládání na Disk**
Třída Image reprezentuje objekt obrázku, takže tato třída poskytuje veškeré nástroje potřebné k vytvoření, načtení a uložení obrázkového souboru. Pro uložení obrázků použijte metodu Save třídy Image. Jedna přetížená verze metody Save přijímá umístění souboru jako řetězec.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Ukládání do Proudu**
Další přetížená verze metody Save přijímá objekt Stream jako argument a uloží obrázkový soubor do proudu.

Pokud je obrázek vytvářen pomocí jakéhokoli z CreateOptions v konstruktoru Image, obrázek je automaticky uložen na cestě nebo do proudu dodaného během inicializace třídy Image voláním metody Save, která nepřijímá žádný parametr.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Nastavení Pro Nahrazování Chybějících Písem**
Vývojáři mohou využít API Aspose.PSD pro .NET k načtení existujících obrázkových souborů PSD pro různé účely, například k nastavení výchozího názvu písma při ukládání dokumentů PSD jako rastrový obrázek (do formátů PNG, JPG a BMP). Toto výchozí písmo by mělo být použito jako náhrada všech chybějících písem (písem, která nejsou nalezena v aktuálním operačním systému). Jakmile je obrázek upraven, soubor bude uložen na disk.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}

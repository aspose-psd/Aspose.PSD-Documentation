---
title: Vytváření, Otevírání a Ukládání Obrázků
type: docs
weight: 30
url: /cs/vytvareni-otevirani-a-ukladani-obrazku/
---

## **Vytváření Obrázkových Souborů**
Aspose.PSD pro Javu umožňuje vývojářům vytvářet vlastní obrázky. Použijte statickou metodu Create vystavenou třídou Image k vytvoření nových obrázků. Vše, co musíte udělat, je dodat odpovídající objekt jedné ze tříd z prostoru jmen ImageOptions pro požadovaný formát výstupního obrázku. Pro vytvoření obrázkového souboru nejprve vytvořte instanci jedné ze tříd z prostoru jmen ImageOptions. Tyto třídy určují formát výstupního obrázku. Níže jsou uvedeny některé třídy z prostoru jmen ImageOptions (všimněte si, že v současné době jsou podporovány pouze formáty souborů PSD):

PsdOptions nastaví možnosti pro vytváření souboru PSD. Obrázkové soubory lze vytvořit nastavením výstupní cesty nebo nastavením proudu.
### **Vytváření Nastavením Cesty**
Vytvořte PsdOptions z prostoru jmen ImageOptions a nastavte různé vlastnosti. Nejdůležitější vlastností k nastavení je vlastnost Source. Tato vlastnost určuje, kde se nachází obrázková data (v souboru nebo v proudu). V následujícím příkladu je zdrojem soubor. Po nastavení vlastností předejte objekt jedné z statických metod Create společně s parametrem width a height. Šířka a výška jsou definovány v pixelech.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Vytváření Použitím Proudu**
Postup pro vytvoření obrázku pomocí proudu je stejný jako při použití cesty. Jediný rozdíl spočívá v tom, že musíte vytvořit instanci StreamSource předáním objektu Stream do jeho konstruktoru a přiřazením ho vlastnosti Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Otevírání Obrázkových Souborů**
Vývojáři mohou použít API Aspose.PSD pro Javu k otevírání existujících obrázkových souborů PSD pro různé účely, například přidání efektů k obrázku nebo převodu existujícího souboru do jiného formátu. Bez ohledu na účel poskytuje Aspose.PSD dvě standardní způsoby, jak otevřít existující soubory: ze souboru nebo z proudu.
### **Otevírání z Disku**
Otevřete obrázkový soubor předáním cesty a názvu souboru jako parametru statické metody Load vystavené třídou Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Otevírání Použitím Proudu**
Někdy je obrázek, který potřebujeme otevřít, uložen jako proud. V takových případech použijte přetíženou verzi metody Load. Tato verze přijímá objekt Stream jako argument pro otevření obrázku.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Načtení Obrázku Jako Vrstvy**
Tento článek demonstruje použití Aspose.PSD k načtení obrázku jako vrstvy. API Aspose.PSD poskytuje efektivní a snadno použitelné metody pro dosažení tohoto cíle. Aspose.PSD vystavil metodu AddLayer třídy PsdImage pro přidání obrázku do souboru PSD jako vrstvy.

Kroky pro načtení obrázku do PSD jako vrstvy jsou jednoduché, jak je uvedeno níže:

- Vytvořte instanci obrázku pomocí třídy PsdImage se zadanou šířkou a výškou.
- Načtěte soubor PSD jako obrázek pomocí metody Load továrny vystavené třídou Image.
- Vytvořte instanci třídy Layer a přiřaďte k ní vrstvu obrázku PSD.
- Přidejte vytvořenou vrstvu pomocí metody AddLayer vystavené třídou PsdImage.
- Uložte výsledky.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Ukládání Obrázkových Souborů**
Aspose.PSD umožňuje vytvářet obrázkové soubory zcela od začátku. Také poskytuje možnosti upravovat existující obrázkové soubory. Jakmile je obrázek vytvořen nebo upraven, je soubor obvykle uložen na disk. Aspose.PSD vám poskytuje metody pro ukládání obrázků na disk zadaním cesty nebo použitím objektu Stream.
### **Ukládání na Disk**
Třída Image představuje objekt obrázku, takže tato třída poskytuje všechny nástroje potřebné pro vytváření, načítání a ukládání souboru s obrázkem. Použijte metodu Save třídy Image k ukládání obrázků. Jedna přetížená verze metody Save přijímá umístění souboru jako řetězec.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Ukládání do Proudu**
Další přetížená verze metody Save přijímá objekt Stream jako argument a ukládá obrázkový soubor do proudu.

Pokud je obrázek vytvořen určením jakéhokoli z CreateOptions v konstruktoru Image, obrázek je automaticky uložen na zadanou cestu nebo proud při inicializaci třídy Image voláním metody Save, která nepřijímá žádný parametr.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Nastavení Pro Nahrazení Chybějících Písem**
Vývojáři mohou použít API Aspose.PSD pro Javu k načítání existujících obrázkových souborů PSD pro různé účely, například nastavení výchozího názvu písma při ukládání PSD dokumentů jako rastrových obrázků (do formátů PNG, JPG a BMP). Toto výchozí písmo by mělo být použito jako náhrada pro všechna písmena, která chybějí (písma, která nejsou nalezena v aktuálním operačním systému). Jakmile je obrázek upraven, soubor bude uložen na disk.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}

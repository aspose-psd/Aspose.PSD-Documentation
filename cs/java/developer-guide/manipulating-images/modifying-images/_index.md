---
title: Úprava obrázků
type: docs
weight: 50
url: /cs/java/uprava-obrazku/
---

## **Dithering pro rastrové obrázky**
Dithering je technika vytváření iluze nových barev a odstínů tím, že se mění vzorek bodů, který skutečně vytváří obraz. Jedná se o nejběžnější způsob snížení barevného rozsahu obrázků na 256 (nebo méně) barev. Aspose.PSD poskytuje podporu pro dithering pro třídu RasterImage pomocí metody Dither, která přijímá dva parametry. První je typu DitheringMethod, který se má použít, s dvěma možnostmi: FloydSteinbergDithering a ThresholdDithering. Druhým parametrem pro metodu Dither je BitCount jako celé číslo. BitCount definuje velikost vzorkování pro výsledek ditheringu. Výchozí hodnota je 1, což představuje černobílou, zatímco povolené hodnoty jsou 1, 4, 8 generující palety s 2, 4 a 256 barvami.

## **Úprava jasu, kontrastu a gammy**
Úpravy barev v digitálních obrazech jsou jednou z hlavních funkcí, které většina knihoven pro zpracování obrazu poskytuje. Úpravy barev lze rozdělit do následujících kategorií:

1. **Jas** odkazuje na světlost nebo tmavost barvy. Zvýšení jasu obrázku zesvětlí všechny barvy, zatímco snížení jasu ztmaví všechny barvy.
2. **Kontrast** odkazuje na zvýraznění objektů nebo detailů v obraze. Zvýšení kontrastu obrahuje rozdíl mezi světlými a tmavými oblastmi tak, že světlé oblasti se stanou světlejšími a tmavé oblasti tmavšími. Snížení kontrastu způsobí, že světlejší a tmavší oblasti zůstanou přibližně stejné, ale celkový obraz se stane homogennějším.
3. **Gama** optimalizuje kontrast a jas nepřímého osvětlení, které osvětluje objekt na obraze.

### **Úprava jasu**
Aspose.PSD pro Java API poskytuje metodu AdjustBrightness pro třídu RasterImage, která může být použita k úpravě jasu obrázku předáním celého čísla jako parametru. Nejvyšší hodnota parametru znamená jasnější obrázek. Zde je originální obrázek a výsledný obrázek k porovnání.

### **Úprava kontrastu**
Metoda AdjustContrast, kterou poskytuje třída RasterImage, může být použita k úpravě kontrastu obrázku, předáním hodnoty typu float jako parametru. Nejvyšší hodnota parametru znamená vyšší kontrast v daném obrázku. Zde je originální obrázek a výsledný obrázek k porovnání.

### **Úprava gama**
Metoda AdjustGamma poskytovaná třídou RasterImage má dvě verze. Jedna z přetížení přijímá jednu hodnotu typu float a provádí korekci gammy pro koeficienty kanálů červené, modré a zelené. Zatímco druhé přetížení přijímá tři hodnoty typu float reprezentující každý barvový koeficient zvlášť. Následující ukázkový kód ukazuje, jak provést úpravu gammy na obrázku.

## **Zamlžení obrázku**
Tento článek demonstruje použití Aspose.PSD pro Javu ke zpracování zamlžení obrázku. API Aspose.PSD poskytuje efektivní a snadno použitelné metody pro dosažení tohoto cíle. Aspose.PSD pro Java zpřístupnil třídu GaussianBlurFilterOptions pro vytvoření efektu zamlžení na počkání. Třída GaussianBlurFilterOptions potřebuje hodnoty poloměru a sigma pro vytvoření efektu zamlžení na obrázku. Kroky k provedení zmenšení jsou tak jednoduché, jak je uvedeno níže:

1. Načtěte obrázek pomocí metody Load zpřístupněné třídou Image.
2. Převedení obrázku do třídy RasterImage.
3. Vytvoření instance třídy GaussianBlurFilterOptions s výchozí konstruktorem nebo zadáním hodnot poloměru a sigma.
4. Zavolejte metodu RasterImage.Filter a současně specifikujte obdélník jako ohraničení obrázku a instanci třídy GaussianBlurFilterOptions.
5. Uložte výsledky.

## **Ověření průhlednosti obrázku**
Tento článek demonstruje použití Aspose.PSD pro Javu k ověření průhlednosti obrázku. Kroky k ověření průhlednosti obrázku jsou tak jednoduché, jak je uvedeno níže:

1. Načtěte obrázek pomocí metody Load zpřístupněné třídou Image.
2. Zkontrolujte průhlednost obrázku, pokud je průhlednost nulová, obrázek je průhledný.

## **Implementace ztrátového kompresoru GIF**
Pomocí Aspose.PSD pro Javu mohou vývojáři nastavit rozdíl mezi pixely. Kompresí GIF je založena na "slovníku" řetězců pixelů viděných. Normální kódovač hledá ve slovníku nejdelší řetězec pixelů, který přesně odpovídá pixelům v obraze. Ztrátový kódovač vybere nejdelší řetězec pixelů, který je "dostatečně podobný" pixelům v obraze. Níže je ukázka kódu této funkcionality.

## **Implementace bicubického zmenšení a zvětšení**
Zmenšení a zvětšení znamená změnu pixelových rozměrů obrázku. Při zmenšování se eliminují pixely a tím se ztrácí informace a detail z obrázku. Při zvětšení se naopak přidávají pixely. Photoshop tyto pixely přidává pomocí interpolace. Tento článek demonstruje, jak můžete provádět bicubické zmenšení a zvětšení pomocí Aspose.PSD pro Javu.

## **Vrstva úpravy Invert**
Tento článek demonstruje, jak můžete provádět vrstvu úpravy **Invert** pomocí Aspose.PSD pro Javu. Vrstva úpravy je speciální druh vrstvy používaný hlavně k úpravě barev. Místo toho, aby měly svůj vlastní obsah, úpravy upravují informace na vrstvách pod nimi. Vrstva úpravy Invert vytváří efekt negativu fotografie inverzí barev obrázku.

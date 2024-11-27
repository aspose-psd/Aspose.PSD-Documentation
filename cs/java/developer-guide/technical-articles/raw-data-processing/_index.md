---
title: Zpracování surových dat
type: docs
weight: 70
url: /cs/java/zpracovani-surovych-dat/
---

## **Zpracování surových dat**
Pro zlepšení výkonu API Aspose.PSD jsme představili metodu pro zpracování surových dat ve verzi 2.4.0. Zpracování surových dat je nyní používáno interně a má externí API, takže může být použito zvenčí knihovny k zlepšení celkového výkonu. Někdy může být zpracování komplikované a vyžadovat vysvětlení. Zpracování surových dat je v současné době k dispozici pouze pro formát BMP.

Pro pomoc vývojářům dosáhnout nejlepšího výkonu poskytuje API Aspose.PSD systém zpracování surových dat, který má externí API pro přizpůsobení. Vývojáři volají rodinu metod LoadRawData a SaveRawData k použití zpracování surových dat. Tyto metody také vyžadují nastavení požadovaného formátu surových dat pomocí třídy RawDataSettings. Třída RawDataSettings umožňuje vývojářům specifikovat libovolný formát surových dat. Nicméně k dosažení nejlepšího výkonu je nutné použít formát surových dat, ve kterém jsou data uložena. Třída RawDataSettings definovaná ve třídě RasterImage pomáhá určit formát surových dat obrázku. Při předávání instance RawDataSettings do metody LoadRawData jsou data vrácena tak, jak jsou, bez jakéhokoli aplikovaného převodu, a mohou tím zlepšit výkon. Naopak, musíte se starat o všechny možné rozlohy formátů surových dat, což může být někdy trochu složité.

Pro zjednodušení postupu, i když za cenu určité penalizace výkonu, můžete specifikovat požadované RawDataSettings instanciováním a inicializací třídy s požadovaným nastavením surových dat. Existují případy, kdy není možné vrátit surová data ve specifikovaném formátu (například převod z barevného prostoru CMYK na RGB není k dispozici ve verzi 2.4.0). Navíc mohou existovat scénáře, kdy není zpracování surových dat vůbec k dispozici pro formát obrázku. Abyste zjistili, zda můžete použít rodinu metod LoadRawData a SaveRawData, musíte se dotázat vlastnosti IsRawDataAvailable.
### **Pohlednost**
Pro formát pixelů RGB jsou k dispozici indexované (na základě palety) a RGB založené formáty surových dat. Indexované formáty surových dat obsahují indexy položek palety v rozsahu 0..(2^počet bitů – 1). Indexované formáty surových dat jsou 1, 2, 4 a 8 bitů na pixel. Zbytek jsou RGB založené formáty surových dat. Při načítání surových dat si dejte pozor, že je k dispozi dostatek bajtů ke načtení dat, jinak dojde k odpovídající výjimce. Velikost pole bajtů můžete odhadnout jednoduše násobením velikosti řádku počtem řádků. Velikost řádku se může lišit a závisí na formátu uložení surových dat.

Pro dosažení nejlepšího výkonu vždy používejte velikost řádku surových dat rovnu hodnotě vlastnosti RasterImage.RawLineSize. Nicméně někdy můžete potřebovat přidat další zarovnání k řádkům surových dat nebo je snížit a pokud tomu tak je, může být použita jiná velikost řádku. Pokud je vyžadováno podmnožina obdélníku obrázku, potom vezměte v úvahu posuny bitů, které mohou nastat pro indexované RGB pixely. Například představte si obrázek s rozměry 100x100 pixelů a formát surových dat s 1 bitem na pixel. Chcete načíst obdélník surových dat s umístěním (7,0) a rozměry (2,1), nebo jinými slovy, požadujete 2 pixely začínající od x=7 a y=0. V tomto případě byste měli získat následující rozvržení dat:

![todo:image_alt_text](raw-data-processing_1.png)

To znamená, že obdržíte 2 bajty, kde první bajt obsahuje 7 nežádoucích pixelů, poté 1 požadovaný pixel a druhý bajt obsahuje 1 požadovaný pixel a pak 7 nežádoucích. Mohlo by se vám zdát, proč jsme neprováděli posun dat a nepřidali tyto 2 pixely do jednoho bajtu? Odpověď je jednoduchá: udržet vysoký výkon. Všechno vnitřní zpracování se obvykle provádí se všemi daty začínajícími od prvního pixelu a končícími posledním dostupným pixelem. Existují vzácné situace, kdy je vyžadována podmnožina pixelů. Kromě toho nemáme ponětí, jak budou tyto pixely zpracovány dále, takže posun by snížil výkon a udělal kód zbytečně složitým. Vždy odhadujte správný bit (není třeba určovat správný byte, protože data vždy přicházejí s prvním vyplněným bytem), kde se požadované pixely začnou. Pro výpočet správného bitu může být použita jednoduchá vzorec: (rect.Left * počet bitů) % 8.
### **Konverze indexovaných RGB barev**
Pro dosažení co nejvyššího výkonu vždy používejte stejné zdrojové a cílové nastavení surových dat, formáty pixelů a velikosti řádků. Nicméně někdy můžete potřebovat provést konverzi dat. Například můžete načíst obrázek s RGB s 1 bitem na pixel a uložit ho s 2 bity na pixel nebo načíst obrázek s 4 bity RGB a snížit jeho barevný rozsah na 2 bity na pixel. V obou případech by měla být použita barevná konverze. Konverze indexovaných RGB obrázků může být někdy zapeklitá a nelze ji provést bez některých nastavení. Musíme určit, jak je mapován rozsah zdrojové barvy na cílový barevný prostor. K dosažení tohoto úkolu máme různé režimy:

- Mapování palety (DitheringMethods.PaletteConversion)
- Mapování surových dat (DitheringMethods.PaletteIgnore)
- Vlastní konverze (DitheringMethods.CustomConverter)

Při použití konverze palety se zdrojový barevný prostor snaží co nejlépe odpovídat cílovému barevnému prostoru. Předpokládejme například, že máme obrázek se 4 bity a následující barvy:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

Zdrojový obrázek vypadá následovně:

![todo:image_alt_text](raw-data-processing_2.png)

A převedeme 4bitový obrázek na 1bitový obrázek s následujícími definovanými barvami palety:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

V režimu konverze palety konvertor čte zdrojovou barvu a určuje cílový index pomocí metody GetNearestColorIndex cílové palety. Hodnota vlastnosti RasterImage.RawFallbackIndex je použita v případě, že metoda GetNearestColorIndex palety poskytne index mimo rozsah. To konvertuje zdrojové barvy na nejbližší cílové barvy z hlediska intenzitních hodnot. Cílový obrázek odpovídá zdrojovému obrázku co nejvíce. Můžete vidět následující výsledek:

![todo:image_alt_text](raw-data-processing_3.png)

V režimu mapování surových dat je použit jiný scénář. Palety zdroje a cíle jsou jednoduše ignorovány a indexy zdroje jsou mapovány na indexy cíle. Když je nalezena hodnota, která nemůže být mapována do cílového rozsahu (při snižování počtu bitů), pak je použita hodnota vlastnosti RasterImage.RawFallbackIndex. Hodnota je ve výchozím stavu 0 a bude mapována na první barvu v cílové palete. Pokud tato hodnota vlastnosti leží mimo rozsah cíle, bude vyvolána odpovídající výjimka. To vede k méně předvídatelným výsledkům, které lze zobrazit na následujícím obrázku:

![todo:image_alt_text](raw-data-processing_4.png)

Režim konverze palety je přesnějším řešením pro problém mapování barev, ale trvá také trochu déle, protože se musí provést výpočty k odhadu správného mapování palet. (Obvykle existuje velmi malý rozdíl ve výkonu mezi oběma metodami.) Naopak režim mapování surových dat je rychlejší a může být použit pro hrubší konverzi barev, kdy přesné mapování barev není tak důležité. Například existují případy, kdy je zdrojová paleta střížená a může být bezpečně konvertována na menší počet bitů, protože přebytečné bity nebyly stejně použity.

Pro použití kteréhokoli z těchto přístupů použijte vlastnost RawDitheringMethod třídy RasterImage. Ve výchozím stavu je nastavena na metodu konverze palety pro dosažení nejlepších výsledků. Tuto vlastnost můžete změnit předtím, než dojde k jakékoli konverzi (například při ukládání obrázku do streamu). Všimněte si, že metody ignorování palety a konverze palety nebudou probíhat, pokud jste načetli obrázek a přepsali některá z původních dat pixelů, protože nová data jdou do mezipaměti a mezipaměť ukládá data ve formátu 32ARGB (k datu 2.4.0, může se změnit). Tento formát je použit k překonání problémů s možnými odlišnými barevnými rozsahy u načtených a uložených obrázků. Navíc metody ignorování palety a konverze palety se nebudou uplatňovat, když je obrázek načten v režimu RGB a konvertován na indexovaný režim nebo naopak.
### **Vlastní konvertory barev**
Někdy není dostatečné použít standardní přístup pro konverzi barev. Mohli byste chtít použít vlastní algoritmus pro úplnou volnost při používání rutin konverze barev. Když jsou formáty pixelů zdrojového a cílového obrázku oba indexované RGB formáty, může být použit jednodušší rozhraní, IIndexedColorConverter. Musíte nastavit vlastnost RasterImage.RawIndexedColorConverter na instanci rozhraní IIndexedColorConverter a použít hodnotu vlastnosti RawDitheringMethod CustomConverter. Když je tato kombinace použita, každá indexovaná barevná konverze prochází touto specifikovanou instancí IIndexedColorConverter. Vlastní indexovaný barevný konvertor má následující metodu definovanou:

```java
 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);
```

Metoda FillIndexedtoIndexedMap je volána, když je vyžadována konverze z indexovaného RGB obrázku do formátu indexovaného RGB obrázku (když jsou konvertovány jakékoliv 1, 2, 4 nebo 8 bity). Pole map má délku všech možných položek formátu zdroje. Musíte to pole zaplnit mapováním z položky palety zdroje na položku palety cíle. Dejte si pozor, že hodnota indexu cíle je v rozmezí 0..(počet bitů - 1) nebo je vyvolána odpovídající výjimka.

Pokud je požadavek na provádění speciálnějšího scénáře konverze barev, měla by být vlastnost RasterImage.RawCustomColorConverter nastavena na instanci rozhraní IColorConverter. Vlastnost RawCustomColorConverter vždy přepisuje vlastnost RawIndexedColorConverter, pokud jsou nastaveny obě a indexovaný barevný konvertor nebude v takovh případě použit. Rozhraní IColorConverter má jedinou metodu:

```java
 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 
```

Metoda Convert je volána pokaždé, když je vyžadována konverze barev. Metoda přijímá surová data v zdrojovém formátu a výstupní buffer ke zpracování formátu barev konvertovaného do cílového. Výstupní buffer by měl stačit ke zpracování konvertovaných dat (pokud je volání rozhraní provedeno interně knihovnou Aspose.PSD) a měl by obsahovat konvertovaná surová data po návratu metody. Metoda Convert může být volána několikrát, dokud není pokryto celé zdrojové data.
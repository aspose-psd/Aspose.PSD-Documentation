---
title: Zpracování surových dat
type: docs
weight: 50
url: /cs/zpracovani-surovych-dat/
---

## **Zpracování surových dat**
Pro zlepšení výkonu API Aspose.PSD jsme s verzí 2.4.0 představili metodu pro zpracování surových dat. Zpracování surových dat je nyní používáno interně a má externí API, takže může být využíváno mimo knihovnu k celkovému zlepšení výkonu. Někdy může být zpracování složité a vyžadovat vysvětlení. Zpracování surových dat je v současné době k dispozici pouze pro formát BMP.

Pro pomoci vývojářům při dosažení nejlepšího výkonu poskytuje API Aspose.PSD systém pro zpracování surových dat s externím API pro přizpůsobení. Vývojáři volají rodinu metod [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) a [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) k používání zpracování surových dat. Tyto metody rovněž vyžadují nastavení požadovaného formátu surových dat pomocí třídy [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings). Třída RawDataSettings umožňuje vývojářům specifikovat libovolný formát surových dat. Nicméně pro dosažení nejlepšího výkonu je třeba použít formát surových dat, ve kterém jsou data uložena. Třída RawDataSettings definovaná ve třídě [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) pomáhá určit surový [datový formát](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat) obrázku. Při předávání instance RawDataSettings do metody LoadRawData jsou data vrácena v původní podobě, bez jakékoli aplikované konverze, což může zlepšit výkon. Naopak je třeba dbát na všechny možné layouty surových dat, což může být někdy trochu komplikované.

Pro zjednodušení procesu zpracování lze za cenu určitého poklesu výkonu specifikovat požadovaná nastavení RawDataSettings instanciováním a inicializací třídy s požadovanými nastaveními surových dat. Existují situace, kdy není možné vrátit surová data ve specifikovaném formátu (například konverze z barevného prostoru CMYK na RGB není dostupná ve verzi 2.4.0). Navíc mohou nastat situace, kdy zpracování surových dat vůbec není dostupné pro formát obrázku. Abychom zjistili, zda lze použít rodinu metod LoadRawData a SaveRawData, je třeba zkontrolovat vlastnost [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable).
### **Pohled**
Pro RGB [datový formát pixelů](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) jsou k dispozici indexované (založené na paletě) a RGB založené formáty surových dat. Indexované formáty surových dat obsahují indexy vstupu palety v rozsahu 0..(2^počet bitů – 1). Indexované formáty surových dat jsou 1, 2, 4 a 8 bitů na pixel. Ostatní formáty jsou založeny na RGB surových datech. Při načítání surových dat si dejte pozor, že jsou k dispozici dostatečné bajty pro načtení dat, jinak bude vyvolána příslušná výjimka. Velikost pole bajtů lze odhadnout jednoduše vynásobením velikosti řádku počtem požadovaných řádků. Velikost řádku se může lišit a závisí na formátu uložení surových dat.

Pro dosažení nejlepšího výkonu vždy používejte velikost řádku surových dat rovnou hodnotě vlastnosti [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize). Nicméně někdy může být třeba přidat další zarovnání do řádků surových dat nebo je snížit a v takovém případě může být použita jiná velikost řádku. Pokud je vyžadován podokruh obrázkového obdélníku, vemte v úvahu posuny bitů, které mohou nastat pro indexované RGB pixely. Předpokládejme například obrázek o rozměrech 100x100 pixelů a formát surových dat 1 bit na pixel. Chcete načíst obdélník surových dat s umístěním (7,0) a rozměry (2,1) nebo s jinými slovy, potřebujete 2 pixely začínající od x=7 a y=0. V tomto případě by vám mělo být vráceno následující uspořádání dat:



![todo:image_alt_text](raw-data-processing_1.png)

To znamená, že obdržíte 2 bajty, kde první bajt obsahuje 7 nechtěných pixelů, pak 1 požadovaný pixel a druhý bajt obsahuje 1 požadovaný pixel a pak 7 nechtěných. Můžete se ptát, proč jsme neprováděli posun dat a dali tyto 2 pixely do jednoho bajtu? Odpověď je jednoduchá: udržet vysoký výkon. Veškeré interní zpracování se typicky provádí se všemi daty začínajícími od prvního pixelu a končícími u posledního dostupného pixelu. Existují zřídka situace, kdy je vyžadována podmnožina pixelů. Kromě toho nemáme tušení, jak budou tyto pixely zpracovány následně, takže posun by snížil výkon a zbytečně by zkomplikoval kód. Vždy odhadněte správný bit (není třeba určit správný bajt, protože data vždy přichází s prvním vyplněným bajtem), kde začnou požadované pixely. Pro výpočet správného bitu lze použít jednoduchý vzorec: (rect.Left * počet bitů) % 8.
### **Konverze barev indexovaných RGB**
Pro dosažení nejvyššího výkonu vždy používejte stejná zdrojová a cílová nastavení surových dat, pixelové formáty a velikosti řádků. Nicméně někdy může být třeba provést konverzi dat. Například můžete načíst obrazek RGB s 1 bitem na pixel a uložit ho s 2 bity na pixel nebo načíst obrazek RGB s 4 bity na pixel a snížit jeho barevný rozsah na 2 bity na pixel. V každém případě je třeba použít barevnou konverzi. Konverze indexovaných RGB obrázků může být někdy složitá a nelze ji provést bez některých nastavení. Musíme určit, jak je zdrojový barevný rozsah mapován na cílový barevný prostor. K provedení této úlohy máme různé [režimy](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods):

- Mapování palety (DitheringMethods.PaletteConversion)
- Mapování surových dat (DitheringMethods.PaletteIgnore)
- Vlastní konverze (DitheringMethods.CustomConverter)

Při použití konverze palety se zdrojový barevný prostor snaží co nejvíce přiblížit cílovému barevnému prostoru. Předpokládejme například, že máme 4bitový obraz s následujícími barvami:
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

A konvertujeme 4bitový obraz na 1bitový obraz s následujícími definovanými barvami palety:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

V režimu konverze palety čte konvertor zdrojovou barvu a určuje cílový index pomocí metody [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) cílové palety. Hodnota vlastnosti [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) je použita v případě, že metoda GetNearestColorIndex palety vrátí index mimo rozsah. Tím se převedou zdrojové barvy na nejbližší cílové barvy z hlediska intenzity hodnot. Cílový obrázek co nejlépe odpovídá zdrojovému obrázku. Můžete vidět následující výsledek:


![todo:image_alt_text](raw-data-processing_3.png)

Při použití režimu mapování surových dat je použit jiný scénář. Palety zdroje a cíle jsou jednoduše ignorovány a indexy zdroje jsou mapovány na indexy cíle. Když je nalezena hodnota, která nemůže být mapována do cílového rozsahu (při snižování počtu bitů), použije se hodnota vlastnosti RasterImage.RawFallbackIndex. Výchozí hodnota je 0 a bude mapována na první barvu ve vybrané paletě. Pokud tato hodnota leží mimo cílový rozsah, bude vyvolána příslušná výjimka. To vede k méně předvídatelným výsledkům, což může být ukázáno na následujícím obrázku:


![todo:image_alt_text](raw-data-processing_4.png)

Režim konverze palety je přesnějším řešením pro problém mapování barev, ale také trvá trochu déle, protože se musí provést výpočty k odhadnutí správného mapování palet. (Obvykle není takřka žádný výkonový rozdíl mezi oběma metodami.) Na druhou stranu režim mapování surových dat provádí trochu rychleji a může být použit pro hrubší barevnou konverzi, když přesné mapování barev není tak důležité. Například existují případy, kdy je zdrojová barevná paleta ořezána a lze ji bezpečně převést na menší počet bitů, protože dodatečné bity stejně nebyly použity.

Pro použití kteréhokoli z těchto přístupů použijte vlastnost RawDitheringMethod třídy RasterImage. Výchozí hodnota je nastavena na metodu konverze palety, aby se dosáhlo nejlepších výsledků. Tuto vlastnost lze změnit před jakýmkoli provedením konverze (například při ukládání obrázku do streamu). Všimněte si, že metody ignorování palety a konverze palety se nebudou provádět, pokud jste načetli obrázek a přepsali některá z původních dat pixelů, protože nová data jdou do mezipaměti a mezipaměť ukládá data ve formátu maximálně dostupné formy 32ARGB (ke dni 2.4.0, může se změnit). Tento formát je použit k překonání problémů s možnými odlišnými barevnými rozsahy pro načtené a uložené obrázky. Navíc metody ignorování palety a konverze palety se budou ignorovat, když je obrázek načten v režimu RGB a převeden do indexovaného režimu nebo naopak.
### **Vlastní barevné konvertory**
Někdy není dostatečné použít standardní přístup pro konverzi barev. Můžete chtít použít vlastní algoritmus pro úplnou svobodu při používání rutin konverze barev. Když jsou zdrojové a cílové obrázky pixelových formátů oba indexované RGB formáty, může být použito jednodušší rozhraní, [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter). Je třeba nastavit vlastnost [RasterImage.RawIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawindexedcolorconverter) na instanci rozhraní IIndexedColorConverter a použít vlastnost [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods). CustomConverter pro hodnotu vlastnosti RawDitheringMethod. Když je tato kombinace použita, pak jakákoli indexovaná barevná konverze prochází touto specifikovanou instancí IIndexedColorConverter. Vlastní
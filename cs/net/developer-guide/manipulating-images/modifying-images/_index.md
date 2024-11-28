---
title: Úprava obrázků
type: docs
weight: 50
url: /cs/net/uprava-obrazku/
---

## **Dithery pro rastrární obrazy**
Dithering je technika vytváření iluze nových barev a odstínů variací vzorku teček, které ve skutečnosti vytvářejí obrázek. Je to nejběžnější způsob, jak snížit barevné rozpětí obrázků na 256 (nebo méně) barev. Aspose.PSD poskytuje podporu pro dithering pro třídu [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) tím, že představuje metodu Dither, která přijímá dva parametry. První je typu DitheringMethod k použití s dvěma možnostmi - FloydSteinbergDithering a ThresholdDithering. Druhým parametrem metody [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) je BitCount typu integer. BitCount definuje velikost vzorku pro výsledek ditheringu. Výchozí hodnota je 1, která reprezentuje černobílou barvu, zatímco povolené hodnoty jsou 1, 4, 8 generující palety s 2, 4 a 256 barvami.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}
## **Nastavení jasu, kontrastu a gammy**
Nastavení barev v digitálních obrázcích je jednou z klíčových funkcí, které většina knihoven zpracování obrázků poskytuje. Úpravy barev lze kategorizovat následovně.

1. Jas se odkazuje na světlost nebo tmavost barvy. Zvýšení jasu obrázku rozjasní všechny barvy, zatímco snížení jasu ztmaví všechny barvy.
1. Kontrast se odkazuje na zvýraznění objektů nebo detailů v obrázku. Zvýšení kontrastu obrázku zvyšuje rozdíl mezi světlými a tmavými oblastmi tak, že světlé oblasti se stávají světlejšími a tmavé oblasti se stávají tmavšími. Snížení kontrastu učiní světlé a tmavé oblasti zhruba stejné, ale celkový obraz se stane více homogenní.
1. Gamma optimalizuje kontrast a jas nepřímého osvětlení, které osvětluje objekt na obrázku.
### **Nastavení jasu**
API Aspose.PSD pro .NET poskytuje metodu [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) pro třídu [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage), která může být použita k úpravě jasu obrázku předáním celočíselné hodnoty jako parametru. Nejvyšší hodnota parametru značí jasnější obrázek. Zde je původní obrázek a výsledný obrázek k porovnání.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}


### **Nastavení kontrastu**
Metoda [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) zpřístupněná třídou [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) může být použita k úpravě kontrastu obrázku předáním hodnoty float jako parametru.

Nejvyšší hodnota parametru značí vyšší kontrast v daném obrázku. Zde je původní obrázek a výsledný obrázek k porovnání.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}
### **Nastavení Gama**
Metoda [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) zpřístupněná třídou [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) má dvě verze. Jedna z přetížení přijímá jednu hodnotu float a provádí korekci Gama pro červené, modré a zelené kanály. Zatímco druhá přetížení přijímá tři hodnoty typu float reprezentující každý barevný koeficient zvlášť. Následující příklad kódu ukazuje, jak provést nastavení Gama na obrázku.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}
## **Rozmazat obrázek**
Tento článek demonstruje použití Aspose.PSD pro .NET k provádění efektu rozmazání na obrázku. API Aspose.PSD zpřístupnilo efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD pro .NET zpřístupnilo třídu [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) pro vytvoření efektu rozmazání na počkání. [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) vyžaduje rádius a sigma hodnoty pro vytvoření efektu rozmazání na obrázku. Kroky k provedení změny velikosti jsou jednoduché jak následuje:

1. Načtěte obrázek pomocí tovární metody Load zpřístupněné třídou Image.
1. Převeďte obrázek do [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Vytvořte instanci třídy [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) s výchozím konstruktorem nebo poskytněte rádius a sigma hodnoty v konstruktoru.
1. Zavolejte metodu [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter při určení obdélníku jako hranice obrázku a instance třídy [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Uložte výsledky.

Následující příklad kódu ukazuje, jak vytvořit efekt rozmazání na obrázku.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}
## **Ověřit průhlednost obrázku**
Tento článek demonstruje použití Aspose.PSD pro .NET k ověření průhlednosti obrázku. Kroky k ověření průhlednosti obrázku jsou jednoduché jak následuje:

1. Načtěte obrázek pomocí tovární metody [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) zpřístupněné třídou [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Zkontrolujte průhlednost obrázku, pokud je průhlednost nulová, obrázek je průhledný.
1. Následující příklad kódu ukazuje, jak zkontrolovat, zda je obrázek průhledný či nikoli.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}
## **Implementovat kompresor GIF s ztrátami**
Pomocí Aspose.PSD pro .NET mohou vývojáři nastavit rozdíl pixelů. Kompresování GIFu je založeno na "slovníku" řetězců pixelů. Běžný kódovač vyhledává v slovníku nejdelší řetězec pixelů, který přesně odpovídá pixelům v obrázku. Ztrátový kódovač vybere nejdelší řetězec pixelů, který je dost "dostatečně podobný" pixelům v obrázku. Níže je ukázán kód demonstrující uvedenou funkčnost.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}
## **Implementovat Bicubic Resampling**
Resampling znamená změnu pixelových rozměrů obrázku. Když převzorkujete dolů, eliminujete pixely a tím odstraňujete informace a detaily z vašeho obrázku. Když převzorkujete nahoru, přidáváte pixely. Photoshop tyto pixely přidává pomocí interpolace. Tento článek ukazuje, jak můžete provést Bicubic Resampling pomocí Aspose.PSD pro .NET.

Níže je ukázán kód demonstrující uvedenou funkčnost.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}
## **Vrstva úpravy barevové rovnováhy**
Tento článek ukazuje použití Aspose.PSD pro .NET k provedení vrstvy úpravy barevové rovnováhy na obrázku. Vrstva úpravy barevové rovnováhy vám umožňuje provádět úpravy barevnosti svých obrázků. Zobrazuje tři barevné kanály a jejich doplňkové barvy a můžete upravovat rovnováhu těchto párů ke změně vzhledu fotografie.

Níže je ukázán kód demonstrující uvedenou funkčnost.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}
## **Vrstva úpravy inverze**
Tento článek ukazuje, jak můžete provést vrstvu úpravy inverze pomocí Aspose.PSD pro .NET. Vrstva úpravy je speciální druh vrstvy používané převážně k barevným korekcím. Místo toho, aby měly vlastní obsah, upravují informace na vrstvách pod nimi. Vrstva úpravy inverze vytváří negativní efekt fotografie inverzí barev obrázku.

Níže je ukázán kód demonstrující uvedenou funkčnost.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}

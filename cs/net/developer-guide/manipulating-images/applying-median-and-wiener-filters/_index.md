---
title: Použití mediánového a Wienerova filtru
type: docs
weight: 10
url: /cs/pouziti-medianoveho-a-wienerova-filtru/
---

## **Použití mediánového a Wienerova filtru**
Mediánový filtr je nelineární digitální filtrační technika, často používaná k odstranění šumu. Takové snížení šumu je typickým předběžným krokem ke zlepšení výsledků pozdějšího zpracování. Wienerův filtr je optimálním stacionárním lineárním filtrem MSE (střední kvadratická chyba) pro obrázky znehodnocené aditivním šumem a rozmazáním. Pomocí Aspose.PSD pro .NET API mohou vývojáři aplikovat mediánový filtr k odstranění šumu z obrázku a mohou aplikovat gauss wiener filtr na obrázky. Tento článek ukazuje, jak mohou být mediánový filtr a gauss wiener filtr aplikovány na obrázky.
### **Použití Mediánového Filtru**
Aspose.PSD poskytuje třídu [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) k použití filtru na [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Následující ukázka kódu ukazuje, jak aplikovat mediánový filtr na rastrový obrázek.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Použití Gauss Wiener Filtru**
Aspose.PSD poskytuje třídu [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) k použití filtru na [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Následující ukázka kódu ukazuje, jak aplikovat gauss wiener filtr na rastrový obrázek.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Použití Gauss Wiener Filtru Pro Barevný obrázek**
Aspose.PSD poskytuje třídu [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) i pro barevné obrázky. Následující ukázka kódu ukazuje, jak aplikovat gauss wiener filtr na barevný obrázek.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Použití Motion Wiener Filtru**
Aspose.PSD poskytuje třídu [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) k použití filtru na [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). Následující ukázka kódu ukazuje, jak aplikovat motion wiener filtr na rastrový obrázek.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Aplikovat korekční filtr na obrázek**
Tento článek ukazuje použití Aspose.PSD pro .NET k provedení korekčních filtrů na obrázku. API Aspose.PSD poskytuje efektivní a snadno použitelné metody k dosažení tohoto cíle. Aspose.PSD pro .NET vystavil třídy [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) a [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) pro filtrace. Třída BilateralSmoothingFilterOptions vyžaduje celé číslo jako velikost. Kroky k provedení změn jsou jednoduché, jak je uvedeno níže:

1. Načtěte obrázek pomocí tovární metody Load vystavené třídou Image.
1. Převeďte obrázek na RasterImage.
1. Vytvořte instanci tříd BilateralSmoothingFilterOptions a SharpenFilterOptions.
1. Zavolejte metodu [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) a zároveň specifikujte obdélník jako ohraničení obrázku a instanci třídy BilateralSmoothingFilterOptions.
1. Zavolejte metodu [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) a zároveň specifikujte obdélník jako ohraničení obrázku a instanci třídy SharpenFilterOptions.
1. Upravte kontrast.
1. Nastavte jas.
1. Uložte výsledky.


## **Použijte algoritmus prahování Bradley**
Prahování obrázků se používá v grafických aplikacích. Cílem prahování obrázku je klasifikovat pixely jako „tmavé“ nebo „světlé“. API Aspose.PSD vám umožňuje použít Bradleyské prahování při převodu obrázků. Následující ukázka kódu ukazuje, jak definovat hodnotu prahu a pak spustit Bradleyský prahovací algoritmus.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}

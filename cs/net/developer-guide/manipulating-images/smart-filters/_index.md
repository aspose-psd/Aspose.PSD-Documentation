---
title: Chytrá manipulace filtru v Aspose.PSD pro C#
weight: 100
type: docs
description: Příklady, jak používat chytré filtry v souboru PSD
keywords: [chytrý filtr, přidat šum, gaussův rozmaz, zvýraznit, filtr, psd filtr, psd api, C#, csharp, ukázkový kód]
url: cs/smart-filters/
---

## Přehled

Existují tři způsoby, jak použít chytré filtry v Aspose.PSD pro C#.

### Přímé použití filtru

Tento příklad ukazuje, jak přímo použít chytré filtry v Aspose.PSD pro C#.

Nejprve určete zdrojový soubor PSD, výstupní soubor pro původní obrázek a výstupní soubor pro aktualizovaný obrázek.

Poté načtěte obrázek PSD pomocí metody `Image.Load` a přetypujte jej na objekt `PsdImage`.

Uložte původní obrázek pomocí metody `Save` se zadaným názvem výstupního souboru.

Vytvořte objekt `SharpenSmartFilter`, který představuje chytrý filtr, který se má použít.

Získejte běžnou vrstvu z obrázku PSD pomocí `psdImage.Layers[1]`.

Vložte filtr `sharpenFilter` na běžnou vrstvu třikrát v cyklu.

Nakonec uložte aktualizovaný obrázek pomocí metody `Save` se zadaným názvem výstupního souboru.

Tento kód ukazuje, jak přímo používat chytré filtry v Aspose.PSD pro C#. Použitím odpovídajících filtrů a jejich aplikací na požadované vrstvy můžete dosáhnout požadovaných efektů na svých obrázcích.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Manipulace chytrými filtry ve chytrých objektech

Tento příklad ukazuje, jak manipulovat s chytrými filtry ve chytrých objektech.

Nejprve určete zdrojový soubor PSD, výstupní soubor pro původní obrázek a výstupní soubor pro aktualizovaný obrázek.

Načtěte obrázek PSD pomocí metody `Image.Load` a přetypujte jej na objekt `PsdImage`.

Uložte původní obrázek pomocí metody `Save` se zadaným názvem výstupního souboru.

Přetypujte druhou vrstvu obrázku PSD na objekt `SmartObjectLayer`.

Upravujte chytré filtry. Tento příklad ukazuje práci s `GaussianBlurSmartFilter` a `AddNoiseSmartFilter`.

Pro `GaussianBlurSmartFilter` aktualizujte hodnoty filtru včetně poloměru, režimu blendu, neprůhlednosti a stavu povolení.

Pro `AddNoiseSmartFilter` nastavte distribuci šumu na `NoiseDistribution.UNIFORM`.

Přidejte nové položky filtru do chytré vrstvy objektu: další `GaussianBlurSmartFilter` a `AddNoiseSmartFilter`.

Aplikujte změny pomocí metody `UpdateResourceValues`.

Přímo aplikujte filtry na vrstvu a na masku vrstvy pomocí metod `Apply` a `ApplyToMask`.

Uložte aktualizovaný obrázek pomocí metody `Save` se zadaným názvem výstupního souboru.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Použití chytrých filtrů na masku vrstvy

Chytré filtry jsou mocným nástrojem pro úpravy obrázků, který uživatelům umožňuje aplikovat různé filtry a efekty. Jednou zajímavou technikou je jejich použití na masky, které umožňují přesnou kontrolu oblastí ovlivněných filtrem.

Maskou je šedá úroveň určující průhlednost určitých oblastí obrázku, selektivně aplikující filtry, úpravy nebo efekty.

Při aplikování chytrých filtrů na masky jsou filtry aplikovány pouze na oblasti určené maskou. Tato přesná kontrola umožňuje manipulaci s intenzitou a rozsahem filtru.

Pro podrobnější informace a příklady se podívejte do [dokumentace Aspose.PSD pro C#](https://docs.aspose.com/psd/net/).


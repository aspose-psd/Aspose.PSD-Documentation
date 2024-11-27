---
title: Manipulace se chytrými filtry v Aspose.PSD pro Python
weight: 100
type: docs
description: Příklady, jak používat chytré filtry v souboru PSD
keywords: [chytrý filtr, přidat šum, Gaussův rozostřený, zaostřit, filtr, PSD filtr, PSD API, python, ukázkový kód]
url: /cs/python-net/smart-filtrovani/
---

## **Přehled**

Existují 3 způsoby, jak použít chytré filtry v Aspose.PSD pro Python.

## **Přímé Použití Filtru**

V tomto ukázkovém kódu můžeme vidět příklad, jak přímo použít chytré filtry v Aspose.PSD pro Python.

Nejprve kód určuje zdrojový soubor PSD, výstupní soubor pro původní obrázek a výstupní soubor pro aktualizovaný obrázek.

Poté kód načte obrázek PSD pomocí metody Image.load() a přetypuje ho na objekt PsdImage.

Původní obrázek je pak uložen pomocí metody save() s určeným názvem výstupního souboru.

Je vytvořen objekt SharpenSmartFilter, který představuje chytrý filtr, který se bude aplikovat.

Následně kód získá běžnou vrstvu z obrázku PSD pomocí im.layers[1].

Následně se pomocí smyčky třikrát aplikuje štípání na běžnou vrstvu.

Nakonec je aktualizovaný obrázek uložen pomocí metody save() a určený název výstupního souboru.

Tento kód ukazuje, jak přímo použít chytré filtry v Aspose.PSD pro Python. Použitím odpovídajících filtrů a jejich aplikací na požadované vrstvy lze dosáhnout požadovaných efektů na obrázcích.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentace-Python-Aspose-psd-smart-filtr-priamo-aplikace.py" >}}

## **Manipulace se Chytrými Filtry v Chytrých Objektech**

Nejprve kód určuje zdrojový soubor PSD, výstupní soubor pro původní obrázek a výstupní soubor pro aktualizovaný obrázek.

Obrázek PSD je načten pomocí metody Image.load() a pak přetypován na objekt PsdImage.

Původní obrázek je uložen pomocí metody save() s určeným názvem výstupního souboru.

Kód pak přetypuje druhou vrstvu obrázku PSD na objekt SmartObjectLayer, který představuje vrstvu chytrého objektu.

Poté kód pokračuje v úpravě chytrých filtrů. V tomto příkladu ukazuje, jak pracovat se dvěma typy chytrých filtrů: GaussianBlurSmartFilter a AddNoiseSmartFilter.

Pro GaussianBlurSmartFilter kód aktualizuje hodnoty filtru, včetně poloměru, režimu míchání, průhlednosti a toho, zda je povolen nebo ne.

Pro AddNoiseSmartFilter kód nastaví distribuci šumu na NoiseDistribution.UNIFORM.

Následně kód přidá do chytré objektové vrstvy dva nové položky filtrů: další GaussianBlurSmartFilter a AddNoiseSmartFilter.

Po přidání nových filtrů kód aplikuje změny pomocí metody update_resource_values().

Nakonec kód ukazuje, jak přímo aplikovat filtry na vrstvu a na masku vrstvy pomocí metod apply() a apply_to_mask().

Aktualizovaný obraz je pak uložen pomocí metody save() a určený název výstupního souboru.

Postupováním podle tohoto ukázkového kódu se můžete naučit, jak pracovat s chytrými filtry v Aspose.PSD pro Python. Knihovna poskytuje širokou škálu chytrých filtrů, každý s vlastním souborem vlastností a metod, které lze upravit k dosažení požadovaných efektů na vašich obrázcích.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentace-Python-Aspose-psd-chytre-filtry-funkce.py" >}}

## **Aplikace Chytrých Filtrů na Masku Vrstvy**

Aplikace Chytrých Filtrů na Masky: Silná Technika Úpravy Obrázků

Chytré filtry jsou populární funkcí v softwaru pro úpravu obrázků, která uživatelům umožňuje aplikovat různé filtry a efekty na své obrázky. Jedna zajímavá technika, kterou lze pomocí chytrých filtrů dosáhnout, je jejich aplikace na masky. V tomto článku prozkoumáme, jak aplikovat chytré filtry na masky a diskutujeme o jejich použití ve světě úprav obrázků.

Co je Maska? Předtím, než se ponoříme do aplikace chytrých filtrů na masky, pojďme nejprve porozumět tomu, co je maska. V úpravě obrázků je maska šedotónový obrázek, který určuje průhlednost určitých částí obrázku. Maska může být použita k selektivní aplikaci filtrů, úprav nebo efektů na konkrétní části obrázku, zatímco je zanecháno jiné oblasti nezměněno.

Aplikace Chytrých Filtrů na Masky: Při aplikaci chytrých filtrů na masky jsou filtry aplikovány pouze na oblasti určené maskou. To umožňuje přesnou kontrolu nad tím, na které části obrázku je filtr aplikován. Manipulací s maskou můžete určit intenzitu a rozsah účinku filtru.

Zkontrolujte prosím předchozí příklad a metodu: [API Reference Aplikace Chytrých Filtrů na Masku](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

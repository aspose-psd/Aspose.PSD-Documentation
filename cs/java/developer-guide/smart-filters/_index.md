---
title: Manipulace chytrými filtry v Aspose.PSD pro Javu
weight: 100
type: docs
description: Příklady, jak používat chytré filtry v souboru PSD
keywords: [chytrý filtr, přidat šum, gaussův rozmazání, zaostřit, filtr, psd filtr, psd API, java, ukázkový kód]
url: cs/java/smart-filters/
---

## **Přehled**

V Aspose.PSD pro Javu jsou 3 metody pro aplikaci chytrých filtrů.

## **Aplikace filtru přímo**

Tento ukázkový kód ukazuje, jak přímo aplikovat chytré filtry v Aspose.PSD pro Javu.

Nejprve kód definuje zdrojový soubor PSD, výstupní soubor pro původní obraz a výstupní soubor pro aktualizovaný obraz.

Poté kód načte obraz PSD pomocí metody Image.load() a převede ho na objekt PsdImage.

Původní obraz je uložen pomocí metody save(), kde je specifikováno jméno výstupního souboru.

Je vytvořen objekt SharpenSmartFilter pro reprezentaci požadovaného chytrého filtru.

Poté kód získá běžnou vrstvu z obrazu PSD pomocí psdImage.getLayers()[1].

Pomocí smyčky je filtr sharpenFilter použit na běžnou vrstvu třikrát.

Aktualizovaný obrázek je nakonec uložen pomocí metody save() s poskytnutým jménem výstupního souboru.

Tento kód ilustruje přímou aplikaci chytrých filtrů v Aspose.PSD pro Javu. Použitím vhodných objektů filtrů a aplikací na požadované vrstvy lze dosáhnout požadovaných efektů na obrázcích.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentace-Java-Aspose-psd-chytrý-filtr-přímá-aplikace.java" >}}

## **Manipulace s chytrými filtry ve chytrých objektech**

Tento kódový úryvek popisuje, jak manipulovat s chytrými filtry ve chytrých objektech v Aspose.PSD pro Javu.

Nejprve kód definuje zdrojový soubor PSD, výstupní soubor pro původní obraz a výstupní soubor pro aktualizovaný obraz.

Obraz PSD je načten pomocí metody Image.load() a poté převeden na objekt PsdImage.

Původní obraz je uložen pomocí metody save(), kde je specifikováno jméno výstupního souboru.

Kód poté převede druhou vrstvu obrazu PSD na objekt SmartObjectLayer, který reprezentuje vrstvu chytrých objektů.

Následně kód demonstruje úpravy chytrých filtrů a předvádí dva typy: GaussianBlurSmartFilter a AddNoiseSmartFilter.

Pro GaussianBlurSmartFilter kód aktualizuje hodnoty filtru jako je poloměr, režim smíchání, průhlednost a stav aktivace.

Pro AddNoiseSmartFilter kód nastavuje distribuci šumu na NoiseDistribution.Uniform.

Následně kód přidá dvě nové položky filtrů do vrstvy chytrých objektů: další GaussianBlurSmartFilter a AddNoiseSmartFilter.

Po přidání nových filtrů kód aplikuje změny pomocí metody updateResourceValues().

Nakonec kód přímo aplikuje filtry na vrstvu a její masku pomocí metod apply() a applyToMask() zvlášť.

Aktualizovaný obrázek je poté uložen pomocí metody save() s poskytnutým jménem výstupního souboru.

Postupováním podle tohoto ukázkového kódu můžete porozumět, jak manipulovat s chytrými filtry ve chytrých objektech v Aspose.PSD pro Javu. Knihovna nabízí širokou škálu chytrých filtrů, každý s vlastním souborem vlastností a metod, které lze upravit k dosažení požadovaných efektů na obrázcích.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentace-Java-Aspose-psd-chytrý-filtr-vlastnosti.java" >}}

## **Aplikace chytrých filtrů na masku vrstvy**

Aplikace chytrých filtrů na masky: Silná technika úpravy obrázku

Chytré filtry, běžné v grafickém softwaru, umožňují uživatelům aplikovat různé filtry a efekty na jejich obrázky. Jednou zajímavou technikou umožněnou chytrými filtry je jejich aplikace na masky. Tento článek zkoumá aplikaci chytrých filtrů na masky a diskutuje o jejich použitelnosti v oblasti úprav obrázků.

Porozumění maskám: Předtím než se ponoříme do aplikace chytrých filtrů na masky, je důležité porozumět konceptu masky. V grafickém úpravě je maska šedotónový obraz, který diktuje průhlednost konkrétních oblastí v rámci obrázku. Masky umožňují selektivní aplikaci filtrů, úprav nebo efektů na konkrétní části obrázku, zatímco zbylé části zůstanou nedotčeny.

Aplikace chytrých filtrů na masky: Když jsou chytré filtry aplikovány na masky, ovlivňují pouze oblasti specifikované maskou, nabízející precizní kontrolu nad dopadem filtru. Manipulací s maskou mohou uživatelé modulovat intenzitu a rozsah efektu filtru.

Prosím odkazujte se na předchozí příklad a metodu: [API Reference Applying Smart Filter To Mask](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

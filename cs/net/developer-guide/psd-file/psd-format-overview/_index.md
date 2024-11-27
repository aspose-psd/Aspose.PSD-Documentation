---
title: Přehled formátu PSD
type: docs
weight: 60
url: /cs/psd-formatovy-prehled/
---

## **Popis**
PSD, Photoshop Document, představuje nativní formát souboru programu Adobe Photoshop používaný pro grafický design a vývoj.

## **Specifikace formátu souboru**
Data v souboru PSD jsou uložena v pořadí bajtů typu big-endian. To znamená, že je třeba prohazovat krátké a dlouhé celé čísla při čtení nebo zápisu na platformě Windows. Formát souboru Photoshop je rozdělen do pěti hlavních částí. Obsahuje mnoho značek délky, které mohou být použity k přechodu z jedné sekce do druhé. Značky délky jsou obvykle doplněny bajty, aby se zaokrouhlily na nejbližší interval o velikosti 2 nebo 4 bajty. Pět hlavních částí jsou:

- Hlavička souboru
- Data barvy módu
- Obrazové zdroje
- Informace o vrstvách a maskách
- Obrazová data

Pro shodu by měla být data zapsána do všech těchto polí v sekci, protože Photoshop může zkusit přečíst celou sekci. To také znamená, že se do vynechaných polí, která se zapisují do souboru, musí zapsat nuly. Pole délky v sekci s délkou ohraničenou značkami by mělo být použito k určení, kdy skončit s čtením. Většinou udává pole délky počet bajtů, ne záznamů, následujících. Při čtení souboru je třeba pamatovat na následující body:

- Hodnoty ve sloupci "Délka" ve všech tabulkách jsou v bajtech.
- Všechny hodnoty definované jako Unicode řetězec jsou složeny z:
- 4bajtového pole délky, představujícího počet znaků ve řetězci (nikoli bajtů).
- Řetězce hodnot Unicode, dva bajty na znak.

## **Funkce formátu**
Soubory PSD mohou obsahovat vrstvy obrázků, vrstvy úprav, masky vrstev, poznámky, informace o souboru, klíčová slova a další prvky specifické pro Photoshop. Soubory Photoshop mají výchozí příponu .PSD a mají maximální výšku a šířku 30 000 pixelů a délkový limit dvou gigabajtů.

## **Jak se může formát použít**
1. Nástroj pro řezání PSD.
1. [Převod PSD](/psd/cs/net/konvertovani-psd-obrazu-na-rastrovy-format/) na HTML
1. Použití [PSD jako šablony](/psd/cs/net/pouziti-psd-souboru-jako-sablon-pro-automatizaci-navrhovani-vizitek/) pro e-maily
1. PSD na konkrétní CMS HTML
1. Identifikační fotografie v souboru PSD (Policejní portrét)
1. Vytvoření pseudo-3D náhledových obrázků pomocí chytrých objektů pro výrobky jako jsou lahve, šálky, trička atd.
1. Rychlá úprava PSD: Automatický tón, Předvolby, Chytrý objekt, Výřez obrázku textové vrstvy

A mnoho dalšího. Pokud jste něco skvělého vytvořili s Aspose.PSD, sdílejte s námi svůj příběh pomocí [Aspose Fór](https://forum.aspose.com/).

Další příklady můžete získat zde:

- [Příběhy z praxe](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Ukázky](/psd/cs/net/ukazky-html/)

---
title: Nastavení vrstvy vyvážení barev
type: docs
weight: 30
url: /cs/java/layer-types/adjustment-layer/color-balance/
---

# Práce s vrstvou vyvážení barev v Photoshopu v Javě

V tomto článku se zaměříme na **nastavení vyvážení barev obrazu** ve formátu souboru PSD v Javě. Budeme používat speciální knihovnu zvanou Aspose.PSD pro Javu, která je nástrojem pro manipulaci s dokumenty Photoshopu.

Jelikož knihovna pracuje se souborem PSD, obsahuje téměř [všechny funkce](https://docs.aspose.com/psd/java/features/) dostupné v editoru Photoshopu, a **vrstva úpravy vyvážení barev** není výjimkou.

Vrstva úpravy vyvážení barev umožňuje změnu vyvážení mezi primárními (RGB) a subtraktivními (CMY) barvami pro stíny, polotóny a světla způsobem rychlým a jednoduchým.

## Úprava vyvážení barev

Jak bylo zmíněno dříve, vrstva úpravy vyvážení barev v Aspose.PSD pro Javu je přesně to, co je **nastavovačem mezi primárními a subtraktivními barvami**. To znamená, že existují tři stupnice pro každý pár barev (cyan/červená, magenta/zelená, žlutá/modrá). Intenzita konkrétní barvy v páru se zvýší, pokud se hodnota posune směrem k ní a naopak. Navíc tyto tři páry jsou přirozené pro každou oblast tónového rozsahu (stíny, polotóny a světla), což zvyšuje flexibilitu tohoto druhu úpravy.

Takže se pojďme těchto znalostí prakticky použít. Pro příklad si vybereme fotografii obličeje ženy s červeným nádechem (b). Obličej je tak červený a my se pokusíme to napravit **přidáním vrstvy úpravy vyvážení barev**, abychom snížili červenou a zvýšili cyankou základně (a), abychom získali obličej, který vypadá přirozeněji (c). Opět, na této fotografii je spousta práce, ale v rámci tohoto článku se omezíme na toto.

![Příklad vrstvy úpravy vyvážení barev](color-balance-adjustment-layer-example-figure-1.png) API vrstvy úpravy vyvážení barev má plochý design. Proto třída [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) je vše, co potřebujete. Nejprve, zachovejte světlost, protože je implicitně deaktivována. Poté přidejte trochu zelené a více žluté pro stíny pomocí odpovídajících metod (jejichž názvy se skládají z konkrétní oblasti tónového rozsahu a názvů barev v páru), poté přidejte více cyanku a trochu modré do polotónů a nakonec přidejte více cyanku a kousek magenty a modré:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Nyní máme obrázek, který jsme chtěli! Je to tak jednoduché, že ne?

Dejte si pozor, že _hodnota každého páru barev musí být v rozsahu od -100 do 100,_ což jsou záporné hodnoty pro subtraktivní barvy a kladné pro primární barvy, stejně jako v editoru Photoshopu.

Podívejte se na naši API referenci, abyste získali další technické detaily o [vrstvě úpravy vyvážení barev](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Závěr

V tomto článku jsme zvažovali, jak programově nastavit vyvážení barev obrazu v Javě pomocí knihovny Aspose.PSD pro Javu. Knihovna obsahuje plně vybavené API pro práci s vrstvami úpravy vyvážení barev v dokumentech Photoshopu.

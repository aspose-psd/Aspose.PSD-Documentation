---
title: Úprava vrstvy filtrace fotografií
type: docs
weight: 30
url: /cs/java/typy-vrstev/adjustment-vrstva/photo-filter/
---

# Práce s úpravou vrstvy filtrace fotografií v Javě

Dnes uvidíme, jak aplikovat vrstvu úpravy filtrace fotografií na existující dokument Photoshopu pomocí aplikace Aspose.PSD pro Javu, což je knihovna pro manipulaci se soubory PSD.

**API vrstvy úpravy filtrace fotografií** mění barevnou rovnováhu obrázku pomocí zatírání. Výsledný obrázek bude vypadat stejně jako po použití skutečného filtru fotoaparátu. Všimněte si, že API vrstvy úpravy filtrace fotografií této knihovny se mírně liší od Photoshopu, protože zatím nejsou předdefinované filtry. Nicméně je stejné ve všech ostatních ohledech. To znamená, že můžete nastavit barvu zatírání, změnit její intenzitu (hustotu) a také použít volbu Uchovávat světlost.

## Přehled API

API vrstvy úpravy filtrace fotografií je poměrně jednoduché na použití. Existuje hlavní třída [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), která slouží jako vstupní bod do této vrstvy úpravy a obsahuje pouze tři veřejné vlastnosti, a to barvu, hustotu a uchování světlosti, pomocí kterých dochází k úpravě.

## Nastavení barvy

Jelikož není o čem moc mluvit, pojďme se **ihned podívat na příklad nastavení barevné rovnováhy** pomocí vrstvy úpravy filtrace fotografií. Přidáme ručně ohřívací filtr (a) do obrázku sochy jelena (b), abychom získali obrázek v teplých tónech (c), které jsou příjemnější na pohled.

![Příklad úpravy vrstvy filtrace fotografií](photo-filter-adjustment-layer-figure-1.png)

Nejprve si všimněte, že [tovární metoda](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) se liší od těch pro [ostatní úpravné vrstvy](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers), protože zde není výchozí metoda (bez argumentů). Proto k přidání vrstvy úpravy filtrace fotografií do načteného dokumentu Photoshopu je vyžadován pouze jeden argument, kterým je barva. Takže pro znovuvytvoření efektu ohřívacího filtru jednoduše předejte oranžovou barvu jako argument tovární metody a poté nastavte hustotu pomocí odpovídajících setterů:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Stojí za to dodat, že vlastnost Hustota má výchozí hodnotu 100 a pravda je výchozí hodnotou vlastnosti Uchovávat světlost (to je důvod, proč tuto možnost nezapínáme explicitně).

## Závěr

V tomto článku jsme zvážili použití API vrstvy úpravy filtrace fotografií knihovny Aspose.PSD pro Javu. Tato pomůcka je snadno použitelná a umožňuje přidat záteň obrázku s proměnlivou hustotou. Jedná se o rychlý způsob úpravy barevné rovnováhy celého obrázku.

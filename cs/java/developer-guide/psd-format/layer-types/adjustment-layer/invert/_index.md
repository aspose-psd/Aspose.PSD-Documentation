---
title: Nastavení vrstvy invertovaného úpravy
type: docs
weight: 30
url: /cs/java/layer-types/adjustment-layer/invert/
---

# Práce s vrstvou invertované úpravy Photoshopu v Javě

V tomto článku vám ukážeme, jak obrátit obrázek v dokumentu Photoshopu na negativní programově v Javě. K tomuto účelu použijeme knihovnu pro manipulaci s formátem souborů PSD nazvanou Aspose.PSD pro Javu.

API pro inverzi barev umožňuje **přidání negativního efektu k obrázku**. Možná už jste viděli, jak [invertovat barvy obrázku pomocí vrstvy úprav Curves](/psd/cs/java/layer-types/adjustment-layer/curves/). Nicméně dnes se podíváme na rychlejší a jednodušší způsob provedení úkolu pomocí vrstvy úprav Invert.

## Přehled API

**API vrstvy invertované úpravy** se skládá z třídy vrstvy samotné, která je [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Tato třída nemá vlastní veřejné členy, protože zdědí všechny veřejné členy z rodičovské třídy ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). Tento fakt zjednodušuje jeho použití, protože jediné, co musíte udělat, je přidat ho do souboru PSD a obrázek se stane negativním.

## Invertovat barvy obrázku

Takže i když se to zdá zřejmé, ukážeme pro jasnost, jak **aplikovat vrstvu invertované úpravy** na obrázek astronauta (a), aby se pro tento obrázek vytvořil negativní efekt (b).

![Příklad obrázku vrstvy invertované úpravy před a po](invert-adjustment-layer-figure-1.png)

Pro **invertování barev obrázku** stačí přidat invertovanou vrstvu úpravy do PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

To je vše! Pro tento typ vrstvy úprav nejsou žádné specifické vlastnosti k nastavení.

## Závěr

V tomto článku jsme se dozvěděli o API vrstvy invertované úpravy v Aspose.PSD pro Javu. Je to snadný nástroj pro získání negativních obrázků, protože API této vrstvy úprav nezahrnuje žádné veřejné členy.

---
title: Použití vrstvy úprav pro zlepšení PSD
weight: 100
type: docs
description: Příklady použití vrstev úprav pomocí Aspose.PSD pro C#
keywords: [vrstva úprav, zvýraznění fotografií, úprava křivek, zlepšení úrovní, invertování, fotografický filtr, PSD API, C#, csharp, ukázkový kód]
url: cs/net/vrstva-uprav-zlepseni/
---

## Přehled

V tomto článku prozkoumáme úpravy vrstev úprav v Aspose.PSD pro C#. Vrstvy úprav jsou mocnou funkcí úpravy obrázků, které vám umožňují provádět nedestruktivní změny na vašich obrázcích. Aspose.PSD poskytuje kompletní sadu tříd vrstev úprav, které můžete použít k modifikaci různých aspektů vašich obrázků.

Pro demonstrování úprav vrstev úprav použijeme ukázkový kód na konci stránky, který načte obrázek PSD a aplikuje různé úpravy na jeho vrstvy.

V kódu níže začínáme načtením obrázku PSD pomocí metody `PsdImage.Load()`. Poté nastavíme možnosti pro uložení výstupního PNG souboru. Třída `PngOptions` nám umožňuje specifikovat typ barvy pro výstupní obrázek.

Následně projdeme každou vrstvu v obrázku PSD a zkontrolujeme její typ pomocí metody `IsAssignable()`. Pokud je vrstva konkrétního typu, přetypujeme ji na tento typ pomocí metody `Cast()` a aplikujeme požadovanou úpravu. Například upravujeme jas a kontrast vrstvy `BrightnessContrastLayer`, měníme úrovně vrstvy `LevelsLayer`, přidáváme bod křivky vrstvě `CurvesLayer`, a tak dále.

Můžete přidat další kód k aplikaci dalších úprav na příslušné vrstvy. Aspose.PSD poskytuje širokou škálu tříd vrstev úprav, jako jsou [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) a další.

Nakonec uložíme upravený obrázek pomocí metody `Save()` třídy `PsdImage`.

Tento kód poskytuje základní přehled o tom, jak upravovat vrstvy úprav v Aspose.PSD pro C#. Můžete přizpůsobit úpravy podle vašich požadavků a objevovat různé dostupné možnosti v dokumentaci API.

## Příklad

Zde je ukázkový kód, který demonstruje použití vrstev úprav pomocí Aspose.PSD pro C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Pro více podrobností a příkladů navštivte [Aspose.PSD pro C# dokumentaci](https://docs.aspose.com/psd/net/).


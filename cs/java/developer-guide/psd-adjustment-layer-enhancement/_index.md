---
title: Využití vrstvy úprav ke zdokonalení PSD
weight: 100
type: docs
description: Příklady využití vrstvy úprav prostřednictvím Aspose.PSD pro Java
keywords: [vrstva úprav, zlepšení fotografií, úprava křivek, zdokonalení úrovní, invertování, fotografický filtr,  psd api, java, ukázkový kód]
url: cs/java/adjustment-layer-enhancement/
---

## **Přehled**

Tento článek zkoumá úpravy vrstev úprav v Aspose.PSD pro Java. Vrstvy úprav jsou výkonnou funkcí úpravy obrázků, která vám umožňuje provést nedestruktivní změny na vašich obrázcích. Aspose.PSD poskytuje komplexní soubor tříd vrstv úprav, které můžete použít k úpravě různých aspektů vašich obrázků.

Pro demonstraci úprav vrstev úprav poskytneme ukázkový úryvek kódu na konci stránky, který načte obrázek PSD a aplikuje různé úpravy na jeho vrstvy.

V následujícím úryvku kódu začínáme načtením obrázku PSD pomocí metody PsdImage.load(). Poté nastavíme možnosti pro uložení výstupního souboru PNG. Třída PngOptions nám umožňuje specifikovat typ barvy pro výstupní obrázek.

Následně iterujeme přes každou vrstvu v obrázku PSD a zkontrolujeme její typ pomocí metody isAssignable(). Pokud je vrstva určitého typu, přetypujeme ji na tento typ pomocí metody cast() a aplikujeme požadovanou úpravu. Například upravujeme jas a kontrast pomocí vrstvy BrightnessContrastLayer, upravujeme úrovně vrstvy LevelsLayer, přidáváme bod do křivek pomocí CurvesLayer a tak dále.

Můžete přidat další kód k aplikaci dalších úprav na příslušné vrstvy. Aspose.PSD poskytuje širokou škálu tříd vrstev úprav, jako jsou [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer) [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) a další.

Nakonec uložíme upravený obrázek pomocí metody save() třídy PsdImage.

Tímto poskytujeme základní přehled o úpravě vrstev úprav v Aspose.PSD pro Java. Můžete upravit úpravy podle svých požadavků a prozkoumat různé možnosti dostupné v dokumentaci API.

Prosím, zkontrolujte úplný příklad níže.

## **Příklad**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}

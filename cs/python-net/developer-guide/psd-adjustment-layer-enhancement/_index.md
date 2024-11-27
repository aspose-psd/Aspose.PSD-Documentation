---
title: Použití vrstvy úprav k vylepšení souboru PSD
weight: 100
type: docs
description: Příklady použití vrstvy úprav pomocí Aspose.PSD pro Python
keywords: [vrstva úprav, vylepšení fotky, úprava křivek, zvýraznění úrovní, inverze, foto filtr,  api souboru PSD, python, ukázkový kód]
url: cs/python-net/vrstva-uprav-vylepseni/
---

## **Přehled**

V tomto článku se budeme zabývat úpravou vrstev úprav v Aspose.PSD pro Python. Vrstvy úprav jsou mocným prvkem v úpravách obrázků, který vám umožňuje provádět nedestruktivní změny na vašich obrázcích. Aspose.PSD poskytuje komplexní sadu tříd vrstev úprav, které můžete použít k úpravě různých aspektů vašich obrázků.

Pro demonstraci úpravy vrstev úprav použijeme ukázkový kód na konci stránky, kter načte obrázek PSD a aplikuje různé úpravy na jeho vrstvy.

V následujícím kódu nejprve načteme obrázek PSD pomocí metody PsdImage.load(). Potom nastavíme možnosti pro uložení výstupních souborů PNG. Třída PngOptions nám umožňuje specifikovat typ barvy pro výstupní obrázek.

Dále projdeme každou vrstvu v obrázku PSD a zkontrolujeme její typ pomocí metody is_assignable(). Pokud je vrstva určitého typu, přetypujeme ji na tento typ pomocí metody cast() a aplikujeme požadovanou úpravu. Například upravíme jas a kontrast vrstvy BrightnessContrastLayer, upravíme úrovně vrstvy LevelsLayer, přidáme křivkový bod vrstvě CurvesLayer a tak dále.

Můžete přidat další kód k aplikaci dalších úprav na jejich příslušné vrstvy. Aspose.PSD poskytuje širokou škálu tříd vrstev úprav, jako jsou [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) a další.

Nakonec uložíme upravený obrázek pomocí metody save() třídy PsdImage.

Tento kód poskytuje základní přehled o tom, jak upravovat vrstvy úprav v Aspose.PSD pro Python. Můžete upravit úpravy podle svých požadavků a prozkoumat různé možnosti dostupné v dokumentaci API.

Zkontrolujte úplný příklad.

## **Příklad**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}

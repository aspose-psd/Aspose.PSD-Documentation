---
title: Vrstva úpravy jasu a kontrastu
type: docs
weight: 30
url: /cs/java/vrstva-typu/vrstva-upravy-jasu-kontrast/
---

# Práce s vrstvou úpravy jasu a kontrastu v Photoshopu

V tomto článku použijeme vrstvu úpravy jasu a kontrastu v dokumentu Adobe® Photoshop® pomocí knihovny Aspose.PSD pro jazyk Java®. Dále se naučíme více o funkcích knihovny souvisejících s tímto typem vrstvy úpravy.

Ale nejprve trochu teorie.

Vrstva úpravy jasu a kontrastu mění jas a kontrast obrázku. Počkejte, co to vlastně znamená? Zvýšení jasu zesvětlí barevnou hodnotu až k bílé a snížení jasu ztmaví barvu až k černé. Zvýšení kontrastu zase zvýší rozdíl mezi světlými a tmavými barvami a snížení kontrastu tento rozdíl naopak zmenší; to znamená, že světlé barvy získávají světlejší odstíny a tmavé barvy získávají tmavší odstíny.

## Podpora barevného režimu

Knihovna umožňuje přidat vrstvu úpravy jasu a kontrastu do obrázků v režimu RGB, CMYK nebo Lab.

## Současné a dřívější chování

Současná implementace knihovny (verze 20.6 v době psaní) používá výchozí algoritmus Photoshopu, který zachovává celý tónový rozsah od stínů po světla, ale zatím nepodporuje dřívější chování. To znamená, že knihovna podporuje vrstvu úpravy jasu a kontrastu v dokumentech vytvořených v nejnovějších verzích Photoshopu (CS4 a novější). Nicméně můžete [požadovat dřívější implementaci vrstvy úpravy jasu a kontrastu](https://forum.aspose.com/c/psd) na našem fóru, pokud ji potřebujete.

## Úprava jasu a kontrastu

Nyní popíšeme, jak pracuje high-level API vrstvy úpravy jasu a kontrastu (až příliš dopředu, API je strukturované). Třída PsdImage obsahuje tovární metodu (addBrightnessContrastAdjustmentLayer) pro vytváření instance třídy BrightnessContrastLayer, která je bránou pro úpravu jasu a kontrastu. Třída BrightnessContrastLayer obsahuje pouze pár metod pro získání a nastavení vlastností jasu a kontrastu a pro změnu jejich hodnot.

![|Příklad vrstvy úpravy jasu a kontrastu v PSD](brightness-contrast-psd-upravova-vrstva-figurka-1.png)

Takže vezměme obrázek psa (b) jako příklad, abychom upravili jeho jas1 a kontrast2 (a), pouze pomocí tovární metody s odpovídajícími argumenty, abychom nakonec dostali obrázek (c), který vypadá živěji:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Poznámky:

1. Hodnota jasu musí být v rozsahu od -150 do 150.
2. Hodnota kontrastu musí být v rozsahu od -50 do 100.

Podívejte se na dokumentaci k [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) pro více podrobností.

## Závěr

V tomto článku jsme získali rychlý přehled o vrstvě úpravy jasu a kontrastu a naučili jsme se, jak upravit jas a kontrast obrázku pomocí tovární metody.

Podívejte se na naši sérii článků o [API pro vrstvy úprav](/cs/java/vrstva-typu/vrstva-upravy-jasu-kontrast/) v Aspose.PSD pro Javu, abyste se dozvěděli víc.

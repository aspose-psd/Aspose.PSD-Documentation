---
title: Křivková vrstva úprav
type: docs
weight: 30
url: /cs/java/typ-vrstvy/vrstva-uprav/kruvky/
---

# Práce s křivkami úprav Photoshop Curves v Javě

Cílem tohoto článku je demonstrovat schopnosti knihovny Aspose.PSD pro Javu při **práci s křivkovými vrstvami úprav** v dokumentech Adobe® Photoshop®. Knihovna je plně autonomní, takže funguje bez instalace editoru fotografií Photoshop. [Plný seznam funkcí](https://docs.aspose.com/psd/java/features/) lze najít v naší znalostní bázi. No a teď zpět k křivkám.

## Přehled API

Nástroj Křivky lze zobrazit jako diagonální čáru (křivku) na grafu s odlesky v pravém horním rohu a stíny v pravém dolním rohu.

Knihovna poskytuje API pro práci s křivkou, konkrétně s třídou [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Tato třída však má **dvě zcela odlišné přístupy** k práci s křivkou. Proto je možné ji upravit vždy pouze v jednom z následujících režimů:

- Spojitý (křivka je zobrazena jako cesta s body v místech ohybu)
- Diskrétní (křivka je zobrazena jako tečkovaná čára)

Knihovna tedy umožňuje upravit křivku pomocí [spojitého](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) a [diskrétního manažera](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) specifikovaném režimu. Níže vysvětlíme, jak použít každou z nich na konkrétním příkladu.

## Úprava barev a tónů pomocí Spojitého manažera křivek

[Manažer Spojitých křivek](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **nastavuje body ohybu spojité křivky** pro složitý kanál (RGB) a také pro každý jednotlivý barevný kanál. K demonstračním účelům budou na ztemnělý obrázek orchestru (a) aplikovány některé úpravy křivek, aby výsledkem byl zesvětlený obrázek s teplejšími barvami (c):

![Obrázek 1 vrstvy úprav křivek](curves-psd-adjustment-layer-figure-1.png)

Protože jsou k dispozici dva manažeři, je nezbytné explicitně vybrat jeden (v tomto případě spojitý manažer), předtím než ho získáme. Poté můžeme přímo přidat body křivky na určitých souřadnicích pro požadované barevné kanály (složité RGB, červené a modré):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

Počátek souřadnic je v levém dolním rohu. Maximální hodnota souřadnice bodu je omezena datovým typem (byte) a je rovna 255 (127 pro znaménkový typ).

Existuje také pár [dalších metod](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager), které můžete použít.

## Úprava tónů pomocí Diskrétního manažera křivek

Diskrétní manažer křivek také umožňuje umístit body křivky (vlastně změnit barvu a tón), ale rozdíl je v tom, jak to dělá. Za prvé, **křivka se skládá z bodů** nebo teček (ne z jedné continues linie). Za druhé, tento manažer **umisťuje body na graf jiným způsobem**. Místo toho **posunuje bod nahoru nebo dolů** s rozsahem hodnot mezi 255 a 0. Výchozí hodnoty bodů křivky postupně rostou od 255 dolů a tvoří křivku, která je pod úhlem 45 stupňů.

S tímto na paměti je snadné vytvořit Photoshop preset „Negativní (RBG)“ a aplikovat ho na obrázek údolí v odstínech šedi, abychom získali nakonec negativní zobrazení údolí:

![Obrázek 2 vrstvy úprav křivek](curves-psd-adjustment-layer-figure-2.png) Nejprve si nezapomeňte vybrat odpovídající manažera, abyste ho mohli použít, a poté nastavit hodnoty bodů křivky ve sestupném pořadí od 255 dolů na 0 pro každý bod křivky (celkem 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Manažer také poskytuje několik [dalších metod](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) pro správu křivky.

## Závěr

V tomto článku jsme se naučili, jak pracovat s křivkovými vrstvami úprav v dokumentech Photoshopu s použitím knihovny Aspose.PSD pro Javu ve dvou zcela odlišných způsobech (spojitý a diskrétní manažeři).

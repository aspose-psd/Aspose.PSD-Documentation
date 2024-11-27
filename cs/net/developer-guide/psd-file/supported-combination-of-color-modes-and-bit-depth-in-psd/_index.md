---
title: Podporovaná kombinace barvových režimů a hloubky bitů v PSD
type: docs
weight: 80
url: /cs/podporovana-kombinace-barvovych-rezimu-a-hloubky-bitu-v-psd/
---

## **Popis**
Aspose.PSD podporuje otevírání souborů PSD s libovolnou kombinací barvového režimu a hloubky bitů v souborech Adobe Photoshop PSD. Můžete otevírat tyto soubory a používat nízkoúrovňové API k úpravě obsahu souboru. Ale pro některé méně populární kombinace mohou nastat konkrétní problémy, některé z nich souvisejí s omezeními barvových režimů.

## **Podporovaná exportní kombinace barvových režimů a hloubky bitů v PSD v režimu pouze pro čtení**

| |Bitmap|Odstíny šedi|Indexované|RGB|CMYK|Vícekanálové|Duotónové|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Hloubka 1|Ano[](https://issue.kharkov.dynabic.com/issues/PSDNET-283)|-|-|-|-|-|-|-|
|Hloubka 8|-|Ano|Ano|Ano|Ano|Ne Q3-Q4|Ne Q3-Q4|Ano[](https://issue.kharkov.dynabic.com/issues/PSDNET-290)|
|Hloubka 16|-|Ano|-|Ano|Ano|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-287)|-|Ne (Q3-Q4)|
|Hloubka 32|-|Ano*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125)|-|Ano*|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-285)|-[](https://issue.kharkov.dynabic.com/issues/PSDNET-288)|-|-|
\* Menší problémy v některých případech

## **Podporovaná exportní kombinace barvových režimů a hloubky bitů v PSD v editovatelném režimu**

| |Bitmap|Odstíny šedi|Indexované|RGB|CMYK|Vícekanálové|Duotónové|Lab|
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
|Hloubka 1|Ano|-|-|-|-|-|-|-|
|Hloubka 8|-|Ano|Ne|Ano|Ano|Ne Q3-Q4|Ne Q3-Q4|Ano*|
|Hloubka 16|-|Ano|-|Ano|Ano*|-|-|Ne (Q3-Q4)|
|Hloubka 32|-|Ne (Q3-Q4)|-|Ne (Q3-Q4)|-|-|-|-|
\* Menší problémy v některých případech

Pokud potřebujete podporu pro konkrétní kombinaci barvového režimu / hloubky bitů, můžete přispět na [Aspose fórech](https://forum.aspose.com/c/psd)

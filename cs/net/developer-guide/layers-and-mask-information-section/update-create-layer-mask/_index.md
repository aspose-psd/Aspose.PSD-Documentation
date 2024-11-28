---
title: Práce s maskami v Aspose.PSD pro С#
weight: 100
type: docs
description: Příklady práce s Clipping, Raster a Vector Maskami v souboru PSD
keywords: [masky, vrstevní maska, vektorová maska, Clipping maska, psd, psd api, C#, csharp, ukázkový kód]
url: cs/net/update-create-layer-mask/
---

## Přehled

Existují tři druhy masek v souborech PSD:
1. Clipping masky
2. Raster masky
3. Vektorové masky

Tento článek pokrývá všechny tři druhy.

### Clipping masky

Clipping masky jsou mocnou funkcí v grafickém návrhu a softwaru pro úpravu obrázků, která vám umožňuje ovládat viditelnost jedné vrstvy na základě tvaru a obsahu druhé vrstvy. V podstatě clipping maska omezuje viditelnost vrstvy na tvar definovaný jinou vrstvou pod ní.

Pro vytvoření clipping masky potřebujete dvě vrstvy: základní vrstvu a maskovací vrstvu. Základní vrstva definuje tvar nebo oblast, která bude viditelná, zatímco maskovací vrstva obsahuje obsah, který bude omezen na tvar základní vrstvy.

Při použití clipping masky je obsah maskovací vrstvy viditelný pouze v mezích základní vrstvy. Jakýkoli obsah mimo hranice základní vrstvy je skryt nebo oříznut.

Clipping masky jsou zvláště užitečné pro aplikování efektů, jako jsou textury nebo vzory, na konkrétní části obrázku nebo uměleckého díla. Použitím clipping masky můžete zajistit, že efekt bude omezen na požadovanou oblast, aniž by ovlivnil zbytek obrázku.

### Raster masky

Raster masky v souborech PSD jsou nezbytné pro ovládání viditelnosti konkrétních oblastí v rámci vrstvy. Na rozdíl od vektorových masek, které používají matematické tvary k definici maskovaných oblastí, raster masky používají informace založené na pixelech k určení, které části vrstvy jsou viditelné nebo skryté.

Raster maska se skládá z odstínového obrazu aplikovaného na vrstvu. Bílé oblasti masky představují viditelné části, zatímco černé oblasti představují skryté části. Odstíny šedé barvy uprostřed vytvářejí částečnou průhlednost nebo polo-viditelné oblasti.

Pomocí rastrových masek můžete dosáhnout složitých efektů maskování, což umožňuje precizní kontrolu viditelnosti vrstvy na základě detailů na úrovni pixelů. Tato funkce je zvláště užitečná pro úkoly, které vyžadují detailní úpravy a míchání v rámci obrázku.

### Vektorové masky

Vektorové masky v souborech PSD jsou všestranným nástrojem používaným k definici viditelnosti specifických oblastí v rámci vrstvy na základě matematických tvarů. Na rozdíl od rastrových masek, které používají informace založené na pixelech, vektorové masky využívají cesty a křivky k vytvoření hladkých a škálovatelných maskovaných oblastí.

Vektorová maska je v podstatě cesta aplikovaná na vrstvu. Tvar cesty určuje, které části vrstvy jsou viditelné a které jsou skryté. Manipulací s kontrolními body a křivkami cesty můžete vytvořit precizní a složité maskované oblasti.

Vektorové masky jsou zvláště užitečné pro vytváření čistých, škálovatelných masek, které lze snadno upravovat bez ztráty kvality. Tato funkce je ideální pro úkoly, které vyžadují vysokou přesnost a flexibilitu při definování viditelných oblastí v rámci vrstvy.

Pro více informací o přidání vektorových masek navštivte stránku [Vektorové masky](psd/cs/cs/layer-vector-mask/).

## Příklad
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

Pro podrobnější informace a příklady navštivte [Aspose.PSD pro C# dokumentaci](https://docs.aspose.com/psd/cs/).

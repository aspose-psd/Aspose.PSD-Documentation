---
title: Práce s maskami v Aspose.PSD pro Python
weight: 100
type: docs
description: Příklady práce s ořezáváním, rastrovými a vektorovými maskami v souboru PSD
keywords: [masky, maska vrstvy, vektorová maska, ořezávání maska, psd, psd api, python, ukázkový kód]
url: cs/python-net/update-create-layer-mask/
---

## **Přehled**

**Přehled**

Existují 3 typy masek v souborech PSD:
1. Masky ořezávání
2. Rastrové masky
3. Vektorové masky

Tento článek pokrývá všechny 3 typy.

**Masky ořezávání**

Masky ořezávání jsou mocnou funkcí v grafickém designu a softwaru pro úpravu obrázků. Umožňují vám ovládat viditelnost jedné vrstvy na základě tvaru a obsahu jiné vrstvy. Jinými slovy, maska ořezávání omezuje viditelnost vrstvy na tvar druhé vrstvy pod ní.

Pro vytvoření masky ořezávání potřebujete nejprve dvě vrstvy: základní vrstvu a vrstvu, kterou chcete oříznout. Základní vrstva definuje tvar nebo oblast, která bude viditelná, zatímco vrstva, kterou chcete oříznout, obsahuje obsah, který bude oříznutý do tvaru základní vrstvy.

Při použití masky ořezávání je obsah ořezané vrstvy viditelný pouze v mezích základní vrstvy. Jakýkoli obsah mimo meze základní vrstvy bude skrytý nebo oříznutý.

Masky ořezávání jsou zvláště užitečné, když chcete aplikovat efekt, jako je textura nebo vzor, do konkrétní oblasti obrázku nebo uměleckého díla. Použitím masky ořezávání můžete omezit efekt na požadovanou oblast bez toho, aniž byste ovlivnili zbytek obrázku.

Podívejte se na příklad na konci stránky.

**Rastrové masky**

Rastrové masky v souborech PSD slouží k ovládání viditelnosti konkrétních oblastí uvnitř vrstvy. Na rozdíl od vektorových masek, které používají matematické tvary k definici ořezaných oblastí, rastrová maska využívá pixelové informace k určení, které části vrstvy jsou viditelné nebo skryté.

Rastrová maska se skládá z obrazu šedi, který se aplikuje na vrstvu. Bílé oblasti masky představují viditelné části, zatímco černé oblasti představují skryté části. Odstíny šedi mezi tím lze použít k vytvoření částečné průhlednosti nebo polo-viditelných oblastí.

Podívejte se na příklad na konci stránky.

**Vektorové masky**

Vektorové masky v souborech PSD jsou univerzálním nástrojem používaným k definici viditelnosti konkrétních oblastí uvnitř vrstvy na základě matematických tvarů. Na rozdíl od rastrových masek, které využívají pixelové informace, vektorové masky využívají cesty a křivky k vytvoření hladkých a měřitelných ořezaných oblastí.

Vektorová maska je podstatně cesta, která je aplikována na vrstvu. Tvar cesty určuje, které části vrstvy jsou viditelné a které části jsou skryté. Manipulací s kontrolními body a křivkami cesty můžete vytvářet přesné a složité ořezané oblasti.

Podívejte se na [stránku Vektorové masky](psd/cs/net/layer-vector-mask/), abyste získali informace o tom, jak mohou být vektorové masky přidány pomocí zdrojů.

## **Příklad**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-update-create-layer-mask.py" >}}

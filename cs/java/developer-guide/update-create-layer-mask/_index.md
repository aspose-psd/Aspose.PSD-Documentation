---
title: Práce s maskami v Aspose.PSD pro Java
weight: 100
type: docs
description: Příklady práce s ořezáváním, rastr a vektorovými maskami v souboru PSD
keywords: [masky, maska vrstvy, vektová maska, maska ořezávání, psd, psd api, java, vzorový kód]
url: cs/java/update-create-layer-mask/
---

## **Přehled**

**Přehled**

Existují 3 typy masek v souborech PSD:
1. Maska ořezávání
2. Rastrová maska
3. Vektorová maska

Tento článek pokrývá všechny 3 typy.

**Maska ořezávání**

Masy ořezávání jsou robustní funkcí v grafickém návrhu a softwaru pro úpravu obrazu, zejména v Javě. Umožňují přesnou kontrolu nad viditelností jedné vrstvy na základě tvaru a obsahu jiné vrstvy. Podstatou masky ořezávání je omezení viditelnosti vrstvy na tvar jiné vrstvy pod ní.

Pro implementaci masky ořezávání v Javě budete potřebovat dvě vrstvy: základní vrstvu a vrstvu, kterou chcete upravit. Základní vrstva definuje tvar nebo oblast, která zůstane viditelná, zatímco vrstva k oříznutí obsahuje obsah, který bude odpovídat tvaru základní vrstvy.

Když se maska ořezávání použije v Javě, obsah oříznuté vrstvy je viditelný pouze v mezích základní vrstvy. Jakýkoli obsah mimo tyto mezery bude skryt nebo oříznut.

Masy ořezávání jsou zvláště cenné při aplikaci efektů, jako jsou textury nebo vzory, na konkrétní oblasti obrázku nebo uměleckého díla. Použitím masky ořezávání můžete omezit efekt na požadovanou oblast, aniž byste ovlivnili zbytek obrázku.

Pro lepší pochopení se odkazujte na příklad na konci stránky.

**Rastrové masky**

Rastrové masky v souborech Java slouží k správě viditelnosti konkrétních oblastí ve vrstvě. Na rozdíl od vektorových masek, které využívají matematické tvary k definici maskovaných oblastí, rastrové masky spoléhají na informace založené na pixelech k určení viditelných nebo skrytých oblastí.

Rastrová maska se skládá ze šedého obrázku aplikovaného na vrstvu. Bílé oblasti masky označují viditelnost, zatímco černé oblasti představují skryté části. Odstíny šedi mezi nimi mohou vytvářet částečnou průhlednost nebo polovzdálené oblasti.

Pro lepší porozumění se odkazujte na příklad na konci stránky.

**Vektorové masky**

Vektorové masky v souborech Java jsou univerzálními nástroji používanými k určení viditelnosti konkrétních oblastí ve vrstvě na základě matematických tvarů. Na rozdíl od rastrových masek, které závisí na pixelech, vektorové masky využívají cesty a křivky k vytvoření hladkých a škálovatelných maskovaných oblastí.

Vektorová maska v podstatě sestává z cesty aplikované na vrstvu. Tvar této cesty určuje, které části vrstvy jsou viditelné a které jsou skryté. Manipulací s kontrolními body a křivkami cesty lze vytvářet přesné a složité maskované oblasti.

Pro informace o přidávání vektorových masek pomocí zdrojů se odkazujte na [stránku s vektorovými maskami](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/).

## **Příklad**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentace-Java-Aspose-psd-update-create-layer-mask.java" >}}

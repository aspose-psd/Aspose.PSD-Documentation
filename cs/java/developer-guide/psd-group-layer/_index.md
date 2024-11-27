---
title: Příklad použití skupinových vrstev v Aspose.PSD pro Java
weight: 100
type: docs
description: Využití skupinové vrstvy souboru PSD pomocí Java
keywords: [skupinová vrstva, skupinová vrstva, přidat vrstvu do skupiny, psd api, java, ukázkový kód]
url: cs/java/psd-group-layer/
---

## **Přehled**

Využití skupinových vrstev v Aspose.PSD pro Java zvyšuje vaši schopnost spravovat a organizovat vrstvy v rámci obrázku typu PSD efektivně. Skupinové vrstvy, také nazývané složkové vrstvy, vám umožňují sloučit více vrstev a aplikovat transformace nebo efekty kolektivně.

Pro začátek vytvořte nový obrázek typu PSD pomocí metody PsdImage.create(). Poté inicializujte nový objekt třídy LayerGroup pomocí metody addLayerGroup objektu PsdImage. Určete požadovaný název pro skupinovou vrstvu ("Složka"), určete index vložení (0) a nastavte booleanovou hodnotu indikující její viditelnost (True).

Následně vytvořte dva objekty vrstvy Layer a nastavte jejich zobrazení pomocí metody setDisplayName. Přidejte tyto vrstvy do skupinové vrstvy pomocí metody addLayer.

K přístupu k vrstvám v rámci skupiny využijte vlastnost layers objektu LayerGroup. Ověřte, že zobrazení první a druhé vrstvy v rámci skupiny je "Vrstva 1" a "Vrstva 2".

Jakmile jste upravili skupinové vrstvy, uložte modifikovaný obrázek PSD pomocí metody save objektu PsdImage.

Toto slouží jako základní příklad, který vám pomůže se seznámit s prací se skupinovými vrstvami pomocí Aspose.PSD pro Java. Knihovna nabízí mnoho pokročilých funkcí pro manipulaci s vrstvami a transformací uvnitř obrázků PSD. Pro další podrobnosti a příklady o využívání skupinových vrstev a dalších funkcí této knihovny se podívejte do dokumentace Aspose.PSD pro Java.

Pro práci se skupinovými vrstvami v Aspose.PSD pro Java využijte třídu LayerGroup. Níže je ukázkový kód ilustrující, jak vytvořit skupinovou vrstvu, přidat do ní vrstvy a uložit modifikovaný obrázek PSD.

Prosím odkazujte se na poskytnutý kompletní příklad.

## **Příklad**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}

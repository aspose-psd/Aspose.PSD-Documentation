---
title: Ukázka použití skupinových vrstev v Aspose.PSD pro Python
weight: 100
type: docs
description: Použití skupinových vrstev v souboru PSD pomocí Pythonu
keywords: [vrstva skupiny, skupinová vrstva, přidání vrstvy do skupiny, psd api, python, ukázkový kód]
url: cs/python-net/psd-group-layer/
---

## **Přehled**

Práce se skupinovými vrstvami v Aspose.PSD pro Python je silná funkce, která vám umožňuje organizovat a manipulovat s vrstvami v rámci obrazu PSD. Skupinové vrstvy, také známé jako složkové vrstvy, poskytují způsob, jak seskupit více vrstev dohromady a aplikovat transformace nebo efekty na celou skupinu.

V této ukázce nejprve vytvoříme nový obraz PSD pomocí metody PsdImage.create. Poté vytvoříme nový objekt LayerGroup pomocí metody add_layer_group objektu PsdImage. Poskytneme název skupinové vrstvy ("Složka"), index, na kterém by měla být vložena (0), a boolean flag, který udává, zda má být skupinová vrstva viditelná (True).

Poté vytvoříme dva objekty Layer a nastavíme jejich zobrazené názvy pomocí vlastnosti display_name. Tyto vrstvy přidáme do skupinové vrstvy pomocí metody add_layer.

Nakonec můžeme přistupovat k vrstvám uvnitř skupiny pomocí vlastnosti layers objektu LayerGroup. V ukázce ověřujeme, že zobrazené názvy první a druhé vrstvy ve skupině jsou "Vrstva 1" a "Vrstva 2" odpovídajícím způsobem.

Po manipulaci se skupinovými vrstvami můžeme uložit modifikovaný obraz PSD pomocí metody save objektu PsdImage.

Toto je pouze základní příklad, jak začít pracovat se skupinovými vrstvami pomocí Aspose.PSD pro Python. Knihovna poskytuje mnoho pokročilých funkcí pro manipulaci a transformaci vrstev v obrazech PSD. Pro více podrobností a příkladů práce se skupinovými vrstvami a dalšími funkcemi knihovny se můžete odkázat na dokumentaci Aspose.PSD pro Python.

Pro práci se skupinovými vrstvami v Aspose.PSD pro Python můžete použít třídu LayerGroup. Zde je ukázková část kódu, která ukazuje, jak vytvořit skupinovou vrstvu, přidat do ní vrstvy a uložit modifikovaný obraz PSD.

Zkontrolujte celý příklad.

## **Příklad**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentace-Python-Aspose-psd-group-layer.py" >}}

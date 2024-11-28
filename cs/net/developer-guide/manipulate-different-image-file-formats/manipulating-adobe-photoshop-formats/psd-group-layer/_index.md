---
title: Příklad použití skupinových vrstev v Aspose.PSD pro C#
weight: 100
type: docs
description: Použití skupinové vrstvy souboru PSD pomocí C#
keywords: [skupinová vrstva, skupinová vrstva, přidání vrstvy do skupiny, psd api, C#, csharp, ukázkový kód]
url: cs/net/psd-group-layer/
---

## Přehled

Skupinové vrstvy v Aspose.PSD pro C# umožňují efektivní organizaci a manipulaci vrstev v souboru PSD. Použitím vrstev složek můžete seskupit více vrstev dohromady a aplikovat transformace nebo efekty na celou skupinu.

Tento příklad ukazuje vytvoření nového obrazu PSD s `PsdImage.Create`. Poté je vytvořen nový objekt `LayerGroup` pomocí `AddLayerGroup` z objektu `PsdImage`. Skupinová vrstva je pojmenována "Složka", vložena na index 0 a nastavena jako viditelná.

Následně jsou vytvořeny dvě objekty `Layer` se nastavenými vlastnostmi `DisplayName`. Tyto vrstvy jsou přidány do skupinové vrstvy pomocí `AddLayer`.

Vrstvy ve skupině lze přistupovat pomocí vlastnosti `Layers` objektu `LayerGroup`. Příklad tvrdí, že zobrazení jmen první a druhé vrstvy ve skupině jsou "Vrstva 1" a "Vrstva 2".

Po úpravách skupinových vrstev je aktualizovaný obraz PSD uložen pomocí metody `Save` objektu `PsdImage`.

Tento základní příklad představuje práci se skupinovými vrstvami pomocí Aspose.PSD pro C#. Knihovna nabízí pokročilé funkce pro manipulaci a transformaci vrstev v souborech PSD. Podrobnější příklady a funkce naleznete v dokumentaci Aspose.PSD pro C#.

Zde je ukázkový kód demonstrující použití skupinové vrstvy v Aspose.PSD pro C#:

## Příklad

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Pro podrobnější informace a příklady navštivte stránku [Dokumentace Aspose.PSD pro C#](https://docs.aspose.com/psd/net/).

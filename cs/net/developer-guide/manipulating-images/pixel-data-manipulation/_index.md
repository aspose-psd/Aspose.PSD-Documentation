---
title: Manipulace s daty pixelů pomocí Aspose.PSD pro C#
weight: 100
type: docs
description: Příklad přímého a rychlého aktualizování surových dat pixelů pomocí rozhraní API Aspose.PSD pro C#
keywords: [upravit pixely, upravit psd, upravit vrstvu, manipulace se surovými daty, upravit psd data, psd api, C#, csharp, ukázkový kód]
url: cs/net/manipulace-s-daty-pixelu/
---

## Úvod

Aspose.PSD je výkonná knihovna, která vám umožňuje pracovat soubory Adobe Photoshop (PSD) v jazyce C#. V tomto článku prozkoumáme, jak manipulovat s daty pixelů v souboru PSD pomocí Aspose.PSD pro C#.

## Přehled

Poskytnutý kód ukazuje, jak vytvořit soubor PSD, přidat novou vrstvu, přímo manipulovat s daty pixelů a uložit upravený obrázek.

### Kroky k manipulaci s daty pixelů

1. **Import požadovaných modulů**:
   Importujte potřebné moduly. Musíte importovat třídy `PsdImage` a `Layer` z knihovny Aspose.PSD.

2. **Definice cest k vstupnímu a výstupnímu souboru**:
   Určete cesty k vstupnímu a výstupnímu souboru.

3. **Otevření vstupního souboru jako proud**:
   Otevřete vstupní soubor jako proud za použití třídy `FileStream` v režimu čtení. Vytvořte objekt `PsdImage` tím, že načtete proud.

4. **Vytvoření nového obrazu PSD**:
   Vytvořte nový obrázek PSD pomocí konstruktoru `PsdImage` a poskytněte šířku a výšku vrstvy jako argumenty.

5. **Přiřadit vrstvu k obrázku PSD**:
   Přiřaďte vrstvu k vlastnosti `Layers` obrázku PSD.

6. **Manipulace s daty pixelů**:
   Načtěte pixely ARGB32 z vrstvy pomocí metody `LoadArgb32Pixels`. Definujte rozsah indexů na základě délky pole pixelů a upravte hodnoty pixelů dle potřeby.

7. **Uložení upravených dat pixelů**:
   Uložte upravená data pixelů zpět do vrstvy pomocí metody `SaveArgb32Pixels`.

8. **Uložení obrazu PSD**:
   Uložte obrázek PSD do výstupního souboru pomocí metody `Save`.

### Příklad

Zde je ukázkový kód demonstrující, jak manipulovat s daty pixelů pomocí Aspose.PSD pro C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### Shrnutí

Aspose.PSD pro C# poskytuje silnou sadu funkcí pro manipulaci s daty pixelů v souborech PSD. Ať už potřebujete upravit pixely na základě konkrétních podmínek nebo vytvořit složité vzory, Aspose.PSD tyto úlohy zjednodušuje a efektivní způsobem.

Pro více podrobností a příkladů navštivte [dokumentaci Aspose.PSD pro C#](https://docs.aspose.com/psd/net/).

---
title: Použití grafického rozhraní API ke zpracování vrstev v souborech PSD
weight: 100
type: docs
description: Příklad použití grafického rozhraní API v Aspose.PSD pro Java
keywords: [aktualizovat vrstvu, kreslit kruh, kreslit elipsu, vyplnit kruh, grafika, psd api, java, ukázkový kód]
url: cs/java/graphics-api/
---

## **Přehled**
Pro začátek načtěte soubor PSD pomocí metody Image.load() nebo vytvořte obraz Psd Image od základu. Použijte proměnnou inputFile k reprezentaci cesty k vašemu souboru PSD a pokud je to nutné, specifikujte jakékoliv možnosti načítání pomocí loadOpt.

Následně přistupte k první vrstvě obrázku PSD pomocí syntaxe psdImage.getLayers()[0] ke získání odkazu na objekt vrstvy pro manipulaci.

Pro úpravu vrstvy vytvořte grafický objekt pomocí vrstvy jako parametru. Tento objekt poskytuje různé metody pro kreslení tvarů a použití štětců.

Objekt Pen je použit k definici barvy a tloušťky obrysu tvarů. Stejně tak se používají štětce jako LinearGradientBrush k definování výplňových barev.

Kreslete tvary na vrstvu pomocí metod jako graphics.drawEllipse() pro obrysy tvarů a graphics.fillEllipse() pro jejich vyplnění.

Po provedení požadovaných změn na vrstvě uložte upravený obrázek PSD pomocí psdImage.save().

Dodatečně můžete upravený obrázek uložit v jiných formátech jako PNG pomocí příslušných možností.

To je vše! Úspěšně jste použili grafické rozhraní API Aspose.PSD pro Java ke zpracování vrstev v souboru PSD. Prozkoumejte další funkce a možnosti knihovny Aspose.PSD pro zlepšení vašich schopností editace obrázků.

Zkontrolujte celý příklad.

## **Příklad**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentace-Java-Aspose-Psd-graphics-api.java" >}}

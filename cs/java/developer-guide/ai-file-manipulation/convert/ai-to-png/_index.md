---
title: Převod AI na PNG pomocí Javy
weight: 100
type: docs
description: Zjistěte, jak může Aspose.PSD pro Javu převést soubor AI na PNG.
keywords: [ai na png, ai formát, soubory ilustrátoru, převést ilustrátor, png, psd api, java, ukázkový kód]
url: cs/java/convert/ai-na-png
---

## **Přehled**
Pro převod souborů AI do formátu PNG pomocí Aspose.PSD pro Javu můžete postupovat následujícím způsobem:

- Nainstalujte Aspose.PSD pro Javu: Začněte stažením a instalací knihovny Aspose.PSD pro Javu. Můžete ji zahrnout jako závislost do svého projektu přidáním do konfigurace aplikace Maven nebo Gradle, nebo ručně přidáním JAR souboru.

- Importujte potřebné moduly: Jakmile jste přidali knihovnu Aspose.PSD do svého projektu, importujte potřebné třídy do vašeho Java kódu. Tyto třídy zahrnují ty, které jsou potřebné pro načítání a manipulaci souborů AI, stejně jako jejich export do formátu PNG.

- Načtěte a manipulujte soubory AI: Využijte třídy poskytované společností Aspose.PSD k načtení vašich souborů AI do vaší Java aplikace. Můžete použít třídu Image k načtení souboru AI a manipulaci s jeho obsahem dle potřeby.

- Exportujte AI do PNG: Po načtení souboru AI vytvořte instanci třídy PsdOptions k nastavení parametrů pro export do PNG. To zahrnuje parametry jako je kvalita obrázku, úroveň komprese a další. Nakonfigurujte tyto možnosti dle vašich požadavků.

- Uložte a použijte PNG: Jakmile nastavíte možnosti exportu, použijte metodu Image.Save k uložení souboru AI jako PNG. Specifikujte požadovanou cestu k souboru, kde chcete uložit výsledný soubor PNG.

- Použijte soubor PNG: Po uložení souboru PNG ho můžete použít pro různé účely, jako je sdílení, zobrazení na webové stránce nebo další zpracování. Výsledný soubor PNG bude obsahovat veškerý obsah původního souboru AI, převedený do formátu PNG.

## **Souhrn**
Celkově použitím Aspose.PSD pro Javu můžete bezproblémově převést soubory AI do formátu PNG, což umožňuje kompatibilitu s různými aplikacemi a zařízeními, které podporují PNG. Proces konverze zahrnuje načtení souboru AI, konfiguraci exportních možností s využitím [PngOptions](https://reference.aspose.com/psd/java/com.aspose.psd.imageoptions/pngoptions/) a uložení výstupu jako soubor PNG pomocí metody PsdImage.save. S Aspose.PSD pro Javu můžete dosáhnout přesných a spolehlivých převodů AI na PNG snadno.

## **Příklad**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose.Psd-Convert-Ai-To-Png.java" >}}

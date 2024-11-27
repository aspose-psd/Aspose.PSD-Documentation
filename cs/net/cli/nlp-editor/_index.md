---
title: Aplikace Aspose.PSD CLI NLP Editor pro .NET
type: docs
weight: 10
url: /cs/net/cli/nlp-editor/
is_root: false
keywords: CLI Photoshop Tool NLP Zpracování přírodním jazykem PSD Konzole Knihovna C# Knihovna PSD API
description: Aplikace Aspose.PSD-based NLP Editor CLI pro formáty souborů PSD, PSB a AI. Automatizace CI/CD bez kódu. Podpora zpracování přírodním jazykem pro úpravu souborů PSD. Stačí napsat svůj požadavek přirozeným jazykem k provedení různých operací, jako je konverze, úprava velikosti a další. Nemá požadavek na instalaci programu Adobe Photoshop nebo Adobe Illustrator a může být spuštěn z konzole bez dalšího kódu.
---

**![Logo produktu Aspose.PSD pro .NET](home_1.png)**

**Vítejte v Aspose.PSD NLP Editor CLI Application pro .NET**

Aplikace Aspose.PSD CLI NLP Editor je lehká konzolová utilita pro úpravu souborů PSD pomocí přírodních jazykových příkazů. Snadná integrace do CI/CD Pipelines.

**Oznam**

Jedná se o experimentální aplikaci. Prosím vyzkoušejte ji a zanechte zpětnou vazbu. Jakákoli zpětná vazba je velmi ceněna. Chceme přenést aplikaci bez kódu na další úroveň. Snadná integrace do libovolné sestavy pipeline nebo firemního procesu je naším cílem.

**Hlavní funkcionality aplikace Aspose.PSD NLP Editor CLI pro .NET**

1. Provádění operací na souborech PSD, PSB, AI pomocí přírodních jazykových příkazů.
2. Podpora různých operací, jako je konverze, úprava velikosti a další.
3. Automatizace CI/CD bez kódu.
4. Podpora psaní požadavků přirozeným jazykem pro úpravu souborů PSD.

## **Použití z příkazové řádky:**

{{% alert color="primary" %}}
Nejprve nainstalujte tento nástroj dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Doporučujeme před prvním použitím spusťte následující příkaz:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Po provedení tohoto příkazu budete moci spustit tuto aplikaci se zkráceným názvem nlp.cli místo Aspose.PSD.CLI.NLP.Editor. Můžete specifikovat vlastní zkrácený název.
{{% /alert %}}


**Dostupné parametry pro aplikaci Aspose.PSD.CLI.Crop**

| **Argument** | **Popis**                         |
|:-------------|:----------------------------------------|
| libovolný text     | Vyžadováno. Váš příkaz v přirozeném jazyce k aktualizaci souboru PSD nebo PSB      |
| license      | Cesta k licenci.                    |
| verbose      | Zobrazit více informací o konkrétním příkazu. |
| setup        | Vytvoří soubor bat ve složce nástrojů pro rychlé volání z konzole. Příklad: --setup psd.nlp. Poté můžete nástroj volat s příkazem psd.nlp |


**Příklady použití**

1. Tento příkaz převede první nalezený soubor (který lze otevřít s aspose.psd) z aktuální složky a uloží jej ve formátu png s průhledností. Licenci bude nastavena. Musíte specifikovat licenci pouze jednou. Při dalších spuštěních bude licenci automaticky načítat z dané cesty. Tento příkaz zobrazí podrobný záznam o zpracování přes NLP, pokud je k dispozici.
{{< highlight bash >}}
  nlp.cli Konvertovat soubor z této složky do formátu png s alfa --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. Tento příkaz najde soubor s nejpodobnějším názvem "smth.psd". Následně upraví kontrast a uloží jej jako jpeg s nejlepší kvalitou. Název výstupního souboru bude vytištěn. Bude to smth.jpg
{{< highlight bash >}}
Upravit kontrast na 10 vrstvě s názvem ellipse v souboru smth.psd a uložit jej jako output.jpg s nejlepší kvalitou
{{< /highlight >}}

3. Tento příkaz namotá soubor na zadané cestě a zmenší jeho velikost na 25 %. Výstupní soubor bude vytištěn. Bude uložen v aktuální složce konzole.
{{< highlight bash >}}
Změnit velikost souboru C:\Users\someuser\Desktop\input.psd na 25 %
{{< /highlight >}}

4. Tento příkaz najde soubor input.psd v  C:\Users\someuser\Desktop\. Následně najde vrstvu s indexem 3 a zmenší ji na šířku 50px a výšku 100px. Tato vrstva bude uložena jako PDF v C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
Změnit velikost vrstvy s indexem 3 v souboru C:\Users\someuser\Desktop\input.psd na šířku 50 a výšku 100 a uložit ji do C:\Users\someuser\Desktop\output.pdf
{{< /highlight >}}

5. Tento příkaz otevře soubor smth.psd v aktuální složce, ale všechny efekty budou zakázány. A poté tento soubor bude převeden do formátu BMP jako output.bmp v aktuální složce.
{{< highlight bash >}}
Otevřít smth.psd bez efektů a uložit jej jako output.bmp
{{< /highlight >}}

**Zkontrolujte prosím další [Aspose.PSD CLI Aplikace](https://docs.aspose.com/psd/net/cli) pro .NET, pokud potřebujete přidat podporu pro formáty PSD, PSB a AI do vaší pracovního postup**

1. [Aspose.PSD CLI Konverze](/psd/cs/net/cli/convert)
2. [Aspose.PSD CLI Oříznutí](/psd/cs/net/cli/crop)
3. [Aspose.PSD CLI Změna velikosti](/psd/cs/net/cli/resize)
4. [Aspose.PSD CLI Export](/psd/cs/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/cs/net/cli/nlp-editor)

**Zkontrolujte prosím Aspose.PSD pro .NET nebo [ostatní platformy]**

Aplikace Aspose.PSD CLI je připravené řešení pro populární operace. Pokud potřebujete flexibilní řešení, zkontrolujte prosím plnou verzi Aspose.PSD.

1. [Aspose.PSD pro .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD pro Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD pro Python pomocí .NET](https://releases.aspose.com/psd/python-net/)

## **Zdroje k Aspose.PSD pro .NET**

Zde najdete odkazy na některé užitečné zdroje, které můžete potřebovat k dokončení úkolů.

- [Aspose.PSD CLI Aplikace pro .NET Online Dokumentace](/psd/cs/net/cli/conversion)
- [Aspose.PSD pro CLI Aplikace pro .NET Poznámky k vydání](/psd/cs/net/cli/conversion/release-notes/)
- [Aspose.PSD pro CLI Aplikace .NET Stránka Produktu](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD pro .NET API Referenční Průvodce](https://reference.aspose.com/net/psd)
- [Stažení Příkladů na GitHub Repository](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD pro .NET Fórum s Bezplatnou Podporou](https://forum.aspose.com/c/psd)
- [Aspose.PSD pro .NET Placená Podpora Helpdesk](https://helpdesk.aspose.com/)


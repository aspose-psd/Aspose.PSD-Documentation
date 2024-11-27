---
title: Aspose.PSD CLI NLP Editor pro .NET 24.6 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD CLI NLP Editor pro .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Klíč**    | **Souhrn**                                                                                    | **Kategorie** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | První vydání aplikací Aspose.PSD CLI: Aspose.PSD.CLI.Export a Aspose.PSD.CLI.NLP.Editor      | Vylepšení    |


## **Příklady použití:**

**PSDNET-2110. První vydání aplikace Aspose.PSD CLI NLP Editor**

## **Použití z příkazové řádky:**

{{% alert color="primary" %}}
Nejprve nainstalujte tento nástroj pro 'dotnet':
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Před prvním použitím doporučujeme spustit následující příkaz:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Po provedení tohoto příkazu budete moci spustit tuto aplikaci s krátkým názvem 'nlp.cli' místo 'Aspose.PSD.CLI.NLP.Editor'. Můžete zadat vlastní krátký název.
{{% /alert %}}

**Příklady použití**

1. Tento příkaz převede první nalezený soubor (který lze otevřít pomocí aspose.psd) z aktuální složky a uloží jej ve formátu png s průhledností. Také bude nastavena licence. Musíte licenci zadat pouze jednou. Při dalším spuštění bude licence použita ze zadané cesty. Tento příkaz zobrazí podrobný protokol zpracování NLP, pokud je k dispozici.
{{< highlight bash >}}nlp.cli Převést soubor z této složky do formátu png s alfa -licenci "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. Tento příkaz najde soubor s nejpodobnějším názvem "smth.psd". Poté upraví kontrast a uloží jej do formátu jpeg s nejlepší kvalitou. Název výstupního souboru bude vytisknut. Bude to smth.jpg
{{< highlight bash >}}Upravit kontrast 10 vrstvy s názvem ellipse v souboru smth.psd a uložit jej do output.jpg s nejlepší kvalitou{{< /highlight >}}

3. Tento příkaz ovine soubor na zadané cestě a zmenší jeho velikost na 25%. Výstupní soubor bude vytisknut. Bude uložen ve složce konzole.
{{< highlight bash >}}Změnit velikost souboru C:\Users\someuser\Desktop\input.psd na 25%{{< /highlight >}}

4. Tento příkaz najde soubor input.psd v C:\Users\someuser\Desktop\. Poté najde vrstvu s indexem 3 a změní její velikost na šířku 50px a výšku 100px. Tato vrstva bude uložena jako PDF v C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Změnit velikost vrstvy s indexem 3 z C:\Users\someuser\Desktop\input.psd na šířku 50 a výšku 100 a uložit jej do C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. Tento příkaz otevře soubor smth.psd v aktuální složce, ale všechny efekty budou deaktivovány. Poté bude tento soubor převeden do formátu BMP a uložen jako output.bmp v aktuální složce.
{{< highlight bash >}}Otevřít smth.psd bez efektů a uložit jej do output.bmp{{< /highlight >}}

**Varování**

Jedná se o experimentální aplikaci. Prosím, vyzkoušejte ji a podělte se o zpětnou vazbu. Jakákoliv zpětná vazba je velmi ceněna. Chceme přinést aplikaci bez kódu na další úroveň. Snahou je snadná integrace do jakéhokoli sestavovacího procesu nebo obchodního procesu.

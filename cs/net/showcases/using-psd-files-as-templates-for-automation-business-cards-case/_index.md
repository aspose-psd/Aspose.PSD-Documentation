---
title: Použití souborů PSD jako šablon pro automatizaci - Případ vizitek
type: docs
weight: 10
url: /cs/pouziti-souboru-psd-jako-sablon-pro-automatizaci-pripad-vizitek/
---

### **Přehled**
Tento článek popisuje často používané případy, kdy je potřeba automaticky aktualizovat některé vrstvy v souboru [PSD](https://wiki.fileformat.com/image/psd/) programově, kdy soubor PSD/PSB má nějakou známou strukturu podobnou šabloně. To lze využít k vytvoření velkého množství vizitek pro různé lidi (Případ vizitek). Nebo potřebujete přeložit soubor PSD do různých jazyků s nahrazením některého grafického materiálu v něm.

Po přečtení tohoto článku budete vědět, jak to udělat:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)

## **Jednoduchý případ**
Například máte nějakou šablonu PSD s známými názvy vrstev. Takže potřebujete změnit, aktualizovat nebo nahradit vrstvu PSD pomocí C#. Nejprve musíte otevřít soubor šablony s pomocí Aspose.PSD.

Jak otevřít soubor PSD pomocí C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)

Poté musíme najít vrstvu, kterou chceme nahradit podle jejího názvu. Zde je jednoduchá implementace tohoto.

Jak najít vrstvu v souboru PSD podle jejího názvu

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}

Když je vrstva nalezena, můžeme ji aktualizovat z běžného způsobu pomocí [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Jak kreslit na vrstvu PSD pomocí Graphics

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

V tomto případě nakreslíme nově načtený [PNG obrázek](https://wiki.fileformat.com/image/png/) na existující vrstvu PSD, takže stará data budou v novém souboru ztracena.

Ale co když potřebujeme také aktualizovat text? Postup bude podobný. Najděte [Textovou vrstvu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) podle jejího názvu a poté ji programově [aktualizujeme Textovou vrstvu souboru Photoshop](/psd/cs/net/render-text-with-different-colors-in-text-layer/).

Jak aktualizovat Textovou vrstvu v Photoshopu pomocí C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}

Nakonec musíme uložit naše změny:

Jak uložit změněný soubor PSD pomocí [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}

Výsledný obrázek:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)

## **Složitý případ s dalšími funkcemi**
Výše jsme ukázali nejjednodušší způsob nahrazení obrázku ve vrstvě souboru PSD.

Ale Aspose.PSD může nabídnout složitější další funkce, jako je přidání nové vrstvy, odstranění starých vrstev a aktualizace textové vrstvy s použitím různých stylů v textu s více řádky.

Můžeme najít [Vrstvu](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer), kterou chceme nahradit, poté najdeme její index ve seznamu vrstev, odstraníme ji a vložíme novou Vrstvu po vytvoření z [Jpeg souboru](https://wiki.fileformat.com/image/jpeg/) na stejné místo.

Vytvořit novou vrstvu z souboru a vložit ji do obrázku PSD pomocí [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}

Na konci tohoto kódu opravíme polohu vrstvy a uložíme nový pole vrstev do obrázku Psd.

Jak zkopírovat vlastnosti vrstvy [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}

A nakonec musíme aktualizovat textové vrstvy v existujícím obrázku PSD pomocí C#. Aspose.PSD podporuje [aktualizaci textové vrstvy po částech](/psd/cs/net/working-with-text-layers/). Každá [textová část](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) má jedinečnou kombinaci stylu a vlastností odstavce.

Jak zkopírovat vlastnosti vrstvy [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}

Výsledkem je změněná šablona PSD pomocí kódu s novou vrstvou z Jpeg, Png, J2k, Bmp, Gif nebo Tiff souboru a víceřádkovým [textem s různými styly](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) v každém řádku.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)

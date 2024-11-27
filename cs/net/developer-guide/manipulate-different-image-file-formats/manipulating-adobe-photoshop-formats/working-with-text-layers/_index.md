---
title: Práce s textovými vrstvami
type: docs
weight: 170
url: /cs/prace-s-textovymi-vrstvami/
---

## **Přidání textové vrstvy**
Aspose.PSD pro .NET vám umožňuje přidat textovou vrstvu do souboru PSD. Postup pro přidání textové vrstvy do souboru PSD je následující:

- Načtěte soubor PSD jako obrázek pomocí metody továrny [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) vystavené třídou [Image](https://reference.aspose.com/psd/net/aspose.psd/image)
- Zavolejte metodu [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer), která přijímá text a instanci třídy [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- Uložte výsledky

Následující ukázka kódu vám ukazuje, jak přidat textovou vrstvu do souboru PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **Nastavení pozice textové vrstvy**
Aspose.PSD pro .NET vám umožňuje nastavit pozici textové vrstvy v souboru PSD. Postup pro nastavení pozice textové vrstvy v souboru PSD je následující:

- Načtěte soubor PSD jako obrázek pomocí tovární metody Load vystavené třídou Image
- Zavolejte metodu AddTextLayer s určením levé a horní pozice textové vrstvy
- Uložte výsledky

Následující ukázka kódu vám ukazuje, jak nastavit pozici textové vrstvy v souboru PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}
## **Získání vlastností textu z textové vrstvy**
Pomocí Aspose.PSD pro .NET můžete získat a aktualizovat vlastnosti textu různých částí textu dostupných v textové vrstvě PSD. Tento článek demonstruje, jak získat odstavce, styly a vlastnosti textu z textové vrstvy a aktualizovat je.

Následující ukázka kódu ukazuje, jak tohoto dosáhnout.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


Zde je další příklad, který demonstruje, jak vývojář může získat formátování textu různých částí textu z [TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer) pomocí [Aspose.PSD pro .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}
## **Aktualizace textové vrstvy v souboru PSD**
Aspose.PSD pro .NET vám umožňuje manipulovat s textem na textové vrstvě souboru PSD. Použijte třídu Aspose.PSD.FileFormats.Psd.Layers.TextLayer k aktualizaci textu v textové vrstvě PSD. Následující ukázka kódu načte soubor PSD, přistoupí k textové vrstvě, aktualizuje text a uloží soubor PSD se novým názvem pomocí metody [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats/psd/layers/textlayer/methods/updatetext/index).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **Podpora textových vrstev za běhu**
Tento článek ukazuje, jak přidat textové vrstvy za běhu do obrázků PSD. Kód ukázky je níže uveden.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}

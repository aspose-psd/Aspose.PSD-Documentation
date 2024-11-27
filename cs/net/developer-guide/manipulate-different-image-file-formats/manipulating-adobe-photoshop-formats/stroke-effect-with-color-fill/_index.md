---
title: Efekt Přesahu s Barevným Výplněm
type: docs
weight: 60
url: /cs/net/efekt-presahu-s-barevnym-vyplnem/
---

## **Efekt Přesahu s Barevným Výplněm**
Tento článek představuje, jak vykreslit efekt přesahu s barevnou výplní. Efekt Přesahu se používá k přidání přesahů a hranic k vrstvám a tvarům. Lze ho použít k vytváření jednobarevných linií, barevných přechodů a vzorovaných hranic.

Postup k vykreslení efektu Přesahu s barevnou výplní je následující:

- Nastavte vlastnost [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource).
- Načtěte soubor PSD jako obrázek pomocí tovární metody Load, kterou poskytuje třída Image, a definujte [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions).
- Nastavte vlastnosti nastavení [**ColorFillSetting.**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)
- Uložte výsledky.

Následující ukázkový kód vám ukazuje, jak vykreslit efekt přesahu s barevnou výplní.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}

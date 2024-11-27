---
title: PSD Převod mezi různými módy barev
type: docs
weight: 50
url: /cs/net/psd-convert-between-different-color-modes/
---

Můžete se dozvědět podporované barevné módy Aspose.PSD z tohoto článku.

Aspose.PSD podporuje například konverzi z 8 na 16 bitů na pixel a naopak. Konverze profilů ICC CMYK a další konverze z jednoho typu bitové hloubky na jiný. Zde můžete vidět příklady, jak převést na stupně šedi v souboru PSD.
## **Převést z módu barev CMYK, RGB, Grayscale na mód barev Grayscale**
Níže uvedený ukázkový kód ukazuje, jak provést konverzi CMYK, RGB nebo stupňů šedi bez Photoshopu.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## **16 bitový obraz photoshopu do režimu 8 bitů stupně šedi**
Co když však potřebujete převést 16bitový obraz Photoshopu do režimu 8 bitů stupně šedi? Musíte použít následující kousek kódu. 8 bitů je běžná bitová hloubka v souborech PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## **Převést Grayscale na RGB**
Další složitý případ je, pokud potřebujete převést obraz Grayscale PSD na obraz RGB.

Stupňovité obrázky mají pouze jednou kanál, ale obrázky RGB mají 3 kanály: R - červená, G - zelená, B - modrá. Aspose.PSD může převést Grayscale na RGB.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}

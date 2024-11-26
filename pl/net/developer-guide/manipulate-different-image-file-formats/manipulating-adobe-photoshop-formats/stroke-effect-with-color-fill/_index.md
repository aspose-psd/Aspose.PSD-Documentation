---
title: Efekt Konturu z Wypełnieniem Koloru
type: docs
weight: 60
url: /pl/net/stroke-effect-with-color-fill/
---

## **Efekt Konturu z Wypełnieniem Koloru**
Ten artykuł demonstruje, jak renderować efekt konturu z wypełnieniem koloru. Efekt konturu służy do dodawania obramowań i konturów do warstw i kształtów. Może być używany do tworzenia jednokolorowych linii, kolorowych gradientów oraz wzorowanych obramowań.

Kroki do renderowania efektu konturu z wypełnieniem koloru są proste:

- Ustaw właściwość [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource).
- Wczytaj plik PSD jako obraz przy użyciu metody fabrycznej Load udostępnionej przez klasę Image i zdefiniuj [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions).
- Ustaw właściwości ustawień [**ColorFillSetting.**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)
- Zapisz wyniki.

Poniższy fragment kodu pokazuje, jak renderować efekt konturu z wypełnieniem koloru.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}

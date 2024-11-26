---
title: Obsługa warstw wypełnienia
type: docs
weight: 50
url: /pl/java/obsługa-warstw-wypełnienia/
---


## **Obsługa warstw wypełnienia kolorem**
Ten artykuł demonstruje, jak wypełnić warstwę PSD kolorem. Aby dodać kolor do warstwy PSD, należy użyć klasy Aspose.PSD.FileFormats.Psd.Layers.FillLayer. Poniższy fragment kodu ładuje plik PSD, uzyskuje dostęp do klasy FillLayer i ustawia kolor za pomocą właściwości FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Przykłady-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Obsługa warstw wypełnienia gradientem**
Ten artykuł demonstruje sposób korzystania z wypełnienia gradientowego warstwy PSD. Interfejsy API Aspose.PSD udostępniły wydajne i łatwe w użyciu metody do osiągnięcia tego celu. Aspose.PSD udostępnił klasy GradientColorPoint i GradientTransparencyPoint do dodania efektu gradientu do warstwy.

Kroki do wypełnienia warstwy PSD wypełnieniem gradientowym są proste, jak poniżej:

- Wczytaj plik PSD jako obraz, korzystając z metody fabrycznej Load udostępnionej przez klasę Image.
- Ustaw właściwości ustawień obiektu FillLayer.
- Utwórz listę punktów kolorów z wymaganymi kolorami i pozycją koloru.
- Utwórz listę punktów przejrzystości z wymaganą przezroczystością i pozycją punktu przejrzystości.
- Wywołaj metodę FillLayer.Update
- Zapisz wynik.

Poniższy fragment kodu pokazuje, jak dodać wypełnienie gradientowe do warstwy PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Przykłady-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Efekt obwódki z wypełnieniem kolorem**
Ten artykuł demonstruje, jak renderować efekt obwódki z wypełnieniem kolorem. Efekt obwódki służy do dodawania linii i obramowań do warstw i kształtów. Może być używany do tworzenia linii w jednolitym kolorze, kolorowych gradientów oraz wzorowanych obramowań.

Kroki do renderowania efektu obwódki z wypełnieniem kolorem są proste, jak poniżej:

- Ustaw właściwość **LoadEffectsResource**.
- Wczytaj plik PSD jako obraz, korzystając z metody fabrycznej Load udostępnionej przez klasę Image i zdefiniuj **PsdLoadOptions**.
- Ustaw właściwości ustawień **ColorFillSetting.**
- Zapisz wynik.

Poniższy fragment kodu pokazuje, jak renderować efekt obwódki z wypełnieniem kolorem.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Przykłady-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}




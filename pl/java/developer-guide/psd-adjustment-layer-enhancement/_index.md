---
title: Korzystanie z warstwy dostosowania do usprawnień PSD
weight: 100
type: docs
description: Przykłady korzystania z warstwy dostosowania za pośrednictwem Aspose.PSD dla Javy
keywords: [warstwa dostosowania, usprawnianie zdjęć, dostosowanie krzywych, usprawnienie poziomów, odwracanie, filtr zdjęć,  psd api, java, przykład kodu]
url: pl/java/adjustment-layer-enhancement/
---

## **Omówienie**

Ten artykuł omawia edycję warstw dostosowania w Aspose.PSD dla Javy. Warstwy dostosowania to potężna funkcja w edycji obrazów, która pozwala na dokonywanie niezniszczających zmian w obrazach. Aspose.PSD zapewnia kompleksowy zestaw klas warstw dostosowania, które można użyć do modyfikacji różnych aspektów obrazów.

Aby zademonstrować edycję warstw dostosowania, udostępnimy kod przykładowy na końcu strony, który wczytuje obraz PSD i stosuje różne dostosowania do jego warstw.

W poniższym fragmencie kodu zaczynamy od wczytania obrazu PSD za pomocą metody PsdImage.load(). Następnie konfigurujemy opcje zapisywania plików wyjściowych PNG. Klasa PngOptions pozwala nam określić typ koloru dla obrazu wyjściowego.

Następnie iterujemy przez każdą warstwę obrazu PSD i sprawdzamy jej typ za pomocą metody isAssignable(). Jeśli warstwa jest określonego typu, rzutujemy ją na ten typ za pomocą metody cast() i stosujemy żądane dostosowanie. Na przykład dostosowujemy jasność i kontrast za pomocą BrightnessContrastLayer, modyfikujemy poziomy za pomocą LevelsLayer, dodajemy punkt krzywej do CurvesLayer, i tak dalej.

Możesz dodać dodatkowy kod, aby zastosować inne dostosowania do odpowiednich warstw. Aspose.PSD zapewnia szeroki zakres klas warstw dostosowania, takich jak [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer),
[SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) i inne.

Na koniec zapisujemy zmodyfikowany obraz za pomocą metody save() klasy PsdImage.

To zapewnia podstawowe omówienie sposobu edycji warstw dostosowania w Aspose.PSD dla Javy. Możesz dostosować dostosowania według własnych wymagań i eksplorować różne opcje dostępne w dokumentacji interfejsu API.

Sprawdź pełny przykład poniżej.

## **Przykład**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentacja-Java-Aspose-dostosowanie-warstwy-enhancement.java" >}}

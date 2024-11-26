---
title: Korzystanie z warstwy dostosowania do usprawnień PSD
weight: 100
type: docs
description: Przykłady korzystania z warstwy dostosowania za pomocą Aspose.PSD dla Pythona
keywords: [warstwa dostosowania, ulepszanie zdjęć, dostosowanie krzywych, ulepszenie poziomów, odwrócenie, filtr fotograficzny,  API psd, python, przykład kodu]
url: pl/python-net/adjustment-layer-enhancement/
---

## **Przegląd**

W tym artykule będziemy badać edycję warstw dostosowania w Aspose.PSD dla Pythona. Warstwy dostosowania są potężną funkcją w edycji obrazów, która pozwala na dokonywanie zmian nieniszczących w zdjęciach. Aspose.PSD zapewnia kompleksowy zestaw klas warstw dostosowania, które można użyć do modyfikacji różnych aspektów obrazów.

Aby zademonstrować edycję warstw dostosowania, użyjemy fragmentu kodu przykładowego na końcu strony, który wczytuje obraz PSD i stosuje różne dostosowania do jego warstw.

W poniższym fragmencie kodu zaczynamy od wczytania obrazu PSD za pomocą metody PsdImage.load(). Następnie ustawiamy opcje zapisu plików PNG wynikowych. Klasa PngOptions pozwala nam określić typ koloru dla obrazu wyjściowego.

Następnie iterujemy przez każdą warstwę obrazu PSD i sprawdzamy jej typ, używając metody is_assignable(). Jeśli warstwa jest określonego typu, rzutujemy ją tego typu za pomocą metody cast() i stosujemy żądane dostosowanie. Na przykład, dostosowujemy jasność i kontrast za pomocą BrightnessContrastLayer, modyfikujemy poziomy za pomocą LevelsLayer, dodajemy punkt krzywej do CurvesLayer, itp.

Możesz dodać dodatkowy kod, aby stosować inne dostosowania do odpowiednich warstw. Aspose.PSD zapewnia szeroki zakres klas warstw dostosowania, takich jak [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) i inne.

Na koniec zapisujemy zmodyfikowany obraz za pomocą metody save() klasy PsdImage.

Ten kod dostarcza podstawowego przeglądu sposobu edycji warstw dostosowania w Aspose.PSD dla Pythona. Możesz dostosować dostosowania zgodnie z wymaganiami i zidentyfikować różne opcje dostępne w dokumentacji interfejsu API.

Sprawdź pełny przykład.

## **Przykład**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}

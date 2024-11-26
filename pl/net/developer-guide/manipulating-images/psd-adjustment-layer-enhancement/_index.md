---
title: Korzystanie z warstw dostosowania do ulepszeń PSD
weight: 100
type: docs
description: Przykłady korzystania z warstw dostosowania za pomocą Aspose.PSD dla C#
keywords: [warstwa dostosowania, ulepszanie zdjęć, dostosowanie krzywych, ulepszenie poziomów, odwrócenie, filtr zdjęć, psd api, C#, csharp, przykład kodu]
url: pl/net/warstwa-dostosowania-ulepszenie/
---

## Przegląd

W tym artykule będziemy eksplorować edycję warstw dostosowania w Aspose.PSD dla C#. Warstwy dostosowania są potężną funkcją w edycji obrazu, która pozwala na dokonywanie zmian nieniszczących w Twoich obrazach. Aspose.PSD zapewnia kompleksowy zestaw klas warstw dostosowania, które można użyć do modyfikowania różnych aspektów obrazów.

Aby zademonstrować edycję warstw dostosowania, skorzystamy z fragmentu kodu przykładowego, który znajduje się na końcu strony i wczytuje obraz PSD i stosuje różne dostosowania do jego warstw.

W poniższym fragmencie kodu zaczynamy od wczytania obrazu PSD za pomocą metody `PsdImage.Load()`. Następnie konfigurujemy opcje zapisywania plików wyjściowych PNG. Klasa `PngOptions` pozwala nam określić typ koloru dla obrazu wynikowego.

Następnie iterujemy przez każdą warstwę obrazu PSD i sprawdzamy jej typ za pomocą metody `IsAssignable()`. Jeśli warstwa jest określonego typu, rzutujemy ją na ten typ za pomocą metody `Cast()` i stosujemy pożądane dostosowanie. Na przykład dostosowujemy jasność i kontrast warstwy `BrightnessContrastLayer`, modyfikujemy poziomy warstwy `LevelsLayer`, dodajemy punkt krzywej do warstwy `CurvesLayer` itp.

Możesz dodać dodatkowy kod, aby zastosować inne dostosowania do ich odpowiednich warstw. Aspose.PSD zapewnia szeroki zakres klas warstw dostosowania, takich jak [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) i inne.

Na koniec zapisujemy zmodyfikowany obraz za pomocą metody `Save()` klasy `PsdImage`.

Ten kod zapewnia podstawowy przegląd edycji warstw dostosowania w Aspose.PSD dla C#. Możesz dostosować dostosowania zgodnie z Twoimi wymaganiami i badać różne opcje dostępne w dokumentacji interfejsu API.

## Przykład

Oto przykładowy kod demonstrujący sposób stosowania warstw dostosowania za pomocą Aspose.PSD dla C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Aby uzyskać bardziej szczegółowe informacje i przykłady, odwiedź [dokumentację Aspose.PSD dla C#](https://docs.aspose.com/psd/net/).


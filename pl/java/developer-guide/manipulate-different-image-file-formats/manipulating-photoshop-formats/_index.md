---
title: Manipulacja formatami Photoshopa
type: docs
weight: 10
url: /pl/java/manipulacja-formatami-photoshopa/
---

## **Zastępowanie kolorów w warstwach PSD**
Aspose.PSD for Java pozwala zmieniać kolor tła każdej warstwy pliku PSD. Proszę użyć klasy Aspose.PSD.FileFormats.Psd.Layers.BackgroundColor, aby zmienić kolor tła warstwy w warstwie PSD. Poniższy fragment kodu wczytuje plik PSD, uzyskuje dostęp do warstwy, aktualizuje kolor tła i zapisuje plik PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.java" >}}
## **Aktualizowanie warstwy tekstowej w pliku PSD**
Aspose.PSD for Java umożliwia manipulowanie tekstem w warstwie tekstowej pliku PSD. Proszę użyć klasy Aspose.PSD.FileFormats.Psd.Layers.TextLayer, aby zaktualizować tekst w warstwie PSD. Poniższy fragment kodu wczytuje plik PSD, uzyskuje dostęp do warstwy tekstowej, aktualizuje tekst i zapisuje plik PSD pod nową nazwą za pomocą metody Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.java" >}}
## **Wykrywanie spłaszczonego pliku PSD**
Aspose.PSD for Java pozwala sprawdzić, czy dany plik PSD jest spłaszczony czy nie. W klasie Aspose.PSD.FileFormats.Psd.PsdImage wprowadzono właściwość IsFlatten, aby osiągnąć tę funkcjonalność. Poniższy fragment kodu wczytuje plik PSD i uzyskuje dostęp do właściwości IsFlatten.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.java" >}}
## **Łączenie warstw PSD**
Ten artykuł pokazuje, jak łączyć warstwy w pliku PSD podczas konwertowania pliku PSD na JPG za pomocą Aspose.PSD. W poniższym przykładzie istniejący plik PSD jest wczytywany przez przekazanie ścieżki pliku do statycznej metody Load klasy Image. Gdy zostanie wczytany, konwertuj/rzutuj obraz na PsdImage. Utwórz instancję klasy JpegOptions i ustaw różne właściwości. Teraz wywołaj metodę Save instancji PsdImage. Poniższy fragment kodu pokazuje, jak łączyć warstwy PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-MergePSDLayers-MergePSDLayers.java" >}}
## **Wsparcie dla odcieni szarości z alfą dla PSD**
Ten artykuł pokazuje, jak wspierać odcienie szarości z alfą dla pliku PSD przy konwertowaniu pliku PSD na PNG za pomocą Aspose.PSD. W poniższym przykładzie, istniejący plik PSD jest wczytywany poprzez przekazanie ścieżki pliku do statycznej metody Load klasy Image. Gdy zostanie wczytany, konwertuj/rzutuj obraz na PsdImage. Utwórz instancję klasy PngOptions i ustaw jego różne właściwości. Ustaw właściwość ColorType na TruecolorWithAlpha. Teraz wywołaj metodę Save instancji PngOptions. Poniższy fragment kodu pokazuje, jak konwertować na odcienie szarości PNG z alfą.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.java" >}}
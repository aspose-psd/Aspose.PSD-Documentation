---
title: Warstwa dostosowania miksera kanałów
type: docs
weight: 30
url: /pl/java/layer-types/adjustment-layer/channel-mixer/
---

# Praca z warstwą dostosowania miksera kanałów w Photoshopie w języku Java

Dzisiaj zajmiemy się tym, jak programowo mieszać kolory kanałów w dokumentach Photoshopa za pomocą języka Java. Ponieważ edytor Photoshopa nie obsługuje skryptów Java, użyjemy specjalnej biblioteki do manipulacji formatem plików PSD o nazwie Aspose.PSD dla języka Java.

Biblioteka zawiera **API do pracy z kanałami kolorów**. Istnieje kilka sposobów mieszania kolorów, ale w tym artykule skupimy się na warstwie dostosowania miksera kanałów.

API warstwy dostosowania miksera kanałów **pozwala na manipulowanie kanałami kolorów** w celu uzyskania przyciemnionych obrazów, tworzenia różnych efektów kolorów lub nawet przekształcenia obrazu na czarno-biały. Następnie omówimy, jak zastosować warstwę dostosowania miksera kanałów do istniejącego dokumentu Photoshopa za pomocą Aspose.PSD dla języka Java, ale najpierw omówimy ogólne funkcje API.

## Przegląd API

Nie ma nic specjalnego w tworzeniu warstwy dostosowania miksera kanałów. Można ją dodać za pomocą [domyślnej metody fabrycznej](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--), która zwraca instancję klasy ChannelMixerLayer. Ta klasa zawiera ogólną funkcjonalność, taką jak opcja monochromatyczna i metoda pobierania kanału wyjściowego. Określony kanał wyjściowy może być jednym z dwóch typów: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) lub [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). Typ [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) zależy od [trybu kolorów](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) obrazu.

## Konwersja obrazu na monochromatyczny

Teraz rozważmy przykład zastosowania warstwy dostosowania miksera kanałów do istniejącego dokumentu Photoshopa. Ponieważ tego rodzaju warstwa dostosowania nie obsługuje jeszcze predefiniowanych ustawień, **odtworzymy predefiniowany zestaw funkcyjny Czarno-Biały podczerwony (RGB) Photoshopa** (a). Preset zostanie zastosowany do obrazu kwitnącego drzewa (b). W rezultacie chcemy uzyskać efekt fotografii podczerwonej (c).

![Przykład warstwy dostosowania miksera kanałów](channel-mixer-adjustment-psd-layer-figure-1.png) Aby odtworzyć predefiniowany zestaw funkcyjny Czarno-Biały podczerwony (RGB) Photoshopa, konieczne jest włączenie flagi monochromatycznej i ustawienie odpowiednich surowych wartości dla każdego koloru (czerwonego, zielonego i niebieskiego) dla kanału wyjściowego Szary:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome(**true**);
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed((**short**)-70);
    grayOutputChannel.setGreen((**short**)-200);
    grayOutputChannel.setBlue((**short**)-30);

Obraz musi być w trybie kolorów RGB, aby kod działał (ze względu na rzutowanie do klasy RgbMixerChannel). Tryb kolorów CMYK jest również obsługiwany, ale tylko dla obrazów z odpowiednim trybem kolorów.

Pamiętaj, że wartość każdego koloru oraz stała muszą znajdować się w zakresie od -200 do 200.

## Wnioski

W tym artykule omówiliśmy, jak pracować z API miksera kanałów Aspose.PSD dla języka Java, aby dostosować kolory w kanałach kolorów oraz konwertować obraz na czarno-biały.

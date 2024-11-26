---
title: Manipulacja Inteligentnymi Filtrami w Aspose.PSD dla Python
weight: 100
type: docs
description: Przykłady użycia Inteligentnych Filtrów w pliku PSD
keywords: [filtr inteligentny, dodaj szum, rozmycie gaussa, wyostrzanie, filtr, filtr PSD, interfejs API PSD, Python, przykład kodu]
url: pl/python-net/smart-filters/
---

## **Przegląd**

Istnieją 3 sposoby na zastosowanie inteligentnych filtrów w Aspose.PSD dla Pythona.

## **Bezpośrednie Stosowanie Filtrów**
W tym przykładowym kodzie możemy zobaczyć, jak bezpośrednio stosować inteligentne filtry w Aspose.PSD dla Pythona.

Najpierw kod określa plik źródłowy PSD, plik wyjściowy dla oryginalnego obrazu oraz plik wyjściowy dla zaktualizowanego obrazu.

Następnie kod wczytuje obraz PSD za pomocą metody Image.load() i rzutuje go na obiekt PsdImage.

Oryginalny obraz jest zapisywany za pomocą metody save(), z określoną nazwą pliku wyjściowego.

Tworzony jest obiekt SharpenSmartFilter, który reprezentuje zastosowany inteligentny filtr.

Kod następnie pobiera zwykłą warstwę z obrazu PSD za pomocą im.layers[1].

Pętla jest następnie używana do zastosowania filtru wyostrzającego do zwykłej warstwy trzy razy.

Na koniec zaktualizowany obraz jest zapisywany za pomocą metody save() i określoną nazwą pliku wyjściowego.

Ten kod demonstruje, jak bezpośrednio stosować inteligentne filtry w Aspose.PSD dla Pythona. Poprzez użycie odpowiednich obiektów filtrów i ich zastosowanie do pożądanych warstw, można osiągnąć pożądane efekty na obrazach.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentacja-Python-Aspose-psd-inteligentny-filtr-bezposrednie-stosowanie.py" >}}

## **Manipulacja Inteligentnymi Filtrami w Obiektach Inteligentnych**

Najpierw kod określa plik źródłowy PSD, plik wyjściowy dla oryginalnego obrazu oraz plik wyjściowy dla zaktualizowanego obrazu.

Obraz PSD jest wczytywany za pomocą metody Image.load(), a następnie rzutowany na obiekt PsdImage.

Oryginalny obraz jest zapisywany za pomocą metody save(), z określoną nazwą pliku wyjściowego.

Następnie kod rzutuje drugą warstwę obrazu PSD na obiekt SmartObjectLayer, reprezentujący warstwę obiektu inteligentnego.

Kod przejmuje następnie edytowanie inteligentnych filtrów. W tym przykładzie demonstruje, jak pracować z dwoma typami inteligentnych filtrów: GaussianBlurSmartFilter i AddNoiseSmartFilter.

Dla GaussianBlurSmartFilter kod aktualizuje wartości filtru, w tym promień, tryb mieszania, przezroczystość i to, czy jest włączony czy nie.

Dla AddNoiseSmartFilter kod ustawia rozkład szumu na NoiseDistribution.UNIFORM.

Następnie kod dodaje dwa nowe elementy filtrów do warstwy obiektu inteligentnego: kolejny GaussianBlurSmartFilter i AddNoiseSmartFilter.

Po dodaniu nowych filtrów, kod zastosowuje zmiany za pomocą metody update_resource_values().

Na koniec kod demonstruje, jak bezpośrednio stosować filtry do warstwy i do maski warstwy za pomocą metod apply() i apply_to_mask(), odpowiednio.

Zaktualizowany obraz jest zapisywany za pomocą metody save() i określoną nazwą pliku wyjściowego.

Korzystając z tego przykładowego kodu, można nauczyć się pracy z inteligentnymi filtrami w Aspose.PSD dla Pythona. Biblioteka dostarcza szeroki zakres inteligentnych filtrów, z własnym zestawem właściwości i metod, które można dostosować, aby osiągnąć pożądane efekty na obrazach.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentacja-Python-Aspose-psd-inteligentny-filtr-cechy.py" >}}

## **Stosowanie Inteligentnych Filtrów do Masek Warstw**

Stosowanie Inteligentnych Filtrów do Masek: Potężna Technika Edycji Obrazu

Inteligentne filtry są popularną funkcją w oprogramowaniu do edycji obrazów, która pozwala użytkownikom zastosować różne filtry i efekty do swoich obrazów. Jedną interesującą techniką, którą można osiągnąć za pomocą inteligentnych filtrów, jest ich zastosowanie do masek. W tym artykule będziemy badać, jak stosować inteligentne filtry do masek i omawiać ich użycie w świecie edycji obrazów.

Co to jest Maski? Zanim zagłębimy się w stosowanie inteligentnych filtrów do masek, najpierw zrozumiejmy, czym jest maska. W edycji obrazów maska to obraz o odcieniach szarości określający przejrzystość określonych obszarów obrazu. Maska może być użyta do selektywnego stosowania filtrów, korekt oraz efektów do określonych części obrazu, pozostawiając inne obszary niezmienione.

Stosowanie Inteligentnych Filtrów do Masek: Podczas stosowania inteligentnych filtrów do masek, filtry są stosowane tylko do obszarów określonych przez maskę. Pozwala to na precyzyjną kontrolę nad tymi obszarami obrazu, które są objęte filtrem. Poprzez manipulację maską można określić intensywność i zakres efektu filtru.

Proszę sprawdzić poprzedni przykład i metodę: [API Referencja Stosowanie Inteligentnego Filtra do Maski](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

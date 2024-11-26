---
title: Mądra manipulacja filtrami w Aspose.PSD dla C#
weight: 100
type: docs
description: Przykłady użycia Mądrych Filtrów w pliku PSD
keywords: [mądry filtr, dodawanie szumu, rozmycie gaussa, wyostrzanie, filtr, filtr PSD, interfejs PSD, C#, csharp, przykład kodu]
url: pl/net/smart-filters/
---

## Przegląd

Istnieją trzy sposoby na zastosowanie mądrych filtrów w Aspose.PSD dla C#.

### Bezpośrednie Zastosowanie Filtra

Ten przykład demonstruje, jak bezpośrednio stosować mądre filtry w Aspose.PSD dla C#.

Najpierw określ źródłowy plik PSD, plik wyjściowy dla oryginalnego obrazu oraz plik wyjściowy dla zaktualizowanego obrazu.

Następnie załaduj obraz PSD za pomocą metody `Image.Load` i przekształć go w obiekt `PsdImage`.

Zapisz oryginalny obraz za pomocą metody `Save` z określoną nazwą pliku wyjściowego.

Utwórz obiekt `SharpenSmartFilter`, reprezentujący mądry filtr, który ma być zastosowany.

Pobierz zwykłą warstwę z obrazu PSD za pomocą `psdImage.Layers[1]`.

Zastosuj filtr `sharpenFilter` do zwykłej warstwy trzy razy w pętli.

Na koniec zapisz zaktualizowany obraz za pomocą metody `Save` z określoną nazwą pliku wyjściowego.

Ten kod demonstruje, jak bezpośrednio stosować mądre filtry w Aspose.PSD dla C#. Przy użyciu odpowiednich obiektów filtrów i ich zastosowania do pożądanych warstw można osiągnąć pożądane efekty na obrazach.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Manipulowanie Mądrymi Filtrami w Mądrych Obiektach

Ten przykład pokazuje, jak manipulować mądrymi filtrami w mądrych obiektach.

Najpierw określ źródłowy plik PSD, plik wyjściowy dla oryginalnego obrazu oraz plik wyjściowy dla zaktualizowanego obrazu.

Załaduj obraz PSD za pomocą metody `Image.Load` i przekształć go w obiekt `PsdImage`.

Zapisz oryginalny obraz za pomocą metody `Save` z określoną nazwą pliku wyjściowego.

Przekształć drugą warstwę obrazu PSD w obiekt `SmartObjectLayer`.

Edytuj mądre filtry. Ten przykład demonstruje pracę z `GaussianBlurSmartFilter` oraz `AddNoiseSmartFilter`.

Dla `GaussianBlurSmartFilter` zaktualizuj wartości filtra, w tym promień, tryb mieszania, poziom przezroczystości oraz stan włączony.

Dla `AddNoiseSmartFilter` ustaw rozkład szumu na `NoiseDistribution.UNIFORM`.

Dodaj nowe elementy filtrów do warstwy mądrego obiektu: kolejny `GaussianBlurSmartFilter` oraz `AddNoiseSmartFilter`.

Zastosuj zmiany za pomocą metody `UpdateResourceValues`.

Zastosuj filtry bezpośrednio do warstwy oraz do maski warstwy za pomocą metod `Apply` i `ApplyToMask` odpowiednio.

Zapisz zaktualizowany obraz za pomocą metody `Save` z określoną nazwą pliku wyjściowego.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Stosowanie Mądrych Filtrów do Maski Warstwy

Mądre filtry są potężnym narzędziem do edycji obrazów, które pozwala użytkownikom stosować różne filtry i efekty. Jedną interesującą techniką jest ich stosowanie do masek, które pozwalają precyzyjnie kontrolować obszary, na które działa filtr.

Maska to obraz w odcieniach szarości określający przezroczystość określonych obszarów obrazu, selektywnie stosując filtry, korekty lub efekty.

Podczas stosowania mądrych filtrów do masek, filtry są stosowane tylko do obszarów określonych przez maskę. Ta precyzyjna kontrola pozwala manipulować intensywnością i zakresem filtrów.

Aby uzyskać bardziej szczegółowe informacje i przykłady, zapoznaj się z [dokumentacją Aspose.PSD dla C#](https://docs.aspose.com/psd/net/).

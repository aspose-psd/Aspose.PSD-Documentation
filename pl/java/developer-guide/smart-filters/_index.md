---
title: Manipulacja inteligentnym filtrem w Aspose.PSD dla Javy
weight: 100
type: docs
description: Przykłady użycia inteligentnych filtrów w plikach PSD
keywords: [inteligentny filtr, dodaj szum, rozmycie gaussowskie, wyostrzanie, filtr, filtr PSD, API PSD, java, przykład kodu]
url: pl/java/smart-filters/
---

## **Opis**

W Aspose.PSD dla Javy istnieją 3 metody stosowania inteligentnych filtrów.

## **Bezpośrednie Zastosowanie Filtra**

Ten przykładowy kod demonstruje, jak bezpośrednio zastosować inteligentne filtry w Aspose.PSD dla Javy.

W pierwszej kolejności kod definiuje plik źródłowy PSD, plik wyjściowy dla oryginalnego obrazu oraz plik wyjściowy dla zaktualizowanego obrazu.

Następnie kod wczytuje obraz PSD za pomocą metody Image.load() i rzutuje go na obiekt PsdImage.

Oryginalny obraz jest zapisywany za pomocą metody save(), podając nazwę pliku wyjściowego.

Tworzony jest obiekt SharpenSmartFilter, który reprezentuje pożądany inteligentny filtr.

Następnie kod pobiera zwykłą warstwę z obrazu PSD, używając psdImage.getLayers()[1].

Pętla jest wykorzystywana do trzykrotnego zastosowania filtru wyostrzania do zwykłej warstwy.

Ostatecznie zaktualizowany obraz jest zapisywany za pomocą metody save(), podając nazwę pliku wyjściowego.

Ten kod ilustruje bezpośrednie zastosowanie inteligentnych filtrów w Aspose.PSD dla Javy. Poprzez wykorzystanie odpowiednich obiektów filtrów i ich zastosowanie do pożądanych warstw, można osiągnąć pożądane efekty na obrazach.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentacja-Java-Aspose-psd-smart-filter-bezposrednie-zastosowanie.java" >}}

## **Manipulacja Inteligentnymi Filtrami w Obiektach Inteligentnych**

Ten fragment kodu przedstawia, jak manipulować inteligentnymi filtrami w obiektach inteligentnych w Aspose.PSD dla Javy.

Początkowo kod definiuje plik źródłowy PSD, plik wyjściowy dla oryginalnego obrazu oraz plik wyjściowy dla zaktualizowanego obrazu.

Obraz PSD jest wczytywany za pomocą metody Image.load(), a następnie rzutowany na obiekt PsdImage.

Oryginalny obraz jest zapisywany za pomocą metody save(), podając nazwę pliku wyjściowego.

Następnie kod rzutuje drugą warstwę obrazu PSD na obiekt SmartObjectLayer, reprezentujący warstwę obiektu inteligentnego.

Następnie, kod demonstruje edytowanie inteligentnych filtrów, pokazując dwa rodzaje: GaussianBlurSmartFilter i AddNoiseSmartFilter.

Dla GaussianBlurSmartFilter, kod aktualizuje wartości filtru takie jak promień, tryb mieszania, przezroczystość i stan aktywacji.

Dla AddNoiseSmartFilter, kod ustawia rozkład szumu na NoiseDistribution.Uniform.

Kolejno, kod dodaje dwa nowe elementy filtrów do warstwy obiektu inteligentnego: kolejny GaussianBlurSmartFilter oraz AddNoiseSmartFilter.

Po dodaniu nowych filtrów, kod stosuje zmiany za pomocą metody updateResourceValues().

Na koniec, kod demonstruje bezpośrednie zastosowanie filtrów do warstwy i jej maski za pomocą metod apply() i applyToMask() odpowiednio.

Następnie zaktualizowany obraz jest zapisywany za pomocą metody save(), podając nazwę pliku wyjściowego.

Korzystając z tego przykładowego kodu, można zrozumieć, jak manipulować inteligentnymi filtrami w obiektach inteligentnych w Aspose.PSD dla Javy. Biblioteka oferuje szeroki zakres inteligentnych filtrów, z własnym zestawem właściwości i metod, które można dostosować, aby osiągnąć pożądane efekty na obrazach.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentacja-Java-Aspose-psd-smart-filter-cechy.java" >}}

## **Stosowanie Inteligentnych Filtrów do Maski Warstwy**

Stosowanie Inteligentnych Filtrów do Masek: Potężna Technika Edycji Obrazu

Inteligentne filtry, powszechne w oprogramowaniu do edycji obrazu, umożliwiają użytkownikom zastosowanie różnorodnych filtrów i efektów do swoich obrazów. Jedną z fascynujących technik umożliwionych przez inteligentne filtry jest ich stosowanie do masek. Niniejszy artykuł przedstawia stosowanie inteligentnych filtrów do masek i omawia ich użyteczność w dziedzinie edycji obrazu.

Zrozumienie Masek: Zanim zagłębimy się w stosowanie inteligentnych filtrów do masek, kluczowe jest zrozumienie pojęcia maski. W edycji obrazu maska to obraz o odcieniach szarości, określający przejrzystość określonych obszarów w obrazie. Maska umożliwia selektywne stosowanie filtrów, korekt czy efektów do konkretnych części obrazu, pozostawiając inne nietknięte.

Stosowanie Inteligentnych Filtrów do Masek: Gdy inteligentne filtry są stosowane do masek, wpływają one tylko na obszary określone przez maskę, oferując precyzyjną kontrolę nad wpływem filtru. Poprzez manipulację maską użytkownicy mogą regulować intensywność i zakres efektu filtra.

Prosimy o odniesienie się do poprzedniego przykładu oraz metody: [API Reference Applying Smart Filter To Mask](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

---
title: Praca z maskami w Aspose.PSD dla С#
weight: 100
type: docs
description: Przykłady pracy z maskami obcinającymi, rastrowymi i wektorowymi w plikach PSD
keywords: [maski, maska warstwy, maska wektorowa, maska obcinająca, psd, psd api, C#, csharp, przykład kodu]
url: pl/net/update-create-layer-mask/
---

## Przegląd

W plikach PSD istnieją trzy rodzaje masek:
1. Maski obcinające
2. Maski rastrowe
3. Maski wektorowe

Ten artykuł obejmuje wszystkie trzy rodzaje.

### Maski obcinające

Maski obcinające są potężną funkcją w oprogramowaniu do grafiki i edycji obrazów, dzięki której można kontrolować widoczność jednej warstwy w oparciu o kształt i zawartość innej warstwy. W skrócie, maska obcinająca ogranicza widoczność warstwy do kształtu zdefiniowanego przez inną warstwę pod nią.

Aby utworzyć maskę obcinającą, potrzebujesz dwóch warstw: warstwy bazowej i warstwy obcinającej. Warstwa bazowa definiuje kształt lub obszar, który będzie widoczny, podczas gdy warstwa obcinająca zawiera treść, która będzie ograniczona do kształtu warstwy bazowej.

Gdy zastosujesz maskę obcinającą, zawartość warstwy obcinającej jest widoczna tylko w granicach warstwy bazowej. Wszelka zawartość poza granicami warstwy bazowej jest ukryta lub przycięta.

Maski obcinające są szczególnie przydatne do stosowania efektów, takich jak tekstury lub wzory, w określonych obszarach obrazu czy dzieła sztuki. Korzystając z maski obcinającej, możesz zapewnić, że efekt jest ograniczony do żądanego obszaru bez wpływu na resztę obrazu.

### Maski rastrowe

Maski rastrowe w plikach PSD są niezbędne do kontrolowania widoczności konkretnych obszarów w ramce. W przeciwieństwie do masek wektorowych, które używają kształtów matematycznych do definiowania obszarów zamaskowanych, maski rastrowe wykorzystują informacje oparte na pikselach do określenia, które części ramki są widoczne lub ukryte.

Maska rastrowa składa się z obrazu w odcieniach szarości, który jest stosowany do warstwy. Białe obszary maski reprezentują widoczne fragmenty, podczas gdy czarne obszary reprezentują ukryte fragmenty. Odcienie szarości między nimi tworzą częściową przezroczystość lub obszary częściowo widoczne.

Korzystając z masek rastrowych, można osiągnąć skomplikowane efekty maskowania, umożliwiając precyzyjną kontrolę widoczności warstwy na podstawie szczegółów na poziomie pikseli. Ta funkcja jest szczególnie przydatna w zadaniach wymagających szczegółowej edycji i łączenia w obrazie.

### Maski wektorowe

Maski wektorowe w plikach PSD są wszechstronnym narzędziem służącym do określania widoczności konkretnych obszarów w warstwie na podstawie kształtów matematycznych. W przeciwieństwie do masek rastrowych, które korzystają z informacji opartych na pikselach, maski wektorowe wykorzystują ścieżki i krzywe do tworzenia gładkich i skalowalnych obszarów zamaskowanych.

Maska wektorowa jest w gruncie rzeczy ścieżką zastosowaną do warstwy. Kształt ścieżki określa, które części warstwy są widoczne, a które są ukryte. Poprzez manipulowanie punktami kontrolnymi i krzywymi ścieżki można tworzyć precyzyjne i skomplikowane obszary maskowane.

Maski wektorowe są szczególnie przydatne do tworzenia czystych, skalowalnych masek, które można łatwo dostosowywać bez utraty jakości. Ta funkcja jest idealna do zadań wymagających dużej precyzji i elastyczności w definiowaniu obszarów widocznych w warstwie.

Aby uzyskać więcej informacji na temat dodawania masek wektorowych, odwiedź stronę [Maski wektorowe](psd/pl/layer-vector-mask/).

## Przykład
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PracaZMaskami-PracaZMaskami.cs" >}}

Aby uzyskać bardziej szczegółowe informacje i przykłady, odwiedź [dokumentację Aspose.PSD dla C#](https://docs.aspose.com/psd/net/).

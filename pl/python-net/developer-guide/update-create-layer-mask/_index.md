---
title: Praca z maskami w Aspose.PSD dla Pythona
weight: 100
type: docs
description: Przykłady pracy z maskami obcinania, rastrowymi i wektorowymi w plikach PSD
keywords: [maski, maska warstwy, maska wektorowa, maska obcinania, psd, api psd, python, przykład kodu]
url: /pl/python-net/update-create-layer-mask/
---

## **Przegląd**

**Przegląd**
	
	W plikach PSD istnieją 3 rodzaje masek:
	1. Maska obcinania
	2. Maska rastrowa
	3. Maska wektorowa
	
	Ten artykuł obejmuje wszystkie 3 rodzaje.


** Maska obcinania **

Maski obcinania są potężną funkcją w projektowaniu graficznym i oprogramowaniu do edycji obrazów. Pozwalają one kontrolować widoczność jednej warstwy na podstawie kształtu i zawartości innej warstwy. Innymi słowy, maska obcinająca ogranicza widoczność warstwy do kształtu innej warstwy pod nią.

Aby utworzyć maskę obcinania, potrzebujesz najpierw dwóch warstw: warstwy podstawowej i warstwy, którą chcesz obciąć. Warstwa podstawowa definiuje kształt lub obszar, który będzie widoczny, podczas gdy warstwa, którą chcesz obciąć, zawiera zawartość, która zostanie przycięta do kształtu warstwy podstawowej.

Podczas stosowania maski obcinającej, zawartość przyciętej warstwy jest widoczna tylko w granicach warstwy podstawowej. Zawartość poza granicami warstwy podstawowej będzie ukryta lub przycięta.

Maski obcinania są szczególnie przydatne, gdy chcesz zastosować efekt, takie jak tekstura lub wzór, do określonego obszaru obrazu lub dzieła sztuki. Korzystając z maski obcinającej, możesz ograniczyć efekt do pożądanego obszaru, nie wpływając na resztę obrazu.

Proszę sprawdzić przykład na końcu strony

** Maski rastrowe ** 

Maski rastrowe w plikach PSD są używane do kontrolowania widoczności określonych obszarów wewnątrz warstwy. W odróżnieniu od masek wektorowych, które wykorzystują kształty matematyczne do zdefiniowania obszarów maskowanych, maski rastrowe wykorzystują informacje oparte na pikselach, aby określić, które części warstwy są widoczne lub ukryte.

Maska rastrowa składa się z obrazu w odcieniach szarości, który jest stosowany do warstwy. Białe obszary maski reprezentują widoczne części, podczas gdy czarne obszary reprezentują ukryte części. Odcienie szarości pomiędzy nimi można wykorzystać do tworzenia częściowej transparentności lub półwidocznych obszarów.

Proszę sprawdzić przykład na końcu strony

** Maski wektorowe **

Maski wektorowe w plikach PSD są wszechstronnym narzędziem używanym do definiowania widoczności określonych obszarów w warstwie na podstawie kształtów matematycznych. W odróżnieniu od masek rastrowych, które wykorzystują informacje oparte na pikselach, maski wektorowe wykorzystują ścieżki i krzywe do tworzenia płynnych i skalowalnych obszarów maskowanych.

Maska wektorowa to w zasadzie ścieżka, która jest stosowana do warstwy. Kształt ścieżki określa, które części warstwy są widoczne, a które są ukryte. Manipulując punktami kontrolnymi i krzywymi ścieżki, można tworzyć precyzyjne i skomplikowane obszary maskowane.

Proszę sprawdzić [stronę o maskach wektorowych](psd/pl/net/layer-vector-mask/) w celu uzyskania informacji na temat dodawania masek wektorowych przy użyciu zasobów.


## **Przykład**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokumentacja-Python-Aspose-psd-update-create-layer-mask.py" >}}

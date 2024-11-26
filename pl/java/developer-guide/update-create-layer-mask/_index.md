---
title: Praca z maskami w Aspose.PSD dla Javy
weight: 100
type: docs
description: Przykłady pracy z maskami obcinania, rastrowymi i wektorowymi w pliku PSD
keywords: [maski, maska warstwy, maska wektorowa, maska obcinania, psd, psd api, java, przykład kodu]
url: pl/java/update-create-layer-mask/
---

## **Przegląd**

**Przegląd**
	
	W plikach PSD występują 3 rodzaje masek:
	1. Maski obcinania
	2. Maski rastrowe
	3. Maski wektorowe
	
	Ten artykuł obejmuje wszystkie 3 rodzaje.

**Maski Obcinania**

Maski obcinania są potężną funkcją w oprogramowaniu do grafiki i edycji obrazów, w szczególności w Javie. Pozwalają na precyzyjną kontrolę widoczności jednej warstwy na podstawie kształtu i zawartości innej warstwy. Zasadniczo maska obcinania ogranicza widoczność warstwy do kształtu innej warstwy znajdującej się poniżej.

Aby zaimplementować maskę obcinania w Javie, potrzebujesz najpierw dwóch warstw: warstwy bazowej i warstwy, którą chcesz obciąć. Warstwa bazowa definiuje kształt lub obszar, który ma pozostać widoczny, podczas gdy warstwa do obcięcia zawiera treść, która dostosuje się do kształtu warstwy bazowej.

Gdy maska obcinania jest stosowana w Javie, treść obciętej warstwy jest widoczna tylko w granicach warstwy bazowej. Każda zawartość poza tymi granicami będzie ukryta lub obcięta.

Maski obcinania są szczególnie przydatne podczas stosowania efektów, takich jak tekstury lub wzory, do konkretnych obszarów obrazu lub dzieła sztuki. Poprzez zastosowanie maski obcinania możesz ograniczyć efekt do pożądanego obszaru, nie wpływając na resztę obrazu.

Proszę odnieść się do przykładu na końcu strony w celu uzyskania jasności.

**Maski Rastrowe**

Maski rastrowe w plikach Javy służą do zarządzania widocznością konkretnych obszarów w warstwie. W przeciwieństwie do masek wektorowych, które wykorzystują kształty matematyczne do definiowania obszarów zakrytych, maski rastrowe polegają na informacjach opartych na pikselach do określenia obszarów widocznych lub ukrytych.

Maska rastrowa składa się z obrazu w odcieniach szarości zastosowanego do warstwy. Białe obszary maski oznaczają widoczność, podczas gdy czarne obszary reprezentują ukryte fragmenty. Odcienie szarości pomiędzy mogą stworzyć częściową przejrzystość lub obszary półprzezroczyste.

Proszę odnieść się do przykładu na końcu strony w celu lepszego zrozumienia.

**Maski Wektorowe**

Maski wektorowe w plikach Javy są wszechstronnymi narzędziami służącymi do określania widoczności konkretnych obszarów w warstwie na podstawie kształtów matematycznych. W przeciwieństwie do masek rastrowych, które zależą od danych opartych na pikselach, maski wektorowe wykorzystują ścieżki i krzywe do tworzenia płynnych i skalowalnych obszarów zakrytych.

Masek wektorowych składa się zasadniczo z ścieżki zastosowanej do warstwy. Kształt tej ścieżki określa, które części warstwy są widoczne, a które są ukryte. Poprzez manipulowanie punktami kontrolnymi i krzywymi ścieżki można tworzyć precyzyjne i złożone obszary zakryte.

Proszę odnieść się do strony [Maski Wektorowe](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) w celu uzyskania informacji na temat dodawania masek wektorowych przy użyciu zasobów.

## **Przykład**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentacja-Java-Aspose-psd-update-create-layer-mask.java" >}}

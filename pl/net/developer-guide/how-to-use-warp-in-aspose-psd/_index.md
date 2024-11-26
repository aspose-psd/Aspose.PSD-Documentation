---
title: Jak korzystać z funkcji Warp w Aspose.PSD
type: docs
weight: 40
url: /pl/net/jak-korzystac-z-funkcji-warp-w-aspose-psd/
---

## **Część 1 – Renderowanie pliku PSD z efektem Warp**

Photoshop zapisuje obraz renderowany po zastosowaniu efektu Warp. Nasza biblioteka może odtworzyć lub ponownie wyrenderować obraz z efektem Warp. Aby włączyć tę funkcję, po prostu ustaw flagę AllowWarpRepaint w ustawieniach podczas otwierania pliku PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentacja-Aspose-PSD-Warp-Rendering-1.cs" >}}

Wynik:
![Aspose.PSD dla .NET - Wynik funkcji Warp 1](warp1.png)

Oprócz renderowania efektu Warp dla SmartLayers, nasza biblioteka obsługuje również Warp dla TextLayers. Kod implementacji pozostaje identyczny, jedyna różnica polega na nazwie pliku.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentacja-Aspose-PSD-Warp-Rendering-2.cs" >}}

Wynik:
![Aspose.PSD dla .NET - Wynik funkcji Warp 2](warp2.png)

**! Uwaga: ** Aktualnie nasza biblioteka obsługuje renderowanie zarówno niestandardowego Warpu (gdzie użytkownicy manipulują punktami siatki) jak i wszystkie standardowe typy Warpów.
* - Aktualnie nasza biblioteka obsługuje niestandardowy Warp z standardową siatką i aktywnie pracujemy nad rozbudową naszego wsparcia, aby wkrótce obejmować wszystkie rodzaje siatek.


## **Część 2 – Modyfikowanie efektu Warp**

Nasza biblioteka pozwala nie tylko renderować, ale także modyfikować (dodawać) efekt Warp.
Modyfikacje te są ułatwione dzięki funkcjom klasy **WarpParams**.

| **Funkcja**  | **Opis**                                                         | 
|:-------------|:----------------------------------------------------------------------------|
| Ograniczenia       | Zwraca granice zniekształconego obrazu.                                     |
| Punkty siatki   | Tablica punktów, gdzie każdy punkt reprezentuje wierzchołek siatki zmian. |
| Wartość        | Wartość efektu Warp dla efektów niestandardowych.                   |
| Obrócone Warpy  | Wyliczenie definiujące kierunek efektów niestandardowych.           |
| Style Wapów   | Wyliczenie definiujące typ efektu Warp.                            |

Poniższy przykład kodu demonstruje, jak określić typ efektu Warp dla Smart Layer i dostosować typ oraz intensywność zniekształcenia efektu.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentacja-Aspose-PSD-Warp-Rendering-3.cs" >}}

Wynik:
![Aspose.PSD dla .NET - Wynik funkcji Warp 3](warp3.png)

## **Część 3 – Dodawanie efektu Warp**

Poniższy przykład kodu demonstruje, jak dodać standardowy efekt Warp do Smart Layer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentacja-Aspose-PSD-Warp-Rendering-4.cs" >}}

Wynik:
![Aspose.PSD dla .NET - Wynik funkcji Warp 4](warp4.png)

Poniższy przykład kodu demonstruje, jak dodać niestandardowy efekt Warp do Smart Layer.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentacja-Aspose-PSD-Warp-Rendering-5.cs" >}}

Wynik:
![Aspose.PSD dla .NET - Wynik funkcji Warp 5](warp5.png)

Poniższy przykład kodu demonstruje, jak dodać efekt Warp do Text Layer. 
**! Uwaga:** Zgodnie ze standardami Photoshopa, efekt Warp dla warstw tekstowych jest zwykle ograniczony do typu standardowego. Niemniej jednak nasza biblioteka obsługuje stosowanie dwóch typów efektów Warp. Należy pamiętać, że takie pliki mogą nie być w pełni kompatybilne z Photoshopem.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Dokumentacja-Aspose-PSD-Warp-Rendering-5.cs" >}}

Wynik:
![Aspose.PSD dla .NET - Wynik funkcji Warp 6](warp6.png)

Nieustannie doskonalimy i poszerzamy możliwości naszego efektu Warp, skupiając się na zwiększeniu jego prędkości, jakości i obsługiwanej funkcjonalności. Bądź na bieżąco z naszymi miesięcznymi wydaniami, aby być na bieżąco z najnowszymi rozwojami.
Twój zespół Aspose.PSD

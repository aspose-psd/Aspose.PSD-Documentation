---
title: Przykład użycia warstw grupowych w Aspose.PSD dla Pythona
weight: 100
type: docs
description: Użycie grupowej warstwy pliku PSD za pomocą Pythona
keywords: [grupowa warstwa, warstwa grupy, dodawanie warstwy do grupy, interfejs API PSD, python, przykład kodu]
url: pl/python-net/psd-group-layer/
---

## **Omówienie**

Praca z warstwami grupowymi w Aspose.PSD dla Pythona to potężna funkcja, która pozwala na organizowanie i manipulowanie warstwami w obrazie PSD. Warstwy grupowe, znane również jako warstwy folderów, umożliwiają grupowanie wielu warstw razem i stosowanie transformacji lub efektów do całej grupy.

W tym przykładzie najpierw tworzymy nowy obraz PSD za pomocą metody PsdImage.create. Następnie tworzymy nowy obiekt warstwy grupowej za pomocą metody add_layer_group obiektu PsdImage. Podajemy nazwę warstwy grupowej ("Folder"), indeks, na którym powinna zostać wstawiona (0) oraz flagę logiczną wskazującą, czy warstwa grupowa powinna być widoczna (True).

Następnie tworzymy dwa obiekty warstw i ustawiamy ich nazwy wyświetlane za pomocą właściwości display_name. Dodajemy te warstwy do warstwy grupowej za pomocą metody add_layer.

Na koniec, możemy uzyskać dostęp do warstw wewnątrz grupy za pomocą właściwości layers obiektu LayerGroup. W tym przykładzie sprawdzamy, czy nazwy wyświetlane pierwszej i drugiej warstwy w grupie to odpowiednio "Warstwa 1" i "Warstwa 2".

Po manipulowaniu warstwami grupowymi, możemy zapisać zmodyfikowany obraz PSD za pomocą metody save obiektu PsdImage.

To tylko podstawowy przykład, który pozwoli Ci rozpocząć pracę z warstwami grupowymi za pomocą Aspose.PSD dla Pythona. Biblioteka ta zapewnia wiele bardziej zaawansowanych funkcji do manipulowania i transformowania warstw w obrazach PSD. Możesz śledzić dokumentację Aspose.PSD dla Pythona, aby uzyskać więcej szczegółów i przykładów dotyczących pracy z warstwami grupowymi i innymi funkcjami biblioteki.

Aby pracować z warstwami grupowymi w Aspose.PSD dla Pythona, możesz użyć klasy LayerGroup. Oto przykładowy fragment kodu demonstrujący, jak utworzyć warstwę grupową, dodać do niej warstwy i zapisać zmodyfikowany obraz PSD.

Proszę sprawdzić pełny przykład.

## **Przykład**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}

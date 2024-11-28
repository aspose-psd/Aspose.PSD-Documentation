---
title: Przykład użycia warstw grupowych w Aspose.PSD dla Javy
weight: 100
type: docs
description: Użycie warstw grupowych pliku PSD za pomocą Javy
keywords: [warstwa grupowa, warstwa grupy, dodawanie warstwy do grupy, psd api, java, przykład kodu]
url: pl/java/psd-group-layer/
---

## **Omówienie**

Wykorzystywanie warstw grupowych w Aspose.PSD dla Javy zwiększa Twoją zdolność do efektywnego zarządzania i organizowania warstw w obrazie PSD. Warstwy grupowe, zwane również warstwami folderowymi, pozwalają na konsolidację wielu warstw i stosowanie transformacji lub efektów zbiorczo.

Aby rozpocząć, utwórz nowy obraz PSD za pomocą metody PsdImage.create(). Następnie zainicjalizuj nowy obiekt LayerGroup za pomocą metody addLayerGroup obiektu PsdImage. Podaj pożądaną nazwę dla warstwy grupowej ("Folder"), określ indeks wstawienia (0) i ustaw flagę logiczną wskazującą na jej widoczność (Prawda).

Następnie utwórz dwie obiekty warstw i ustaw ich nazwy wyświetlania za pomocą metody setDisplayName. Dodaj te warstwy do warstwy grupowej za pomocą metody addLayer.

Aby uzyskać dostęp do warstw w grupie, skorzystaj z właściwości layers obiektu LayerGroup. Potwierdź, że nazwy wyświetlania pierwszej i drugiej warstwy w grupie to odpowiednio "Warstwa 1" i "Warstwa 2".

Po manipulacji warstwami grupowymi, zapisz zmodyfikowany obraz PSD za pomocą metody save obiektu PsdImage.

Jest to podstawowy przykład pomagający Ci zapoznać się z pracą z warstwami grupowymi za pomocą Aspose.PSD dla Javy. Biblioteka oferuje mnóstwo zaawansowanych funkcji do manipulacji warstwami i transformacjami w obrazach PSD. Aby uzyskać dalsze szczegóły i przykłady dotyczące wykorzystywania warstw grupowych i innych funkcji biblioteki, zajrzyj do dokumentacji Aspose.PSD dla Javy.

Aby pracować z warstwami grupowymi w Aspose.PSD dla Javy, skorzystaj z klasy LayerGroup. Poniżej znajduje się fragment kodu ilustrujący, jak utworzyć warstwę grupową, dodać do niej warstwy i zapisać zmodyfikowany obraz PSD.

Zapoznaj się z pełnym przykładem dostarczonym poniżej.

## **Przykład**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}

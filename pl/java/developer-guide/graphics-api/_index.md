---
title: Korzystanie z interfejsu API grafiki do edycji warstw w plikach PSD
weight: 100
type: docs
description: Przykład korzystania z interfejsu API grafiki w Aspose.PSD dla Javy
keywords: [aktualizacja warstwy, rysowanie koła, rysowanie elipsy, rysowanie wypełnionego koła, grafika, api PSD, java, przykład kodu]
url: pl/java/graphics-api/
---

## **Przegląd**
Aby rozpocząć, załaduj plik PSD za pomocą metody Image.load() lub utwórz obraz PSD od podstaw. Użyj zmiennej inputFile do reprezentowania ścieżki do pliku PSD i określ ewentualne opcje wczytywania za pomocą loadOpt, jeśli jest to konieczne.

Następnie uzyskaj dostęp do pierwszej warstwy obrazu PSD, korzystając z składni psdImage.getLayers()[0], aby uzyskać odniesienie do obiektu warstwy do manipulacji.

Aby edytować warstwę, utwórz obiekt Graphics, przekazując warstwę jako parametr. Ten obiekt udostępnia różne metody do rysowania kształtów i stosowania pędzli.

Do zdefiniowania koloru i grubości obwódki kształtów używany jest obiekt Pen. Podobnie, pędzle jak LinearGradientBrush są używane do zdefiniowania kolorów wypełnienia.

Rysuj kształty na warstwie za pomocą metod takich jak graphics.drawEllipse(), aby zarysować kształty, i graphics.fillEllipse(), aby je wypełnić.

Po dokonaniu żądanych zmian w warstwie, zapisz zmodyfikowany obraz PSD za pomocą psdImage.save().

Dodatkowo, można zapisać zmodyfikowany obraz w innych formatach, takich jak PNG, korzystając z odpowiednich opcji.

To wszystko! Skorzystałeś pomyślnie z interfejsu API grafiki Aspose.PSD dla Javy do edycji warstw w pliku PSD. Odkrywaj więcej funkcji i możliwości biblioteki Aspose.PSD, aby zwiększyć możliwości edycji obrazów.

Sprawdź pełny przykład.

## **Przykład**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}

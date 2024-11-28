---
title: Aktualizacja warstwy wypełnienia PSD za pomocą Pythona
weight: 100
type: docs
description: Przykłady korzystania z wszystkich typów warstw korekcyjnych, w tym koloru wypełnienia, wypełnienia gradientem i wypełnienia wzorem
keywords: [warstwa wypełnienia, Kolor wypełnienia, Wypełnienie gradientem, Wypełnienie wzorem, interfejs API PSD, python, przykład kodu]
url: pl/python-net/psd-wytyczna-warstwy-edycji-wypelnienia/
---

## **Przegląd**

Aby utworzyć zwykłą warstwę, można użyć funkcji create_regular_layer dostarczonej w kodzie. Ta funkcja przyjmuje parametry left, top, width i height, aby zdefiniować położenie i rozmiar warstwy. Tworzy nową warstwę, ustawia jej granice i wypełnia ją określonym kolorem.

Aby utworzyć warstwę wypełnienia kolorem, można użyć metody FillLayer.create_instance z parametrem FillType.COLOR. Po utworzeniu warstwy wypełnienia można uzyskać dostęp do jej ustawień wypełnienia, korzystając z własności fill_settings i ustawić kolor, korzystając z własności color klasy ColorFillSettings. W dostarczonym kodzie kolor jest ustawiony na Color.coral. Właściwość clipping warstwy wypełnienia jest ustawiona na 1, co sprawia, że warstwa działa jako maska obcinająca.

Aby utworzyć warstwę wypełnienia gradientem, można użyć metody FillLayer.create_instance z parametrem FillType.GRADIENT. Podobnie jak w przypadku warstwy wypełnienia kolorem, można uzyskać dostęp do ustawień wypełnienia, korzystając z własności fill_settings i ustawić punkty kolorów gradientu oraz punkty przezroczystości. W dostarczonym kodzie punkty kolorów gradientu są zdefiniowane przy użyciu klasy GradientColorPoint, a punkty przezroczystości są zdefiniowane przy użyciu klasy GradientTransparencyPoint. Właściwość clipping warstwy wypełnienia również jest ustawiona na 1.

Aby utworzyć warstwę wypełnienia wzorem, można użyć metody FillLayer.create_instance z parametrem FillType.PATTERN. Ponownie można uzyskać dostęp do ustawień wypełnienia, korzystając z własności fill_settings i ustawić dane wzoru oraz inne właściwości. W dostarczonym kodzie dane wzoru są zdefiniowane przy użyciu klasy PatternFillSettings, a właściwość clipping jest ustawiona na 1.

Po utworzeniu warstw wypełnienia można dodać je do obrazu PSD, korzystając z metody add_layer. Można również określić nazwę wyświetlania i inne właściwości dla każdej warstwy wypełnienia.

Wreszcie można zapisać obraz PSD i odpowiadający mu obraz PNG, korzystając z dostarczonego kodu. Opcje PNG są ustawione na używanie truecolor z alfą dla przejrzystości.

Proszę sprawdzić pełny przykład.

## **Przykład**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-fill-layer-editing.py" >}}

---
title: Aktualizacja warstwy wypełnienia PSD za pomocą Javy
weight: 100
type: docs
description: Przykłady wykorzystania wszystkich rodzajów warstw korekcyjnych, w tym Wypełnienie kolorem, Wypełnienie gradientem i Wypełnienie wzorem
keywords: [warstwa wypełnienia, Wypełnienie kolorem, Wypełnienie gradientem, Wypełnienie wzorem, api psd, java, przykład kodu]
url: pl/java/psd-fill-layer-editing/
---

## **Przegląd**

Utworzenie zwykłej warstwy polega na użyciu funkcji createRegularLayer, która wymaga parametrów do zdefiniowania pozycji i rozmiaru warstwy. Ta funkcja tworzy nową warstwę, ustawia jej granice i wypełnia ją określonym kolorem.

Dla warstwy wypełnienia kolorem wykorzystujesz metodę FillLayer.createInstance z parametrem FillType.Color. Po utworzeniu warstwy wypełnienia uzyskaj dostęp do jej ustawień wypełnienia za pomocą właściwości fill_settings i ustaw pożądany kolor za pomocą właściwości kolor klasy ColorFillSettings. W tym kontekście kolor jest ustawiony na Color.getCoral(). Dodatkowo właściwość clipping warstwy wypełnienia jest ustawiona na 1, co powoduje, że działa ona jako maska do przycinania.

Warstwy wypełnienia gradientem są tworzone w podobny sposób za pomocą metody FillLayer.create_instance, ale z parametrem FillType.Gradient. Tak jak w przypadku warstw wypełnienia kolorem, uzyskujesz dostęp do ustawień wypełnienia poprzez fill_settings i ustawiasz punkty kolorów gradientu oraz punkty przejrzystości. W tym przykładzie punkty kolorów gradientu są definiowane za pomocą klasy GradientColorPoint, a punkty przejrzystości za pomocą klasy GradientTransparencyPoint. Właściwość clipping warstwy wypełnienia jest również ustawiona na 1. 

Warstwy wypełnienia wzorem są tworzone za pomocą FillLayer.createInstance z parametrem FillType.Pattern. Ponownie uzyskaj dostęp do ustawień wypełnienia poprzez fill_settings i ustaw dane wzoru oraz inne właściwości. W tym kodzie dane wzoru są zdefiniowane za pomocą klasy PatternFillSettings, a właściwość clipping jest ustawiona na 1.

Gdy utworzysz warstwy wypełnienia, dodaj je do obrazu PSD za pomocą metody addLayer, określając nazwę wyświetlaną i inne właściwości dla każdej warstwy wypełnienia.

Na koniec zapisz obraz PSD wraz z odpowiadającym mu obrazem PNG za pomocą dostarczonego kodu. Opcje PNG są skonfigurowane do użycia prawdziwego koloru z alfą dla przejrzystości.

Zachęcam do zapoznania się z pełnym przykładem dla większych szczegółów.

## **Przykład**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokumentacja-Java-Aspose-psd-fill-layer-editing.java" >}}

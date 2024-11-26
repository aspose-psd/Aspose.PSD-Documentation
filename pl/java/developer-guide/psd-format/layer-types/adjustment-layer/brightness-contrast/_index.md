---
title: Warstwa regulacji jasności i kontrastu
type: docs
weight: 30
url: /pl/java/rodzaje-warstw/warstwa-regulacji/jasnosc-kontrast/
---

# Praca z warstwą regulacji jasności/kontrastu w Photoshopie w języku Java

W tym artykule zastosujemy regulację jasności/kontrastu do dokumentu Adobe® Photoshop® za pomocą biblioteki Aspose.PSD dla Javy®. Ponadto dowiemy się więcej o funkcjach biblioteki związanych z tego rodzaju warstwą regulacji.

Ale najpierw trochę teorii.

Warstwa regulacji jasności/kontrastu zmienia jasność i kontrast obrazu. Ale zanim przejdziemy dalej, co to tak naprawdę oznacza? Zwiększenie jasności rozjaśni wartość koloru aż do białego, natomiast zmniejszenie jasności zaciemni wartość koloru aż do czarnego. Z kolei zwiększenie kontrastu zwiększy różnicę między jasnymi i ciemnymi kolorami, a zmniejszenie kontrastu odpowiednio zmniejszy tę różnicę; oznacza to, że jasne kolory stają się jaśniejsze, a ciemne kolory stają się ciemniejsze.

## Obsługa trybu kolorów

Biblioteka pozwala dodawać warstwę regulacji jasności/kontrastu do obrazów w trybie kolorów RGB, CMYK lub Lab.

## Obecne i klasyczne zachowanie

Obecna implementacja biblioteki (v20.6 w chwili pisania) używa domyślnego algorytmu Photoshopa, który zachowuje pełny zakres tonalny od cieni po światła, ale jeszcze nie obsługuje klasycznego zachowania. Oznacza to, że biblioteka obsługuje warstwę regulacji jasności/kontrastu w dokumentach stworzonych w najnowszych wersjach Photoshopa (CS4 i nowsze). Jednakże, jeśli potrzebujesz, możesz [poprosić o klasyczną implementację warstwy regulacji jasności/kontrastu](https://forum.aspose.com/c/psd) na naszym forum.

## Regulacja jasności i kontrastu

Teraz opiszmy, jak działa interfejs API warstwy regulacji jasności/kontrastu na wysokim poziomie (w związku z tym, API jest jasne). Klasa PsdImage zawiera metodę fabryczną (addBrightnessContrastAdjustmentLayer) do tworzenia instancji klasy BrightnessContrastLayer, która stanowi bramę do regulacji jasności i kontrastu. Klasa BrightnessContrastLayer zawiera tylko parę metod getterów i setterów do dostępu do właściwości jasności i kontrastu oraz zmiany ich wartości.

![|Przykład warstwy regulacji jasności/kontrastu w PSD](jasnosc-kontrast-przyklad-warstwy-1.png)

Zastosujmy teraz regulację jasności i kontrastu obrazu psa, na przykład, aby dostosować jego jasność1 i kontrast2 (a), korzystając tylko z metody fabrycznej z odpowiednimi argumentami, aby ostatecznie uzyskać obraz (c), który wygląda bardziej wyrazisty:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Uwagi:

1. Wartość jasności musi zawierać się w zakresie od -150 do 150.
2. Wartość kontrastu musi zawierać się w zakresie od -50 do 100.

Zajrzyj do dokumentacji [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) po więcej szczegółów.

## Podsumowanie

W tym artykule poznaliśmy szybki przegląd warstwy regulacji jasności/kontrastu oraz nauczyliśmy się, jak regulować jasność i kontrast obrazu za pomocą metody fabrycznej.

Zajrzyj do naszej serii [artykułów na temat interfejsów API warstw regulacji](/pl/psd/java/rodzaje-warstw/warstwa-regulacji/) Aspose.PSD dla Javy, aby dowiedzieć się więcej.

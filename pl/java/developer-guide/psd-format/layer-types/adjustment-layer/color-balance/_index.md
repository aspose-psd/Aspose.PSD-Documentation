---
title: Warstwa Korygowania Balansu Kolorów
type: docs
weight: 30
url: /pl/java/layer-types/adjustment-layer/color-balance/
---

# Praca z warstwą korygowania balansu kolorów w Photoshopie w języku Java

W tym artykule zajmiemy się **dostosowaniem balansu kolorów obrazu** w formacie pliku PSD w języku Java. Będziemy korzystać ze specjalnej biblioteki o nazwie Aspose.PSD for Java, która jest narzędziem do manipulowania dokumentami Photoshopa.

Ponieważ biblioteka działa z formatem pliku PSD, zawiera praktycznie [wszystkie funkcje](https://docs.aspose.com/psd/java/features/) dostępne w edytorze Photoshopa, a **warstwa korygowania balansu kolorów** nie jest wyjątkiem.

Warstwa korygowania balansu kolorów umożliwia zmianę balansu między kolorami podstawowymi (RGB) i subtraktywnymi (CMY) dla cieni, pośrednich tonów i świateł w prosty i szybki sposób.

## Dostosowanie Balansu Kolorów

Jak wspomniano wcześniej, warstwa korygowania balansu kolorów w Aspose.PSD for Java to po prostu **balanser między kolorami podstawowymi i subtraktywnymi**. Oznacza to, że istnieją trzy skale dla każdej pary kolorów (cyjan/czerwień, magenta/zielony, żółty/niebieski). Intensywność konkretnego koloru w parze zwiększy się, jeśli wartość będzie się zbliżać do niego, i na odwrót. Ponadto te trzy pary są właściwe dla każdego obszaru zakresu tonalnego (cienie, pośrednie tony i światła), co zwiększa elastyczność tego rodzaju dostosowania.

Więc zastosujmy tę wiedzę w praktyce. Na przykład wybierzmy czerwonawy zdjęcie twarzy kobiety (b). Twarz jest tak czerwonawa, że mamy zamiar to naprawić, dodając **warstwę korygowania balansu kolorów** w celu zmniejszenia czerwieni i zwiększenia cyjanu w zasadzie (a), aby uzyskać bardziej naturalny wygląd twarzy (c). Ponownie, jest wiele pracy do wykonania z tym obrazem, ale w ramach tego artykułu to wszystko, co zrobimy.

![Przykład warstwy korygowania balansu kolorów](color-balance-adjustment-layer-example-figure-1.png) API warstwy korygowania balansu kolorów ma płaski design. Dlatego [klasa ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) jest wszystkim, czego potrzebujesz. Po pierwsze, zachowaj luminancję, ponieważ jest ona domyślnie wyłączona. Następnie dodaj trochę zieleni i więcej żółci dla cieni, używając odpowiednich metod (których nazwy składają się z nazwy konkretnego obszaru zakresu tonalnego oraz nazw kolorów w parze koloru), następnie dodaj więcej cyjanu i nieco niebieskiego dla pośrednich tonów, a na koniec dodaj więcej cyjanu oprócz trochę magenty i niebieskiego:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Teraz mamy zdjęcie, którego chcieliśmy! To jest takie proste, prawda?

Zwróć uwagę, że _wartość każdej pary kolorów musi być w zakresie od -100 do 100_, tj. wartości ujemne dla kolorów subtraktywnych i dodatnie dla kolorów podstawowych, tak jak w edytorze Photoshopa.

Zajrzyj do naszego odnośnika API, aby dowiedzieć się więcej technicznych szczegółów na temat [warstwy korygowania balansu kolorów](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Podsumowanie

W tym artykule omówiliśmy, jak dostosować balans kolorów obrazu programistycznie w języku Java, korzystając z biblioteki Aspose.PSD for Java. Biblioteka zawiera w pełni funkcjonalne API do pracy z warstwami korygowania balansu kolorów w dokumentach Photoshopa.

---
title: Konwertowanie PSD między różnymi trybami kolorystycznymi
type: docs
weight: 50
url: /pl/net/psd-convert-between-different-color-modes/
---

Możesz dowiedzieć się, które tryby kolorystyczne obsługuje Aspose.PSD z tego artykułu.

Aspose.PSD obsługuje konwersję na przykład z 8 na 16 bitów na piksel i odwrotnie. Konwersje profili ICC CMYK oraz inne konwersje z jednego rodzaju głębokości bitowej na drugą. Tutaj można zobaczyć przykłady konwersji na odcienie szarości w plikach PSD.
## Konwertuj z trybu kolorystycznego CMYK, RGB, odcienie szarości do trybu kolorystycznego Grayscale
Poniższy przykładowy kod demonstruje, jak dokonać konwersji CMYK, RGB lub odcieni szarości bez użycia Photoshopa.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## Obraz 16-bitowy z Photoshopa w trybie odcieni szarości 8-bitowych
Co jednak, jeśli potrzebujesz przekonwertować obraz odcieni szarości 16-bitowy z Photoshopa na tryb odcieni szarości 8-bitowy? Musisz użyć poniższego fragmentu kodu. 8 bitów to powszechna głębia bitowa w plikach PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## Konwertuj z odcieni szarości na RGB
Innym złożonym przypadkiem jest konieczność przekonwertowania obrazu PSD odcieni szarości na obraz RGB.

Obrazy odcieni szarości mają tylko jeden kanał, ale obrazy RGB mają 3 kanały: R - czerwony, G - zielony, B - niebieski. Aspose.PSD może przekonwertować odcienie szarości na RGB.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}

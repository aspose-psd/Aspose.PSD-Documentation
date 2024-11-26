---
title: Notatki wydania Aspose.PSD dla Javy 19.4
type: docs
weight: 20
url: /pl/java/aspose-psd-dla-java-19-4-notatki-o-wydaniu/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dla Aspose.PSD dla Javy 19.4

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDJAVA-1|Umożliwia funkcję wczytywania plików obrazów JPEG/PNG/etc do PsdImage bez bezpośredniego wczytywania (co nie jest obsługiwane w Aspose.PSD)|Funkcja|
|PSDJAVA-2|Wsparcie dla trybu koloru RGB z 16 bitami/ kanał (64 bity na kolor)|Funkcja|
|PSDJAVA-3|Wsparcie dla warstwowych masek wektorowych i dostosowanych operacji FlipRotate warstw tekstowych|Funkcja|
|PSDJAVA-4|Wszystkie azjatyckie znaki nie są renderowane poprawnie|Błąd|
|PSDJAVA-5|Symbole \r\n są interpretowane jako podwójne znaki nowej linii, co jest nieprawidłowe|Błąd|
|PSDJAVA-6|Jeśli warstwa tekstowa jest aktualizowana za pomocą łańcucha zawierającego końce linii, to plik PSD staje się nieczytelny|Błąd|
|PSDJAVA-7|Jeśli warstwa tekstowa jest aktualizowana za pomocą łańcucha zawierającego symbole tabulacji, przetwarzanie kończy się wyjątkiem|Błąd|
# **Zmiany w API publicznym**
# **Dodane API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **Usunięte API:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
...
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceNonTransparentColors(System.Int32)
- T:Aspose.PSD.FileFormats.Tiff.TiffImage
- ...
# **Przykłady użycia:**

**PSDJAVA-1. Umożliwia funkcję wczytywania plików obrazów JPEG/PNG/etc do PsdImage bez bezpośredniego wczytywania (co nie jest obsługiwane w Aspose.PSD)**

{{< highlight java >}}

Kod przykładu...

{{< /highlight >}}

**PSDJAVA-2. Wsparcie dla trybu koloru RGB z 16 bitami/ kanał (64 bity na kolor)**

{{< highlight java >}}

Kod przykładu...

{{< /highlight >}}

**PSDJAVA-3. Wsparcie dla warstwowych masek wektorowych i dostosowanych operacji FlipRotate warstw tekstowych**

{{< highlight java >}}

Kod przykładu...

{{< /highlight >}}

**PSDJAVA-4. Wszystkie azjatyckie znaki nie są renderowane poprawnie**

[**Sprawdź załączony przykład**](attachments/92602686/92766213.java)

**PSDJAVA-5. Symbole \r\n są interpretowane jako podwójne znaki nowej linii, co jest nieprawidłowe**

{{< highlight java >}}

Kod przykładu...

{{< /highlight >}}

**PSDJAVA-6. Jeśli warstwa tekstowa jest aktualizowana za pomocą łańcucha zawierającego końce linii, to plik PSD staje się nieczytelny**

{{< highlight java >}}

Kod przykładu...

{{< /highlight >}}

**PSDJAVA-7. Jeśli warstwa tekstowa jest aktualizowana za pomocą łańcucha zawierającego symbole tabulacji, przetwarzanie kończy się wyjątkiem**

{{< highlight java >}}

Kod przykładu...

{{< /highlight >}}
---
title: Praca z warstwami tekstowymi
type: docs
weight: 170
url: /pl/praca-z-warstwami-tekstowymi/
---

## **Dodaj warstwę tekstową**
Aspose.PSD dla .NET pozwala na dodawanie warstw tekstowych w pliku PSD. Kroki do dodania warstwy tekstowej w pliku PSD są proste, jak poniżej:

- Wczytaj plik PSD jako obraz za pomocą metody fabrycznej [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) udostępnionej przez klasę [Obraz](https://reference.aspose.com/psd/net/aspose.psd/image)
- Wywołaj metodę [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer), która przyjmuje tekst i instancję klasy [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- Zapisz wyniki

Poniższy fragment kodu pokazuje, jak dodać warstwę tekstową w pliku PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Przykłady-CSharp-Aspose-ModyfikowanieIkonwersjaObrazów-PSD-DodajWarstwęTekstową-DodajWarstwęTekstową.cs" >}}

## **Ustaw pozycję warstwy tekstowej**
Aspose.PSD dla .NET pozwala na ustalenie pozycji warstwy tekstowej w pliku PSD. Etapy ustawienia pozycji warstwy tekstowej w pliku PSD są proste, jak poniżej:

- Wczytaj plik PSD jako obraz za pomocą metody fabrycznej Load udostępnionej przez klasę Obraz
- Wywołaj metodę AddTextLayer ze wskazaniem pozycji lewej i górnej warstwy tekstowej
- Zapisz wyniki

Poniższy fragment kodu pokazuje, jak ustawić pozycję warstwy tekstowej w pliku PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Przykłady-CSharp-Aspose-ModyfikowanieIkonwersjaObrazów-PSD-UstawPozycjęWarstwyTekstowej-UstawPozycjęWarstwyTekstowej.cs" >}}

## **Pobierz właściwości tekstu z warstwy tekstowej**
Korzystając z Aspose.PSD dla .NET, można pobrać i zaktualizować właściwości tekstu różnych części tekstu dostępnych w warstwie tekstowej PSD. Ten artykuł demonstruje, jak pobrać paragrafy, style i właściwości tekstu z warstwy tekstowej i zaktualizować je.

Poniższy fragment kodu pokazuje, jak wykonać to wymaganie.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Przykłady-CSharp-Aspose-ModyfikowanieIkonwersjaObrazów-PSD-PobierzWłaściwościTekstuZWarstwyTekstowej-PobierzWłaściwościTekstuZWarstwyTekstowej.cs" >}}

Oto kolejny przykład, który demonstruje, jak programista może uzyskać formatowanie tekstu różnych fragmentów tekstu z [WarstwyTekstu](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer) za pomocą [Aspose.PSD dla .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Przykłady-CSharp-Aspose-ModyfikowanieIkonwersjaObrazów-PSD-UzyskajWłaściwościFormatowaniaTekstuZWarstwyTekstowej-UzyskajWłaściwościFormatowaniaTekstuZWarstwyTekstowej.cs" >}}

## **Zaktualizuj warstwę tekstową w pliku PSD**
Aspose.PSD dla .NET pozwala na manipulowanie tekstem w warstwie tekstowej pliku PSD. Proszę użyj klasy Aspose.PSD.FileFormats.Psd.Layers.TextLayer do zaktualizowania tekstu w warstwie PSD. Poniższy fragment kodu wczytuje plik PSD, uzyskuje dostęp do warstwy tekstowej, aktualizuje tekst i zapisuje plik PSD pod nową nazwą za pomocą metody [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer/methods/updatetext/index).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Przykłady-CSharp-Aspose-ModyfikowanieIkonwersjaObrazów-PSD-ZaktualizujWarstwęTekstowąWPlikuPSD-ZaktualizujWarstwęTekstowąWPlikuPSD.cs" >}}

## **Wsparcie dla warstw tekstowych w trakcie wykonywania**
Ten artykuł pokazuje, jak dodać warstwy tekstowe w trakcie wykonywania dla obrazów PSD. Poniżej podano fragment kodu.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Przykłady-CSharp-Aspose-RysowanieIFormatowanieObrazów-DodajEfektWTrakcieWykonywania-DodajEfektWTrakcieWykonywania.cs" >}}

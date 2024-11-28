---
title: Przegląd formatu PSD
type: docs
weight: 60
url: /pl/net/psd-format-overview/
---

## **Opis**
PSD, Dokument Photoshop, reprezentuje natywny format pliku używany do projektowania grafiki i rozwoju w programie Adobe Photoshop.
## **Specyfikacja formatu pliku**
Dane w pliku PSD są przechowywane w kolejności bajtów big-endian. Oznacza to zamianę krótkich i długich liczb podczas odczytywania lub zapisywania na platformie Windows. Format pliku Photoshop jest podzielony na pięć głównych części. Posiada wiele znaczników długości, które mogą być używane do przechodzenia z jednej sekcji do drugiej. Znaczniki długości są zazwyczaj uzupełniane bajtami, aby zaokrąglić do najbliższej wielokrotności 2 lub 4 bajtów. Pięć głównych części to:

- Nagłówek pliku
- Dane trybu kolorów
- Zasoby obrazów
- Informacje o warstwach i maskach
- Dane obrazu

Dla zgodności dane powinny być zapisane we wszystkich tych polach w sekcji, ponieważ Photoshop może próbować odczytać całą sekcję. Oznacza to również, że zera powinny być zapisywane w pominiętych polach podczas zapisywania do pliku. Pole długości w sekcjach z długością ograniczoną powinno być używane do określenia momentu zakończenia odczytywania. W większości przypadków pole długości wskazuje liczbę bajtów, a nie rekordów, które następują. Poniższe punkty należy pamiętać podczas odczytywania pliku.

- Wartości w kolumnie "Długość" we wszystkich tabelach są podane w bajtach.
- Wszystkie wartości zdefiniowane jako ciągi znaków Unicode składają się z:
- 4-bajtowego pola długości reprezentującego liczbę znaków w ciągu znaków (nie bajtów).
- Ciągu wartości Unicode, dwa bajty na znak.
## **Funkcje formatu**
Pliki PSD mogą zawierać warstwy obrazu, warstwy korekty, maski warstw, adnotacje, informacje o pliku, słowa kluczowe i inne elementy specyficzne dla Photoshopa. Pliki Photoshop mają domyślne rozszerzenie.PSD i mają maksymalną wysokość i szerokość 30 000 pikseli oraz ograniczenie długości dwóch gigabajtów.
## **Jak może być używany**
1. Narzędzie do krojenia PSD.
1. [Konwersja PSD](/psd/pl/net/konwertowanie-obrazu-psd-na-format-rastrowy/) na HTML
1. Korzystanie z [PSD jako szablonu](/psd/pl/net/używanie-plików-psd-jako-szablonów-do-aktywności-kart-biznesowych/) do celów e-mailowych.
1. PSD do HTML w określonym CMS.
1. Podobizna w pliku PSD (Rysunek policyjny).
1. Tworzenie obrazów podglądowych w pseudo-3D za pomocą obiektów inteligentnych dla takich produktów jak butelki, kubki, koszulki, itp.
1. Szybka edycja PSD: Autoton, Presety, Obiekt inteligentny, Wycięcie obrazu z warstwy tekstowej.

I wiele więcej. Jeśli stworzyłeś coś wspaniałego za pomocą Aspose.PSD, podziel się z nami swoim studium przypadku korzystając z [Forum Aspose](https://forum.aspose.com/).


Dodatkowe przykłady możesz znaleźć tutaj:

- [Studia przypadków](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Prezentacje](/psd/pl/net/pokazy-html/)

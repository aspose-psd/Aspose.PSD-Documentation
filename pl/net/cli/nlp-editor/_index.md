---
title: Aplikacja Aspose.PSD CLI NLP Editor dla .NET
type: docs
weight: 10
url: /pl/net/cli/nlp-editor/
is_root: false
keywords: CLI Narzędzie Photoshop NLP Natural-Language-Processing PSD Konsola Biblioteka C# API PSD
description: Aplikacja Aspose.PSD CLI NLP Editor oparta na Aspose.PSD dla formatów plików PSD, PSB i AI. Automatyzacja CI/CD bez kodu. Obsługuje przetwarzanie języka naturalnego do edycji plików PSD. Wystarczy napisać żądanie w języku naturalnym, aby wykonać różne operacje takie jak konwersja, dostosowanie, zmiana rozmiaru i inne. Nie wymaga instalacji programu Adobe Photoshop ani Adobe Illustrator, może być uruchamiany z konsoli bez dodatkowego kodu.
---

**![Logo Produktu Aspose.PSD dla .NET](home_1.png)**

**Witaj w aplikacji Aspose.PSD NLP Editor CLI dla .NET**

Aplikacja Aspose.PSD CLI NLP Editor to lekka narzędzie konsolowe do edycji plików PSD za pomocą poleceń w języku naturalnym. Łatwa integracja z potokami CI/CD.

**Oświadczenie**

Jest to aplikacja eksperymentalna. Prosimy wypróbować ją i zostawić opinię. Każda opinia jest bardzo ceniona. Chcemy podnieść aplikację bez kodu do następnego poziomu. Naszym celem jest łatwa integracja z dowolnym cyklem kompilacji lub procesem biznesowym.

**Główne funkcje aplikacji Aspose.PSD NLP Editor CLI dla .NET**

1. Wykonywanie operacji na plikach PSD, PSB, AI za pomocą poleceń w języku naturalnym.
2. Obsługuje różne operacje, takie jak konwersja, dostosowanie, zmiana rozmiaru i inne.
3. Automatyzacja CI/CD bez użycia kodu.
4. Obsługuje pisanie żądań w języku naturalnym do edycji plików PSD.

## **Użycie z wiersza poleceń:**

{{% alert color="primary" %}}
Najpierw zainstaluj to narzędzie dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Zalecamy uruchomić następujące polecenie przed pierwszym użyciem:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Po tym poleceniu będziesz mógł uruchomić tę aplikację pod krótką nazwą nlp.cli zamiast Aspose.PSD.CLI.NLP.Editor. Możesz określić własną krótką nazwę.
{{% /alert %}}

**Dostępne parametry dla Aplikacji Aspose.PSD.CLI.Crop**

| **Argument** | **Opis**                         |
|:-------------|:----------------------------------------|
| dowolny tekst     | Wymagane. Twoje polecenie w języku naturalnym do aktualizacji pliku PSD lub PSB      |
| licencja      | Ścieżka do licencji.                    |
| verbose      | Wyświetla więcej informacji na temat określonego polecenia. |
| setup        | Tworzy plik bat w folderze narzędzi dla szybkiego wywołania z konsoli. Przykład: --setup psd.nlp. Następnie możesz wywołać narzędzie poleceniem psd.nlp |


**Przykłady użycia**

1. To polecenie przekonwertuje pierwszy znaleziony plik (który można otworzyć za pomocą aspose.psd) z bieżącego folderu i zapisze go w formacie png z przezroczystością. Dodatkowo ustawiona zostanie licencja. Licencję należy określić tylko raz. W kolejnych uruchomieniach licencja zostanie użyta z określonej ścieżki. To polecenie pokaże szczegółowe dzienniki przetwarzania NLP, jeśli są dostępne.
{{< highlight bash >}}
  nlp.cli Konwertuj plik z tego folderu do formatu png z alfą --license "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. To polecenie znajdzie plik o najbardziej podobnej nazwie do "smth.psd". Następnie dostosuje kontrast i zapisze go w formacie jpeg z najlepszą jakością. Nazwa pliku wyjściowego zostanie wyświetlona. Będzie to smth.jpg
{{< highlight bash >}}
Dostosuj kontrast na 10 warstwie o nazwie elipsa w pliku smth.psd i zapisz jako output.jpg z najlepszą jakością
{{< /highlight >}}

3. To polecenie zwinie plik na określonej ścieżce i zmniejszy jego rozmiar o 25%. Nazwa pliku wyjściowego zostanie wyświetlona. Zostanie on zapisany w aktualnym folderze konsoli.
{{< highlight bash >}}
Zmniejsz rozmiar pliku C:\Users\someuser\Desktop\input.psd o 25%
{{< /highlight >}}

4. To polecenie znajdzie plik input.psd w C:\Users\someuser\Desktop\. Następnie znajdzie warstwę o indeksie 3 i zmniejszy ją do szerokości 50px i wysokości 100px. Następnie ta warstwa zostanie zapisana jako PDF w C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
Zmniejsz warstwę o indeksie 3 z pliku C:\Users\someuser\Desktop\input.psd do szerokości 50 i wysokości 100 i zapisz ją w C:\Users\someuser\Desktop\output.pdf
{{< /highlight >}}

5. To polecenie otworzy plik smth.psd w bieżącym folderze, ale wszystkie efekty zostaną wyłączone. Następnie ten plik zostanie przekonwertowany do formatu BMP i zapisany jako output.bmp w bieżącym folderze.
{{< highlight bash >}}
Otwórz smth.psd bez efektów i zapisz go jako output.bmp
{{< /highlight >}}

**Sprawdź inne [aplikacje Aspose.PSD CLI](https://docs.aspose.com/psd/net/cli) dla .NET, jeśli potrzebujesz dodatkowego wsparcia dla formatów PSD, PSB i AI w swoim procesie pracy**

1. [Aspose.PSD CLI Konwersja](/psd/pl/net/cli/convert)
2. [Aspose.PSD CLI Kadrowanie](/psd/pl/net/cli/crop)
3. [Aspose.PSD CLI Zmiana Rozmiaru](/psd/pl/net/cli/resize)
4. [Aspose.PSD CLI Eksport](/psd/pl/net/cli/export)
5. [Aspose.PSD CLI NLP Editor](/psd/pl/net/cli/nlp-editor)

**Sprawdź Aspose.PSD dla .NET lub [inne platformy]**

Aplikacje Aspose.PSD CLI to gotowe do użycia rozwiązanie dla popularnych operacji. Jeśli potrzebujesz elastycznego rozwiązania, sprawdź pełną wersję Aspose.PSD

1. [Aspose.PSD dla .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD dla Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD dla Python via .NET](https://releases.aspose.com/psd/python-net/)

## **Zasoby Aspose.PSD dla .NET**

Poniżej znajdziesz linki do przydatnych zasobów, które mogą być potrzebne do wykonania zadań.

- [Aspose.PSD CLI Aplikacje dla .NET Dokumentacja Online](/psd/pl/net/cli/conversion)
- [Aspose.PSD dla CLI Aplikacji dla .NET Notatki o Wersji](/psd/pl/net/cli/conversion/release-notes/)
- [Aspose.PSD dla CLI Aplikacji .NET Strona Produktu](https://products.aspose.com/psd/net/cli)
- [Aspose.PSD dla .NET Przewodnik po Interfejsie API](https://reference.aspose.com/net/psd)
- [Pobierz Przykłady z Repozytorium GitHub](https://github.com/aspose-psd/CLI-Applications)
- [Aspose.PSD dla .NET Darmowe Forum Pomocy Technicznej](https://forum.aspose.com/c/psd)
- [Aspose.PSD dla .NET Płatne Centrum Pomocy Technicznej](https://helpdesk.aspose.com/)

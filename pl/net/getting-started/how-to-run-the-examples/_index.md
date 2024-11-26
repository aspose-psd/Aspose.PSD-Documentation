---
title: Jak uruchomić przykłady
type: docs
weight: 90
url: /pl/net/jak-uruchomic-przyklady/
description: Dowiedz się, jak uruchomić przykłady dotyczące biblioteki formatu pliku PSD hostowanej na GitHubie.
---

## **Wymagania sprzętowe**
Upewnij się, że spełniasz poniższe wymagania przed pobraniem i uruchomieniem przykładów.

1. Visual Studio 2010 lub nowsza wersja
1. Zainstalowany menedżer pakietów NuGet w programie Visual Studio. Upewnij się, że jest zainstalowana najnowsza wersja interfejsu API NuGet w programie Visual Studio. Aby uzyskać szczegółowe informacje na temat instalacji menedżera pakietów NuGet, sprawdź [http://docs.nuget.org/ndocs/guides/install-nuget](http://docs.nuget.org/ndocs/guides/install-nuget)
1. Przejdź do Narzędzia->Opcje->Menedżer pakietów NuGet->Źródła pakietów i upewnij się, że opcja **nuget.org** jest zaznaczona
1. Przykładowy projekt korzysta z funkcji automatycznego przywracania pakietów NuGet, dlatego wymagane jest aktywne połączenie internetowe. Jeśli nie masz aktywnego połączenia internetowego na maszynie, na której mają zostać wykonane przykłady, sprawdź [Instalacja](/psd/pl/net/installation/), aby dodać odwołanie do pliku Aspose.Imaging.dll do projektu przykładu.
## **Pobierz z GitHuba**
Wszystkie przykłady Aspose.PSD dla .NET są hostowane na [GitHubie](https://github.com/aspose-psd/Aspose.PSD-for-.NET).

- Możesz albo sklonować repozytorium za pomocą ulubionego klienta GitHub, albo pobrać plik ZIP stąd [tutaj](https://github.com/aspose-psd/Aspose.PSD-for-.NET/archive/master.zip).
- Rozpakuj zawartość pliku ZIP do dowolnego folderu na swoim komputerze. Wszystkie przykłady znajdują się w folderze **Przykłady**.
- Istnieje plik rozwiązania Visual Studio dla C#.
- Projekty są stworzone w Visual Studio 2013, ale pliki rozwiązania są kompatybilne z Visual Studio 2010 SP1 i nowszymi wersjami.
- Otwórz plik rozwiązania w programie Visual Studio i zbuduj projekt.
- Podczas pierwszego uruchomienia zależności zostaną automatycznie pobrane za pośrednictwem NuGet.
- Folder **Dane** w głównym folderze **Przykłady** zawiera pliki wejściowe, których używają przykłady w języku CSharp. Konieczne jest pobranie folderu **Dane** wraz z projektem przykładów.
- Otwórz plik RunExamples.cs, wszystkie przykłady są wywoływane stamtąd.
- Odkomentuj przykłady, które chcesz uruchomić w ramach projektu.

Jeśli masz jakiekolwiek problemy z konfiguracją lub uruchamianiem przykładów, prosimy o kontakt przez nasze Forum.
## **Współtwórz**
Jeśli chcesz dodać lub ulepszyć przykład, zachęcamy do współtworzenia projektu. Wszystkie przykłady i projekty w przewodniku dostępnym w tym repozytorium są otwartym oprogramowaniem i mogą być swobodnie wykorzystywane w twoich własnych aplikacjach.

Aby przyczynić się do projektu, możesz rozebrać repozytorium, edytować kod źródłowy i utworzyć żądanie pull request. Przejrzymy zmiany i włączymy je do repozytorium, jeśli zostaną uznane za pomocne.

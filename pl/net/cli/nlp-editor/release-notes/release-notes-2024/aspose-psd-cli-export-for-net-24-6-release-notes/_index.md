---
title: Wersja 24.6 - Notatki Wydania Aspose.PSD CLI NLP Edytor dla .NET
type: docs
weight: 90
url: /pl/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD CLI NLP Edytor dla .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **Klucz**   | **Podsumowanie**                                                                           | **Kategoria** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Pierwsze Wydanie Aplikacji Aspose.PSD CLI: Aspose.PSD.CLI.Export i Aspose.PSD.CLI.NLP.Editor |  Usprawnienie |


## **Przykłady Użycia:**

**PSDNET-2110. Pierwsze wydanie Aplikacji Edytora NLP Aspose.PSD CLI**

## **Użycie z linii poleceń:**

{{% alert color="primary" %}}
Najpierw zainstaluj ten narzędzie dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

Przed pierwszym użyciem zalecamy wywołanie następującego polecenia:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
Po tym poleceniu możliwe będzie uruchomienie tej aplikacji za pomocą krótkiej nazwy nlp.cli zamiast Aspose.PSD.CLI.NLP.Editor. Możesz także określić własną krótką nazwę.
{{% /alert %}}

**Przykłady użycia**

1. To polecenie przekonwertuje pierwszy znaleziony plik (który można otworzyć przez aspose.psd) z bieżącego folderu i zapisze go w formacie png z przezroczystością. Dodatkowo, licencja zostanie skonfigurowana. Licencję musisz określić tylko raz. W kolejnych uruchomieniach licencja będzie pobierana z określonej ścieżki. To polecenie pokaże szczegółowy dziennik przetwarzania NLP, jeśli jest dostępny. 
{{< highlight bash >}}nlp.cli Konwertuj plik z tego folderu do formatu png z alfą --licencja "C:\Aspose\PlikLicencji.lic --szczegółowy "{{< /highlight >}}

2. To polecenie znajdzie plik o najbardziej podobnej nazwie do "smth.psd". Następnie dostosuje kontrast i zapisze go w formacie jpeg z najlepszą jakością. Nazwa pliku wyjściowego zostanie wyświetlona. Będzie to smth.jpg 
{{< highlight bash >}}Dopasuj kontrast dla warstwy 10 o nazwie elipsa w pliku smth.psd i zapisz go do output.jpg z najlepszą jakością{{< /highlight >}}

3. To polecenie zwinie plik na określonej ścieżce i zmniejszy jego rozmiar o 25%. Nazwa pliku wyjściowego zostanie wyświetlona. Zostanie on zapisany w bieżącym folderze konsoli.
{{< highlight bash >}}Zmień rozmiar pliku C:\Użytkownicy\nazwa_użytkownika\Pulpit\wejście.psd na 25%{{< /highlight >}}

4. To polecenie znajdzie plik wejściowy.psd w C:\Użytkownicy\nazwa_użytkownika\Pulpit\. Następnie znajdzie warstwę o indeksie 3 i zmieni jej rozmiar na szerokość 50px i wysokość 100px. Następnie ta warstwa będzie zapisana jako PDF w C:\Użytkownicy\nazwa_użytkownika\Pulpit\wyjście.pdf
{{< highlight bash >}}Zmień rozmiar warstwy o indeksie 3 z pliku wejściowego.psd w C:\Użytkownicy\nazwa_użytkownika\Pulpit\ na szerokość 50 i wysokość 100 i zapisz jako C:\Użytkownicy\nazwa_użytkownika\Pulpit\wyjście.pdf{{< /highlight >}}

 5. To polecenie otworzy plik smth.psd w bieżącym folderze, ale wszystkie efekty zostaną wyłączone. Następnie ten plik zostanie przekonwertowany do formatu BMP i zapisany jako output.bmp w bieżącym folderze.
 {{< highlight bash >}}Otwórz smth.psd bez efektów i zapisz go jako output.bmp{{< /highlight >}}

**Ostrzeżenie**

To jest aplikacja eksperymentalna. Proszę spróbować jej i zostawić opinie. Każda opinia jest bardzo mile widziana. Naszym celem jest doprowadzenie aplikacji NO-Code na wyższy poziom. Łatwa integracja z dowolnym potokiem budowania lub procesem biznesowym jest naszym celem.

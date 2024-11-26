---
title: Licencjonowanie
type: docs
weight: 70
url: /pl/net/licencjonowanie/
description: Oceń bibliotekę PSD Photoshop C# z NuGet i zastosuj licencję za pomocą pliku lub strumienia, aby usunąć wszelkie ograniczenia z zainstalowanej wersji ewaluacyjnej.
---

## **Ograniczenia w wersji ewaluacyjnej**
Możesz pobrać wersję ewaluacyjną Aspose.PSD dla .NET z [NuGet](https://www.nuget.org/packages/Aspose.psd/). Wersja ewaluacyjna oferuje te same funkcje co w pełni licencjonowana wersja komponentu, ale z kilkoma ograniczeniami. Po zakupie Aspose.PSD, zastosowanie licencji usuwa wszelkie ograniczenia z zainstalowanej wersji ewaluacyjnej. Wersja ewaluacyjna Aspose.PSD dla .NET zapewnia pełną funkcjonalność produktu, ale ma tylko dwa ograniczenia:

- **Znak wodny na każdym obrazie**: Każdy zapisany, zmodyfikowany lub wyeksportowany obraz ma znak wodny z napisem "Evaluation Only. Created with Aspose.PSD. Copyright 2010-2018 Aspose Pty Ltd.". Małe obrazy, na których nie mieści się pełny znak wodny, mają zamiast tego dwa ukośne linie na obrazie.
- **Brak obsługi podstawowej funkcjonalności rysowania**: W trybie ewaluacji piksele obrazów nie mogą być wczytywane lub zapisywane na obrazie. Aby rysować obrazy, należy zamiast tego używać zaawansowanej funkcjonalności rysowania. To ograniczenie dotyczy funkcji zależnych od podstawowej funkcjonalności rysowania. Aspose.PSD dla .NET pozwala zarejestrować własny format pliku. Jednak ta funkcja zależy od podstawowej funkcjonalności rysowania, więc nie ma sensu korzystać z niej w trybie ewaluacji, ponieważ nie można zmieniać zawartości tych plików.

Jeśli chcesz przetestować Aspose.PSD dla .NET bez ograniczeń ewaluacyjnych, poproś o tymczasową licencję na 30 dni. Aby uzyskać więcej informacji, zapoznaj się z [Jak uzyskać tymczasową licencję?](https://purchase.aspose.com/temporary-license).
## **O pliku licencyjnym**
Po zakończeniu oceny Aspose.PSD możesz zakupić licencję na stronie [Aspose](https://purchase.aspose.com/default.aspx). Zapoznaj się z różnymi rodzajami subskrypcji oferowanymi. Jeśli masz jakiekolwiek pytania, nie wahaj się skontaktować z [zespołem sprzedaży Aspose](https://company.aspose.com/contact). Każda licencja Aspose zawiera jednoroczną subskrypcję na aktualizacje oprogramowania. Po pierwszym roku odnów swoje subskrypcje, aby nadal uzyskiwać najnowsze funkcje i poprawki. Wsparcie techniczne jest bezpłatne i nieograniczone, i jest udzielane zarówno licencjonowanym, jak i użytkownikom w trybie ewaluacyjnym poprzez nasze [Fora Wsparcia](https://forum.aspose.com/). Licencja to plik XML zawierający takie informacje, jak nazwa produktu, liczba licencjonowanych programistów, data wygaśnięcia subskrypcji i inne. Plik jest cyfrowo podpisany, więc nie modyfikuj go: nawet nieumyślne dodanie dodatkowego przejścia do nowej linii unieważnia plik. Po zakupie Aspose.PSD musisz zastosować licencję przed utworzeniem, edycją lub manipulacją obrazami. Jeśli zapomnisz zastosować licencję, wszystkie obrazy będą miały znak wodny ewaluacji. Licencję należy ustawić tylko raz na aplikację lub proces, który opracowujesz.
## **Gdzie zastosować licencję w aplikacji**
Miejsce zastosowania licencji zależy od rodzaju aplikacji, którą opracowujesz. Postępuj zgodnie z tymi prostymi zasadami:

- Zastosuj licencję tylko raz na domenę aplikacji. Wielokrotne wywoływanie License.SetLicense nie jest szkodliwe, ale marnuje czas procesora.
- Zastosuj licencję przed wywołaniem jakichkolwiek klas Aspose.PSD dla .NET.
- **Aplikacje Windows Forms lub konsolowe**: Wywołaj License.SetLicense w kodzie startowym, przed użyciem jakichkolwiek klas Aspose.PSD dla .NET.
- **Aplikacji ASP.NET**: Wywołaj License.SetLicense z pliku Global.asax.cs (Global.asax.vb) w chronionej metodzie Application_Start. W ten sposób jest wywoływane raz, gdy aplikacja się uruchamia. Nie wywołuj License.SetLicense w metodach Page_Load, w przeciwnym razie licencja jest ładowna za każdym razem, gdy jest ładowana strona internetowa.
- **Aplikacje Silverlight**: Wywołaj License.SetLicense zdarzenie Application_Startup w pliku App.xaml.cs (App.xaml.vb).
- **Biblioteka klas**: Wywołaj License.SetLicense z konstruktora statycznego klasy korzystającej z Aspose.PSD. Konstruktor statyczny wykonuje się przed utworzeniem instancji klasy, zapewniając prawidłowe ustawienie licencji Aspose.PSD.
## **Zastosowanie licencji**
Możesz łatwo pobrać wersję ewaluacyjną Aspose.PSD z NuGet [strona pobierania] (https://www.nuget.org/packages/Aspose.psd/). Wersja ewaluacyjna zapewnia dokładnie takie same możliwości jak licencjonowana wersja Aspose.PSD. Ponadto, wersja ewaluacyjna staje się licencjonowana po zakupieniu licencji i dodaniu kilku linii kodu do zastosowania licencji.
### **Użycie pliku lub strumienia**
Jeśli chcesz uniknąć pracy z ograniczeniami wersji ewaluacyjnej, musisz ustawić licencję przed użyciem Aspose.PSD. Licencję należy ustawić tylko raz na aplikację (lub proces).
### **Zastosowanie licencji z pliku**
Najprostszym sposobem zastosowania licencji jest umieszczenie pliku licencji w tym samym folderze co Aspose.PSD.dll. Następnie możesz określić nazwę pliku w kodzie zamiast pełnej ścieżki.



{{< highlight java >}}

// Utwórz instancję licencji i zastosuj licencję za pomocą pełnej ścieżki

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}



Podczas wywoływania metody SetLicense, nazwa licencji powinna być taka sama jak nazwa pliku licencji. Na przykład, jeśli zmienisz nazwę pliku licencji na "Aspose.PSD.lic.xml", powinieneś użyć tej nazwy licencji dla metody SetLicense.
### **Zastosowanie licencji za pomocą strumienia**
Możliwe jest również wczytanie licencji ze strumienia, jak pokazano poniżej.



{{< highlight java >}}



// Utwórz instancję licencji i zastosuj licencję za pomocą strumienia

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);

{{< /highlight >}}
### **Sprawdzanie statusu licencji**
Klasa Aspose.PSD.License ma właściwość IsLicensed, która zwróci true, jeśli licencja została prawidłowo ustawiona.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Licencja jest ustawiona!");

}

{{< /highlight >}}
### **Użycie zasobu osadzonego**
Praktycznym sposobem pakowania licencji wraz z aplikacją i zapewnieniem, że nie zostanie ona utracona, jest dołączenie jej jako zasobu osadzonego do jednej z zestawów, które korzystają z Aspose.PSD. Aby dołączyć plik licencji jako zasób osadzony:

1. W programie Visual Studio .NET kliknij menu **Plik** i wybierz **Dodaj istniejący element**.
1. Dołącz plik licencji (rozszerzenie .lic) do projektu.
1. Wybierz plik w Eksploratorze rozwiązań.
1. W oknie Właściwości ustaw **Działanie kompilacji** na **Zasób osadzony**.

Nie trzeba wywoływać metod System.Reflection.Assembly's GetExecutingAssembly lub GetManifestResourceStream w ramach Microsoft .NET Framework do dostępu do osadzonej licencji. Zamiast tego wbuduj plik jako zasób w projekcie, a następnie przekaż nazwę pliku licencji do metody SetLicense. Klasa License automatycznie odnajduje plik licencji w osadzonych zasobach. Poniżej pokazano przykład, jak dołączyć licencję jako zasób osadzony i zastosować ją w aplikacji.



{{< highlight java >}}

// Utwórz instancję klasy License

Aspose.PSD.License license = new Aspose.PSD.License();

// Przekaż nazwę pliku z osadzoną licencją

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **Sprawdzanie statusu licencji**
Klasa Aspose.PSD.License ma właściwość IsLicensed, która zwróci true, jeśli licencja została prawidłowo ustawiona.



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("Licencja jest ustawiona!");

}

{{< /highlight >}}

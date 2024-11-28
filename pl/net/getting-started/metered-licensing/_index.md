---
title: Licencjonowanie według zużycia
type: docs
weight: 80
url: /pl/net/licencjonowanie-wedlug-zuzycia/
description: Biblioteka PSD Photoshop C# Aspose umożliwia deweloperom zastosowanie klucza licencyjnego według zużycia, który jest nowym mechanizmem licencyjnym i będzie używany razem z istniejącą metodą licencjonowania.
---

{{% alert color="primary" %}}

Aspose.PSD umożliwia deweloperom zastosowanie klucza licencyjnego według zużycia. Jest to nowy mechanizm licencyjny. Nowy mechanizm licencyjny będzie używany razem z istniejącą metodą licencjonowania. Klienci, którzy chcą być naliczani na podstawie użycia funkcji API, mogą korzystać z licencjonowania według zużycia. Aby uzyskać więcej informacji, zapoznaj się z sekcją [FAQ dotyczącą Licencjonowania według zużycia](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}
## **Licencjonowanie według zużycia**
Oto proste kroki w celu użycia klasy Metered.

1. Utwórz instancję klasy Metered.
1. Przekaż klucze publiczny i prywatny do metody `setMeteredKey`.
1. Wykonaj przetwarzanie (wykonaj zadanie).
1. Wywołaj metodę `getConsumptionQuantity` z klasy Metered.
1. Zwróci ona ilość/zużycie żądań API zrealizowanych do tej pory.

Poniżej znajduje się przykładowy kod demonstrujący ustawienie publicznego i prywatnego klucza według zużycia.

{{< highlight java >}}

 // Utwórz instancję klasy Metered z PSD

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Uzyskaj dostęp do właściwości setMeteredKey i przekaż klucze publiczny i prywatny jako parametry

metered.SetMeteredKey("*****", "*****");



// Pobierz ilość danych według zużycia przed wywołaniem API

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// Wyświetl informacje

Console.WriteLine("Ilość zużyta przed: " + amountbefore.ToString());

// Pobierz ilość danych według zużycia po wywołaniu API

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// Wyświetl informacje

Console.WriteLine("Ilość zużyta po: " + amountafter.ToString());

{{< /highlight >}}

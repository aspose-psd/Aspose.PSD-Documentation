---
title: Licencjonowanie z pomiarem zużycia
type: docs
weight: 70
url: /pl/java/licencjonowanie-z-pomiar-metra/
---

{{% alert color="primary" %}} 

Aspose.PSD pozwala programistom stosować klucz z pomiarem zużycia. Jest to nowy mechanizm licencyjny. Nowy mechanizm licencyjny będzie używany równolegle z istniejącą metodą licencjonowania. Klienci, którzy chcą być rozliczani na podstawie korzystania z funkcji interfejsu API, mogą skorzystać z licencjonowania z pomiarem zużycia. Aby uzyskać więcej szczegółów, zapoznaj się z sekcją [Najczęściej zadawane pytania dotyczące Licencjonowania z Pomiarem Zużycia](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}} 

## **Licencjonowanie z pomiarem zużycia**
Oto proste kroki do użycia klasy Metered.

1. Utwórz instancję klasy Metered.
1. Przekaż klucze publiczny i prywatny do metody setMeteredKey.
1. Wykonuj przetwarzanie (wykonywane zadanie).
1. Wywołaj metodę getConsumptionQuantity klasy Metered.
1. Zwróci ona ilość/ilość żądań interfejsu API, które do tej pory zostały zużyte.

Poniżej znajduje się przykładowy kod demonstrujący, jak ustawić publiczny i prywatny klucz metra.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}

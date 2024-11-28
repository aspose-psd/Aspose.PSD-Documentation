---
title: Znane problemy
type: docs
weight: 40
url: /pl/net/known-issues/
---

## **.NET Compact Framework**
- Obserwuje się, że na niektórych określonych wersjach systemu Windows, takich jak Windows Mobile 5.0-6.0, zestawy Compact Framework podpisane certyfikatem (lub podwójnie podpisanym certyfikatem) nie działają zgodnie z oczekiwaniami i nie są w stanie poprawnie się załadować (występuje wyjątek TypeLoadException). Aby rozwiązać ten problem, użytkownik musi usunąć wszystkie certyfikaty, a następnie użyć zaktualizowanego zestawu. Należy pamiętać, że podjęcie tego działania odbywa się na własne ryzyko, a nie gwarantujemy poprawnego działania w związku ze zmianą zestawu. Nie wysyłamy zestawów bez podpisu, ponieważ stanowiłoby to potencjalne zagrożenie dla bezpieczeństwa. Zamiast tego klienci powinni unikać korzystania z tak starych systemów operacyjnych, jeśli to możliwe, i/lub aktualizować system operacyjny do nowszych wersji lub paczek serwisowych, które rozwiązują problem podpisywania certyfikatów.

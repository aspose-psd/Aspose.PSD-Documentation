---
title: Poprawa Wydajności Aspose.PSD przy Użyciu Dostosowanego Cache'a
type: docs
weight: 30
url: /pl/java/aspose-psd-poprawa-wydajnosci-uzywajac-dostosowanego-cachea/
---

## **Poprawia Wydajność Dzięki Dostosowanemu Cache'owi**
Aspose.PSD używa pamięci podręcznej do przechowywania danych tymczasowych. Mechanizm jest łatwy w użyciu, dostosowywalny i transparentny. Zapewnia, że nie ma problemów z wydajnością podczas przetwarzania obrazu. Ten artykuł wyjaśnia, jak dostosować cache za pomocą interfejsu API Aspose.PSD dla Javy.
### **Dostosowywanie Cache'a**
Gdy proces potrzebuje tymczasowego przechowywania danych, te dane są przydzielane do cache'a. Cache może być przestrzenią w pamięci lub na dysku i jest ustawiany przez użytkownika. Gdy tymczasowe dane nie są już potrzebne, przestrzeń jest zwalniana. Statystyki przydzielonej przestrzeni można w każdej chwili sprawdzić. Jak Aspose.PSD przydziela i używa cache'a, można dostosować. Ta sekcja opisuje różne ustawienia, ich domyślne wartości i poniższe fragmenty kodu pokazują, jak mogą one być używane.
### **Ustawianie, Gdzie Ma Być Przydzielony Cache**
Aby dostosować, w jaki sposób przestrzeń cache'a jest przydzielana, należy ustawić własność CacheType. Domyślnie cache jest przydzielany w pamięci, a gdy nie ma więcej dostępnej przestrzeni, jest on przydzielany na dysku. To zachowanie jest rejestrowane w trybie Auto. Tryb Auto jest elastyczny i maksymalizuje wydajność. Istnieją także inne tryby:

- tryb CacheOnDiskOnly: przydział tylko na dysk.
- tryb CacheInMemoryOnly: przydział tylko w pamięci.

Wybranie trybu CacheOnDiskOnly może prowadzić do złej wydajności.
### **Ustawianie Rozmiaru Cache'a**
Ustaw maksymalną przestrzeń (w bajtach), która może być przydzielona na dysk lub w pamięci, ustawiając właściwości MaxDiskSpaceForCache i MaxMemoryForCache odpowiednio. Domyślne wartości obu parametrów są ustawione na 0, co oznacza, że nie ma górnego limitu.
### **Kontrolowanie Realokacji Cache'a**
Jeśli nie ma wystarczającej przestrzeni dostępnej w pamięci (zdefiniowanej przez parametr MaxMemoryForCache) podczas przydzielania nowego cache'a, ten cache jest przydzielany na dysku. Jeśli nie ma wystarczającej przestrzeni na dysku, rzucany jest wyjątek. Proces przydzielania cache'a przechodzi z pamięci na dysk, ale nie na odwrót. Właściwość ExactReallocateOnly służy do kontrolowania realokacji pamięci. Realokacja jest najbardziej prawdopodobna dla uprzednio przydzielonych cache'ów. Może się zdarzyć, gdy system zdaje sobie sprawę, że przydzielona przestrzeń nie będzie wystarczająca. Jeśli ExactReallocateOnly jest ustawione na domyślną wartość, False, przestrzeń jest realokowana do tej samej średnicy. Gdy jest ustawiona na True, realokacja nie może przekroczyć maksymalnej określonej przestrzeni. W tym przypadku istniejący cache w pamięci (który wymaga realokacji) jest zwalniany, a przestrzeń jest przydzielana na dysku.
### **Przykłady Programów**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}

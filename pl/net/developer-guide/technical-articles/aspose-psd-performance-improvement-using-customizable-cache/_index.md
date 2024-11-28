---
title: Poprawa wydajności Aspose.PSD za pomocą dostosowalnej pamięci podręcznej
type: docs
weight: 20
url: /pl/net/poprawa-wydajnosci-aspose-psd-za-pomoca-dostosowalnej-pamieci-podrzecznej/
---

## **Poprawia wydajność za pomocą dostosowalnej pamięci podręcznej**
[Aspose.PSD](https://products.aspose.com/psd/family) wykorzystuje pamięć podręczną do tymczasowego przechowywania danych. Mechanizm ten jest łatwy w użyciu, dostosowalny i transparentny. Zapewnia brak problemów z wydajnością podczas przetwarzania obrazów. Niniejszy artykuł wyjaśnia, jak dostosować pamięć podręczną za pomocą interfejsu API Aspose.PSD dla .NET.

### **Dostosowywanie pamięci podręcznej**
Gdy proces wymaga tymczasowego przechowywania danych, te dane są przydzielane w pamięci podręcznej. Pamięć podręczna może znajdować się w pamięci lub na dysku i jest ustawiana przez użytkownika. Gdy dane tymczasowe nie są już potrzebne, miejsce jest zwalniane. Statystyki przydzielonej przestrzeni można sprawdzić w dowolnym momencie. Można dostosować sposób alokacji i wykorzystania pamięci podręcznej przez Aspose.PSD. Niniejszy dział opisuje różne ustawienia i ich domyślne wartości, a poniższe fragmenty kodu pokazują, jak mogą być użyte.

### **Określanie lokalizacji przydzielania pamięci podręcznej**
Aby dostosować sposób lokalizacji pamięci podręcznej, należy ustawić właściwość [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Domyślnie pamięć podręczna jest przydzielana w pamięci, a gdy nie ma już dostępnej przestrzeni w pamięci, przydzielana jest na dysku. To zachowanie jest reprezentowane przez tryb Auto. Tryb Auto jest elastyczny i maksymalizuje wydajność. Istnieją także inne tryby:

- tryb CacheOnDiskOnly: przydzielanie wyłącznie na dysku.
- tryb CacheInMemoryOnly: przydzielanie wyłącznie w pamięci.

Wybór trybu CacheOnDiskOnly może skutkować słabą wydajnością.

### **Ustawianie rozmiaru pamięci podręcznej**
Określ maksymalną przestrzeń (w bajtach), która może być przydzielona na dysku lub w pamięci, ustawiając odpowiednio właściwości [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) i [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache). Domyślnie obie wartości są ustawione na 0, co oznacza brak górnego limitu.

### **Kontrolowanie prze-alokacji pamięci podręcznej**
Jeśli nie ma wystarczającej przestrzeni dostępnej w pamięci (zgodnie z właściwością MaxMemoryForCache) podczas przydzielania nowej pamięci podręcznej, pamięć podręczna jest przydzielana na dysku. Jeśli nie ma wystarczająco dużo miejsca na dysku, zostaje zgłoszony wyjątek. Proces przydzielania pamięci podręcznej przechodzi z pamięci na dysk, ale nie na odwrót. Właściwość [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) jest używana do kontroli ponownego przydzielania pamięci. Przydział ponowny jest najprawdopodobniej dokonywany dla prealokowanej pamięci podręcznej. Może się to zdarzyć, gdy system stwierdzi, że przydzielona przestrzeń nie będzie wystarczająca. Jeśli ExactReallocateOnly jest ustawione na domyślną wartość False, przestrzeń jest ponownie przydzielona do tego samego nośnika. Gdy jest ustawione na True, ponowne alokacje nie mogą przekroczyć maksymalnej określonej przestrzeni. W tym przypadku istniejąca przydzielona pamięć podręczna w pamięci (która wymaga ponownej alokacji) jest zwolniona, a rozszerzona przestrzeń jest przydzielana na dysku.

### **Przykłady programów**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}
